---
title: Modèle de contrôle VirtualizedItem
description: Fournit des instructions et des conventions pour l’implémentation de IVirtualizedItemProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: 7a95e92f-7ccb-4c9b-8986-1d2de7038e47
keywords:
- UI Automation, implémentation du modèle de contrôle VirtualizedItem
- UI Automation, modèle de contrôle VirtualizedItem
- UI Automation, IVirtualizedItemProvider
- IVirtualizedItemProvider
- implémentation des modèles de contrôle VirtualizedItem d’UI Automation
- Modèles de contrôle VirtualizedItem
- modèles de contrôle, IVirtualizedItemProvider
- modèles de contrôle, implémenter des VirtualizedItem UI Automation
- modèles de contrôle, VirtualizedItem
- interfaces, IVirtualizedItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8dac9e34dd9bff5d0ba2d245aa2fb8de621f40a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520577"
---
# <a name="virtualizeditem-control-pattern"></a>Modèle de contrôle VirtualizedItem

Fournit des instructions et des conventions pour l’implémentation de [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **VirtualizedItem** est utilisé pour prendre en charge les éléments virtualisés, qui sont des éléments représentés par des éléments d’automatisation d’espace réservé dans l’arborescence Microsoft UI Automation.

Les éléments virtualisés peuvent inclure des éléments récupérés à partir d’un contrôle qui prend en charge le modèle de contrôle [ItemContainer](uiauto-implementingitemcontainer.md) , ou un objet incorporé virtualisé récupéré à partir d’un contrôle qui prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) . L’espace réservé pour un élément virtualisé peut ne pas avoir de données chargées pour toutes les propriétés UI Automation et peut retourner [**UIA \_ E \_ ELEMENTNOTAVAILABLE**](uiauto-error-codes.md) en réponse aux requêtes pour les propriétés qui ne sont pas disponibles. Le modèle de contrôle **VirtualizedItem** fournit une méthode pour la réalisation d’un élément virtuel afin que des informations complètes soient rendues disponibles pour l’élément et qu’un élément Automation complet puisse être créé pour l’élément dans l’arborescence UI Automation.

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IVirtualizedItemProvider**](#required-members-for-ivirtualizeditemprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **VirtualizedItem** , notez les conventions et recommandations suivantes :

-   Tout élément d’espace réservé UI Automation qui peut être virtualisé doit prendre en charge le modèle de contrôle **VirtualizedItem** en exposant l’interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .
-   Quand [**IVirtualizedItemProvider ::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) on l’appelle, l’objet d’espace réservé doit être mis à jour avec des implémentations complètes de ses propriétés et modèles de contrôle.
-   Quand [**IVirtualizedItemProvider ::**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) on l’appelle, le fournisseur peut modifier la fenêtre d’affichage afin que l’élément virtualisé entre en vue. La remise de l’élément dans l’affichage n’est pas obligatoire. Toutefois, les éléments non virtualisés hors écran doivent prendre en charge la méthode [**IScrollItemProvider :: ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) .

## <a name="required-members-for-ivirtualizeditemprovider"></a>Membres requis pour **IVirtualizedItemProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IVirtualizedItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivirtualizeditemprovider) .



| Membres nécessaires                                           | Type de membre | Notes |
|------------------------------------------------------------|-------------|-------|
| [**Optimiser**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivirtualizeditemprovider-realize) | Méthode      | None  |



 

Ce modèle de contrôle n’est associé aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Implémentation du modèle de contrôle ItemContainer d’UI Automation](uiauto-implementingitemcontainer.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Utilisation d’éléments virtualisés](uiauto-workingwithvirtualizeditems.md)
</dt> </dl>

 

 




