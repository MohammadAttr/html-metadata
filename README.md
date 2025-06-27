html-metadata Library
=====================

Version 1.0
-----------

A lightweight Pug/Jade mixin library for managing HTML metadata tags with ease.

Features
--------

*   Simplifies SEO metadata management
*   Generates Open Graph (OG) tags
*   Creates Twitter card metadata
*   Handles other essential HTML meta tags
*   Centralized configuration for consistent metadata across pages

Installation
------------

1. Simply include the mixin file in your Pug/Jade project:
``` 
include path/to/html-metadata.pug
```
2. You can use inheritance for more professional control :
```
extends path/to/html-metadata.pug
```
Usage
-----

### 1\. Initialization

First, initialize the global metadata variables:

    +init("url", "title", "description", "image-url")
    

### 2\. SEO Metadata

Add standard SEO meta tags:

    +seo("author", ["keyword1", "keyword2", "keyword3"])
    

### 3\. Open Graph Tags

Generate OG tags for social media sharing:

    +og
    

### 4\. Twitter Card Tags

Create Twitter-specific meta tags:

    +twitter
    

### 5\. Other Essential Tags

Add miscellaneous important tags:

    +Others("theme-color")
    

Mixins Reference
----------------

### init(url, title, description, imageSite)

Initializes the global metadata variables.

**Parameters:**

*   `url` Canonical URL of the page And For social media links
*   `title` Page title
*   `description` Page description
*   `imageSite` URL of the social sharing image

### seo(author, keywordsArray)

Generates standard SEO meta tags.

**Parameters:**

*   `author` Content author
*   `keywordsArray` Array of keywords

### og()

Generates Open Graph meta tags using the initialized values.

### twitter()

Generates Twitter Card meta tags using the initialized values.

### Others(themeColor)

Generates miscellaneous important tags.

**Parameters:**

*   `themeColor` Theme color for mobile browsers

### 
Example
-------

Complete implementation example:
```pugjs
//- Initialize
- description = "A sample page description" 
- keywords = ["sample", "page", "keywords"]
+init("https://example.com", "Sample Page", description, "https://example.com/image.jpg")

// SEO Metadata
+seo("John Doe", keywords)

// Open-Graph Tags
+og

// Twitter Tags
+twitter 

// Other Tags
+Others("#3a7bd5")
```

Benefits
--------

*   Consistent metadata across all pages
*   Reduced code duplication
*   Easy maintenance and updates
*   Improved SEO implementation
*   Better social media sharing

Requirements
------------

*   Pug/Jade template engine

License
-------

MIT License - Free to use in both personal and commercial projects.
