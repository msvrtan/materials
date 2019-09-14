https://github.com/myclabs/php-enum/blob/master/src/Enum.php


<?php

namespace MyApp\Checkout\PaymentMethod;

enum PaymentMethodType
{
    const CREDIT_CARD = 'cc';
    const PAYPAL = 'pp';
    const CASH = 'cash';
    const SEPA = 'sepa';
}

or


<?php

namespace MyApp\Checkout\PaymentMethod;

enum PaymentMethodType
{
    const CREDIT_CARD = 'cc'
        , PAYPAL = 'pp'
        , CASH = 'cash'
        , SEPA = 'sepa';
}

or


<?php

namespace MyApp\Checkout\PaymentMethod;

enum PaymentMethodType
{
    const CREDIT_CARD = 'cc',
          PAYPAL = 'pp',
          CASH = 'cash',
          SEPA = 'sepa';
}


vs

<?php

namespace MyApp\Checkout\PaymentMethod;

use MyCLabs\Enum\Enum;

class PaymentMethodType extends Enum
{
    const CREDIT_CARD = 'cc';
    const PAYPAL = 'pp';
    const CASH = 'cash';
    const SEPA = 'sepa';

    public static function CREDIT_CARD(): self
    {
        return new self(self::CREDIT_CARD);
    }

    public static function PAYPAL(): self
    {
        return new self(self::PAYPAL);
    }

    public static function CASH(): self
    {
        return new self(self::CASH);
    }

    public static function SEPA(): self
    {
        return new self(self::SEPA);
    }
}
