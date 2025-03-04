---
UID: NF:mfobjects.IMFAttributes.GetUINT32
title: IMFAttributes::GetUINT32 (mfobjects.h)
description: Retrieves a UINT32 value associated with a key.
helpviewer_keywords: ["GetUINT32","GetUINT32 method [Media Foundation]","GetUINT32 method [Media Foundation]","IMFAttributes interface","IMFAttributes interface [Media Foundation]","GetUINT32 method","IMFAttributes.GetUINT32","IMFAttributes::GetUINT32","e47495e0-3274-4ce2-9fd3-d2fb2afb7578","mf.imfattributes_getuint32","mfobjects/IMFAttributes::GetUINT32"]
old-location: mf\imfattributes_getuint32.htm
tech.root: mf
ms.assetid: e47495e0-3274-4ce2-9fd3-d2fb2afb7578
ms.date: 12/05/2018
ms.keywords: GetUINT32, GetUINT32 method [Media Foundation], GetUINT32 method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetUINT32 method, IMFAttributes.GetUINT32, IMFAttributes::GetUINT32, e47495e0-3274-4ce2-9fd3-d2fb2afb7578, mf.imfattributes_getuint32, mfobjects/IMFAttributes::GetUINT32
f1_keywords:
- mfobjects/IMFAttributes.GetUINT32
dev_langs:
- c++
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfuuid.lib
- mfuuid.dll
api_name:
- IMFAttributes.GetUINT32
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFAttributes::GetUINT32


## -description



Retrieves a <b>UINT32</b> value associated with a key.




## -parameters




### -param guidKey [in]

GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_UINT32</b>.


### -param punValue [out]

Receives a <b>UINT32</b> value. If the key is found and the data type is <b>UINT32</b>, the method copies the value into this parameter. Otherwise, the original value of this parameter is not changed.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified key was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">
The attribute value is not a <b>UINT32</b>.

</td>
</tr>
</table>
 




## -remarks



This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/attributes-and-properties">Attributes and Properties</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeuint32">MFGetAttributeUINT32</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type">MF_ATTRIBUTE_TYPE</a>
 

 

