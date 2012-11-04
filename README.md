#CodeIgniter Starter

[By Geoff Doty](https://github.com/n2geoff)


## Overview

The purpose of this repository is to re-structure the default Codeigniter structure with something that is a little more agile to changes and updates.

### Folder Structure

	codeigniter/
		2.1.3/				<-- Original System Folder
			core/
    		database/
    		fonts/
    		helpers/
			language/
			libraries/

	application/			<-- application, ie. example.com
		private/			<-- Original Application Folder
			cache/
			config/
			controllers/
			core/
			errors/
			helpers/
			hooks/
			language/
			libraries/
			logs/
			models/
			migrations/ 	<-- Added 
			third_party/
			views/
		public/
			css/
			img/
			js/
			user_guide/		<-- Original User Guide
			


### Codeigniter System Structure (aka 2.1.3)

The `codeigniter/2.1.3` folder structure change allows switching between versions of Codeigiter by simply updating your `$system_path` setting in `application/public/index.php`.  

    $system_path = '../../codeigniter/2.1.3';


### Codeigniter Application Structure

The _application folder_ is still where all you application code lives, only now it includes -- all your application code.  Your javascript files, your stylesheets, and your images, all self-contained under one folder.  Contained within a single folder, allows you to easily run multipule applications from the same codeigniter instance.


### Public Folder

A place to store all your web accessible content, such as images, stylesheets, ect... 

>`application/public/` folder is the entry point for your web accessible content.

#### Apache VirtualHost Example

    <VirtualHost application.dev:80>
        DocumentRoot "<path>/application/public/"
        ServerName application.dev
        ErrorLog "logs/application-error.log"
        CustomLog "logs/application-access.log" combined
    </VirtualHost>






