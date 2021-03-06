---
title: "Controlling Color, Line Style, and other Shape Properties | Microsoft Docs"
ms.custom: ""
ms.date: "2018-06-30"
ms.prod: "visual-studio-tfs-dev14"
ms.reviewer: ""
ms.suite: ""
ms.tgt_pltfrm: ""
ms.topic: "article"
ms.assetid: c06d0066-24aa-4c65-b91c-c2089b81ec8d
caps.latest.revision: 4
author: gewarren
ms.author: gewarren
manager: "douge"
---
# Controlling Color, Line Style, and other Shape Properties
[!INCLUDE[vs2017banner](../includes/vs2017banner.md)]

The latest version of this topic can be found at [Controlling Color, Line Style, and other Shape Properties](https://docs.microsoft.com/visualstudio/modeling/controlling-color-line-style-and-other-shape-properties).  
  
Some shape properties such as color can be 'exposed’ – that is, linked to a domain property of the shape. Others have to be controlled directly.  
  
## Exposing a property  
 Some shape properties such as color can be linked to the value of a domain property.  
  
 In the DSL Definition, select a shape, connector or diagram class. On its context menu, choose **Add Exposed**, and then choose the property you want, such as Fill Color.  
  
 The shape now has a domain property that you can set in program code or as a user.  
  
## Dynamically updating an exposed property  
 Typically you want to make the exposed property dependent on another property. For example, you might want a shape to turn red whenever a particular domain property is less than zero. To make this dependency, create a [rule](../modeling/rules-propagate-changes-within-the-model.md). For example:  
  
```csharp  
using System;  
using System.Collections.Generic;  
using System.Linq;  
using Microsoft.VisualStudio.Modeling;  
using Microsoft.VisualStudio.Modeling.Diagrams;  
namespace ExampleNamespace  
{  
 // Attribute associates the rule with class:  
 [RuleOn(typeof(CarShape), FireTime = TimeToFire.TopLevelCommit)]  
 // The rule is a class derived from one of the abstract rules:  
 class CarShapeAddRule : AddRule  
 {  
 // Override the abstract method:  
 public override void ElementAdded(ElementAddedEventArgs e)  
 {  
 base.ElementAdded(e);  
 CarShape shape = e.ModelElement as CarShape;  
 Store store = shape.Store;  
 // Ignore this call if we're currently loading a model:  
 if (store.TransactionManager.CurrentTransaction.IsSerializing)   
  return;  
 Car car = shape.ModelElement as Car;  
 // Code here propagates change as required - for example:  
 shape.FillColor = car.Somebool ? System.Drawing.Color.Red : System.Drawing.Color.Green;   
 }  
}  
 // The rule must be registered:  
 public partial class ExampleDomainModel  
 {  
 protected override Type[] GetCustomDomainModelTypes()  
 {  
  List<Type> types = new List<Type>(base.GetCustomDomainModelTypes());  
  types.Add(typeof(CarShapeAddRule));  
  // If you add more rules, list them here.   
  return types.ToArray();  
 }  
 }  
}  
```



