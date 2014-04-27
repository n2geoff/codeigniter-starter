CodeIgniter Starter Project
----

A re-structured version Codeigniter, bootstraped with some of the webs best libraries to provide a scaleable, out-of-the-box development stack.

#### What's Included
- [Codeigniter - 2.1.4](http://ellislab.com/codeigniter)
- [Rest Server](https://github.com/philsturgeon/codeigniter-restserver)
- [Modular Extensions - fecd39c](https://bitbucket.org/wiredesignz/codeigniter-modular-extensions-hmvc/)
- [HTML5 Boilerplate - 4.3](http://html5boilerplate.com/)
- [Twitter Bootstrap - 3.1.1](http://getbootstrap.com/)
- [JQuery - 1.10.2](http://jquery.com/)

## Setup

### 1. Clone Repo

    clone git://github.com/n2geoff/codeigniter-starter.git

### 2. Configure Apache Virtual Host

    <VirtualHost application.dev:80>
        DocumentRoot "<path>/application/public/"
        ServerName application.dev
        ErrorLog "logs/application-error.log"
        CustomLog "logs/application-access.log" combined
    </VirtualHost>

### 3. Start Developing



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
			fonts/
			img/
			js/
			user_guide/		<-- Original User Guide
			
### System Structure

The `codeigniter/2.1.4` folder structure change allows switching between versions of Codeigiter by simply updating your `$system_path` setting in `application/public/index.php`.  

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




