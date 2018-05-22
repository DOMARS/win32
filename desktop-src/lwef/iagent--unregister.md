---
title: IAgent Unregister
description: IAgent Unregister
ms.assetid: 'd81cde72-f9ff-45aa-9dbf-faea9a478c3c'
---

# IAgent::Unregister

\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]

``` syntax
HRESULT Unregister(
   long dwSinkID  //notification sink ID
);
```

Unloads the character data for the specified character from the [**Characters**](https://msdn.microsoft.com/library/windows/desktop/ms696372) collection.

-   Returns S\_OK to indicate the operation was successful.

<dl> <dt>

<span id="dwSinkID"></span><span id="dwsinkid"></span><span id="DWSINKID"></span>*dwSinkID*
</dt> <dd>

The notification sink ID.

</dd> </dl>

Use this method when you no longer need Microsoft Agent services, such as when your application shuts down.

## See Also

[**IAgent::Register**](iagent--register.md)


 

 



