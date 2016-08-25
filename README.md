[![Build Status](https://api.travis-ci.org/ITDSystems/alvex-uploader.svg?branch=master)](https://travis-ci.org/ITDSystems/alvex-uploader)

Alvex Uploader
========================


Attach files from local drive or select existing files in the repository on any form:
* packageItems on workflow forms
* cm:content associations on any custom form


Build
-----
Option 1:
Build it via [alvex-meta](https://github.com/ITDSystems/alvex-meta). It allows to build a stable version with all dependencies inside the package.

Option 2:
Build from this repo. The component may be packaged in two ways: *amp* and *jar*.
To build amp use `mvn clean package`, to build installable jar use `mvn -P make-jar clean package`.

**Note!**
Don't forget to build and install dependecies! This component depends on [alvex-common](https://github.com/ITDSystems/alvex-common) so you should install it first.

**Note**: this project requires Maven 3.3.9 at least.

Use
-----

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
