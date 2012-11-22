Add the following snipets to the .htaccess file in the target directory.

Targets
=======

### Target a file

    <Files file_name>
        ...
        ...
    </Files>
    
### Target a group of files

    <Files ~ "\.(zip)$">
        ...
        ...
    </Files>
    

Protect access
==============

### Deny access to the directory

    order allow,deny
    deny from all
    

Index files
===========

### Specify which files are considered as index files

    DirectoryIndex index.php index.html
    
Authentication
==============

### Add a basic auth

    AuthType Basic
    AuthUserFile /path/to/your/.htpasswd
    AuthName "Text to display when passwd is asked"
    require valid-user
    
Redirections
============

### To redirect a visitor to http://site.com

    Redirect / http://www.site.com            
    
### Redirecting a visitor when he request certain pages

    Redirect /dir http://www.site.com
    RedirectMatch (.*)\cmd.exe$ http://www.site.com$1     
