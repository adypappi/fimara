# FIMARA ERP & CRM


Fimara ERP & CRM is a modern software package that helps manage your organization's activity (contacts, suppliers, invoices, orders, stocks, agenda…).

It's an Open Source Software suite (written in PHP with optional JavaScript enhancements) designed for small, medium or large companies, foundations and freelancers.

You can freely use, study, modify or distribute it according to its licence.

You can use it as a standalone application or as a web application to access it from the Internet or a LAN.


## LICENSE

Fimara is released under the terms of the GNU General Public License as published by the Free Software Foundation; either version 3 of the License, or (at your option) any later version (GPL-3+).

See the [COPYING](https://github.com/adypappi/fimara/blob/develop/COPYING) file for a full copy of the license.

Other licenses apply for some included dependencies. See [COPYRIGHT](https://github.com/Adypappi/fimara/blob/develop/COPYRIGHT) for a full list.

## INSTALLING

### Simple setup

If you have low technical skills and you're looking to install Fimara ERP/CRM in just a few clicks.
### Advanced setup

You can use a web server and a supported database (MariaDB, MySQL or PostgreSQL) to install the standard version.

On GNU/Linux, first check if your distribution has already packaged Fimara.

#### Generic install steps:

- Check that your installed PHP version is supported [see PHP support](https://fimara.adipappi.net/index.php/Releases).

- Uncompress the downloaded .zip archive to copy the "fimara/htdocs" directory and all its files inside your web server root or get the files directly from GitHub (recommanded if you know git as it makes it easier if you want to upgrade later):

  `git clone https://github.com/fimara/fimara -b x.y`     (where x.y is main version like 3.6, 9.0, ...)

- Set up your web server to use "*fimara/htdocs*" as root if your web server does not have an already defined directory to point to.

- Create an empty `htdocs/conf/conf.php` file and set *write* permissions for your web server user (*write* permission will be removed once install is finished)

- From your browser, go to the fimara "install/" page

  The URL will depends on how you web setup was setup to point to your fimara installation. It may looks like:

  `http://localhost/fimara/htdocs/install/`

  or

  `http://localhost/fimara/install/`

  or

  `http://yourdolibarrvirtualhost/install/`

- Follow the installer instructions


### Saas/Cloud setup

If you don't have time to install it yourself, you can try some commercial 'ready to use' Cloud offers (See https://saas.fimara.org). However, this third solution is not free.


## UPGRADING

Fimara supports upgrading, usually without the need for any (commercial) support (depending on if you use any commercial extensions). It supports upgrading all the way from any version after 2.8 without breakage. This is unique in the ERP ecosystem and a benefit our users highly appreciate!
 
- At first make a backup of your Fimara files & than [see](https://wiki.fimara.org/index.php/Installation_-_Upgrade#Upgrade_Dolibarr)
- Check that your installed PHP version is supported by the new version [see PHP support](./doc/phpmatrix.md).
- Overwrite all old files from 'fimara' directory with files provided into the new version's package.
- At first next access, Fimara will redirect you to the "install/" page to follow the upgrade process.
  If an `install.lock` file exists to lock any other upgrade process, the application will ask you to remove the file manually (you should find the `install.lock` file in the directory used to store generated and uploaded documents, in most cases, it is the directory called "*documents*").


## WHAT'S NEW

See the [ChangeLog](https://github.com/Adypappi/fimara/blob/develop/ChangeLog) file.


## FEATURES

### Main application/modules (all optional)

- Third-Parties Management: Customers, Prospects (Leads) and/or Suppliers + Contacts 
- Members/Membership/Foundation management 

 Product Management 
- Products and/or Services catalog 
- Stock / Warehouse management + Inventory 
- Barcodes 
- Batches / Lots / Serials 
- Product Variants 
- Bill of Materials (BOM)
- Manufacturing Orders 

 Customer/Sales Management 
- Customers/Prospects + Contacts management 
- Opportunities or Leads management 
- Commercial proposals management 
- Customer Orders management 
- Contracts/Subscription management 
- Interventions management 
- Ticket System 
- Shipping management 
- Customer Invoices/Credit notes and payment management 
- Point of Sale (POS) 

 Supplier/Purchase Management 
- Suppliers/Vendors + Contacts 
- Supplier (price) requests 
- Purchase Orders management 
- Delivery/Receiption 
- Supplier Invoices/credit notes and payment management 
- INCOTERMS 

 Finance / Accounting 
- Invoices / Payments 
- Bank accounts management 
- Direct debit orders management (European SEPA) 
- Accounting management 
- Donations management 
- Loan management 
- Margins 
- Reports 

 Collaboration 
- Shared calendar/agenda (with ical and vcal export for third party tools integration) 
- Projects & Tasks management 
- Ticket System 
- Surveys

 HR 
- Employee's leave requests management 
- Expense reports 
- Recruitment management 
- Timesheets 


### Other application/modules

- Electronic Document Management (EDM) 
- Bookmarks management
- Reporting
- Data export/import
- Barcodes 
- Margin calculations
- LDAP connectivity
- ClickToDial integration
- Mass emailing
- RSS integration
- Skype integration
- Social platforms linking 
- Payment platforms integration (PayPal, Stripe, Paybox...)
- Email-Collector

(around 100 modules available by default, 1000+ on the addon market place)


### Other general features

- Localization in most major languages
- Multi-Language Support
- Multi-Users and groups with finely grained rights
- Multi-Currency
- Multi-Company (by adding of an external module)

- Very user friendly and easy to use
- customizable Dashboard
- Highly customizable: enable only the modules you need, add user personalized fields, choose your skin, several menu managers (can be used by internal users as a back-office with a particular menu, or by external users as a front-office with another one)

- APIs (REST, SOAP)
- Code that is easy to understand, maintain and develop (PHP with no heavy framework; trigger and hook architecture)

- Support a lot of country specific features:
  - Spanish Tax RE and ISPF
  - French NPR VAT rate (VAT called "Non Perçue Récupérable" for DOM-TOM)
  - Canadian double taxes (federal/province) and other countries using cumulative VAT
  - Tunisian tax stamp
  - Argentina invoice numbering using A,B,C...
  - Compatible with [European directives] (https://europa.eu/legislation_summaries/taxation/l31057_en.htm) (2006/112/CE ... 2010/45/UE)
  - Compatible with European GDPR rules
  - ...
- Flexible PDF & ODT generation for invoices, proposals, orders...
- …


### System Environment / Requirements

- PHP
- MariaDB, MySQL or PostgreSQL 
- Compatible with all Cloud solutions that match PHP & MySQL or PostgreSQL prerequisites.


## WHAT FIMARA CAN'T DO YET

These are features that Fimara does **not** yet fully support:

- Tasks dependencies in projects
- Payroll module
- No native embedded Webmail, but you can send email to contacts in Fimara with e.g. offers, invoices, etc.
- Fimara can't do coffee (yet)


## DOCUMENTATION

Administrator, user, developer and translator's documentations are available along with other community resources in the [Wiki](https://wiki.fimara.org).


## CONTRIBUTING

This project exists thanks to all the people who contribute. 
Please read the instructions how to contribute (report a bug/error, a feature request, send code ...)  [[Contribute](https://github.com/Fimara/fimara/blob/develop/.github/CONTRIBUTING.md)]

A view on Contributors:

<a href="https://github.com/Adypappi/fimara/graphs/contributors"><img src="https://opencollective.com/fimara/contributors.svg?width=890&button=false" /></a>


## CREDITS

Fimara is the work of many contributors over the years and uses some fine PHP libraries.

See [COPYRIGHT](https://github.com/Adypappi/fimara/blob/develop/COPYRIGHT) file.


## NEWS AND SOCIAL NETWORKS

Follow Fimara project on:

- [YouTube](https://www.youtube.com/user/Fimara)
- [GitHub](https://github.com/Adypappi/fimara)


