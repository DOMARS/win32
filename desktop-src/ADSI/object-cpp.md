---
title: OBJECT.CPP
description: In the example provider component, a code example of object lists, including using a filter, is in Object.cpp. Supported methods are listed in the following table.
audience: developer
author: REDMOND\\markl
manager: REDMOND\\mbaldwin
ms.assetid: 'cb59ab96-c58e-47cb-9031-5432e83771bd'
ms.prod: 'windows-server-dev'
ms.technology: 'active-directory-domain-services'
ms.tgt_platform: multiple
keywords: ["OBJECT.CPP"]
---

# OBJECT.CPP

In the example provider component, a code example of object lists, including using a filter, is in Object.cpp. Supported methods are listed in the following table.



| Object                               | Description                                 |
|--------------------------------------|---------------------------------------------|
| **ObjectTypeList::ObjectTypeList**   | Creator: Build a list using the filter.     |
| **ObjectTypeList::~ObjectTypeList**  | Standard destructor.                        |
| **ObjectTypeList::GetCurrentObject** | Retrieve the current object from the list.  |
| **ObjectTypeList::Next**             | Bump the index.                             |
| **ObjectTypeList::Reset**            | Reset the index.                            |
| **IsValidFilter**                    | Check the integrity of the filter.          |
| **BuildDefaultObjectArray**          | Build an array of objects using the filter. |
| **BuildObjectArray**                 | Build an object array.                      |



 

 

 



