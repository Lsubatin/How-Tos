---
title: How to Configure SAP HANA 2.0, express edition Telemetry
description: Learn more about the telemetry feature, and disable telemetry if desired.
tags: [  tutorial>beginner, tutorial>how-to, products>sap-hana\,-express-edition ]
---
## Prerequisites
 - You have installed SAP HANA 2.0, express edition using either the [Installing Binary](http://www.sap.com/developer/tutorials/hxe-ua-installing-binary.html) or [Installing the VM Image](http://www.sap.com/developer/tutorials/hxe-ua-installing-vm-image.html) tutorial.
 - In the [Installing Binary](http://www.sap.com/developer/tutorials/hxe-ua-installing-binary.html) or [Installing the VM Image](http://www.sap.com/developer/tutorials/hxe-ua-installing-vm-image.html) tutorial, you specified your HTTP(s) Proxy settings in Cockpit. (Required only for users behind a corporate firewall.)

## Next Steps
 - [View similar How-Tos](http://www.sap.com/developer/tutorials.html) or [View all How-Tos](http://www.sap.com/developer/tutorials.html)

## How-To Details

Telemetry is enabled by default in SAP HANA 2.0, express edition. Use this tutorial to learn more about the telemetry feature, and disable telemetry if desired.


### Time to Complete
**5 Min**.

---

### What is Telemetry?

When you install SAP HANA 2.0, express edition, Telemetry is enabled by default. You can disable telemetry after installation is complete. Telemetry sends anonymous performance statistics and usage statistics to SAP, so that SAP can focus development efforts on areas most vital to the SAP HANA 2.0, express edition customer base.

>**Important**: Your privacy is critical to SAP. Telemetry collects anonymous usage information while ensuring complete privacy. No identifying information or private information is collected, and you can opt out of telemetry at any time.

If you are inside a corporate firewall and use a proxy for connecting to http and https servers, you need to identify your proxy settings, log in to Cockpit, and update the  **Cockpit Settings > Proxy** page.

>**Note**: If you do not update the Cockpit proxy settings, telemetry will not work properly. For instructions on specifying your proxy settings in Cockpit, see topic **Test XSC, XSA, and Web IDE (Server + Applications Virtual Machine Only)** in tutorial [Start Using SAP HANA 2.0, express edition (Virtual Machine Method)](http://www.sap.com/developer/tutorials/hxe-ua-getting-started-vm.html) or **Test XSC and XSA (Applications Package Only)** in tutorial [Start Using SAP HANA 2.0, express edition (Binary Installer Method)](http://www.sap.com/developer/tutorials/hxe-ua-getting-started-binary.html).

### Disable and Enable Telemetry Using SQL

Disable Telemetry if you wish to stop sending anonymous telemetry data to SAP.

1. Start SAP HANA 2.0, express edition and log in as `hxeadm`.

2. Run:
    ```
    /usr/sap/<sid>/home/bin/hxe_telemetry.sh -i 90 -u SYSTEM -p <your_password> -d SystemDB --disable
    ```
    >**Tip**: If you installed using the Virtual Machine method, `<sid>` is `HXE`.

3. To re-enable telemetry, run:
    ```
    /usr/sap/<sid>/home/bin/hxe_telemetry.sh -i 90 -u SYSTEM -p <your_password> -d SystemDB --enable
    ```
    >**Tip**: If you installed using the Virtual Machine method, `<sid>` is `HXE`.

If you want to learn more about the `hxe_telemetry.sh` script, type **`./hxe_telemetry.sh --help`**

## Next Steps
 - [View similar How-Tos](http://www.sap.com/developer/tutorials.html) or [View all How-Tos](http://www.sap.com/developer/tutorials.html)
