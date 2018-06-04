---
title: IMimeHeaderTable FindFirstRow method
description: Begins to iterate through the row handles in the header table and finds the first header.
ms.assetid: e9202acd-13e5-4b55-a86b-4567938a000b
keywords:
- FindFirstRow method Windows Mail (formerly Outlook Express)
- FindFirstRow method Windows Mail (formerly Outlook Express) , IMimeHeaderTable interface
- IMimeHeaderTable interface Windows Mail (formerly Outlook Express) , FindFirstRow method
topic_type:
- apiref
api_name:
- IMimeHeaderTable.FindFirstRow
api_location:
- Inetcomm.dll
api_type:
- COM
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# IMimeHeaderTable::FindFirstRow method

Begins to iterate through the row handles in the header table and finds the first header.

## Syntax


```C++
HRESULT FindFirstRow(
  [in]  LPFINDHEADER pFindHeader,
  [out] LPHHEADERROW phRow
);
```



## Parameters

<dl> <dt>

*pFindHeader* \[in\]
</dt> <dd>

Type: **LPFINDHEADER**

Specifies a pointer to a [**FINDHEADER**](oe-findheader.md) structure.

</dd> <dt>

*phRow* \[out\]
</dt> <dd>

Type: **LPHHEADERROW**

Receives the handle of the header row.

</dd> </dl>

## Return value

Type: **HRESULT**

Returns one of the following values.



| Return code                                                                                        | Description                                                                   |
|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**S\_OK**</dt> </dl>               | Indicates success.<br/>                                                 |
| <dl> <dt>**E\_INVALIDARG**</dt> </dl>       | Indicates that *pFindHeader* or *phRow* is **NULL**. <br/>              |
| <dl> <dt>**MIME\_E\_NOT\_FOUND**</dt> </dl> | Indicates that *phRow* is invalid because there are no more rows. <br/> |



 

## Remarks

After a client calls this method, it should call [**IMimeHeaderTable::FindNextRow**](oe-imimeheadertable-findnextrow.md), with the same *pFindHeader* pointer to continue the iteration.

If *pFindHeader*-&gt;**pszHeader** is **NULL**, all the rows in the header table are iterated. Otherwise, only the headers whose names match *pFindHeader*-&gt;**pszHeader** are enumerated.

## Requirements



|                                     |                                                                                                                |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows XP \[desktop apps only\]<br/>                                                                    |
| Minimum supported server<br/> | Windows Server 2003 \[desktop apps only\]<br/>                                                           |
| Product<br/>                  | Outlook Express 6.0<br/>                                                                                 |
| Header<br/>                   | <dl> <dt>Mimeole.h</dt> </dl>                           |
| IDL<br/>                      | <dl> <dt>Mimeole.idl</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Inetcomm.dll (version 6.0 or later)</dt> </dl> |



 

 




