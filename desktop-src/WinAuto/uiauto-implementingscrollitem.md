---
title: Modèle de contrôle ScrollItem
description: Fournit des instructions et des conventions pour l’implémentation de IScrollItemProvider, y compris des informations sur les méthodes.
ms.assetid: ea0d7438-218c-4925-b24c-a8011f305b9d
keywords:
- UI Automation, implémentation du modèle de contrôle ScrollItem
- UI Automation, modèle de contrôle ScrollItem
- UI Automation, IScrollItemProvider
- IScrollItemProvider
- implémentation des modèles de contrôle ScrollItem d’UI Automation
- Modèles de contrôle ScrollItem
- modèles de contrôle, IScrollItemProvider
- modèles de contrôle, implémenter des ScrollItem UI Automation
- modèles de contrôle, ScrollItem
- interfaces, IScrollItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7233dfe649d166a3172ff2dda3122895f259abcc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127010485"
---
# <a name="scrollitem-control-pattern"></a>Modèle de contrôle ScrollItem

Fournit des instructions et des conventions pour l’implémentation de [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider), y compris des informations sur les méthodes. Le modèle de contrôle **ScrollItem** est utilisé pour prendre en charge les contrôles enfants individuels des conteneurs qui implémentent [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider). L’existence du modèle de contrôle **ScrollItem** sur un contrôle n’implique pas que son conteneur ou un ancêtre doit implémenter le modèle de contrôle **Scroll** .

Quand le conteneur implémente le modèle de contrôle **Scroll** , le modèle de contrôle **ScrollItem** agit comme un canal de communication entre un contrôle enfant et son conteneur pour garantir que le conteneur peut modifier le contenu (ou la région) actuellement visible dans sa fenêtre d’affichage pour afficher le contrôle enfant. Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).

Cette rubrique contient les sections suivantes.

-   [Conventions et directives d'implémentation](#implementation-guidelines-and-conventions)
-   [Membres requis pour **IScrollItemProvider**](#required-members-for-iscrollitemprovider)
-   [Rubriques connexes](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **ScrollItem** , notez les conventions et recommandations suivantes :

-   Les éléments contenus dans un contrôle de [fenêtre](uiauto-supportwindowcontroltype.md) ou de **canevas** ne sont pas requis pour implémenter l’interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) . Toutefois, ils doivent également exposer un emplacement valide pour la propriété [**IUIAutomationElement :: CurrentBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentboundingrectangle) (ou [**CachedBoundingRectangle**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedboundingrectangle)). Cela permettra à une application cliente UI Automation de Microsoft d’utiliser les méthodes de modèle de contrôle [**IUIAutomationScrollPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationscrollpattern) sur le conteneur pour afficher l’élément enfant.

## <a name="required-members-for-iscrollitemprovider"></a>Membres requis pour **IScrollItemProvider**

La méthode suivante est requise pour l’implémentation de l’interface [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider) .



| Membres nécessaires                                                    | Type de membre | Notes |
|---------------------------------------------------------------------|-------------|-------|
| [**ScrollIntoView**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollitemprovider-scrollintoview) | Méthode      | None  |



 

Ce modèle de contrôle n’est associé à aucune propriété ni à aucun événement.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Selection (modèle de contrôle)](uiauto-implementingselection.md)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> </dl>

 

 




