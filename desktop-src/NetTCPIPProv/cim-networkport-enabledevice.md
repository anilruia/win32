---
Description: The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.
ms.assetid: bcf7a9a2-76ca-44c8-8f0b-ad391a0cbaa5
title: EnableDevice method of the CIM\_NetworkPort class
ms.technology: desktop
ms.prod: windows
ms.author: windowssdkdev
ms.topic: article
ms.date: 05/31/2018
---

# EnableDevice method of the CIM\_NetworkPort class

The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.

Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE). If successful, the Device\\'s StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled). Note that this method\\'s function overlaps with the RequestedState property. RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request. Invoking the EnableDevice method should set the RequestedState property appropriately.

The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred. In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method. The strings to which the ValueMap contents are \\'translated\\' may also be specified in the subclass as a Values array qualifier.

## Syntax


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## Parameters

<dl> <dt>

*Enabled* \[in\]
</dt> <dd>

If TRUE enable the device, if FALSE disable the device.

</dd> </dl>

## Return value

TBD

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows 8<br/>                                                                    |
| Minimum supported server<br/> | Windows Server 2012<br/>                                                          |
| Namespace<br/>                | Root\\standardcimv2<br/>                                                          |
| MOF<br/>                      | <dl> <dt>NetTCPIP.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>NetTCPIP.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_NetworkPort**](cim-networkport.md)
</dt> </dl>

 

 



