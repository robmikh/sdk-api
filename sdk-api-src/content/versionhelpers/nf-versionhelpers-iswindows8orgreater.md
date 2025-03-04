---
UID: NF:versionhelpers.IsWindows8OrGreater
title: IsWindows8OrGreater function (versionhelpers.h)
description: Indicates if the current OS version matches, or is greater than, the Windows 8 version.
helpviewer_keywords: ["IsWindows8OrGreater","IsWindows8OrGreater function","base.iswindows8orgreater","versionhelpers/IsWindows8OrGreater"]
old-location: base\iswindows8orgreater.htm
tech.root: winprog
ms.assetid: D11971C8-2E8F-4AD2-BE0B-FEFEC8949125
ms.date: 12/05/2018
ms.keywords: IsWindows8OrGreater, IsWindows8OrGreater function, base.iswindows8orgreater, versionhelpers/IsWindows8OrGreater
f1_keywords:
- versionhelpers/IsWindows8OrGreater
dev_langs:
- c++
req.header: versionhelpers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Kernel32.lib; Ntdll.lib
req.dll: Kernel32.dll; Ntdll.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Kernel32.dll
- ntdll.dll
api_name:
- IsWindows8OrGreater
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IsWindows8OrGreater function


## -description


Indicates  if the current OS version matches, or is greater than, the Windows 8 version.


## -parameters






## -returns



True if the current OS version matches, or is greater than, the Windows 8 version; otherwise, false.




## -remarks



This function does not differentiate between client and server releases.  It will return <b>true</b> if the current OS version number is equal to or higher than the version of the client named in the call. For example,  a call to <a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp3orgreater">IsWindowsXPSP3OrGreater</a> will return <b>true</b> on Windows Server 2008. Applications that need to distinguish between server and client versions of Windows should call <a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsserver">IsWindowsServer</a>.

For situations where a Windows Server version number isn't shared with a Windows client release, you can use <a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsversionorgreater">IsWindowsVersionOrGreater</a> to confirm.


#### Examples

The inline functions defined in the <b>VersionHelpers.h</b> header file let you verify the operating system version by returning a <b>Boolean</b> value when testing for a version of Windows.

For example, if your application requires Windows 8 or later, use the following test.


```cpp
#include <VersionHelpers.h>
…
    if (!IsWindows8OrGreater())
    {
       MessageBox(NULL, "You need at least Windows 8", "Version Not Supported", MB_OK);
    }

```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7orgreater">IsWindows7OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows7sp1orgreater">IsWindows7SP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindows8point1orgreater">IsWindows8Point1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsserver">IsWindowsServer</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistaorgreater">IsWindowsVistaOrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp1orgreater">IsWindowsVistaSP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsvistasp2orgreater">IsWindowsVistaSP2OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxporgreater">IsWindowsXPOrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp1orgreater">IsWindowsXPSP1OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp2orgreater">IsWindowsXPSP2OrGreater</a>



<a href="https://docs.microsoft.com/windows/desktop/api/versionhelpers/nf-versionhelpers-iswindowsxpsp3orgreater">IsWindowsXPSP3OrGreater</a>
 

 

