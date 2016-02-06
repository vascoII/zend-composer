# zend-composer
Zend 1.x using composer

# Using composer for zendframework1 in vendor folder : 
- Using the zf tool:
      zf create project zend-composer-jwt
- In public/index.php:
      comment get_include_path() 

      // Ensure library/ is on include_path
        set_include_path(implode(PATH_SEPARATOR, array(
        realpath(APPLICATION_PATH . '/../library'),
        // get_include_path(),
    )));

- Using composer in zend-composer-jwt DIR
      composer init
      bla bla bla until: Would you like to define your dependencies (require) interactively [yes]?yes
      Search for a package: zendframework1
      Enter number for line zendframework/zendframework1 
      Enter version: 1.* for the latest 1.x version
      Search for a package []: return
      no
      Type composer install : Composer download the latest version of Zend Framework and place it in your projects ./vendor directory.

- In public/index.php and tests/bootstrap.php:
      replace // get_include_path(), by realpath(APPLICATION_PATH . '/../vendor/zendframework/zendframework1/library')
