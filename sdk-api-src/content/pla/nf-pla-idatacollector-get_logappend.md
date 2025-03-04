---
UID: NF:pla.IDataCollector.get_LogAppend
title: IDataCollector::get_LogAppend (pla.h)
description: Retrieves or sets a value that indicates if PLA should append the collected data to the current file.
helpviewer_keywords: ["IDataCollector interface [PLA]","LogAppend property","IDataCollector.LogAppend","IDataCollector.get_LogAppend","IDataCollector::LogAppend","IDataCollector::get_LogAppend","IDataCollector::put_LogAppend","LogAppend property [PLA]","LogAppend property [PLA]","IDataCollector interface","base.idatacollector_logappend","get_LogAppend","pla.idatacollector_logappend","pla/IDataCollector::LogAppend","pla/IDataCollector::get_LogAppend","pla/IDataCollector::put_LogAppend"]
old-location: pla\idatacollector_logappend.htm
tech.root: PLA
ms.assetid: c9843647-2c36-4d08-98d0-4df63b054993
ms.date: 12/05/2018
ms.keywords: IDataCollector interface [PLA],LogAppend property, IDataCollector.LogAppend, IDataCollector.get_LogAppend, IDataCollector::LogAppend, IDataCollector::get_LogAppend, IDataCollector::put_LogAppend, LogAppend property [PLA], LogAppend property [PLA],IDataCollector interface, base.idatacollector_logappend, get_LogAppend, pla.idatacollector_logappend, pla/IDataCollector::LogAppend, pla/IDataCollector::get_LogAppend, pla/IDataCollector::put_LogAppend
f1_keywords:
- pla/IDataCollector.LogAppend
dev_langs:
- c++
req.header: pla.h
req.include-header: 
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
req.dll: Pla.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Pla.dll
api_name:
- IDataCollector.LogAppend
- IDataCollector.get_LogAppend
- IDataCollector.put_LogAppend
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollector::get_LogAppend


## -description


Retrieves or sets a value that indicates if PLA should append the collected data to the current file.

This property is read/write.


## -parameters


## -remarks



A validation error occurs if this property conflicts with the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logcircular">IDataCollector::LogCircular</a> or <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logoverwrite">IDataCollector::LogOverwrite</a> properties. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logcircular">IDataCollector::LogCircular</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logoverwrite">IDataCollector::LogOverwrite</a>
 

 

