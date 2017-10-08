
## About Clean-Slate-Laravel

Clean-Slate-Laravel is a version of Laravel/Laravel that has been cleaned up and prepared for an ideal greenfield experience when starting a new Laravel project. It includes customizations and suggestions specifically for a dev environment running on a Windows PC (because I'm on a PC, and I built this project starter primarily for my own use). 

## Steps for Starting a New Project

- Create a project database.
- Create a local virtual host (if desired) with a custom local url for the project under development.
- Create a project directory.

(Note: For Laragon users in Windows, the above steps can be done automatically via Menu->Quick create->Laravel, which will also run a Composer install of Laravel. You will be asked to supply a project name. You will get a MySQL db named "project-name", an Nginx virtual host at http://project-name.dev, and a project directory at C:\laragon\www\project-name.)

- Clone Clean-Slate-Laravel into the project directory. (Use git clone. Note: If Laravel has already been installed, e.g. via a Laragon quick-create, erase everything from the project directory before running git clone.)
- Update the .env file, changing at minimum APP_NAME (=project-name), APP_URL (=virtual-host-url if a virtual host was created), DB_DATABASE (=name-of-the-database), DB_USERNAME (=probably "root" for dev mode), and DB_PASSWORD (=probably blank for dev mode).
- Update the timezone config in config/app.php if you don't want to default to Mountain Time zone.
- Review the "scripts" in the package.json file, which have been modified to deal with a bug on Windows systems. (To change these back to defaults, replace them with the "scripts" from the laravel/laravel Github repo.)

## License
Clean-Slate-Laravel and the Laravel framework is open-sourced software licensed under the [MIT license](http://opensource.org/licenses/MIT).
