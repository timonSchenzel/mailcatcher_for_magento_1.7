# Mailcatcher Driver For Magento 1.7
## Step 1.
copy `app/code/local/Mage/Core/Model/Email/Template.php` inside your code base.

## Step 2.
Configure your app: `app/etc/local.xml`.
Add this example code and edit the email setting if needed.
Port 1025 is default for mailcatcher.
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
## Step 3.
Install mailcatcher (https://mailcatcher.me/).
From your terminal run: `gem install mailcatcher`

## Step 4.
Boot mailcatcher.
From your terminal run: `mailcatcher`.

## Step 5.
Receiver emails.
So send an email and go to: `http://127.0.0.1:1080`.

## Optional
If you want to specify a custom smtp or http port, you can do this:
From your terminal run: `mailcatcher --smtp-port 1026 --http-port 1081`.
Now you have to set the port to `1026` inside `app/etc/local.xml` and you are able to view the email at: `http://127.0.0.1:1081`.
