![Logo](img/logosmblack.png)

---

# InvoiceNinja API Example Usage (Product and Invoicing)

*Developed by C.A Torino, TechRad*
* Links to TechRad ZA.
    * [Website](https://www.techrad.co.za)
    * [Tutorial website](https://tutorials.techrad.co.za)
    * [Support website](https://support.techrad.co.za)
    * [API](https://www.techrad.co.za/api/public/apps/fusio)

### Summary

Setting up Invoiceninja version 5 on a shared hosting system.

Invoiceninja is built with _Laravel_, _Flutter_ and _React_ but at this time the _React_ frontend works best for me on a desktop PC.

Invoiceninja has decent PDF invoices with a space for company logos, however the free version will include Invoiceninjas logo as well.

It has a decent API and includes `2FA` as well as email notifications for logins and other events.

### Setup steps


#### 1
Create a MySQL database and take note of the credentials.

#### 2
Go to https://github.com/invoiceninja/invoiceninja/releases download and extract the archive onto your shared hosting _FTP_ repository folder.

At the time of this writing I was using `v5.5.49`

#### 3
You will also need to _copy/rename_ the `.env.example` file to `.env`

#### 4
Browse to https://my.url.co.za/public/setup in order to view the setup check page, from then on everything is self explanatory.

#### 5
Once you are finished with the wizard you will need to add a cronjob.

In my case: _konsoleh_ > __Web Hosting_ > _Domain_ > _Manage Services_ > under configuration click _Cronjob Manager_.

Then click Add and fill in `cd public_html/my.url.co.za && /usr/bin/php8.1 -d register_argc_argv=On artisan schedule:run`.

Note I had to specifically choose `php8.1` to get the job to run properly Invoiceninja 5 requires `php8.1` as a minimum.

Save the Cronjob the fastest times I could run mine was every *2 hours* so had to select that option.

#### Another important note

On shared hosting to clear the cache you will need to either empty to contents of `/bootstrap/cache/*` OR run `https://faq.techrad.co.za/update?secret=secret`.

You will need to do this whenever you have errors like broken images in _PDF_ invoices etc.

### Links
* [InvoiceNinja Swaggerhub API Docs](https://app.swaggerhub.com/apis/invoiceninja/invoiceninja)
* []()
