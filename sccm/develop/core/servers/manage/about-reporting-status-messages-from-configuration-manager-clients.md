---
title: "Reporting Status Messages from Clients | Microsoft Docs"
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
ms.assetid: 4a5c2726-4ad8-4f94-95ba-acc24cc61faa
caps.latest.revision: 5
author: "shill-ms"
ms.author: "v-suhill"
manager: "mbaldwin"
---
# About Reporting Status Messages from Configuration Manager Clients
You can raise System Center Configuration Manager client status messages in the Windows event log by using a compiled Managed Object Format (MOF) file on client computers. This can be useful for administrators who are managing servers with System Center Operations Manager. A System Center Configuration Manager status message that is raised by the System Center Configuration Manager client can be caught by the Operations Manager agent on the same computer, which in turn raises an Operations Manager alert for the System Center Configuration Manager status message.  

 The following example MOF file shows how to raise System Center Configuration Manager program status messages:  

```  
#pragma namespace("\\\\.\\root\\ccm\\policy\\machine\\requestedconfig")  
instance of CCM_EventForwarder_Configuration  
{  
    InstanceID = "SmsSoftwareDistribution.EventLog";  
    Name = "SmsEventLogForwarder";  
    PolicyID = "SomePolicyID";  
    PolicyInstanceID = "SomePolicyInstance";  
    PolicyRuleID = "SomeRuleID";  
    PolicySource = "Local";  
    PolicyVersion = "1";  
        QueryList           = {  
                            "SELECT * FROM SoftDistProgramStartedEvent",  
                            "SELECT * FROM SoftDistProgramCompletedSuccessfullyEvent",  
                            "SELECT * FROM SoftDistProgramCompletedSuccessfulMIFEvent",  
                            "SELECT * FROM SoftDistProgramErrorEvent",  
                            "SELECT * FROM SoftDistProgramErrorMIFEvent",  
                            "SELECT * FROM SoftDistProgramExceededTime",  
                            "SELECT * FROM SoftDistProgramPrelimSuccessEvent",  
                            "SELECT * FROM SoftDistProgramUnexpectedRebootEvent",  
                            "SELECT * FROM SoftDistWarningProgramErrorEvent"  
                            };    
};  
```  

## See Also  
 [About Configuration Manager Status Summarizers](../../../../develop/core/servers/manage/about-configuration-manager-status-summarizers.md)
