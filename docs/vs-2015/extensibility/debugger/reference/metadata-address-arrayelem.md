---
title: "METADATA_ADDRESS_ARRAYELEM | Microsoft Docs"
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
  - "METADATA_ADDRESS_ARRAYELEM"
helpviewer_keywords: 
  - "METADATA_ADDRESS_ARRAYELEM structure"
ms.assetid: 24321be5-7c17-4038-82a1-c20a2b68ff3c
caps.latest.revision: 7
ms.author: "gregvanl"
manager: "ghogen"
---
# METADATA_ADDRESS_ARRAYELEM
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [METADATA_ADDRESS_ARRAYELEM](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/metadata-address-arrayelem).  
  
This structure represents an array element within an array.  
  
## Syntax  
  
```cpp  
typedef struct _tagMETADATA_ADDRESS_ARRAYELEM {  
   _mdToken tokMethod;  
   DWORD    dwIndex;  
} METADATA_ADDRESS_ARRAYELEM;  
```  
  
```csharp  
public struct METADATA_ADDRESS_ARRAYELEM {  
   public int  tokMethod;  
   public uint dwIndex;  
}  
```  
  
## Terms  
 tokMethod  
 The ID of the array this element is a part of.  
  
 [C++] `_mdToken` is a `typedef` for a 32-bit `int`.  
  
 dwIndex  
 The index of this element within the array.  
  
## Remarks  
 This structure is part of the union in the [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md) structure when the `dwKind` field of the `DEBUG_ADDRESS_UNION` structure is set to `ADDRESS_KIND_ARRAYELEM` (a value from the [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md) enumeration).  
  
## Requirements  
 Header: sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll  
  
## See Also  
 [Structures and Unions](../../../extensibility/debugger/reference/structures-and-unions.md)   
 [DEBUG_ADDRESS_UNION](../../../extensibility/debugger/reference/debug-address-union.md)   
 [ADDRESS_KIND](../../../extensibility/debugger/reference/address-kind.md)

