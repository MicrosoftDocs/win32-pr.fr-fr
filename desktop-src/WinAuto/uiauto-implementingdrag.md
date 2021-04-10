---
title: Faire glisser le modèle de contrôle
description: Fournit des recommandations et des conventions pour implémenter le modèle de contrôle Drag à l’aide de IDragProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Drag est utilisé pour prendre en charge les contrôles glissables ou les contrôles avec des éléments glissables.
ms.assetid: 9853E9CB-D04B-4F67-8E9E-7F1F99BACEA7
keywords:
- UI Automation, implémenter le modèle de contrôle Drag
- UI Automation, faire glisser le modèle de contrôle
- UI Automation, IDragProvider
- IDragProvider
- implémentation des modèles de contrôle Drag d’UI Automation
- Faire glisser les modèles de contrôle
- modèles de contrôle, IDragProvider
- modèles de contrôle, implémenter UI Automation faire glisser
- modèles de contrôle, faites glisser
- interfaces, IDragProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 548f0212eca37e1890596143f27e9af70e1fb19a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031461"
---
# <a name="drag-control-pattern"></a>Faire glisser le modèle de contrôle

Fournit des recommandations et des conventions pour implémenter le modèle de contrôle **Drag** à l’aide de [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **Drag** est utilisé pour prendre en charge les contrôles glissables ou les contrôles avec des éléments glissables.

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **Drag** , utilisez les conventions et recommandations suivantes :

-   L’interface [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) prend en charge deux styles de glissement différents : le style source/cible et le style source uniquement. Vous devez choisir le style qui convient le mieux à vos scénarios de glisser-déplacer :
    -   **Style source/cible :** Chaque cible de déplacement possible est représentée par un élément qui implémente l’interface [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) . Pendant une opération glisser, les événements Microsoft UI Automation proviennent de l’élément qui est glissé, et des éléments de la cible de déplacement.
    -   **Style de la source uniquement :** Les cibles de dépôt ne sont pas représentées par les éléments UI Automation. Pendant une opération glisser, les événements proviennent uniquement de l’élément qui est glissé.
-   [**IDragProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idragprovider) est une interface en lecture seule destinée à la surveillance des opérations de glisser-déplacer. Vous ne pouvez pas l’utiliser pour contrôler une opération glisser. Vous pouvez automatiser les opérations glisser-déplacer en envoyant une entrée de souris à un contrôle.
-   La propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) est requise.
-   Les propriétés [**IDragProvider ::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) et [**IDragProvider ::D ropeffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects) sont requises pour une implémentation de style source uniquement et interdites pour une implémentation de style source/cible. Dans une implémentation de style source/cible, les éléments de cible de déplacement peuvent être interrogés pour leurs effets de suppression.
-   La propriété [**IDragProvider :: GrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) représente le déplacement de plusieurs éléments. Lorsque l’utilisateur commence l’opération glisser, vous devez créer un nouvel élément UI Automation pour servir d’élément source d’événement. Ce nouvel élément déclenche tous les événements que l’élément source aurait déclenchés en mode source/cible ou source uniquement, alors qu’aucun des éléments en cours de glissement ne déclenche aucun événement. Lorsque l’opération glisser est terminée, détruisez l’élément source de l’événement.
-   L’élément doit déclencher des événements de modification de propriété pour les propriétés **DropEffect** ([**UIA \_ DragDropEffectPropertyId**](uiauto-control-pattern-propids.md)) et **DropEffects** ([**UIA \_ DragDropEffectsPropertyId**](uiauto-control-pattern-propids.md)) lorsqu’elles changent. Les événements de modification de propriété pour les autres propriétés sont autorisés, mais peuvent être déduits à partir des événements requis **DragStart** ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)), **DragCancel** ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)) et **DragComplete** ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   

## <a name="required-members-for-idragprovider"></a>Membres requis pour **IDragProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IDragProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idragprovider) .



| Membres nécessaires                                                                        | Type de membre | Notes                                                                         |
|-----------------------------------------------------------------------------------------|-------------|-------------------------------------------------------------------------------|
| [**IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed)                                     | Propriété    | Aucun                                                                          |
| [**DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect)                                   | Propriété    | Requis pour une implémentation du style source uniquement.                      |
| [**DropEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffects)                                 | Propriété    | Obligatoire s’il y a plus d’un effet de dépôt possible pour l’élément retiré. |
| [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems)                         | Méthode      | Requis pour une opération glisser sur plusieurs éléments.                                  |
| [**UIA \_ faire glisser \_ DragStartEventId**](uiauto-event-ids.md)       | Événement       | Aucun                                                                          |
| [**UIA \_ faire glisser \_ DragCancelEventId**](uiauto-event-ids.md)     | Événement       | Aucun                                                                          |
| [**UIA \_ faire glisser \_ DragCompleteEventId**](uiauto-event-ids.md) | Événement       | Aucun                                                                          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Modèle de contrôle DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Prise en charge d’UI Automation pour le glisser-déplacer](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 