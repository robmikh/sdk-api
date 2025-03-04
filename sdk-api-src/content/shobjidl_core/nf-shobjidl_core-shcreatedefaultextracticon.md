---
UID: NF:shobjidl_core.SHCreateDefaultExtractIcon
title: SHCreateDefaultExtractIcon function (shobjidl_core.h)
description: Creates a standard icon extractor, whose defaults can be further configured via the IDefaultExtractIconInit interface.
helpviewer_keywords: ["SHCreateDefaultExtractIcon","SHCreateDefaultExtractIcon function [Windows Shell]","_shell_SHCreateDefaultExtractIcon","shell.SHCreateDefaultExtractIcon","shobjidl_core/SHCreateDefaultExtractIcon"]
old-location: shell\SHCreateDefaultExtractIcon.htm
tech.root: shell
ms.assetid: 483dc9ae-4820-47f1-888e-ad7a6bdf3d29
ms.date: 12/05/2018
ms.keywords: SHCreateDefaultExtractIcon, SHCreateDefaultExtractIcon function [Windows Shell], _shell_SHCreateDefaultExtractIcon, shell.SHCreateDefaultExtractIcon, shobjidl_core/SHCreateDefaultExtractIcon
f1_keywords:
- shobjidl_core/SHCreateDefaultExtractIcon
dev_langs:
- c++
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Shell32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Shell32.dll
- ext-ms-win-shell-shell32-l1-2-1.dll
- Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
- SHCreateDefaultExtractIcon
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SHCreateDefaultExtractIcon function


## -description


Creates a standard icon extractor, whose defaults can be further configured via the <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit">IDefaultExtractIconInit</a> interface.


## -parameters




### -param riid

Type: <b>REFIID</b>

A reference to interface ID.


### -param ppv [out]

Type: <b>void**</b>

The address of <a href="https://docs.microsoft.com/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idefaultextracticoninit">IDefaultExtractIconInit</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The intended usage for this function is as follows:
            
                


```
IExtractIcon *pxi;

IDefaultExtractIconInit *pdxi;

HRESULT hr = SHCreateDefaultExtractIcon(IID_PPV_ARGS(&pdxi);

 if (SUCCEEDED(hr)) &&

      SUCCEEDED(hr = pdxi->SetFlags(GIL_PERCLASS)) &&

      SUCCEEDED(hr = pdxi->SetKey(hkey)) &&   // optional

      SUCCEEDED(hr = pdxi->SetNormalIcon(L"this.dll", 1)) &&

      SUCCEEDED(hr = pdxi->SetOpenIcon(NULL, SIID_FOLDEROPEN)) && // optional

      SUCCEEDED(hr = pdxi->SetDefaultIcon(NULL, SIID_FOLDER)) && // optional

      SUCCEEDED(hr = pdxi->SetShortcutIcon(L"this.dll", 2))) // optional

{

      hr = pdxi->QueryInterface(IID_PPV_ARGS(&pxi)) 

}

 if (pdxi)

{

    pdxi->Release();

}
```




