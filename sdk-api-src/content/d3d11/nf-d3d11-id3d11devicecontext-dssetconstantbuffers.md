---
UID: NF:d3d11.ID3D11DeviceContext.DSSetConstantBuffers
title: ID3D11DeviceContext::DSSetConstantBuffers (d3d11.h)
description: Sets the constant buffers used by the domain-shader stage.
helpviewer_keywords: ["13e5cd44-c36b-5d23-3dc8-d47d8d5bbce9","DSSetConstantBuffers","DSSetConstantBuffers method [Direct3D 11]","DSSetConstantBuffers method [Direct3D 11]","ID3D11DeviceContext interface","ID3D11DeviceContext interface [Direct3D 11]","DSSetConstantBuffers method","ID3D11DeviceContext.DSSetConstantBuffers","ID3D11DeviceContext::DSSetConstantBuffers","d3d11/ID3D11DeviceContext::DSSetConstantBuffers","direct3d11.id3d11devicecontext_dssetconstantbuffers"]
old-location: direct3d11\id3d11devicecontext_dssetconstantbuffers.htm
tech.root: direct3d11
ms.assetid: ae2b8269-59b0-44e9-8173-89baf20436f1
ms.date: 12/05/2018
ms.keywords: 13e5cd44-c36b-5d23-3dc8-d47d8d5bbce9, DSSetConstantBuffers, DSSetConstantBuffers method [Direct3D 11], DSSetConstantBuffers method [Direct3D 11],ID3D11DeviceContext interface, ID3D11DeviceContext interface [Direct3D 11],DSSetConstantBuffers method, ID3D11DeviceContext.DSSetConstantBuffers, ID3D11DeviceContext::DSSetConstantBuffers, d3d11/ID3D11DeviceContext::DSSetConstantBuffers, direct3d11.id3d11devicecontext_dssetconstantbuffers
f1_keywords:
- d3d11/ID3D11DeviceContext.DSSetConstantBuffers
dev_langs:
- c++
req.header: d3d11.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D11.lib
- D3D11.dll
api_name:
- ID3D11DeviceContext.DSSetConstantBuffers
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11DeviceContext::DSSetConstantBuffers


## -description


Sets the constant buffers used by the domain-shader stage.


## -parameters




### -param StartSlot [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index into the zero-based array to begin setting constant buffers to (ranges from 0 to <b>D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT</b> - 1).
          


### -param NumBuffers [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers to set (ranges from 0 to <b>D3D11_COMMONSHADER_CONSTANT_BUFFER_API_SLOT_COUNT</b> - <i>StartSlot</i>).
          


### -param ppConstantBuffers [in, optional]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>*</b>

Array of constant buffers (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a>) being given to the device.
          


## -remarks



The method will hold a reference to the interfaces passed in.
          This differs from the device state behavior in Direct3D 10.
        

The Direct3D 11.1 runtime, which is available starting with Windows 8, can bind a larger number of <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11buffer">ID3D11Buffer</a> resources to the shader than the maximum constant buffer size that is supported by shaders (4096 constants – 4*32-bit components each).  When you bind such a large buffer, the shader can access only the first 4096 4*32-bit component constants in the buffer, as if 4096 constants is the full size of the buffer.
        

If the application wants the shader to access other parts of the buffer, it must call the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11devicecontext1-dssetconstantbuffers1">DSSetConstantBuffers1</a> method instead.
        

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>
 

 

