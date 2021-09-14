---
title: Grid (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IGridProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Grid est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- UI Automation, implémenter le modèle de contrôle Grid
- UI Automation, modèle de contrôle Grid
- UI Automation, IGridProvider
- IGridProvider
- implémentation de modèles de contrôle de grille UI Automation
- Modèles de contrôle Grid
- modèles de contrôle, IGridProvider
- modèles de contrôle, implémenter la grille UI Automation
- modèles de contrôle, grille
- interfaces, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010502"
---
# <a name="grid-control-pattern"></a>Grid (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **Grid** est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.

Les enfants de cet élément doivent implémenter [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) et être organisés dans un système de coordonnées logiques à deux dimensions qui peut être parcouru par ligne et par colonne. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IGridProvider**](#required-members-for-igridprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Grid** , notez les conventions et recommandations suivantes :

-   Les coordonnées de grille sont de base zéro avec la cellule supérieure gauche (ou supérieure droite en fonction des paramètres régionaux) qui ont des coordonnées (0, 0).
-   Si une cellule est vide, un élément Microsoft UI Automation doit être retourné pour permettre la prise en charge de la propriété [**IGridItemProvider :: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) pour cette cellule. Cela est possible quand la disposition des éléments enfants de la grille est semblable à celle d’un tableau non justifié (consultez l’exemple ci-dessous).

    ![exemple de contrôle Grid avec des coordonnées vides](images/grid.png)

-   Une grille avec un seul élément est toujours nécessaire pour implémenter [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) s’il est logiquement considéré comme une grille. Le nombre d’éléments enfants de la grille est immatériel.
-   Selon l’implémentation du fournisseur, les lignes et les colonnes masquées peuvent être chargées dans l’arborescence UI Automation et sont donc reflétées dans les propriétés [**IGridProvider :: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) et [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) . Si les lignes et les colonnes masquées n’ont pas encore été chargées, elles ne doivent pas être comptabilisées.
-   [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) n’active pas la manipulation active d’une grille ; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) doit être implémenté pour activer cette fonctionnalité.
-   Utilisez un [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) pour écouter les changements structurels ou de disposition apportés à la grille, tels que les cellules qui ont été ajoutées, supprimées ou fusionnées.
-   Utilisez un [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) pour suivre le parcours des éléments ou des cellules d’une grille.

## <a name="required-members-for-igridprovider"></a>Membres requis pour **IGridProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .



| Membres nécessaires                                        | Type de membre | Notes |
|---------------------------------------------------------|-------------|-------|
| [**RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | Propriété    | None  |
| [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | Propriété    | None  |
| [**GetItem**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | Méthode      | None  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[GridItem (modèle de contrôle)](uiauto-implementinggriditem.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




