---
title: GridItem (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IGridItemProvider, y compris des informations sur les propriétés. Le modèle de contrôle GridItem est utilisé pour prendre en charge les contrôles enfants individuels des conteneurs qui implémentent IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- UI Automation, implémentation du modèle de contrôle GridItem
- UI Automation, modèle de contrôle GridItem
- UI Automation, IGridItemProvider
- IGridItemProvider
- implémentation des modèles de contrôle GridItem d’UI Automation
- Modèles de contrôle GridItem
- modèles de contrôle, IGridItemProvider
- modèles de contrôle, implémentation de GridItem UI Automation
- modèles de contrôle, GridItem
- interfaces, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672662"
---
# <a name="griditem-control-pattern"></a>GridItem (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), y compris des informations sur les propriétés. Le modèle de contrôle **GridItem** est utilisé pour prendre en charge les contrôles enfants individuels des conteneurs qui implémentent [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).

Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IGridItemProvider**](#required-members-for-igriditemprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **GridItem** , notez les conventions et recommandations suivantes :

-   Les coordonnées de grille ont une base zéro et la cellule supérieure gauche possède les coordonnées (0, 0).
-   Les cellules fusionnées signalent leurs propriétés de [**ligne**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) et de [**colonne**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) en fonction de leur cellule d’ancrage sous-jacente, tel que défini par le fournisseur Microsoft UI Automation. En règle générale, il s’agit de la ligne la plus haute ou de la colonne la plus à gauche.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) ne fournit pas de manipulation active de la grille telle que la fusion ou le fractionnement des cellules.
-   Les contrôles qui implémentent [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) peuvent généralement être parcourus (autrement dit, un client UI Automation peut se déplacer vers des contrôles adjacents) à l’aide du clavier.

## <a name="required-members-for-igriditemprovider"></a>Membres requis pour **IGridItemProvider**

Les propriétés suivantes sont requises pour implémenter l’interface [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) .



| Membres nécessaires                                                  | Type de membre | Notes |
|-------------------------------------------------------------------|-------------|-------|
| [**Haut**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | Propriété    | Aucun  |
| [**Chronique**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | Propriété    | Aucun  |
| [**RowSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | Propriété    | Aucun  |
| [**ColumnSpan**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | Propriété    | Aucun  |
| [**ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | Propriété    | Aucun  |



 

Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Grid (modèle de contrôle)](uiauto-implementinggrid.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




