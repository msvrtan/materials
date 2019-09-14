<?php
namespace MyApp\User\Input;


struct UserRegistrationDetails{
    UserId $userId;
    string $username;
    string $password;
    string $emailAddress;
    bool   $active;
    string $firstName;
    string $lastName;
    \DateTimeImmutable $registeredAt;
}


vs


<?php

namespace MyApp\User\Input;


class UserRegistrationDetails{
    /** @var UserId */
    private $userId;
    /** @var string */
    private $username;
    /** @var string */
    private $password;
    /** @var string */
    private $emailAddress;
    /** @var bool */
    private $active;
    /** @var string */
    private $firstName;
    /** @var string */
    private $lastName;
    /** @var \DateTimeImmutable */
    private $registeredAt;

    public function __construct(
        UserId $userId,
        string $username,
        string $password,
        string $emailAddress,
        bool $active,
        string $firstName,
        string $lastName,
        \DateTimeImmutable $registeredAt
    ) {
        $this->userId = $userId;
        $this->username = $username;
        $this->password = $password;
        $this->emailAddress = $emailAddress;
        $this->active = $active;
        $this->firstName = $firstName;
        $this->lastName = $lastName;
        $this->registeredAt = $registeredAt;
    }

    public function getUserId() : UserId
    {
        return $this->userId;
    }

    public function getUsername() : string
    {
        return $this->username;
    }

    public function getPassword() : string
    {
        return $this->password;
    }

    public function getEmailAddress() : string
    {
        return $this->emailAddress;
    }

    public function isActive() : bool
    {
        return $this->active;
    }

    public function getFirstName() : string
    {
        return $this->firstName;
    }

    public function getLastName() : string
    {
        return $this->lastName;
    }

    public function getRegisteredAt() : \DateTimeImmutable
    {
        return $this->registeredAt;
    }
}



<?php

namespace MyApp\User\Input;


class UserRegistrationDetails{
    private UserId $userId;
    private string $username;
    private string $password;
    private string $emailAddress;
    private bool $active;
    private string $firstName;
    private string $lastName;
    private \DateTimeImmutable $registeredAt;

    public function __construct(
        UserId $userId,
        string $username,
        string $password,
        string $emailAddress,
        bool $active,
        string $firstName,
        string $lastName,
        \DateTimeImmutable $registeredAt
    ) {
        $this->userId = $userId;
        $this->username = $username;
        $this->password = $password;
        $this->emailAddress = $emailAddress;
        $this->active = $active;
        $this->firstName = $firstName;
        $this->lastName = $lastName;
        $this->registeredAt = $registeredAt;
    }

    public function getUserId() : UserId
    {
        return $this->userId;
    }

    public function getUsername() : string
    {
        return $this->username;
    }

    public function getPassword() : string
    {
        return $this->password;
    }

    public function getEmailAddress() : string
    {
        return $this->emailAddress;
    }

    public function isActive() : bool
    {
        return $this->active;
    }

    public function getFirstName() : string
    {
        return $this->firstName;
    }

    public function getLastName() : string
    {
        return $this->lastName;
    }

    public function getRegisteredAt() : \DateTimeImmutable
    {
        return $this->registeredAt;
    }
}