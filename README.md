# trpdownload_nbcluster

Authored by Sofia Robb

## Need to update this info for this module
Works with the Trpdownload_api module to create a file for download that contains:
-  Feature uniquename  
-  tissue type from the [tripal-analysis-expression](http://tripal.info/extensions/modules/tripal-analysis-expression)  
-  expression value from the [tripal-analysis-expression](http://tripal.info/extensions/modules/tripal-analysis-expression)


To use add the following code to a feature node pane:

`<a href="<?php print url('chado/expression/csv', array('query' => array('feature_id'=>$feature->feature_id))) ?>">Download</a>`
