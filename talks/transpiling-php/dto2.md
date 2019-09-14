<?php
namespace MyApp\User\Input;

use MyApp\User\UserId;

struct UserRegistrationDetails{
    UserId $userId;
    string $username;
}


vs

PHP < 7.0
<?php
namespace MyApp\User\Input;

use MyApp\User\UserId;

class UserRegistrationDetails{
    /** @var UserId */
    private $userId;
    /** @var string */
    private $username;

    /** @param string $username */
    public function __construct(UserId $userId, $username) {
        $this->userId = $userId;
        $this->username = $username;
    }

    /** @return UserId */
    public function getUserId(){
        return $this->userId;
    }
    /** @return string */
    public function getUsername(){
        return $this->username;
    }
}


PHP 7.0,7.1,7,2,7,3
class UserRegistrationDetails{
    /** @var UserId */
    private $userId;
    /** @var string */
    private $username;

    public function __construct( UserId $userId, string $username) {
        $this->userId = $userId;
        $this->username = $username;
    }

    public function getUserId() : UserId
    {
        return $this->userId;
    }

    public function getUsername() : string
    {
        return $this->username;
    }
}

PHP 7.4
class UserRegistrationDetails{
    private UserId $userId;
    private string username;

    public function __construct( UserId $userId, string $username) {
        $this->userId = $userId;
        $this->username = $username;
    }

    public function getUserId() : UserId
    {
        return $this->userId;
    }

    public function getUsername() : string
    {
        return $this->username;
    }
}

