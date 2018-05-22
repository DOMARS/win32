---
title: MetricValueCollection AddItem method
description: Creates and adds a MetricValue whose value is an INT.
ms.assetid: 'A6578E8B-EA3A-49D9-B434-65E76221A686'
keywords: ["AddItem method Access Execution Engine", "AddItem method Access Execution Engine , MetricValueCollection interface", "MetricValueCollection interface Access Execution Engine , AddItem method"]
topic_type:
- apiref
api_name:
- MetricValueCollection.AddItem
api_location:
- AxeCore.dll
api_type:
- COM
---

# MetricValueCollection::AddItem method

Creates and adds a [**MetricValue**](metricvalue-struct.md) whose value is an **INT**.

## Syntax


```C++
virtual HRESULT AddItem(
  [in]������������LPCWSTR ����programmaticName,
  [in]������������INT ��������value,
  [out, optional]�MetricValue **metricValue
) = 0;
```



## Parameters

<dl> <dt>

*programmaticName* \[in\]
</dt> <dd>

The programmatic name.

</dd> <dt>

*value* \[in\]
</dt> <dd>

The value.

</dd> <dt>

*metricValue* \[out, optional\]
</dt> <dd>

The **MetricValue** that this method creates.

</dd> </dl>

## Return value

If the function succeeds, it returns **S\_OK**. If it fails, it returns an error value.

## Remarks

A **MetricValueCollection** holds data from an **Issue/MetricValues**, **Iteration/MetricValues**, or **TestCase/MetricValues** element.

A **MetricValue** object holds data from a **MetricValues/MetricValue** element.

The programmatic name is the value of element **MetricValue/ProgrammaticName**.

The value is the value of element **MetricValue/Value**.

## Requirements



|                                     |                                                                                         |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Minimum supported client<br/> | Windows�7 \[desktop apps only\]<br/>                                              |
| Minimum supported server<br/> | Windows Server�2008�R2 \[desktop apps only\]<br/>                                 |
| Header<br/>                   | <dl> <dt>AxeRuntime.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>AxeCore.dll</dt> </dl>  |



## See also

<dl> <dt>

[**MetricValueCollection**](metricvaluecollection.md)
</dt> </dl>

�

�




