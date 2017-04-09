## Get Current store Id
```php
<?php
//inject \Magento\Store\Model\StoreManagerInterface $storeManage
$this->storeManager = $storeManager;
$id = $this->storeManager->getStore()->getId();
//Get BaseURL:
$baseUrl = $this->storeManager->getStore()->getBaseUrl();
```
