WordPress' Media Uploader to Amazon S3


Plugins Overview 

There are two plugins required as a Amazon web service and WP Offload S3. 

which uses its libraries and its settings to connect to AWS services.Setting as follows.  

note:*indicates selected option

https://wordpress.org/plugins/amazon-web-services/


Amazon Web Service


Wordpress Amazon Web Service configuration:
define( 'AWS_ACCESS_KEY_ID', '********************' );

define( 'AWS_SECRET_ACCESS_KEY', '****************************************' );

Save Changes.




WP Offload s3

path: https://wordpress.org/plugins/amazon-s3-and-cloudfront/

Active WP Offload s3 Plugins and configuration as follows

1.  Create a Bucket name 
ENABLE/DISABLE THE PLUGIN

ON : Copy Files to S3
When a file is uploaded to the Media Library, copy it to S3. Existing files are not copied to S3.

ON : Rewrite File URLs
For Media Library files that have been copied to S3, rewrite the URLs so that they are served from S3/CloudFront instead of your server.

CONFIGURE FILE URLS
PREVIEW  : http://****.*******.com/ Folder Name /image name.jpg

Domain: choose your Domain

Bucket name as subdomain

http://bucket-name.s3.amazon.com/…

Bucket name in path

http://s3.amazon.com/bucket-name/…

*Bucket name as domain

http://bucket-name/…

CloudFront or custom domain



ON : Path
By default the path is the same as your local WordPress files:*****/images name.jpg/png/giff

OFF: Year/Month
Add the Year/Month in the URL. 

SSL:
    *Same as request
    When the request is https://, use https:// for the file URL as well.
    Always SSL
    Forces https:// to be used.
    You cannot use the "Bucket as a subdomain" domain option when using SSL.
    Always non-SSL
    Forces http:// to be used.




ADVANCED OPTIONS:

All OFF
