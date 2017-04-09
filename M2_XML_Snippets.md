## Custom Log File
```xml
<preference for="Psr\Log\LoggerInterface" type="Magento\Framework\Logger\Monolog" />
<type name="Magento\Framework\Logger\Monolog">
	<arguments>
		<argument name="name" xsi:type="string">main</argument>
		<argument name="handlers" xsi:type="array">
			<item name="system" xsi:type="object">Magento\Framework\Logger\Handler\System</item>
			<item name="debug" xsi:type="object">Magento\Framework\Logger\Handler\Debug</item>
		</argument>
	</arguments>
</type>
```
