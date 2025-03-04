---
UID: NF:mi.MI_DestinationOptions_SetNumber
title: MI_DestinationOptions_SetNumber function (mi.h)
description: Sets a custom numeric option value.
helpviewer_keywords: ["MI_DestinationOptions_SetNumber","MI_DestinationOptions_SetNumber function [Windows Management Infrastructure (MI)]","mi/MI_DestinationOptions_SetNumber","wmi_v2.mi_destinationoptions_setnumber"]
old-location: wmi_v2\mi_destinationoptions_setnumber.htm
tech.root: wmi_v2
ms.assetid: 46e81ecd-7fb5-465a-8caa-04288c559fea
ms.date: 12/05/2018
ms.keywords: MI_DestinationOptions_SetNumber, MI_DestinationOptions_SetNumber function [Windows Management Infrastructure (MI)], mi/MI_DestinationOptions_SetNumber, wmi_v2.mi_destinationoptions_setnumber
f1_keywords:
- mi/MI_DestinationOptions_SetNumber
dev_langs:
- c++
req.header: mi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Mi.h
api_name:
- MI_DestinationOptions_SetNumber
targetos: Windows
req.typenames: 
req.redist: Windows Management Framework 3.0 on Windows Server 2008 R2 with SP1, Windows 7 with SP1, and Windows Server 2008 with SP2
ms.custom: 19H1
---

# MI_DestinationOptions_SetNumber function


## -description


Sets a custom numeric option value.


## -parameters




### -param options [in, out]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a> object returned from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a> function.


### -param optionName

A null-terminated string that represents the name of option to set.


### -param optionValue [in]

New option value.


## -returns



A value of the <a href="https://docs.microsoft.com/windows/desktop/api/mi/ne-mi-mi_result">MI_Result</a> enumeration that specifies the function return code. This can be one of the following codes.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_application_newdestinationoptions">MI_Application_NewDestinationOptions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mi/ns-mi-mi_destinationoptions">MI_DestinationOptions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/mi/nf-mi-mi_destinationoptions_getnumber">MI_DestinationOptions_GetNumber</a>
 

 

