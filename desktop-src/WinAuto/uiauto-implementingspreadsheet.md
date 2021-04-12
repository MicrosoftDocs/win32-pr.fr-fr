---
title: Spreadsheet (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ISpreadsheetProvider, y compris des informations sur les méthodes.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- UI Automation, implémenter le modèle de contrôle Spreadsheet
- UI Automation, modèle de contrôle Spreadsheet
- UI Automation, ISpreadsheetProvider
- ISpreadsheetProvider
- implémentation du modèle de contrôle Spreadsheet d’UI Automation
- Spreadsheet (modèle de contrôle)
- modèles de contrôle, ISpreadsheetProvider
- modèles de contrôle, implémenter une feuille de calcul UI Automation
- modèles de contrôle, feuille de calcul
- interfaces, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315774"
---
# <a name="spreadsheet-control-pattern"></a>Spreadsheet (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), y compris des informations sur les méthodes. Des liens vers des références supplémentaires sont répertoriés à la fin de la rubrique. Le modèle de contrôle **Spreadsheet** est utilisé pour exposer le contenu d’une feuille de calcul ou d’un autre document basé sur la grille.

Le modèle de contrôle **Spreadsheet** est étroitement lié au modèle de contrôle [Grid](uiauto-implementinggrid.md) ; les contrôles qui implémentent le modèle de contrôle **Spreadsheet** doivent également implémenter le modèle de contrôle Grid. Les contrôles peuvent également implémenter le modèle de contrôle [table](uiauto-implementingtable.md) , le cas échéant. Pour obtenir des exemples de contrôles qui implémentent ces modèles de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Spreadsheet** , notez les conventions et recommandations suivantes :

-   Si une feuille de calcul implémente l’interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , ses cellules doivent implémenter l’interface [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .
-   La méthode [**ISpreadsheetProvider :: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) est destinée à fournir le même type de navigation qu’une application peut fournir avec une fonctionnalité de **saut à étiquette** . De nombreux feuilles de calcul permettent à des cellules spécifiques de recevoir un nom convivial ou une étiquette. **GetItemByName** permet au client de rechercher une cellule en fonction de son nom convivial. Cette méthode ne doit pas récupérer de cellules qui contiennent le texte de nom, car les résultats peuvent être très ambigus. Si le programme de feuille de calcul permet à plusieurs cellules d’une même feuille de calcul d’avoir le même nom convivial ou étiquette, le comportement d’automatisation de l’interface utilisateur de Microsoft n’est pas défini.

## <a name="required-members-for-ispreadsheetprovider"></a>Membres requis pour **ISpreadsheetProvider**

La méthode suivante est requise pour l’implémentation de l’interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .



| Membres nécessaires                                                       | Type de membre | Notes |
|------------------------------------------------------------------------|-------------|-------|
| [**GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | Méthode      | Aucun  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 