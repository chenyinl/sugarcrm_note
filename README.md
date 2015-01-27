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
