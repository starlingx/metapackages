======
Metapackages
======
This repository contains the StarlingX metapackages,
which are designed to group together StarlingX packages responsible
for implementing certain system features, such as software updates,
distributed cloud, kubernetes, etc.

These packages may include additional scripts related to its respective
feature, but, in general, they simply list related packages in its dependencies.

This repository is not intended to be developed standalone, but rather as part
of the StarlingX Source System, which is defined by the StarlingX manifest [1]_.

For more information about StarlingX, please refer to the documentation [2]_.

======
Instructions for developers
======

To create a new metapackage, take another metapackage as a starting point and update:

- dependencies in the control file
- any occurrences of the metapackage name
- metapackage information in files/metadata.xml

Place any required files or directories into the "files" folder.
They will be installed to /usr/local/share/metapackages/RELEASE/NAME/
Be mindful that file permissions will be preserved when creating the metapackage.


References
==========
.. [1] https://opendev.org/starlingx/manifest.git
.. [2] https://docs.starlingx.io/
