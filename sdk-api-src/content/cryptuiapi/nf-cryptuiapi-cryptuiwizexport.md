---
UID: NF:cryptuiapi.CryptUIWizExport
title: CryptUIWizExport function (cryptuiapi.h)
description: Exports a certificate, a certificate trust list (CTL), a certificate revocation list (CRL), or a certificate store to a file.
helpviewer_keywords: ["CRYPTUI_WIZ_EXPORT_NO_DELETE_PRIVATE_KEY","CRYPTUI_WIZ_EXPORT_PRIVATE_KEY","CRYPTUI_WIZ_IGNORE_NO_UI_FLAG_FOR_CSPS","CRYPTUI_WIZ_NO_UI","CRYPTUI_WIZ_NO_UI_EXCEPT_CSP","CryptUIWizExport","CryptUIWizExport function [Security]","cryptuiapi/CryptUIWizExport","security.cryptuiwizexport"]
old-location: security\cryptuiwizexport.htm
tech.root: security
ms.assetid: 62537d51-c761-4180-b857-58c819ea66aa
ms.date: 12/05/2018
ms.keywords: CRYPTUI_WIZ_EXPORT_NO_DELETE_PRIVATE_KEY, CRYPTUI_WIZ_EXPORT_PRIVATE_KEY, CRYPTUI_WIZ_IGNORE_NO_UI_FLAG_FOR_CSPS, CRYPTUI_WIZ_NO_UI, CRYPTUI_WIZ_NO_UI_EXCEPT_CSP, CryptUIWizExport, CryptUIWizExport function [Security], cryptuiapi/CryptUIWizExport, security.cryptuiwizexport
f1_keywords:
- cryptuiapi/CryptUIWizExport
dev_langs:
- c++
req.header: cryptuiapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptui.lib
req.dll: Cryptui.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Cryptui.dll
api_name:
- CryptUIWizExport
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CryptUIWizExport function


## -description


The <b>CryptUIWizExport</b> function exports a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate</a>, a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL), a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL), or a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate store</a> to a file. The export can be performed with or without user interaction.


## -parameters




### -param dwFlags [in]

 Contains flags that modify the behavior of the function. This can be zero or a combination of one or more of the following values.

<div class="alert"><b>Note</b>  Except for <b>CRYPTUI_WIZ_NO_UI</b>, none of the following constants are defined in a published header file. To use these constants, you must define them by using the specified values.</div>
<div> </div>
<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_NO_UI"></a><a id="cryptui_wiz_no_ui"></a><dl>
<dt><b>CRYPTUI_WIZ_NO_UI</b></dt>
<dt>0x0001</dt>
</dl>
</td>
<td width="60%">
This function will perform the export based on the information in the <a href="https://docs.microsoft.com/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_info">CRYPTUI_WIZ_EXPORT_INFO</a> structure pointed to by <i>pExportInfo</i> without displaying any user interface. If this flag is not specified, this function will display a wizard to guide the user through the export process.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_IGNORE_NO_UI_FLAG_FOR_CSPS"></a><a id="cryptui_wiz_ignore_no_ui_flag_for_csps"></a><dl>
<dt><b>CRYPTUI_WIZ_IGNORE_NO_UI_FLAG_FOR_CSPS</b></dt>
<dt>0x0002</dt>
</dl>
</td>
<td width="60%">
Suppress all user interfaces generated by <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs). This option can be overridden by the <b>CRYPTUI_WIZ_NO_UI_EXCEPT_CSP</b> option.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_NO_UI_EXCEPT_CSP"></a><a id="cryptui_wiz_no_ui_except_csp"></a><dl>
<dt><b>CRYPTUI_WIZ_NO_UI_EXCEPT_CSP</b></dt>
<dt>0x0003</dt>
</dl>
</td>
<td width="60%">
Suppress all user interfaces except those generated by CSPs. This option overrides the <b>CRYPTUI_WIZ_IGNORE_NO_UI_FLAG_FOR_CSPS</b> option.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_PRIVATE_KEY"></a><a id="cryptui_wiz_export_private_key"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_PRIVATE_KEY</b></dt>
<dt>0x0100</dt>
</dl>
</td>
<td width="60%">
Skip the <b>Export Private Key</b> page and assume that the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">private key</a> is to be exported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTUI_WIZ_EXPORT_NO_DELETE_PRIVATE_KEY"></a><a id="cryptui_wiz_export_no_delete_private_key"></a><dl>
<dt><b>CRYPTUI_WIZ_EXPORT_NO_DELETE_PRIVATE_KEY</b></dt>
<dt>0x0200</dt>
</dl>
</td>
<td width="60%">
Disable the <b>Delete the private key</b> check box in the <b>Export File Format</b> page.

</td>
</tr>
</table>
 


### -param hwndParent [in]

The handle of the window to use as the parent of the dialog box that this function creates. This parameter is ignored if the <b>CRYPT_WIZ_NO_UI</b> flag is set in <i>dwFlags</i>.


### -param pwszWizardTitle [in]

A pointer to a null-terminated Unicode string that contains the title to use in the dialog box that this function creates. This parameter is ignored if the <b>CRYPT_WIZ_NO_UI</b> flag is set in <i>dwFlags</i>.


### -param pExportInfo [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_info">CRYPTUI_WIZ_EXPORT_INFO</a> structure that contains information about producing the export wizard.


### -param pvoid [in]

If the <b>dwSubjectChoice</b> member of  the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_certcontext_info">CRYPTUI_WIZ_EXPORT_INFO</a> structure that <i>pExportInfo</i> references is <b>CRYPTUI_WIZ_EXPORT_CERT_CONTEXT</b>, and if the  <b>CRYPTUI_WIZ_NO_UI</b> flag is set in <i>dwFlags</i>, this parameter is a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_certcontext_info">CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO</a> structure. 

If the <b>CRYPTUI_WIZ_NO_UI</b> flag is not set in <i>dwFlags</i>, this parameter is optional and can be <b>NULL</b>. If this parameter is not <b>NULL</b>, the <a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_certcontext_info">CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO</a> structure contains the values that are displayed to the user as the default choices.


## -returns



If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
the <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.




## -see-also




<a href="/windows/win32/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_certcontext_info">CRYPTUI_WIZ_EXPORT_CERTCONTEXT_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cryptuiapi/ns-cryptuiapi-cryptui_wiz_export_info">CRYPTUI_WIZ_EXPORT_INFO</a>



<a href="https://docs.microsoft.com/windows/desktop/api/cryptuiapi/nf-cryptuiapi-cryptuiwizimport">CryptUIWizImport</a>
 

 

