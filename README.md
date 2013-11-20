Builder plugin for Intellij
================
An Intellij plugin to generate a nested static Builder for a Class.

Install
-------
* Download the .jar file from https://git.squareup.com/rhall/builder-plugin/releases
* From Intellij: Preferences -> Plugins -> Install plugin from disk...
* Restart Intellij

Update
------
* Follow the Install instructions for the latest release .jar file.
* Intellij seems to be buggy and will report the plugin can be upgraded.  Just ignore.  The version should be correct on the right pane.
* If something goes wrong, you can always uninstall the plugin and install the latest version.

Use
-------
* From a Class, right click -> Generate... -> Builder...
* Remove any fields you don't want and select which fields are nullable

Features
--------
* Select what fields you want to include in the Builder.
* Select fields are non-null and <code>Preconditions.checkNotNull</code>s will be added to constructor.
* If <code>javax.persistence</code> annotations exist on fields, nullable will be inferred.
* Can optionally generate getters, which will return a Guava <code>Optional</code> if the field is nullable.
