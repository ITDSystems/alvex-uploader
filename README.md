[![Build Status](https://api.travis-ci.org/ITDSystems/alvex-uploader.svg?branch=master)](https://travis-ci.org/ITDSystems/alvex-uploader)

# Alvex Uploader

Attach files from local drive or select existing files in the repository on any Alfresco Share form:
* packageItems on workflow forms
* cm:content associations on any custom form

![Uploader](http://alvexcore.com/images/docs/uploader.png)

Compatible with Alfresco 5.1 and 5.2.

This component requires:
* [Alvex Utils](https://github.com/ITDSystems/alvex-utils)

# Using this project

Recommended way to use Alvex components is to include them as dependencies to your Maven project. Follow [this guide](https://github.com/ITDSystems/alvex#recommended-way-include-alvex-to-your-project-via-maven-configuration) to include this component to your project.

# Build from source

To build Alvex follow [this guide](https://github.com/ITDSystems/alvex#build-component-from-source).

# Quick Start

### Using Files uploader on workflow forms

Add *PackageItems* field to the form and use the following field configuration in Appearance section of your type Share configuration:

```
<field id="packageItems">
  <control template="/alvex-uploader.ftl">
    <control-param name="uploadDirectory">uploads</control-param>
    <control-param name="createUploadDirectory">true</control-param>
  </control>
</field>
```

All uploaded documents will be saved to the folder named in parameter *uploadDirectory*.

### Using Files uploader on other forms

Use the following field configuration in Appearance section of your type Share configuration:

```
<field id="prefix:files">
  <control template="/alvex-uploader.ftl">
    <control-param name="uploadDirectory">uploads</control-param>
    <control-param name="createUploadDirectory">true</control-param>
    <control-param name="viewType">mini</control-param>
  </control>
</field>
```

*prefix:files* should be an association with cm:content element or its child.


