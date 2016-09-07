[![Build Status](https://api.travis-ci.org/ITDSystems/alvex-uploader.svg?branch=master)](https://travis-ci.org/ITDSystems/alvex-uploader)

# Alvex Uploader


Attach files from local drive or select existing files in the repository on any form:
* packageItems on workflow forms
* cm:content associations on any custom form

# Downloads

Alvex component builds are automatically published to [nexus.itdhq.com](http://nexus.itdhq.com) by Travis CI.

# Build

To build Alvex follow [this guide](https://github.com/ITDSystems/alvex#build-component-from-source).

## Use


![image](http://docs.alvexcore.com/en-US/Alvex/2.1/html-single/Admin_Guide/images/img38.png)
```
<field id="packageItems">
  <control template="/alvex-uploader.ftl">
    <control-param name="uploadDirectory">uploads</control-param>
    <control-param name="createUploadDirectory">true</control-param>
  </control>
</field>
```

```
<field id="prefix:files">
  <control template="/alvex-uploader.ftl">
    <control-param name="uploadDirectory">uploads</control-param>
    <control-param name="createUploadDirectory">true</control-param>
    <control-param name="viewType">mini</control-param>
  </control>
</field>
```

Detailed guide is coming soon.
