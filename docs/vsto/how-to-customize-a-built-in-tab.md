---
title: "How to: Customize a Built-in Tab | Microsoft Docs"
ms.custom: ""
ms.date: "02/02/2017"
ms.technology: 
  - "office-development"
ms.topic: "conceptual"
dev_langs: 
  - "VB"
  - "CSharp"
helpviewer_keywords: 
  - "Ribbon [Office development in Visual Studio], tabs"
  - "built-in tabs [Office development in Visual Studio]"
author: TerryGLee
ms.author: tglee
manager: douge
ms.workload: 
  - "office"
---
# How to: Customize a Built-in Tab
  You can add groups and controls to a built-in tab. A built-in tab is a tab that's already on the Ribbon of a Microsoft Office application. For example, the **Data** tab is a built-in tab in Excel. When you create a custom group, it appears last on the tab, but you can move your group anywhere on the tab.  
  
 [!INCLUDE[appliesto_ribbon](../vsto/includes/appliesto-ribbon-md.md)]  
  
> [!NOTE]  
>  You can add groups to a built-in tab, but you cannot remove built-in groups from a built-in tab.  
  
### To add groups to a built-in tab  
  
1.  Right-click the Ribbon code file in **Solution Explorer**, and then click **View Designer**.  
  
    > [!NOTE]  
    >  If the Ribbon code file doesn't appear in **Solution Explorer**, you must add a **Ribbon item** to your project. See [How to: Get Started Customizing the Ribbon](../vsto/how-to-get-started-customizing-the-ribbon.md).  
  
2.  Right-click any tab in the Ribbon designer, and then click **Properties**.  
  
3.  In the **Properties** window, expand the **ControlId** property, and then set the **ControlIdType** property to **Office**.  
  
4.  Set the **OfficeId** property to the *control ID* of the built-in tab that you want to customize.  
  
     The control ID is the name that uniquely identifies tabs, groups, and controls that are built into Microsoft Office applications.  
  
     For a list of control IDs, see [Office 2010 Help Files: Office Fluent User Interface Control Identifiers](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
5.  From the **Office Ribbon Controls** tab of the **Toolbox**, drag groups onto the tab.  
  
    > [!NOTE]  
    >  Built-in groups do not appear in the designer. Therefore, the only way to determine whether you are working with a built-in tab is to examine the **ControlId** property of the tab.  
  
### To position groups on a built-in tab  
  
1.  In the Ribbon Designer, select a custom group.  
  
2.  In the **Properties** window, expand the **Position** property.  
  
3.  Set the **PositionType** property to the appropriate value:  
  
    -   **BeforeOfficeId** positions the group before a specified built-in group.  
  
    -   **AfterOfficeId** positions the group after a specified built-in group.  
  
4.  Set the **OfficeId** property to the control ID of a built-in group.  
  
     For a list of control IDs, see [Office 2010 Help Files: Office Fluent User Interface Control Identifiers](http://go.microsoft.com/fwlink/?LinkID=181052).  
  
## See Also  
 [Ribbon Overview](../vsto/ribbon-overview.md)   
 [Ribbon Designer](../vsto/ribbon-designer.md)   
 [Ribbon XML](../vsto/ribbon-xml.md)   
 [Walkthrough: Creating a Custom Tab by Using the Ribbon Designer](../vsto/walkthrough-creating-a-custom-tab-by-using-the-ribbon-designer.md)   
 [Walkthrough: Creating a Custom Tab by Using Ribbon XML](../vsto/walkthrough-creating-a-custom-tab-by-using-ribbon-xml.md)   
 [How to: Get Started Customizing the Ribbon](../vsto/how-to-get-started-customizing-the-ribbon.md)   
 [How to: Change the Position of a Tab on the Ribbon](../vsto/how-to-change-the-position-of-a-tab-on-the-ribbon.md)   
 [How to: Add Controls to the Backstage View](../vsto/how-to-add-controls-to-the-backstage-view.md)   
 [How to: Show Add-in User Interface Errors](../vsto/how-to-show-add-in-user-interface-errors.md)  
  
  