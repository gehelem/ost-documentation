---
title: Quick install
weight : 22
---
{{% notice style="note" title="Warning" icon="exclamation-triangle" %}}
Do not use on an existing installation, unless you carefully check what the script does
(especially at the nginx level)
{{% /notice %}}

This method installs all the necessary components to use OST.
it is simple to use, works on a Raspberry Pi, a VM (Virtualbox), or a classic PC.
From a blank Ubuntu install, from the command line:

```shell
cd
wget https://raw.githubusercontent.com/gehelem/OST/main/install.sh
chmod +x install.sh
./install.sh
```

This script installs everything you need to have an operational set:
- Indi server
- Nginx
- Some Astrometry.net indexes
- OST web interface
- Indiwebmanager
- OST service

At the end of this script you can create your indiwebmanager profile,
and start the indi server there:

![Indiweb](/images/indiweb.png)

Then go to the OST home page:

![OST1](/images/ost1.png)