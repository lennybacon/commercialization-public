---
title: IControlErrorInfo
description: IControlErrorInfo
MSHAttr:
- 'PreferredSiteName:MSDN'
- 'PreferredLib:/library/windows/hardware'
ms.assetid: 47dd2be1-9217-4045-b530-c8b022c3c794
ms.mktglfcycl: operate
ms.sitesec: msdn
ms.author: dawnwood
ms.date: 05/05/2017
ms.topic: article


---

# IControlErrorInfo


Provides functions that obtain information about errors that occur when the control manager performs an operation. The error indicates the type of object on which the error occurred: profile, collector, or provider. This interface can be nested to provide a hierarchy of error information. The interface derives from the COM [IErrorInfo](http://go.microsoft.com/fwlink/p/?linkid=217161) interface, which provides functions that access detailed contextual error information.

## Syntax


```
{
  typedef enum
  {
    ObjectType_Unknown,
    ObjectType_Profile,
    ObjectType_Collector,
    ObjectType_Provider
  } CObjectType;
  [id(1), helpstring("GetObjectType")] HRESULT GetObjectType
    ([out, retval] CObjectType* pObjectType);
  [id(2), helpstring("GetHResult")] HRESULT GetHResult
    ([out, retval] HRESULT* pHResult);
  [id(3), helpstring("GetInnerErrorInfo")] HRESULT GetInnerErrorInfo
    ([out, retval] IUnknown** ppVal);
};
```

## Functions


The following table describes the functions of this interface.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Function</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="getobjecttype.md" data-raw-source="[GetObjectType](getobjecttype.md)">GetObjectType</a></p></td>
<td><p>Returns the type that produced the error.</p></td>
</tr>
<tr class="even">
<td><p><a href="gethresult.md" data-raw-source="[GetHResult](gethresult.md)">GetHResult</a></p></td>
<td><p>Returns an HRESULT value that indicates the error code.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getinnererrorinfo.md" data-raw-source="[GetInnerErrorInfo](getinnererrorinfo.md)">GetInnerErrorInfo</a></p></td>
<td><p>Returns additional information about the error.</p></td>
</tr>
</tbody>
</table>

 

## Related topics


[Interfaces](interfaces-wprcontrol.md)

 

 







