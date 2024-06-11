# Asset Indexes Extra plugin for Craft CMS
This Craft CMS plugin helps you to add extra functionalities to Asset Indexes utility in Craft CMS.

## License & Pricing
This is going to be a commercial plugin available through the [Craft plugin store](https://plugins.craftcms.com/developer/vnali).

## Requirement
Craft 5 and higher.

## Main features:
- Gnerate elements and items (entries, products and digital products) from assets on running asset indexes utility. 
- Log asset indexes results.
- Limit access to volumes on asset indexes utility.

## Log asset indexes results
You can easily log asset indexes utility results by enabling 'Create a Log record when an asset created.' item on plugin general setting.
After enabling this option, after running asset indexes utility, when an asset is createdd, a log record is also created.
Logs can be see on 'admin/asset-indexes-extra/logs/index' page.

## Limit access to volumes on asset indexes utility
In general settings page, there is an option, 'Only list the volumes that user has related permission.' and you can limit volumes that shown to users on asset indexes utlity
and asset indxeses option page. You can filter list of volumes to 'View Assets' and 'Save Assets'.

## Gnerate elements and items (entries, products and digital products) from assets on running asset indexes utility.
You can create extra options for asset indexes utility. 
after an asset is created by asset indexes utility, this plugin check for available options based the volume of created asset.
then plugin creates an item (currently entries, products, digital products) specified in this option.
