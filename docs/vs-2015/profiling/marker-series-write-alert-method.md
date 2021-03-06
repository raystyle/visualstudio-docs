---
title: "marker_series::write_alert Method | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-dev14"
ms.reviewer: ""
ms.suite: ""
ms.technology: 
  - "vs-ide-debug"
ms.tgt_pltfrm: ""
ms.topic: "article"
f1_keywords: 
  - "cvmarkersobj/Concurrency::diagnostic:marker_series::write_alert"
helpviewer_keywords: 
  - "Concurrency::diagnostic:marker_series::write_alert method"
ms.assetid: 9d5465c7-f862-47a7-b249-4116605075a6
caps.latest.revision: 8
author: "mikejo5000"
ms.author: "mikejo"
manager: "ghogen"
---
# marker_series::write_alert Method
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [marker_series::write_alert Method](https://docs.microsoft.com/visualstudio/profiling/marker-series-write-alert-method).  
  
Writes an alert to the Concurrency Visualizer trace file.  
  
## Syntax  
  
```  
void write_alert(  
   _In_ LPCTSTR _Format,  
   ...  
);  
```  
  
#### Parameters  
 `_Format`  
 A composite format string that contains text intermixed with zero or more format items, which correspond to objects in the argument list.  
  
## Requirements  
 **Header:** cvmarkersobj.h  
  
 **Namespace:** Concurrency::diagnostic  
  
## See Also  
 [marker_series Class](../profiling/marker-series-class.md)



