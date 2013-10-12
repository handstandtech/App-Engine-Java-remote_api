# Default Backup Version of Java App Engine for Java - Created by [Handstand Technologies, LLC](http://handstandtech.com)

A default "backup" version to deploy onto App Engine

## NOTES

- /* is protected and only accessible by Administrators
- Bulk Loader is accessible via /remote_api

## REQUIREMENTS

- Uses Google App Engine 1.8.1
- Eclipse Project using the Google Plugin for Eclipse Juno

## INSTRUCTIONS

- In the war/WEB-INF/appengine-web.xml file, change *APPSPOT_NAME_GOES_HERE* to your appspot id

## COMMANDS
- appcfg.py create_bulkloader_config --filename=bulkloader.yaml --url=http://backup.APPSPOT_NAME_GOES_HERE.appspot.com/_ah/remote_api
- appcfg.py download_data --url=http://backup.APPSPOT_NAME_GOES_HERE.appspot.com/_ah/remote_api --filename=backupfile