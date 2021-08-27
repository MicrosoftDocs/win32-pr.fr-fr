---
title: Modèle de contrôle TableItem
description: Fournit des instructions et des conventions pour l’implémentation de ITableItemProvider, y compris des informations sur les méthodes. Le modèle de contrôle TableItem est utilisé pour prendre en charge les contrôles enfants des conteneurs qui implémentent ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- UI Automation, implémentation du modèle de contrôle TableItem
- UI Automation, modèle de contrôle TableItem
- UI Automation, ITableItemProvider
- ITableItemProvider
- implémentation des modèles de contrôle TableItem d’UI Automation
- Modèles de contrôle TableItem
- modèles de contrôle, ITableItemProvider
- modèles de contrôle, implémenter des TableItem UI Automation
- modèles de contrôle, TableItem
- interfaces, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babb64114bb761b0b6e93a7cc9c0036cb01bb8946eb813bcd0fc3e821d44a183
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098269"
---
# <a name="tableitem-control-pattern"></a>Modèle de contrôle TableItem

Fournit des instructions et des conventions pour l’implémentation de [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), y compris des informations sur les méthodes. Le modèle de contrôle **TableItem** est utilisé pour prendre en charge les contrôles enfants des conteneurs qui implémentent [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).

L’accès aux fonctionnalités des cellules individuelles est fourni par l’implémentation simultanée requise de [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider). Ce modèle de contrôle est analogue à **IGridItemProvider** , à la différence que tout contrôle qui implémente [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) doit exposer par programmation la relation entre la cellule individuelle et ses informations de ligne et de colonne. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ITableItemProvider**](#required-members-for-itableitemprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **TableItem** , notez les conventions et recommandations suivantes :

-   Pour obtenir des fonctionnalités d’élément de grille associées, consultez [modèle de contrôle GridItem](uiauto-implementinggriditem.md).

## <a name="required-members-for-itableitemprovider"></a>Membres requis pour **ITableItemProvider**

Les méthodes suivantes sont requises pour implémenter l’interface [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .



| Membres nécessaires                                                               | Type de membre | Remarques |
|--------------------------------------------------------------------------------|-------------|-------|
| [**GetColumnHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | Méthode      | Aucun  |
| [**GetRowHeaderItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | Méthode      | Aucun  |



 

Ce modèle de contrôle n’est associé à aucune propriété ni à aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Table (modèle de contrôle)](uiauto-implementingtable.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




