### Setup Upgrade
```cmd
php bin/magento setup:upgrade
```

### Flush Caches
```cmd
php bin/magento cache:flush
```

### Deploy Static Content
```cmd
php bin/magento setup:static-content:deploy
```

### Deploy Static Content for specific Theme
```cmd
php bin/magento setup:static-content:deploy --theme Magento/luma --theme Magento/second_theme
```

### Clean Caches
```cmd
php bin/magento cache:clean
```

### Reindex All Indexes
```cmd
php bin/magento indexer:reindex
```

### Run the single-tenant DI(Dependency Injection) Compiler
```cmd
php bin/magento setup:di:compile
```
