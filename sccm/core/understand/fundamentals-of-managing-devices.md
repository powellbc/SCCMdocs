---
title: "Fundamentals of managing devices | Microsoft Docs"
description: "Learn how to use System Center Configuration Manager to manage devices."
ms.custom: na
ms.date: 12/04/2016
ms.prod: configuration-manager
ms.reviewer: na
ms.suite: na
ms.technology:
  - configmgr-other
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2bca3db9-115a-451d-8c93-f073ceefe0c7
caps.latest.revision: 6
author: nbigmanms.author: nbigmanmanager: angrobe

---
# Fundamentals of managing devices with System Center Configuration Manager*Applies to: System Center Configuration Manager (Current Branch)*
System Center Configuration Manager can manage two broad categories of devices:

**Clients** are devices such as workstations, laptops, servers, and mobile devices on which you install the Configuration Manager client software. Some management functions, such as hardware inventory, require this client software.  

**Managed devices** can include *clients*, but typically means mobile devices on which you do not install the Configuration Manager client software and that you manage by using Microsoft Intune, or Configuration Manager's built-in on-premises mobile device management.

You can also group and identify devices based on user, not just client type.

## Managing devices with the Configuration Manager client

To manage a device using the Configuration Manager client software, you must either discover the device on your network and then deploy the client software to that device, or manually install the client software on a new computer and then have that computer join your site when it joins your network. To discover devices that do not yet have client software installed, run one or more of the built-in discovery methods. After a device is discovered, use one of several methods to install the client software. For information on using discovery, see [Run discovery for System Center Configuration Manager](../../core/servers/deploy/configure/run-discovery.md).  

 After discovering devices that are supported to run the Configuration Manager client software, you can use one of several methods to get the software installed. After the software is installed and the client is assigned to a primary site, you can begin to manage the device.  Common installation methods include 'Client push installation', 'software update-based installation, using Group Policy,  manual installation on a computer, or including the client as part of an operating system image you deploy.  

 After the client is installed, you can simplify the tasks of managing devices by using collections. Collections are groups of devices or users that you create so that you can manage them as a group. For example, you might want to install a mobile device application on all mobile devices that are enrolled by Configuration Manager. If this is the case, you could use the **All Mobile Devices** collection.  

 For more information, see these topics:  

-   [Choose a device management solution for System Center Configuration Manager](../../core/plan-design/choose-a-device-management-solution.md)  

-   [Client installation methods in System Center Configuration Manager](../../core/clients/deploy/plan/client-installation-methods.md)  

-   [Introduction to collections in System Center Configuration Manager](../../core/clients/manage/collections/introduction-to-collections.md)  

### Client settings  
 When you first install Configuration Manager, all clients in the hierarchy are configured by using default client settings that you can change. These client settings include configuration options like how  frequently devices communicate with the site, whether the client is enabled for software updates and other management operations, or whether users can enroll their mobile devices to be managed by Configuration Manager.  

You can create custom client settings and then assign them to collections.  Members of the collection are configured to have the custom settings and you can create multiple custom client settings that are applied in the order that you specify (by numerical order).  If there are conflicting settings, the setting that has the lowest order number overrides the other settings.  

The following diagram shows an example of how you could create and apply custom client settings.  

 ![Client settings](media/ClientSettings.gif)  

 To learn more about client settings, see  
                [How to configure client settings in System Center Configuration Manager](../../core/clients/deploy/configure-client-settings.md) and  [About client settings in System Center Configuration Manager](../../core/clients/deploy/about-client-settings.md).

## Managing devices without the Configuration Manager client  
 Configuration Manager supports managing some devices that have not installed the client software (and that are not managed by Microsoft Intune). For more information see [Manage mobile devices with on-premises infrastructure in System Center Configuration Manager](../../mdm/understand/manage-mobile-devices-with-on-premises-infrastructure.md) and  [Manage mobile devices with System Center Configuration Manager and Exchange](../../mdm/deploy-use/manage-mobile-devices-with-exchange-activesync.md).  

## User-based management  
 Configuration Manager collections of Active Directory Domain Services users. When you use a user collection, you can install software on all computers that members of the collection log into, and configure **user device affinity** so that the software you deploy installs on only the devices that are specified as a user's primary device. A user can have one or more primary devices.  

 One of the ways in which users can control their software deployment experience is by using the computer client interface, **Software Center**. Software Center is automatically installed on client computers and accessed from the users' Start menu. The Software Center lets users manage their own software, as well as perform the following:  

-   Install software  

-   Schedule software to automatically install outside working hours  

-   Configure when Configuration Manager can install software on their device  

-   Configure access settings for remote control, if remote control is enabled in Configuration Manager  

-   Configure options for power management if an administrative user has enabled this  

 A link in Software Center lets users connect to the **Application Catalog**, where they can browse for, install, and request software. In addition,  the Application Catalog lets users configure some preference settings,  wipe their mobile devices, and (when you allow this configuration) specify their own primary devices for user device affinity.   

 Because Application Catalog is a website that is hosted in IIS, users can also access the Application Catalog directly from a browser, from the intranet, or from the Internet.  
