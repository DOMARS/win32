---
title: Publishing Under a Computer Object
description: Typically, host-based services create SCPs under the computer object for the host computer. Host-based services are services closely tied to a single host computer.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: 'ecd7d8bc-4714-408a-856c-7cab8360bf81'
ms.prod: 'windows-server-dev'
ms.technology: 'active-directory-domain-services'
ms.tgt_platform: multiple
---

# Publishing Under a Computer Object

Typically, host-based services create SCPs under the computer object for the host computer. Host-based services are services closely tied to a single host computer.

**To create SCPs under a computer object**

1.  Call the [**GetComputerObjectName**](https://msdn.microsoft.com/library/windows/desktop/ms724304) function to get the distinguished name (DN) in the directory of the computer object for the local computer.
2.  Use that DN to bind to the computer object and create the SCP.

For more information and a code example, see [How Clients Find and Use a Service Connection Point](how-clients-find-and-use-a-service-connection-point.md).

Be aware that only domain-member computers have valid computer objects in the directory.

To get the DNS or NetBIOS name of the local computer, call the [**GetComputerNameEx**](https://msdn.microsoft.com/library/windows/desktop/ms724301) function.

 

 



