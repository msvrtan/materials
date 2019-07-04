




So, when I'm onboarding new person to a project, what they usually have to do is


git checkout git://project

vagrant up

vagrant ssh

composer install

db-setup.sh


###



 - how to deploy?
 - manual deploy due to big table
 - filter tables for migrations to ignore `schema_filter`

 - dont add products/users in loop, personalize data!
 

 Fixtures

 doctrine/doctrine-fixtures-bundle 
  -> doctrine/data-fixtures

 doctrine/doctrine-migrations-bundle
  -> doctrine/migrations 



https://symfony.com/doc/master/bundles/DoctrineMigrationsBundle/index.html


######################################################



Why/how/what

I want to move fast, 
In order to move fast, I need to automate things, 
And having code as data/infastracture is one of the ways to achive that



I want to onboard people quickly
In order to move fast, independent if that is a new hire or colleague that never worked on this product or project, a collegue that was out for vacation or sick
I need to automate things
And having database changes is one of those things

