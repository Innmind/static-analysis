# static-analysis

This is a meta package to alias all the dependencies required for Innmind packages to run static analysis.

## Installation

```sh
composer require --dev innmind/static-analysis
```

## Usage

Once the package is required you need to create the file `psalm.xml` with the following content:

```xml
<?xml version="1.0"?>
<psalm
    errorLevel="1"
    resolveFromConfigFile="true"
    findUnusedBaselineEntry="true"
    findUnusedCode="false"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xmlns="https://getpsalm.org/schema/config"
    xsi:schemaLocation="https://getpsalm.org/schema/config vendor/vimeo/psalm/config.xsd"
>
    <projectFiles>
        <directory name="src" />
        <ignoreFiles>
            <directory name="vendor" />
        </ignoreFiles>
    </projectFiles>
</psalm>
```
