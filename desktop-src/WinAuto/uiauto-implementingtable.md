---
title: Table (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ITableProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle table est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- UI Automation, implémenter le modèle de contrôle table
- UI Automation, modèle de contrôle table
- UI Automation, ITableProvider
- ITableProvider
- implémentation de modèles de contrôle de table UI Automation
- Modèles de contrôle de table
- modèles de contrôle, ITableProvider
- modèles de contrôle, implémenter une table UI Automation
- modèles de contrôle, table
- interfaces, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104570999"
---
# <a name="table-control-pattern"></a>Table (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **table** est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.

Les enfants de l’élément conteneur doivent implémenter [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) et être organisés dans un système de coordonnées logiques à deux dimensions qui peut être parcouru par ligne et par colonne. Ce modèle de contrôle est analogue à [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , à la différence que tout contrôle qui implémente [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) doit également exposer une relation d’en-tête de colonne et/ou de ligne pour chaque élément enfant. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **ITableProvider**](#required-members-for-itableprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **table** , notez les conventions et recommandations suivantes :

-   L’accès au contenu de cellules individuelles s’effectue par le biais d’un système de coordonnées logiques à deux dimensions ou d’un tableau fourni par l’implémentation simultanée requise de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).
-   Un en-tête de colonne ou de ligne peut figurer dans un objet table ou être un objet d’en-tête séparé, associé à un objet table.
-   Les en-têtes de colonne et de ligne peuvent inclure un en-tête principal et des en-têtes de prise en charge quelconques.
    > [!Note]  
    > Ce concept devient évident dans une feuille de calcul Microsoft Excel où un utilisateur a défini une colonne **First Name** . Cette colonne contient maintenant deux en-têtes, y compris l’en-tête de **prénom** défini par l’utilisateur, et la désignation alphanumérique pour cette colonne assignée par l’application.

     

-   Consultez [modèle de contrôle Grid](uiauto-implementinggrid.md) pour obtenir des fonctionnalités de grille associées.

    L’illustration suivante montre un tableau avec des en-têtes de colonnes complexes.

    ![table avec en-têtes de colonnes complexes](images/uia-valuepattern-colorpicker.jpg)

    L’illustration suivante montre une table avec une propriété [**ITableProvider :: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambiguë.

    ![table avec une propriété RowOrColumnMajor ambiguë](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a>Membres requis pour **ITableProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .



| Membres nécessaires                                                   | Type de membre | Notes |
|--------------------------------------------------------------------|-------------|-------|
| [**RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | Propriété    | Aucun  |
| [**GetColumnHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | Méthode      | Aucun  |
| [**GetRowHeaders**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | Méthode      | Aucun  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Modèle de contrôle TableItem](uiauto-implementingtableitem.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




