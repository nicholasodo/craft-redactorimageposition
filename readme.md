# Craft Redactor Image Position
Adds the ability to apply image positions via the Redactor edit modal.

## Installation
1. Download & unzip the file and place the `redactorimageposition` directory into your `craft/plugins` directory
2.  -OR- do a `git@github.com:picdorsey/craft-redactorimageposition.git` directly into your `craft/plugins` folder.  You can then update it with `git pull`
4. Install plugin in the Craft Control Panel under Settings > Plugins
5. The plugin folder should be named `redactorimageposition` for Craft to see it.  GitHub recently started appending `-master` (the branch name) to the name of the folder for zip file downloads.

### Redactor Config
On installation, the `imagePosition` plugin should automatically be added to your Redactor configuration files located at `craft/config/redactor`. **Some environments lack the correct privledges to write to these files and the `imagePosition` plugin must be added manually.**

### HTML purifier
Craft's Redactor HTML purifier config may strip the tags and classes added by this plugin. Add a new file called `/craft/config/htmlpurifier/Standard.json` with the following JSON (or any custom settings) to correct this:
```
{
    "HTML.Allowed": ["figure","span"],
    "Attr.AllowedClasses": ["c-figure", "c-figure--inline", "c-figure--left", "c-figure--right", "c-figure--full", "c-figure__image", "c-figure__caption" ]
}
```
Credit to @sam327

## Screenshots
![Screenshot](https://raw.github.com/picdorsey/craft-redactorimageposition/master/images/screenshot.png)
![Screenshot](https://raw.github.com/picdorsey/craft-redactorimageposition/master/images/screenshot2.png)
