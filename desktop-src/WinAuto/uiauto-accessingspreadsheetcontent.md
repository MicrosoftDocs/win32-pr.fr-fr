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
# <a name="accessing-spreadsheet-content"></a>Accès au contenu d’une feuille de calcul

Un contrôle basé sur du texte qui contient le contenu d’une feuille de calcul peut permettre aux clients d’accéder au contenu en prenant en charge les modèles de contrôle [Spreadsheet](uiauto-implementingspreadsheet.md) et [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) . Cette rubrique décrit comment les applications clientes UI Automation de Microsoft peuvent accéder au contenu d’une feuille de calcul.

Pour déterminer si un contrôle textuel prend en charge les modèles de contrôle [Spreadsheet](uiauto-implementingspreadsheet.md) et [SpreadsheetItem](uiauto-implementingspreadsheetitem.md) , récupérez d’abord l’interface [**IUIAutomationElement**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement) pour le contrôle (consultez [obtention d’éléments UI Automation](uiauto-obtainingelements.md)). Ensuite, appelez la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) , en spécifiant un identificateur de modèle de contrôle de [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) ou [**UIA \_ SpreadsheetItemPatternId**](uiauto-controlpattern-ids.md)et un variant qui reçoit la valeur true si le contrôle prend en charge le modèle de contrôle particulier.

Pour accéder au contenu de la feuille de calcul, récupérez l’interface [**IUIAutomationSpreadsheetPattern**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetpattern) en appelant la méthode [**IUIAutomationElement :: GetCurrentPattern**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getcurrentpattern) et en spécifiant [**UIA \_ SpreadsheetPatternId**](uiauto-controlpattern-ids.md) comme identificateur de modèle de contrôle. Ensuite, utilisez la méthode [**IUIAutomationSpreadsheetPattern :: GetItemByName**](/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationspreadsheetpattern-getitembyname) pour obtenir l’interface [**IUIAutomationSpreadsheetItem**](/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationspreadsheetitempattern) pour un élément de feuille de calcul particulier (généralement une cellule). Utilisez les propriétés et les méthodes de l’interface **IUIAutomationSpreadsheetItem** pour récupérer la formule de la cellule et les annotations associées à la cellule. Pour plus d’informations sur les annotations, consultez [récupération des annotations.](uiauto-usingtextrangeobjects.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)
</dt> <dt>

[Utilisation de contrôles textuels](uiauto-workingwithtextbasedcontrols.md)
</dt> </dl>

 

 