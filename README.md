Dashboard - Socialize US - Install
========================

Welcome to our group project
Here's how to install the dashboard that will allow you to list/add/edit each of our event: 

What's included
--------------

```
SocializeUS/
├── app/
│   ├── config
│   │   ├── config_dev.yml
│   │   ├── config_prod.yml
│   │   ├── config_test.yml
│   │   ├── config.yml
│   │   ├── parameters.yml
│   │   ├── parameters.yml.dist
│   │   ├── routing_dev.yml
│   │   ├── routing.yml
│   │   ├── security.yml
│   │   ├── services.yml
│   ├── ressources
│   │   ├── views
├── AppCache.php
├── AppKernel.php
├── autoload.php
├── bin/
│   ├── console
│   └── symfony_requirements
└── src/
    ├── AppBundle
    │   │   ├── AppBundle.php
    │   │   ├── Controller
    │   │   ├── Entity
    │   │   │   │   ├── User.php
    │   │   │   │   ├── Event.php
└── tests
└── var
└── vendor
└── web
```

Install
--------------
Clone the repository, then go to the project cd MyPathToTheFolder and do
```
composer install

php bin/console doctrine:database:create

php bin/console assets:install --symlink

php bin/console doctrine:schema:update --dump-sql --force

php bin/console server:run
```
Pour créer un super admin :
```
php bin/console fos:user:create adminuser --super-admin
```

Route
--------------
```
 ----------------------------------- ---------- -------- ------ -----------------------------------
   Name                                Method     Scheme   Host   Path
  ----------------------------------- ---------- -------- ------ -----------------------------------
   _assetic_66d1c6c                    ANY        ANY      ANY    /css/66d1c6c.css
   _assetic_66d1c6c_0                  ANY        ANY      ANY    /css/66d1c6c_homepage_1.css
   _wdt                                ANY        ANY      ANY    /_wdt/{token}
   _profiler_home                      ANY        ANY      ANY    /_profiler/
   _profiler_search                    ANY        ANY      ANY    /_profiler/search
   _profiler_search_bar                ANY        ANY      ANY    /_profiler/search_bar
   _profiler_info                      ANY        ANY      ANY    /_profiler/info/{about}
   _profiler_phpinfo                   ANY        ANY      ANY    /_profiler/phpinfo
   _profiler_search_results            ANY        ANY      ANY    /_profiler/{token}/search/results
   _profiler_open_file                 ANY        ANY      ANY    /_profiler/open
   _profiler                           ANY        ANY      ANY    /_profiler/{token}
   _profiler_router                    ANY        ANY      ANY    /_profiler/{token}/router
   _profiler_exception                 ANY        ANY      ANY    /_profiler/{token}/exception
   _profiler_exception_css             ANY        ANY      ANY    /_profiler/{token}/exception.css
   _twig_error_test                    ANY        ANY      ANY    /_error/{code}.{_format}
   homepage                            ANY        ANY      ANY    /
   easyadmin                           ANY        ANY      ANY    /admin/
   admin                               ANY        ANY      ANY    /admin/
   fos_user_security_login             GET|POST   ANY      ANY    /login
   fos_user_security_check             POST       ANY      ANY    /login_check
   fos_user_security_logout            GET|POST   ANY      ANY    /logout
   fos_user_profile_show               GET        ANY      ANY    /profile/
   fos_user_profile_edit               GET|POST   ANY      ANY    /profile/edit
   fos_user_registration_register      GET|POST   ANY      ANY    /register/
   fos_user_registration_check_email   GET        ANY      ANY    /register/check-email
   fos_user_registration_confirm       GET        ANY      ANY    /register/confirm/{token}
   fos_user_registration_confirmed     GET        ANY      ANY    /register/confirmed
   fos_user_resetting_request          GET        ANY      ANY    /resetting/request
   fos_user_resetting_send_email       POST       ANY      ANY    /resetting/send-email
   fos_user_resetting_check_email      GET        ANY      ANY    /resetting/check-email
   fos_user_resetting_reset            GET|POST   ANY      ANY    /resetting/reset/{token}
   fos_user_change_password            GET|POST   ANY      ANY    /profile/change-password
   fos_user_group_list                 GET        ANY      ANY    /group/list
   fos_user_group_new                  GET|POST   ANY      ANY    /group/new
   fos_user_group_show                 GET        ANY      ANY    /group/{groupName}
   fos_user_group_edit                 GET|POST   ANY      ANY    /group/{groupName}/edit
   fos_user_group_delete               GET        ANY      ANY    /group/{groupName}/delete
   ranking                             ANY        ANY      ANY    /ranking
  ----------------------------------- ---------- -------- ------ -----------------------------------
```
