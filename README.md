[![Build Status](https://api.travis-ci.org/ITDSystems/alvex-uploader.svg?branch=master)](https://travis-ci.org/ITDSystems/alvex-uploader)

# Alvex Uploader

Attach files from local drive or select existing files in the repository on any form:
* packageItems on workflow forms
* cm:content associations on any custom form

![image](http://docs.alvexcore.com/en-US/Alvex/2.1/html-single/Admin_Guide/images/img38.png)

Compatible with Alfresco 5.1.

This component depends on:
* [Alvex Utils](https://github.com/ITDSystems/alvex-utils)

# Downloads

Download ready-to-use Alvex components via [Alvex](https://github.com/ITDSystems/alvex#downloads).

# Build

To build Alvex follow [this guide](https://github.com/ITDSystems/alvex#build-component-from-source).

# Use

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


