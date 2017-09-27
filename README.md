
In mid-2017, the portal server for Okidokeys BLE smart locks has been shut down, rendering multiple devices worthless. 
These simple static files can work as a replacement API endpoint, making it possible to use the lock again.


Instructions:

1. Reset your smart lock (long press hidden push button).

2. Edit the provided .html files JSON content `DEVICE_OCSN` value to match your lock serial number. According to your needs, change other values - e.g. set your own PIN in `PINCODE`, lock name, user name, image URL etc.

3. Upload the .html and .htaccess files to a web server. 

4. Patch original [Okidokeys Android mobile application](https://play.google.com/store/apps/details?id=com.okidokeys.smartapp) to point to your server instead original one (edit `ProdBaseURL` in `/assets/www/js/openways/tools/constant.js`).

5. Sync the lock in mobile application (second icon down on the left, then choose the lock, "Sync" and tap picture). Now the lock is initialized and mobile application has 500 keys stored for offline use. Do not close the mobile application yet. In case you encounter an error, clear application data, reset the lock and try again.

6. After successful initialization, rename `.htaccess_after_setup` to `.htaccess` on your server. In this way we prevent the mobile application from key reuse ("Your keys are outdated") problem.


Using these files be aware that keys to your lock are now public. It is recommended to create your own files. More information and detailed instructions:

https://smartlockpicking.com/tutorial/my-smart-lock-vendor-disappeared


