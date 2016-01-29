# at_tools
This module makes the life of [Adaptive Theme](https://www.drupal.org/project/adaptivetheme) users easier
by regenerating all the AT active themes' css files

## Rationale
When working with an Adaptive Theme and using SASS the generated css files pose a problem with version control.
Normally after a user makes changes to the SASS files and regenerates the CSS, commiting those changes to version
control is challenging since almost always when the user gets the latest changes before uploading hers there will
be conflicts in those files.

A common workaround this is to not version the CSS files to avoid conflicts, but when such a step is taken a extra
layer of complexity is added to the build system that deploys code changes, since now it needs to compile the SASS
files after each deploy.

This module takes care of that problem by regenerating the CSS files when Drupal's cache is cleared, and since that
step is almost always necessary after a new deploy it doesnt add any complexity to the deploy workflow

## Usage

- Install the module
- Remove the CSS files generated in all AT themes in your project from version control
- Enjoy!
