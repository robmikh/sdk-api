---
UID: NF:d3d10.ID3D10Device.PSSetConstantBuffers
title: ID3D10Device::PSSetConstantBuffers (d3d10.h)
description: Set the constant buffers used by the pixel shader pipeline stage.
helpviewer_keywords: ["ID3D10Device interface [Direct3D 10]","PSSetConstantBuffers method","ID3D10Device.PSSetConstantBuffers","ID3D10Device::PSSetConstantBuffers","PSSetConstantBuffers","PSSetConstantBuffers method [Direct3D 10]","PSSetConstantBuffers method [Direct3D 10]","ID3D10Device interface","d3d10/ID3D10Device::PSSetConstantBuffers","direct3d10.id3d10device_pssetconstantbuffers","e734dbaf-deb3-e52f-f92f-645994c1bd7d"]
old-location: direct3d10\id3d10device_pssetconstantbuffers.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10device_pssetconstantbuffers.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Device interface [Direct3D 10],PSSetConstantBuffers method, ID3D10Device.PSSetConstantBuffers, ID3D10Device::PSSetConstantBuffers, PSSetConstantBuffers, PSSetConstantBuffers method [Direct3D 10], PSSetConstantBuffers method [Direct3D 10],ID3D10Device interface, d3d10/ID3D10Device::PSSetConstantBuffers, direct3d10.id3d10device_pssetconstantbuffers, e734dbaf-deb3-e52f-f92f-645994c1bd7d
f1_keywords:
- d3d10/ID3D10Device.PSSetConstantBuffers
dev_langs:
- c++
req.header: d3d10.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D10.lib
- D3D10.dll
api_name:
- ID3D10Device.PSSetConstantBuffers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Device::PSSetConstantBuffers


## -description


Set the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">constant buffers</a> used by the <a href="https://docs.microsoft.com/previous-versions/bb205146(v=vs.85)">pixel shader</a> pipeline stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the device's zero-based array to begin setting constant buffers to.


### -param NumBuffers [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers to set.


### -param ppConstantBuffers [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>*</b>

Array of constant buffers (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10buffer">ID3D10Buffer</a>) being given to the device.


## -remarks



The method will not hold a reference to the interfaces passed in. For that reason, applications should be careful not to release an interface currently in use by the device.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a>
 

 

