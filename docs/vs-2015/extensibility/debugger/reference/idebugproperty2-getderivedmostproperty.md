---
title: "IDebugProperty2::GetDerivedMostProperty | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "IDebugProperty2::GetDerivedMostProperty"
helpviewer_keywords: 
  - "IDebugProperty2::GetDerivedMostProperty"
ms.assetid: cc86b461-62d1-4340-8209-c65037fd8b02
caps.latest.revision: 10
ms.author: "gregvanl"
manager: "ghogen"
---
# IDebugProperty2::GetDerivedMostProperty
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDebugProperty2::GetDerivedMostProperty](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugproperty2-getderivedmostproperty).  
  
Gets the derived-most property of a property.  
  
## Syntax  
  
```cpp#  
HRESULT GetDerivedMostProperty (   
   IDebugProperty2** ppDerivedMost  
);  
```  
  
```csharp  
int GetDerivedMostProperty (   
   out IDebugProperty2 ppDerivedMost  
);  
```  
  
#### Parameters  
 `ppDerivedMost`  
 [out] Returns an [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) object that represents the derived-most property.  
  
## Return Value  
 If successful, returns `S_OK`; otherwise returns error code. Returns `S_GETDERIVEDMOST_NO_DERIVED_MOST` if there is no derived-most property to retrieve.  
  
## Remarks  
 For example, if this property describes an object that implements `ClassRoot` but which is actually an instantiation of `ClassDerived` that is derived from `ClassRoot`, then this method returns an [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md) object describing the `ClassDerived` object.  
  
## See Also  
 [IDebugProperty2](../../../extensibility/debugger/reference/idebugproperty2.md)

