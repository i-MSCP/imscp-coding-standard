i-MSCP Coding Standard
==============================

Repository with all coding standard ruleset for i-MSCP repositories.

Installation
------------

1. Install the module via composer by running:

   ```bash
   $ composer require --dev imscp/imscp-coding-standard
   ```

2. Add composer scripts into your `composer.json`:

   ```json
   "scripts": {
     "cs-check": "phpcs",
     "cs-fix": "phpcbf"
   }
   ```

3. Create file `phpcs.xml` on base path of your repository with content:

   ```xml
   <?xml version="1.0"?>
   <ruleset name="i-MSCP Coding Standard">
       <rule ref="./vendor/imscp/imscp-coding-standard/ruleset.xml"/>

       <!-- Paths to check -->
       <file>config</file>
       <file>src</file>
       <file>test</file>
   </ruleset>
   ```

You can add or exclude some locations in that file.
For a reference please see: https://github.com/squizlabs/PHP_CodeSniffer/wiki/Annotated-ruleset.xml

Usage
-----

* To run checks only:

   ```shell
      $ composer cs-check
   ```

* To automatically fix many CS issues:
 
   ```shell
      $ composer cs-fix
   ```
