---
title: "GetImageProperties Method in SMS_ImagePackage | Microsoft Docs"
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
ms.assetid: 5a94ccee-0516-41f0-b947-52d4c8f27d55
caps.latest.revision: 7
author: "shill-ms"
ms.author: "v-suhill"
manager: "mbaldwin"
---
# GetImageProperties Method in Class SMS_ImagePackage
The `GetImageProperties` Windows Management Instrumentation (WMI) class method, in Configuration Manager, reads all metadata from the specified .wim source file for an image to an XML string.  

 The following syntax is simplified from Managed Object Format (MOF) code and defines the method.  

## Syntax  

```  
SInt32 GetImageProperties(  
      String SourceImagePath,  
      String ImageProperty  
);  
```  

#### Parameters  
 `SourceImagePath`  
 Data type: `String`  

 Qualifiers: [in]  

 Path to the .wim source file to query for metadata, for example, \\\server\share\boot.wim.  

 `ImageProperty`  
 Data type: `String`  

 Qualifiers: [out]  

 XML document containing the image metadata.  

## Return Values  
 An `SInt32` data type that is 0 to indicate success or non-zero to indicate failure.  

 For information about handling returned errors, see [About Configuration Manager Errors](../../../develop/core/understand/about-configuration-manager-errors.md).  

## Remarks  
 This method accesses the source .wim file metadata by using the `ImageProperty` property of [SMS_ImagePackage Server WMI Class](../../../develop/reference/osd/sms_imagepackage-server-wmi-class.md). For more information, see [How to View the Properties for an Operating System Image](../../../develop/osd/how-to-view-the-properties-for-an-operating-system-image.md).  

## Requirements  

## Runtime Requirements  
 For more information, see [Configuration Manager Server Runtime Requirements](../../../develop/core/reqs/server-runtime-requirements.md).  

## Development Requirements  
 For more information, see [Configuration Manager Server Development Requirements](../../../develop/core/reqs/server-development-requirements.md).  

## See Also  
 [SMS_ImagePackage Server WMI Class](../../../develop/reference/osd/sms_imagepackage-server-wmi-class.md)   
 [ReloadImageProperties Method in Class SMS_ImagePackage](../../../develop/reference/osd/reloadimageproperties-method-in-class-sms_imagepackage.md)
