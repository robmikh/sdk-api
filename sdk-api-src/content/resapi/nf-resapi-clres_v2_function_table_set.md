---
UID: NF:resapi.CLRES_V2_FUNCTION_TABLE_SET
title: CLRES_V2_FUNCTION_TABLE_SET macro (resapi.h)
description: Initializes a function table for version 2.0 of the Resource API.
helpviewer_keywords: ["CLRES_V2_FUNCTION_TABLE_SET","CLRES_V2_FUNCTION_TABLE_SET macro [Failover Cluster]","mscs.clres_v2_function_table_set","resapi/CLRES_V2_FUNCTION_TABLE_SET"]
old-location: mscs\clres_v2_function_table_set.htm
tech.root: MsCS
ms.assetid: DFBCD256-F4E0-4C78-AD4A-54A229B40C5E
ms.date: 12/05/2018
ms.keywords: CLRES_V2_FUNCTION_TABLE_SET, CLRES_V2_FUNCTION_TABLE_SET macro [Failover Cluster], mscs.clres_v2_function_table_set, resapi/CLRES_V2_FUNCTION_TABLE_SET
f1_keywords:
- resapi/CLRES_V2_FUNCTION_TABLE_SET
dev_langs:
- c++
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
- ResApi.h
api_name:
- CLRES_V2_FUNCTION_TABLE_SET
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CLRES_V2_FUNCTION_TABLE_SET macro


## -description


Initializes a 
    function table for version 2.0 of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-api">Resource API</a>.


## -parameters




### -param _Name

The name of the function table.


### -param _Version

The version of the function table, such as <b>CLRES_VERSION_V2_00</b>.


### -param _Prefix

The prefix that is appended to the front of each entry point name in the function table.


### -param _Arbitrate

The name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-parbitrate_routine">Arbitrate</a> entry point.


### -param _Release

The name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-prelease_routine">Release</a> entry point.


### -param _ResControl

The name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_control_routine">ResourceControl</a> entry point.


### -param _ResTypeControl

The name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-presource_type_control_routine">ResourceTypeControl</a> entry 
       point.


### -param _LooksAlive

The name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-plooks_alive_routine">LooksAlive</a> entry 
       point.


### -param _IsAlive

The name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pis_alive_routine">IsAlive</a> entry 
       point.


### -param _Cancel

The name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pcancel_routine">Cancel</a> entry 
       point.


## -remarks



The <b>CLRES_V2_FUNCTION_TABLE_SET</b> macro creates a 
     function table for version 2.0 of the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/resource-api">Resource API</a> using the version specified by the 
     <i>Version</i> parameter and the label specified by the <i>Name</i> 
     parameter. The actual names of the entry points are generated by combining the prefix specified in the 
     <i>Prefix</i> parameter with the generic names as defined in the Resource API. For example, if 
     <i>Prefix</i> is set to the string "FileShare", then the name of the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_routine">Open</a> function would be "FileShareOpen". The optional entry point functions may be set to <b>NULL</b>.

The resulting function table includes the following members.

<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td>
<i>Prefix</i>

</td>
<td>
Name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-popen_v2_routine">OpenV2</a> entry point.

</td>
</tr>
<tr>
<td>
<i>Prefix</i>

</td>
<td>
Name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pclose_routine">Close</a> entry point.

</td>
</tr>
<tr>
<td>
<i>Prefix</i>

</td>
<td>
Name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-ponline_v2_routine">OnlineV2</a> entry point.

</td>
</tr>
<tr>
<td>
<i>Prefix</i>

</td>
<td>
Name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-poffline_v2_routine">OfflineV2</a> entry point.

</td>
</tr>
<tr>
<td>
<i>Prefix</i>

</td>
<td>
Name of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/nc-resapi-pterminate_routine">Terminate</a> entry point.

</td>
</tr>
</table>
 

To view the format of the function table, see the 
     <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/resapi/ns-resapi-clres_function_table">CLRES_FUNCTION_TABLE</a> structure.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mscs/macros">Failover Cluster Macros</a>
 

 

