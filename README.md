# sugarcrm_note
##To be able to see Lead ID in the list view, add the followin line in custom/modules/Leads/metadata/listviewdefs.php
```
'ID' =>
  array (
    'width' => '20%',
    'label' => 'LBL_ID',
    'default' => true,
    //'value' => '$focus->id',
    'link' => true,
  ),
```

##To allow ID (like Lead ID) in the email.
command out 'id' on Var $badFields = array () on line 93 in /modules/EmailTemplate.php

##To change the fields of Leads (or accounts...) in the Target List's View:
Create empty script modules/ProspectLists/metadata/studio.php and go to Admin -> Studio -> Target Lists.

##If the imap_open lib is not available, the edit view page for Inbound email will be disable.
To enable it, command out "$xtpl->assign('IE_DISABLED', 'DISABLED');" on line 229 at /modules/InboundEmail/EditView.php

##To enable POP3, add "$sugar_config['allow_pop_inbound'] = true;" on /config_override.php.
## To Add custom field to Mass Update ##

##To Check if the request is from REST or an user through UI, use 
```
isset( $_RQUEST["rest_data"] ) //true for REST, false for user throught
```
