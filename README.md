### Fork from: https://github.com/lolautruche/SQLIImport/

# SQLIImport for eZ Publish
##Source Handlers tests

This fork is just for testing purpose. It adds a new source handler class for a **Local XML File**.


## Installation

1. Clone and activate the extension
2. Create a new eZ Class: Test Import (`testimport`) with the following fields:

		title (Input Text)
		content (XML Block)
		image (Image)
		attachment (File)

3. Copy the `doc/feedtest.xml` file and customize the image and file values according to your file system
4. Customize the `RSSFeed` value within the `settings/sqliimport.ini.append.php` file with your own xml file
5. Run the sqlimport script with the following command from the `ezpublish_legacy` directory:
    	
		php extension/sqliimport/bin/php/sqlidoimport.php

6. Run the cronjob or launch the following command from the `ezpublish_legacy` directory:
    
		php runcronjobs.php sqliimport_run

## File

The example file is available to the following path:

        classes/sourcehandlers/sqlirsslocalimporthandler.php