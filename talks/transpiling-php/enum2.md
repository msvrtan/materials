https://github.com/myclabs/php-enum/blob/master/src/Enum.php


<?php

namespace MyApp\Checkout\Payment;

enum PaymentMethodType
{
    const CREDIT_CARD = 'cc';
    const PAYPAL = 'pp';
    const CASH = 'cash';
    const SEPA = 'sepa';
}

enum PaymentProvider
{
    const COMPANY1 = 'c1';
    const COMPANY2 = 'c2';
    const COMPANY3 = 'c3';
    const COMPANY4 = 'c4';
    const COMPANY5 = 'c5';
}

enum PaymentStatus
{
    const PENDING = 1;
    const PAID = 2;
    const CANCELLED = 3;
    const REFUNDED = 4;
}
