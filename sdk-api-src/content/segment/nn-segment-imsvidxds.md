---
UID: NN:segment.IMSVidXDS
title: IMSVidXDS (segment.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later. The IMSVidXDS interface provides access to the extended data services. The MSVidXDS feature exposes this interface.
helpviewer_keywords: ["IMSVidXDS","IMSVidXDS interface [Microsoft TV Technologies]","IMSVidXDS interface [Microsoft TV Technologies]","described","IMSVidXDSInterface","mstv.imsvidxds","segment/IMSVidXDS"]
old-location: mstv\imsvidxds.htm
tech.root: mstv
ms.assetid: ddd172fe-2f93-4b1b-b325-81be024bf74c
ms.date: 12/05/2018
ms.keywords: IMSVidXDS, IMSVidXDS interface [Microsoft TV Technologies], IMSVidXDS interface [Microsoft TV Technologies],described, IMSVidXDSInterface, mstv.imsvidxds, segment/IMSVidXDS
f1_keywords:
- segment/IMSVidXDS
dev_langs:
- c++
req.header: segment.h
req.include-header: Msvidctl.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Segment.idl
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
- COM
api_location:
- segment.h
api_name:
- IMSVidXDS
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMSVidXDS interface


## -description




<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 or later.</div>
<div> </div>


The <b>IMSVidXDS</b> interface provides access to the extended data services. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dd695263(v=vs.85)">MSVidXDS</a> feature exposes this interface.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMSVidXDS</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>. <b>IMSVidXDS</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMSVidXDS</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/segment/nf-segment-imsvidxds-get_channelchangeinterface">get_ChannelChangeInterface</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the channel change interface.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IMSVidXDS)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/msvidfeature">IMSVidFeature</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/video-control-interfaces">Video Control Interfaces</a>
 

 

