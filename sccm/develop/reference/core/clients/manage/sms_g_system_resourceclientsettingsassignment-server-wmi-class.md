---
title: "SMS_G_SYSTEM_ResourceClientSettingsAssignment Class | Microsoft Docs"
ms.custom: ""
ms.date: "09/20/2016"
ms.prod: "configuration-manager"
ms.reviewer: ""
ms.suite: ""
ms.technology:
  - "configmgr-other"
ms.tgt_pltfrm: ""
ms.topic: "article"
applies_to:
  - "System Center Configuration Manager (current branch)"
ms.assetid: 6561a03d-01a3-4fe2-b6cf-220dd743421e
caps.latest.revision: 4
author: "shill-ms"
ms.author: "v-suhill"
manager: "mbaldwin"
---
# SMS_G_SYSTEM_ResourceClientSettingsAssignment Server WMI Class
The `SMS_G_System_ResourceClientSettingsAssignment` Windows Management Instrumentation (WMI) class is an SMS Provider server class, in System Center Configuration Manager, that represents resource-specific (device or user) client agent settings assignments.  

 The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.  

## Syntax  

```  
Class SMS_G_System_ResourceClientSettingsAssignment : SMS_G_System  
{  
     String AssignmentUniqueID;  
     String CollectionName;  
     UInt32 ID;  
     String Name;  
     UInt32 Priority;  
     String UniqueID;  
     UInt32 ResourceID;  
     UInt32 Type;  
};  
```  

## Methods  
 The `SMS_G_System_ResourceClientSettingsAssignment` class does not define any methods.  

## Properties  
 `AssignmentUniqueID`  
 Data type: `String`  

 Access type: Read/Write  

 Qualifiers: [key]  

 Assignment Unique ID.  

 `CollectionName`  
 Data type: `String`  

 Access type: Read/Write  

 Qualifiers: None  

 Name of the collection.  

 `ID`  
 Data type: `UInt32`  

 Access type: Read/Write  

 Qualifiers: None  

 Identifier.  

 `Priority`  
 Data type: `UInt32`  

 Access type: Read/Write  

 Qualifiers: None  

 Identifier.  

 `UniqueID`  
 Data type: `String`  

 Access type: Read/Write  

 Qualifiers: None  

 Unique identifier for the settings.  

 `ResourceID`  
 Data type: `UInt32`  

 Access type: Read/Write  

 Qualifiers: [key]  

 See [SMS_G_System Server WMI Class](../../../../../develop/reference/core/clients/manage/sms_g_system-server-wmi-class.md).  

 `Type`  
 Data type: `UInt32`  

 Access type: Read-only  

 Qualifiers: None  

 Settings type. Possible values are:  

|||  
|-|-|  
|1|Device|  
|2|User|  

## Requirements  

## Runtime Requirements  
 For more information, see [Configuration Manager Server Runtime Requirements](../../../../../develop/core/reqs/server-runtime-requirements.md).  

## Development Requirements  
 For more information, see [Configuration Manager Server Development Requirements](../../../../../develop/core/reqs/server-development-requirements.md).  

## See Also  
 [Resource Management Server WMI Classes](../../../../../develop/reference/core/clients/manage/configuration-manager-resource-management-server-wmi-classes.md)
