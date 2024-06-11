# Asset Indexes Extra plugin for Craft CMS
This Craft CMS plugin helps you to add extra functionalities to Asset Indexes utility in Craft CMS.

## License & Pricing
This is going to be a commercial plugin available through the [Craft plugin store](https://plugins.craftcms.com/developer/vnali).

## Requirement
Craft 5 and higher.

## Main features:
- Generate elements and items (entries, products and digital products) from assets on running asset indexes utility.
  - please request if you need another items
- Log asset indexes results.
- Limit access to volumes on asset indexes utility.

## Log asset indexes results
You can easily log asset indexes utility results by enabling 'Create a Log ...' on this plugin general setting.  
By enabling this option, after running asset indexes utility, when an asset is created, a log record is also created.  
Logs are availble on 'admin/asset-indexes-extra/logs/index' page.

## Limit access to volumes on asset indexes utility
In general settings page, there is an option, 'Only list the volumes that user has related permission.'.  You can limit volumes that shown to users on asset indexes utlity
and asset indxeses option page. You can filter list of volumes to 'View Assets' and 'Save Assets'.

## Gnerate elements and items (entries, products and digital products) from assets on running asset indexes utility.
You can create extra options for asset indexes utility. 
After an asset is created by asset indexes utility, this plugin check for available asset indexes options based the volume of created asset.
Based on applied asset indexes option, plugin creates an item (currently entries, products, digital products) specified in this option.

### create an option for asset indxes utlity:
from Asset Indexes Extra menu, select options.

`Volumes`  
You can filter volumes that related to this asset indexes option.

`Item Type`  
Specify which item you want to create by this asset indexes option.
 - Based on selected item, there are sub items that you should select. for example, after selecting 'entry',  section and entry type and sites should be selected.

`Field Mapping`  
If you want to use an indexed asset on created item, specify the custom field for this asset.

`Select users`   
Specify this option can be used by which users.
  - for example, if userA run asset indexes for vol1, if an option matches for vol1 but userA is not selected for this option, creation of specified item is skipped.
  - if asset indexes utility run by console, this option is ignored.

`Log`  
By enabling the 'Log' option, a log record is created or the current log record is updated. 
- a log record might be created earlier on creatoin of asset on asset index if General log setting is enabled. in this case current log record for the asset 
is updated.

`Enable`  
You can enable/disable this option temporarily

## Permissions

Label | Permission | Description
--- | --- | ---
Manage asset indexes options | *assetIndexesExtra-manageOptions* | Can managee options for asset indexes utility.
View logs | *assetIndexesExtra-viewLogs* | Can view the logs.
Delete logs | *assetIndexesExtra-deleteLogs* | Can delete the logs.
User can skip access check | *assetIndexesExtra-canSkipAccessCheck* | The user with this permission can create items without having permissions related to creation of those items. for example the user can create an entry by ruuning asset indexes on an section/entrytype/site which user have not access to them.
Manage plugin Settings | *assetIndexesExtra-manageSettings* | Managing plugin settings.

## FAQ

## Known issues

## Contact
Feel free to contact me by email at vnali.dev@gmail.com or direct message me via 'vnali' on [Craft CMS Discord](https://craftcms.com/discord) channel.
