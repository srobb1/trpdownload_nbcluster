# trpdownload_nbcluster

Authored by Sofia Robb

Works with the Trpdownload_api module to create 

 1) CSV file for download that contains:
 -  NBCluster Feature uniquename  
 -  NBCluster Feature name
 2) FASTA file for download that contains
 -  NBCluster Feature uniquename
 -  NBCluster Feature name
 -  NBCluster Feature sequence  


To use add the following code to a feature node pane:

Get the query from the form and append to the urls below. This is code from a 'Footer: Global: Text area' in my view.
```
<?php 

$url_array = array();
foreach ($_GET as $key => $value) { 
     if ( $key != 'q' ){   
          $parts = preg_split('/\s+/', $value);
          $v=join(' ', $parts);
          $url_array[] = "$key=$v";
     }
}

$fasta_url = "/chado/nbcluster/fasta?"   .  join('&', $url_array);
$csv_url = "/chado/nbcluster/csv?"  .  join('&', $url_array); 

print 'Download Results: <a href="' . $fasta_url . '">FASTA</a> | <a href="' . $csv_url . '">CSV</a><p>';


?>
```
