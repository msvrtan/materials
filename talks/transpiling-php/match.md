https://github.com/myclabs/php-enum/blob/master/src/Enum.php


<?php

namespace MyApp\Checkout\Payment;

enum PaymentStatus
{
    const PENDING = 1;
    const PAID = 2;
    const CANCELLED = 3;
    const REFUNDED = 4;

    function __toString():string{
        match $this->value{
            PENDING : "pending",
            PAID : "paid",
            CANCELLED : "cancelled",
            REFUNDED : "refunded",
        }
    }
}



<?php

namespace MyApp\Checkout\Payment;

enum PaymentStatus
{
    const PENDING = 1;
    const PAID = 2;
    const CANCELLED = 3;
    const REFUNDED = 4;

    function smallIconFileName():string{
        match $this->value{
            PENDING :   "pending.png",
            PAID :      "paid.jpeg",
            CANCELLED : "cancelled.gif",
            REFUNDED :  "refunded.png",
        }
    }
}


vs

<?php

namespace MyApp\Checkout\Payment;

class PaymentStatus extends Enum
{
    const PENDING = 1;
    const PAID = 2;
    const CANCELLED = 3;
    const REFUNDED = 4;

    ...

    public function smallIconFileName(): string
    {
        switch ($this->value) {
            case self::PENDING:
                return 'pending.png';
            case self::PAID:
                return 'paid.jpeg';
            case self::CANCELLED:
                return 'cancelled.gif';
            case self::REFUNDED:
                return 'refunded.png';
        }
    }
}
