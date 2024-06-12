# Asset Indexes Extra plugin for Craft CMS
This Craft CMS plugin helps you to add extra functionalities to the Asset Indexes utility in Craft CMS.

## License & Pricing
This is a commercial plugin available through the [Craft plugin store](https://plugins.craftcms.com/developer/vnali).

## Requirement
Craft 5 and higher.

## Main features:
- Generate elements and items (entries, products, and digital products) from assets on running asset indexes utility.
  - please request if you need another item.
- Log asset indexes results.
- Limit access to volumes on asset indexes utility.  

## Gnerate elements and items (entries, products ,and digital products) from assets on running asset indexes utility.
You can create extra options for asset indexes utility.  
After an asset is created by the asset indexes utility, this plugin checks for available asset indexes options based the volume of created asset.  
Based on the applied asset indexes option, the plugin creates an item (currently entries, products, digital products) specified in this option.
 - entries, products, digital products that were created by this plugin are always disabled so admins be able to audit them before publish.

### Create an option for asset indexes utlity:
To create an option for asset indexes utility, select options sub menu from Asset Indexes Extra. You should fill in these fields in the provided form:  

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
- a log record might be created earlier on creatoin of asset on asset index if General log setting is enabled. in this case current log record for the asset 
is updated.

`Enable`  
You can enable/disable this option temporarily

![asset-indexes-options](https://github.com/vnali/asset-indexes-extra-documentation/assets/55586085/c95c8dcc-374a-486f-9cf1-0b87acd7c1a6)


## Log asset index results
You can easily log asset index results by enabling 'Create a Log ...' on this plugin's general setting.  
By enabling this option, after running asset indexes utility, when an asset is created, a log record is also created.  
Items created by asset indexes options also can be logged by enabling the `Log` light switch in each option.
Logs are available on 'admin/asset-indexes-extra/logs/index' page.

Items available in logs:  

`Id`
Specify the Id of a log record. 
The color of the info icon is:   
<b>Green:</b> If the item specified in this option is created.  
<b>Red:</b> If the item specified in option is not created because of some errors and `Log` option general setting is disabled so successful asset creation is not reflected in the log.  
<b>Orange:</b> If item specified in option is not created because of some errors but `Log` option in general setting is enabled so successful asset creation is reflected in the log.

`Volume`
Specify that this log is result of indexing which volume.

`Option`
Specify this log is the result of which asset indexes option (if Log is disabled for the option, value is empty)

`Item`
the Filename of the indexed item.

`User`
The user who runs asset indexes utility. return empty if the user is deleted or asset indexes are run via CLI.

`CLI`
if asset indexes are run via CLI.

`Detail`  
By clicking this item you can see more details of a log record.

`Created`
The datetime when log is created based on site timezone.


![logs](https://github.com/vnali/asset-indexes-extra-documentation/assets/55586085/4c601436-481f-46f1-8f76-64f937ee5dda)


## Limit access to volumes on asset indexes utility
In the general settings page, there is an option, 'Only list the volumes that user has related permission.'.  You can limit volumes that shown to users on the asset indexes utility
and asset indexes option page. You can filter list of volumes to 'View Assets' and 'Save Assets'.  

## Permissions

Label | Permission | Description
--- | --- | ---
Manage asset indexes options | *assetIndexesExtra-manageOptions* | Can manage options for asset indexes utility.
View logs | *assetIndexesExtra-viewLogs* | Can view the logs.
Delete logs | *assetIndexesExtra-deleteLogs* | Can delete the logs.
User can skip access check | *assetIndexesExtra-canSkipAccessCheck* | The user with this permission can create items without having permissions related to the creation of those items. for example, the user can create an entry by running asset indexes on a section/entrytype/site to which user have not access.
Manage plugin Settings | *assetIndexesExtra-manageSettings* | Managing plugin settings.

## FAQ

## Known issues

## Contact
Feel free to contact me by email at vnali.dev@gmail.com or direct message me via 'vnali' on [Craft CMS Discord](https://craftcms.com/discord) channel.
