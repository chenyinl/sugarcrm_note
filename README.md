# sugarcrm_note
To be able to see Lead ID in the list view, add the followin line in custom/modules/Leads/metadata/listviewdefs.php
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

To allow ID (like Lead ID) in the email.
command out 'id' on Var $badFields = array () on line 93 in /modules/EmailTemplate.php

To change the fields of Leads (or accounts...) in the Target List's View:
Create empty script modules/ProspectLists/metadata/studio.php and go to Admin -> Studio -> Target Lists.
