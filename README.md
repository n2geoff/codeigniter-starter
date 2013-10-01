CodeIgniter Starter
----

A re-structured version Codeigniter, bootstraped with some of the webs best libraries.

#### Whats Included
- Codeigniter         2.1.4
- Rest Server
- Modular Extentions  5.4
- Twitter Bootstrap   2.3.2
- JQuery              1.10.2

## Setup

###1. Clone Repo

    clone git://github.com/n2geoff/codeigniter-starter.git

###2. Configrue Apache Virtual Host

    <VirtualHost application.dev:80>
        DocumentRoot "<path>/application/public/"
        ServerName application.dev
        ErrorLog "logs/application-error.log"
        CustomLog "logs/application-access.log" combined
    </VirtualHost>

###3. Start Developing



## Folder Structure

	codeigniter/
		2.1.4/				<-- Original System Folder
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
			modules/        <-- Added
			migrations/ 	<-- Added 
			third_party/
			views/
		public/
			css/
			img/
			js/
			user_guide/		<-- Original User Guide
			
### System Structure

The `codeigniter/2.1.3` folder structure change allows switching between versions of Codeigiter by simply updating your `$system_path` setting in `application/public/index.php`.  

    $system_path = '../../codeigniter/2.1.4';

>To add another version of Codeigniter, create a folder representing the Codeigniter version (2.1.4) and copy the contents of the `system` into that folder.


### Application Structure

The _application folder_ is still where all you application code lives, only now it includes -- all your application code.  Your javascript files, your stylesheets, and your images.  

The goal is two-fold

1. Self-contained Application
2. Have Multiple Applications


### Public Folder

A place to store all your web accessible content, such as images, stylesheets, ect... 

>`application/public/` folder is the entry point for your web accessible content.


# Todo

- Integrate HTML5 Boilerplate
- More...




