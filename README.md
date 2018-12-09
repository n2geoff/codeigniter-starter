CodeIgniter Starter Project
----

A re-structured version CodeIgniter 3.x, designed to support multiple application under a single CodeIgniter install.  In addition, it provides a simple migration path for newer CodeIgniter versions.

Some of webs best libraries are added provide a scalable, out-of-the-box development stack for both front-end and back-end.

#### What's Included
- [Codeigniter - 3.1.9](http://www.codeigniter.com)
- [Rest Server - 3.0.3](https://github.com/chriskacerguis/codeigniter-restserver)
- [Modular Extensions - fecd39c](https://bitbucket.org/wiredesignz/codeigniter-modular-extensions-hmvc/)
- [HTML5 Boilerplate - 6.1](http://html5boilerplate.com/)

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
		3.1.9/				<-- Original System Folder
			core/
			database/
			fonts/
			helpers/
			language/
			libraries/
	
	application/			<-- application, ie. example.com
		private/			<-- Original application folder
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

The `codeigniter/2.2.2` folder structure change allows switching between versions of Codeigiter by simply updating your `$system_path` setting in `application/public/index.php`.  

    $system_path = '../../codeigniter/3.1.9';

>To add another version of Codeigniter, create a folder representing the Codeigniter version (3.1.9) and copy the contents of the `system` into that folder.

### Application Structure

The _application folder_ is still where all you application code lives, only now it includes -- **all your application code**.  Your javascript files, your stylesheets, and your images.  

**The goal is two-fold**

1. Self-contained Applications
2. Support for Multiple Applications

### Public Folder

A place to store all your web accessible content, such as images, stylesheets, javascript, and opens up a path to develop rich client-side apps with a CodeIgniter backend using REST services! 

>`application/public/` folder is the entry point for your web accessible content.