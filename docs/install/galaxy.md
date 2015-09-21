# Overview

SNVPhyl can be directly installed within an existing Galaxy instance.  There are two necessary steps that must take place for installing to a local Galaxy:

1. Installing the SNVPhyl dependency tools.
2. Importing the SNVPhyl Galaxy workflows.

## Installing the SNVPhyl Tools

The SNVPhyl tools are managed within a Galaxy Toolshed.  In particular, within <https://irida.corefacility.ca/galaxy-shed/view/nml/suite_snvphyl> (the [IRIDA][] toolshed).

You will have to enable this toolshed within Galaxy before SNVPhyl can be used.  The toolshed can be enabled by adding it to the `config/tool_sheds_conf.xml` Galaxy configuration file.  Please find this file and add the line:

```xml
<tool_shed name="IRIDA" url="https://irida.corefacility.ca/galaxy-shed"/>
```

Once this line is added, please restart Galaxy.  If you navigate to **Admin**, and then from here nagivate to **Tools and Tool Shed > Search Tool Shed**, you should see the IRIDA toolshed show up.

![irida-toolshed][]

Once the IRIDA toolshed is installed, you should be able to search for the `suite_snvphyl` repository.

![suite-snvphyl-repository][]

Please follow through the steps to install this suite of tools, making sure to leave **Handle repository dependencies?** and **Handle tool dependencies?** checked.

![snvphyl-tool-dependencies][]

## Import SNVPhyl Galaxy workflows

The current SNVPhyl Galaxy workflows can be found at [SNVPhyl 0.2 Paired-end][] and [SNVPhyl 0.2 Paired-end invalid positions][].  Please import these workflow files into Galaxy by navigating to **Workflow > Upload or import workflow**.  On completion you should have a set of workflows available.

![snvphyl-import-workflows][]

Installation should now be complete.  Please see the [Usage][] documentation for more information on how to use SNVPhyl.

[IRIDA]: http://irida.ca
[irida-toolshed]: images/irida-toolshed.png
[suite-snvphyl-repository]: images/suite-snvphyl-repository.png
[snvphyl-tool-dependencies]: images/snvphyl-tool-dependencies.png
[Usage]: ../user/usage.md
[snvphyl-import-workflows]: images/snvphyl-import-workflows.png
[SNVPhyl 0.2 Paired-end]: ../workflows/SNVPhyl/0.2/snvphyl-workflow-0.2.ga
[SNVPhyl 0.2 Paired-end invalid positions]: ../workflows/SNVPhyl/0.2/snvphyl-workflow-0.2-invalid-positions.ga
