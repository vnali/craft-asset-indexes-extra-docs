# Asset Indexes Extra plugin for Craft CMS
This Craft CMS plugin helps you to add extra functionalities to the Asset Indexes utility in Craft CMS.

## License & Pricing
This is a commercial plugin available through the [Craft plugin store](https://plugins.craftcms.com/developer/vnali).

## Requirement
Craft 5 and higher.

## Main features:
- Generate elements and items (entries, products, and digital products, ...) from assets on running asset indexes utility.
- Log asset index results.
- Limit access to volumes on asset indexes utility.  

## Generate elements and items (entries, products, and digital products) from assets on running asset indexes utility.
You can create extra options for asset indexes utility.  
After an asset is created by the asset indexes utility, this plugin checks for available asset index options based on the volume of the created asset.  
Based on the applied asset index option, the plugin creates an item (currently entries, products, digital products) specified in this option.
 - entries, products , and digital products that were created by this plugin are always disabled so admins are able to audit them before publishing.

### Create an option for asset indexes utility:
To create an option for asset indexes utility, select the `options` sub-menu from the Asset Indexes Extra menu. You should fill in these fields in the provided form:  

`Volumes`  
You can filter volumes that are related to this asset indexes option.

`Item Type`  
Specify which item you want to create by this asset indexes option.
 - Based on the selected item, there are sub-items that you should select. for example, after selecting 'entry',  section and entry type and sites should be selected.

`Field Mapping`  
If you want to use an indexed asset on a created item, specify the custom field for this asset.

`Select users`   
Specify this option can be used by which users.
  - for example, if userA runs asset indexes for vol1, if an option matches for vol1 but userA is not selected for this option, the creation of the specified item is skipped.
  - if asset indexes utility run by console, this option is ignored.

`Log`  
By enabling the 'Log' option, a log record is created or the current log record is updated. 
- a log record might be created earlier on the creation of an asset via asset indexes utility if the General log setting is enabled. in this case current log record for the asset 
is updated.

`Enable`  
You can enable/disable this option temporarily

![asset-indexes-options](https://github.com/vnali/asset-indexes-extra-documentation/assets/55586085/c95c8dcc-374a-486f-9cf1-0b87acd7c1a6)


## Log asset index results
You can easily log asset index results by enabling 'Create a Log ...' on this plugin's general setting.  
By enabling this option, after running the asset indexes utility, when an asset is created, a log record is also created.  
Items created by asset index options also can be logged by enabling the `Log` light switch in each option.
Logs are available on the 'admin/asset-indexes-extra/logs/index' page.

Items available in logs:  

`Id`
Specify the ID of a log record. 
The color of the info icon is:   
<b>Green:</b> If the item specified in this option is created.  
<b>Red:</b> If the item specified in the option is not created because of some errors and the `Log` option general setting is disabled so successful asset creation is not reflected in the log.  
<b>Orange:</b> If the item specified in the option is not created because of some errors but the `Log` option in the general setting is enabled so successful asset creation is reflected in the log.

`Volume`
Specify that this log is the result of indexing which volume.

`Option`
Specify this log is the result of which asset indexes option (if Log is disabled for the option, value is empty)

`Item`
the Filename of the indexed item.

`User`
The user who runs asset indexes utility. return empty if the user is deleted or asset indexes are run via CLI.

`CLI`
if asset indexes are run via CLI.

`Detail`  
By clicking this item you can see more details of a log record. Created assets and items can be edited quickly via slideout by clicking on element chips.

`Created`
The date when the log is created in the site timezone.

The logs can be searched via item's filename, result text, volume name, and username who run asset indexes.

![logs](https://github.com/vnali/asset-indexes-extra-documentation/assets/55586085/4c601436-481f-46f1-8f76-64f937ee5dda)


## Limit access to volumes on asset indexes utility
In the general settings page, there is an option, 'Only list the volumes that the user has related permission.'.  You can limit volumes that are shown to users on the asset indexes utility
and asset indexes option page. You can filter the list of volumes to 'View Assets' and 'Save Assets'.  

## Permissions

Label | Permission | Description
--- | --- | ---
Manage asset indexes options | *assetIndexesExtra-manageOptions* | Can manage options for asset indexes utility.
View logs | *assetIndexesExtra-viewLogs* | Can view the logs.
Delete logs | *assetIndexesExtra-deleteLogs* | Can delete the logs.
User can skip access check | *assetIndexesExtra-canSkipAccessCheck* | The user with this permission can create items without having permissions related to the creation of those items. for example, the user can create an entry by running asset indexes on a section/entrytype/site to which the user has no access.
Manage plugin Settings | *assetIndexesExtra-manageSettings* | Managing plugin settings.

## FAQ

## Known issues

## Contact
Feel free to contact me by email at vnali.dev@gmail.com or direct message me via 'vnali' on [Craft CMS Discord](https://craftcms.com/discord) channel.
