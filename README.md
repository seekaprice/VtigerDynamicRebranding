# VtigerDynamicRebranding
Project to modify Vtiger so users can rebrand the crm after install 
using a user interface.

## Job Description

Modify VTiger installation package to remove all vtiger static text 
and image branding and allow the user to rebrand the CRM 
with their own branding using a UI interface. 
All rebranding should be stored in a single branding config (branding.config.php) 
file seperate from the existing VTiger config file. 
This file will then be included in the vtiger config file (config.inc.php). 

#### The project will include but not limited to the following tasks :

* Modify any sql crud operation that include branding, this includes sql 
crud operations during install, and any subsequent sql operations. 
Any reference to branding must use values stored in branding.config.php.

* Modify (if necessary) any View Controllers to work with the branding 
values stored in branding.config.php.

* Modify any template files to use the values stored in branding.config.php 
or a default generic value if branding value is not available.

* Modify any files that use static text for branding values and change 
the file to use values stored in the branding.config.php file. 
Example: the file languages\en-us\Settings\Vtiger.php contains 
constant variables that hole static text values with vtiger branding. 
All these values must use the variable values stored in branding.config.php.

* Create an interface so the user can change the branding to their own brand, 
such as domain text, brand name, and logos/images. 
The interface will modify the values stored in branding.config.php 
and that will update through out the entire site. Images will need 
to be generated one or more images the user uploads.

The rebranding interface should be available after CRM installation 
and should be part of the CRM. Prior to CRM installation, 
all branding will be our BzCRM branding which will be the 
default values for branding until the user changes 
it in the branding interface.

## Additional Notes
There is a seperate Vtiger module for customers to login to the CRM.
The module is called CustomerPortal. We like this portal to be include in
the project.

The git repo contains the vtiger install source in the "vtigercrm" folder
and the customer portal inside the "vtigercrm-customerportal-7.0.0" folder.

There is a sample installed vtiger crm to look at, but it's best you install a copy
on your own development machine for testing. The sample is not the final product. 
It is meant as an example visual. You can visit the sample at https://nofb.org/Crm
Contact me for the username and password.