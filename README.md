# Sapling
## A Hugo Theme specifically for daycare and similar service industry companies

This theme is in development and not ready for use...yet

# Development Notes

## BaseOf File
The baseof.html file is the default style that is picked up for all pages.  

In the <head> tag, baseof.html calls head.html to create the heading information.

In the <body> tag, baseof.html calls the partial/header.html, partial/footer.html and creates the "main" block.


## Index File



## Config file
The config.toml file controls all options and specifications for the deployed site.  Required or generally necessary options are documented below.

### Site Title
title: This sets the title for the site in the tab or browser header.  It is not used in any of the sites displayed information.
theme: This will be set to "sapling" (obviously...)

### Site Params
companyName = "Wonder Of...Learning Center"
logoImage = "images/logo.png" 200px
iconImage = "images/icon.png" 60px
subtitle = "Technology. Music. And everything between."
fontawesome = "https://kit.fontawesome.com/dc511c6fde.js"
colorTheme = "https://www.w3schools.com/lib/w3-theme-orange.css"
location: Sets the city/town location for the header

### Contact Params
The contact params are a range of items to disply multiple contact options in the header.

contact: Actual contact information (such as email, phone #, website, fax #, etc.)
icon: FontAwesome (or other) icon for type of contact specified above

# Notes on the functioning site


## Adding content to a site

### Header information

#### Contact Information
Update the params.contact entries in config.toml to add or edit contact information.

#### Location
Update the Site params location entry to add or edit the location information.
### Covers

## Subtree Instructions
Run from the head of the daycare site project:
git subtree pull --prefix themes/sapling/ sapling master --squash
