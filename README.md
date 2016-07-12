# Mailcatcher Driver For Magento 1.7
## Step 1.
copy `app/code/local/Mage/Core/Model/Email/Template.php` inside your code base.

## Step 2.
Configure your app: `app/etc/local.xml`.
Add this example code and edit the email setting if needed.
```xml
<config>
    <global>
        <email>
            <driver>mailcatcher</driver>
            <host>localhost</host>
            <port>1025</port>
        </email>
   	</global>
</config>
```
