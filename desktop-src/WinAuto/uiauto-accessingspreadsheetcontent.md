---
title: Accès au contenu d’une feuille de calcul
description: Cette rubrique décrit comment les applications clientes UI Automation de Microsoft peuvent accéder au contenu d’une feuille de calcul.
ms.assetid: F32EFA46-222B-4A4E-9938-10DE0F6A2CA7
keywords:
- clients, accès au contenu d’une feuille de calcul
- clients, contrôles textuels
- clients, modèle de contrôle Spreadsheet
- clients, modèle de contrôle SpreadsheetItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31495086614f34aeff378a8565200fa03f2dad62
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316230"
---
# <a name="accessing-spreadsheet-content"></a><span data-ttu-id="47807-107">Accès au contenu d’une feuille de calcul</span><span class="sxs-lookup"><span data-stu-id="47807-107">Accessing Spreadsheet Content</span></span>

<span data-ttu-id="47807-108">Un contrôle basé sur du texte qui contient le contenu d’une feuille de calcul peut permettre aux clients d’accéder au contenu en prenant en charge les modèles de contrôle [Spreadsheet](uiauto-implementingspreadsheet.md) et [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) .</span><span class="sxs-lookup"><span data-stu-id="47807-108">A text-based control that contains spreadsheet content can enable clients to access the content by supporting the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns.</span></span> <span data-ttu-id="47807-109">Cette rubrique décrit comment les applications clientes UI Automation de Microsoft peuvent accéder au contenu d’une feuille de calcul.</span><span class="sxs-lookup"><span data-stu-id="47807-109">This topic describes how Microsoft UI Automation client applications can access the content of a spreadsheet.</span></span>

<span data-ttu-id="47807-110">Pour déterminer si un contrôle textuel prend en charge les modèles de contrôle [Spreadsheet](uiauto-implementingspreadsheet.md) et [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , récupérez d’abord l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour le contrôle (consultez [obtention d’éléments UI Automation](uiauto-obtainingelements.md)). Ensuite, appelez la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , en spécifiant un identificateur de modèle de contrôle de [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) ou [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)et un variant qui reçoit la valeur true si le contrôle prend en charge le modèle de contrôle particulier.</span><span class="sxs-lookup"><span data-stu-id="47807-110">To determine whether a text-based control supports the [Spreadsheet](uiauto-implementingspreadsheet.md) and [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) control patterns, first retrieve the [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) interface for the control (see [Obtaining UI Automation Elements](uiauto-obtainingelements.md).) Next, call the [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method, specifying a control pattern identifier of [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) or [**UIA\_SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md), and a variant that receives TRUE if the control supports the particular control pattern.</span></span>

<span data-ttu-id="47807-111">Pour accéder au contenu de la feuille de calcul, récupérez l’interface [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) en appelant la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) et en spécifiant [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) comme identificateur de modèle de contrôle.</span><span class="sxs-lookup"><span data-stu-id="47807-111">To access the spreadsheet content, retrieve the [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) interface by calling [**IUIAutomationElement::GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) method and specifying [**UIA\_SpreadsheetPatternId**](uiauto-controlpattern-ids.md) as the control pattern identifier.</span></span> <span data-ttu-id="47807-112">Ensuite, utilisez la méthode [**IUIAutomationSpreadsheetPattern :: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) pour obtenir l’interface [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) pour un élément de feuille de calcul particulier (généralement une cellule).</span><span class="sxs-lookup"><span data-stu-id="47807-112">Next, use the [**IUIAutomationSpreadsheetPattern::GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) method to get the [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) interface for a particular spreadsheet item (typically a cell).</span></span> <span data-ttu-id="47807-113">Utilisez les propriétés et les méthodes de l’interface **IUIAutomationSpreadsheetItem** pour récupérer la formule de la cellule et les annotations associées à la cellule.</span><span class="sxs-lookup"><span data-stu-id="47807-113">Use the properties and methods of the **IUIAutomationSpreadsheetItem** interface to retrieve the formula for the cell, and any annotations associated with the cell.</span></span> <span data-ttu-id="47807-114">Pour plus d’informations sur les annotations, consultez [récupération des annotations.](uiauto-usingtextrangeobjects.md)</span><span class="sxs-lookup"><span data-stu-id="47807-114">For more information about annotations, see [Retrieving Annotations.](uiauto-usingtextrangeobjects.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="47807-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="47807-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47807-116">Prise en charge d’UI Automation pour le contenu textuel</span><span class="sxs-lookup"><span data-stu-id="47807-116">UI Automation Support for Textual Content</span></span>](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[<span data-ttu-id="47807-117">Utilisation de contrôles textuels</span><span class="sxs-lookup"><span data-stu-id="47807-117">Working with Text-based Controls</span></span>](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 