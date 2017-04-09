### Get Current Store Id
```php
<?php
//inject \Magento\Store\Model\StoreManagerInterface $storeManage
$this->storeManager = $storeManager;
$id = $this->storeManager->getStore()->getId();
//Get BaseURL:
$baseUrl = $this->storeManager->getStore()->getBaseUrl();
```

### Collection joined with table
```php
<?php
$joinConditions = 'u.field1 = e.field1';
$prodCollection->getSelect()->join(
	['u' => 'table1'],
	$joinConditions,
	[]
);
//Multiple conditions
$joinConditions[] = "u.sku = e.sku";
$joinConditions[] = "e.type_id= 'simple' ";
$joinConditions = implode(
	' AND ', $joinConditions
);
```

### Get Product Collection without new Block creation
```php
<?php
$objectManager = \Magento\Framework\App\ObjectManager::getInstance();
/** @var \Magento\Catalog\Model\ResourceModel\Product\Collection $productCollection */
$productCollection = $objectManager->create('Magento\Catalog\Model\ResourceModel\Product\Collection');
/** Apply filters here */
$productCollection->load();
```

### Get Current Magento Version
```php
<?php
//Updated to use object manager
$objectManager = \Magento\Framework\App\ObjectManager::getInstance();
$productMetadata = $objectManager->get('Magento\Framework\App\ProductMetadataInterface');
$version = $productMetadata->getVersion(); //will return the magento version
```
#### ---OR---
```php
<?php
$productMetadata = new \Magento\Framework\App\ProductMetadata();
$version = $productMetadata->getVersion();
```

### Print to Log from anywhere
```php
<?php
$writer = new \Zend\Log\Writer\Stream(BP . '/var/log/test.log');
$logger = new \Zend\Log\Logger();
$logger->addWriter($writer);
$logger->info('Your text message');
$logger->info(print_r($yourArray, true));
```
