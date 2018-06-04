---
title: MMCN\_MINIMIZED message
description: The MMCN\_MINIMIZED notification message is sent to the snap-in's IComponent implementation when a window for which it owns the result pane is being minimized or maximized.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: 54fccd83-aa89-4b9d-a9fe-145b850f455c
ms.prod: windows-server-dev
ms.technology: microsoft-management-console
ms.tgt_platform: multiple
keywords:
- MMCN_MINIMIZED message MMC
topic_type:
- apiref
api_name:
- MMCN_MINIMIZED
api_location:
- Mmc.h
api_type:
- HeaderDef
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# MMCN\_MINIMIZED message

The **MMCN\_MINIMIZED** notification message is sent to the snap-in's [**IComponent**](/windows/desktop/api/Mmc/nn-mmc-icomponent) implementation when a window for which it owns the result pane is being minimized or maximized.

## Parameters

<dl> <dt>

*lpDataObject* \[in\]
</dt> <dd>

A pointer to the data object of the currently selected scope item.

</dd> <dt>

*arg* 
</dt> <dd>

**TRUE** if the window has been minimized; otherwise **FALSE**.

</dd> <dt>

*param* 
</dt> <dd>

Not used.

</dd> </dl>

## Return value

<dl> <dt>

**S\_OK**
</dt> <dd>

The snap-in successfully handled the notification.

</dd> <dt>

**S\_FALSE**
</dt> <dd>

The snap-in does not handle the notification. MMC then performs a default operation for the notification.

</dd> </dl>

## Requirements



|                                     |                                                                                  |
|-------------------------------------|----------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows Vista<br/>                                                         |
| Minimum supported server<br/> | Windows Server 2008<br/>                                                   |
| Header<br/>                   | <dl> <dt>Mmc.h</dt> </dl> |



## See also

<dl> <dt>

[**IComponent::Notify**](/windows/desktop/api/Mmc/nf-mmc-icomponent-notify)
</dt> </dl>

 

 




