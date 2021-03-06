---
title: "IDebugTypeFieldBuilder | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-sdk"
ms.tgt_pltfrm: ""
ms.topic: "article"
helpviewer_keywords: 
  - "IDebugTypeFieldBuilder interface"
ms.assetid: 2dfed0be-6972-4bec-baec-f0b78df9ef97
caps.latest.revision: 7
ms.author: "gregvanl"
manager: "ghogen"
---
# IDebugTypeFieldBuilder
[!INCLUDE[vs2017banner](../../../includes/vs2017banner.md)]

The latest version of this topic can be found at [IDebugTypeFieldBuilder](https://docs.microsoft.com/visualstudio/extensibility/debugger/reference/idebugtypefieldbuilder).  
  
Represents the ability to create a field that represents a type.  
  
## Syntax  
  
```  
IDebugTypeFieldBuilder : IUnknown  
```  
  
## Notes for Callers  
 This interface is obtained from the symbol provider.  
  
## Methods  
 This interface implements the following methods:  
  
|Method|Description|  
|------------|-----------------|  
|[CreatePrimitive](../../../extensibility/debugger/reference/idebugtypefieldbuilder-createprimitive.md)|Creates an object that represents a primitive type.|  
|[CreatePointerToType](../../../extensibility/debugger/reference/idebugtypefieldbuilder-createpointertotype.md)|Creates a pointer to the specified type.|  
  
## Requirements  
 Header: Sh.h  
  
 Namespace: Microsoft.VisualStudio.Debugger.Interop  
  
 Assembly: Microsoft.VisualStudio.Debugger.Interop.dll

