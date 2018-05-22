---
title: EnableDevice method of the CIM\_LogicalPort class
description: The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\markl
ms.assetid: '9eafaf5c-eae2-4923-94a5-1b2069b32942'
ms.prod: 'windows-server-dev'
ms.technology:
- 'iscsi-target'
- 'windows-management-instrumentation'
ms.tgt_platform: multiple
keywords: ["EnableDevice method iSCSI Software Target API", "EnableDevice method iSCSI Software Target API , CIM_LogicalPort class", "CIM_LogicalPort class iSCSI Software Target API , EnableDevice method"]
topic_type:
- apiref
api_name:
- CIM_LogicalPort.EnableDevice
api_location:
- SMiSCSITargetProv.dll
api_type:
- COM
---

# EnableDevice method of the CIM\_LogicalPort class

The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method. Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE). If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled). Note that this method's function overlaps with the RequestedState property. RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request. Invoking the EnableDevice method should set the RequestedState property appropriately. The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred. In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method. The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.

## Syntax


```mof
uint32 EnableDevice(
  [in]�boolean Enabled
);
```



## Parameters

<dl> <dt>

*Enabled* \[in\]
</dt> <dd>

If TRUE enable the device, if FALSE disable the device.

</dd> </dl>

## Requirements



|                                     |                                                                                                  |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Minimum supported client<br/> | None supported<br/>                                                                        |
| Minimum supported server<br/> | Windows Server�2012�R2<br/>                                                                |
| Namespace<br/>                | Root\\CIMv2\\Storage\\iScsiTarget<br/>                                                     |
| MOF<br/>                      | <dl> <dt>SmIscsiTarget.mof</dt> </dl>     |
| DLL<br/>                      | <dl> <dt>SMiSCSITargetProv.dll</dt> </dl> |



## See also

<dl> <dt>

[**CIM\_LogicalPort**](cim-logicalport.md)
</dt> </dl>

�

�




