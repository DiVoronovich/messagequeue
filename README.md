# One more Connection "default" is not defined

In this class `\Magento\MessageQueue\Model\Plugin\ResourceModel\Lock` there is a dependency `\Magento\Framework\MessageQueue\Lock\WriterInterface`

This dependency hydrated with the config at

```
[Progress: 2 / 1432]
Enabling Maintenance Mode...
```

When there is no env.php and connection details as well.

At the moment dependency mode is disabling this class is trying to get a connection (but it was already hydrated long ago)  - it doesn't have a connection and I'm getting the following response:

```
[Progress: 1429 / 1432]
Disabling Maintenance Mode:

In ResourceConnection.php line 148:

Connection "default" is not defined  
```
