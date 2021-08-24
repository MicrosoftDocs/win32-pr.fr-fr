---
title: Dock (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IDockProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Dock est utilisé pour exposer les propriétés d’ancrage d’un contrôle dans un conteneur d’ancrage.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- UI Automation, implémenter le modèle de contrôle Dock
- UI Automation, modèle de contrôle Dock
- UI Automation, IDockProvider
- IDockProvider
- implémentation des modèles de contrôle Dock UI Automation
- modèles de contrôle d’ancrage
- modèles de contrôle, IDockProvider
- modèles de contrôle, implémenter Dock UI Automation
- modèles de contrôle, ancrer
- interfaces, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb0afd6a291a9e26c43d1aff957c7b7e9cd8c752040a661551b8eaf5b12b86e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118115097"
---
# <a name="dock-control-pattern"></a>Dock (modèle de contrôle)

Fournit des instructions et des conventions pour l’implémentation de [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **Dock** est utilisé pour exposer les propriétés d’ancrage d’un contrôle dans un conteneur d’ancrage.

Un conteneur d’ancrage est un contrôle qui vous permet de réorganiser des éléments enfants horizontalement et verticalement, les uns par rapport aux autres. L’illustration suivante montre un conteneur d’ancrage avec deux éléments enfants. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

![capture d’écran montrant un conteneur d’ancrage avec deux enfants ancrés](images/dockxmpl.jpg)

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IDockProvider**](#required-members-for-idockprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Dock** , notez les conventions et recommandations suivantes :

-   [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) n’expose aucune propriété du conteneur d’ancrage ni aucune propriété des contrôles qui sont ancrés adjacents au contrôle actuel dans le conteneur d’ancrage.
-   Les contrôles sont ancrés les uns par rapport aux autres selon leur ordre de plan actuel ; plus leur positionnement dans l’ordre de plan est haut, plus ils sont placés loin du bord spécifié du conteneur d’ancrage.
-   Si le conteneur d’ancrage est redimensionné, tout contrôle ancré dans le conteneur est repositionné sur le même bord que celui auquel il était ancré à l’origine. Les contrôles ancrés sont également redimensionnés pour remplir tout l’espace dans le conteneur d’après le comportement d’ancrage de leur propriété [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) . Par exemple, si **DockPosition \_ Top** est spécifié, les côtés gauche et droit du contrôle sont développés pour remplir tout l’espace disponible. Si **DockPosition \_ Fill** est spécifié, les quatre côtés du contrôle sont développés pour remplir tout l’espace disponible.
-   Sur un système à écrans multiples, les contrôles doivent être ancrés au côté gauche ou droit de l’écran actif. Si ce n’est pas possible, ils doivent être ancrés au côté gauche de l’écran le plus à gauche ou au côté droit de l’écran le plus à droite.

## <a name="required-members-for-idockprovider"></a>Membres requis pour **IDockProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .



| Membres nécessaires                                                | Type de membre | Notes |
|-----------------------------------------------------------------|-------------|-------|
| [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | Propriété    | Aucun  |
| [**SetDockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | Méthode      | Aucun  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




