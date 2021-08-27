---
title: Modèle de contrôle DropTarget
description: Fournit des recommandations et des conventions pour implémenter le modèle de contrôle DropTarget à l’aide de IDropTargetProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: DD5EE4A0-E6C0-4657-A60F-7F59FC569E04
keywords:
- UI Automation, implémentation du modèle de contrôle DropTarget
- UI Automation, modèle de contrôle DropTarget
- UI Automation, IDropTargetProvider
- IDropTargetProvider
- implémentation des modèles de contrôle DropTarget d’UI Automation
- Modèles de contrôle DropTarget
- modèles de contrôle, IDropTargetProvider
- modèles de contrôle, implémenter des DropTarget UI Automation
- modèles de contrôle, DropTarget
- interfaces, IDropTargetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03cc425c9d41a70150eba2431c6fd317f2f8c23f878f7a0615025aec25b85b68
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098309"
---
# <a name="droptarget-control-pattern"></a>Modèle de contrôle DropTarget

Fournit des recommandations et des conventions pour implémenter le modèle de contrôle **dropTarget** à l’aide de [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle **dropTarget** est utilisé pour prendre en charge les contrôles qui peuvent être la cible d’une opération de glisser-déplacer.

## <a name="implementation-guidelines-and-conventions"></a>Conventions et directives d'implémentation

Lorsque vous implémentez le modèle de contrôle **dropTarget** , utilisez les conventions et recommandations suivantes :

-   Le modèle **dropTarget** doit être pris en charge lorsqu’une opération glisser est en cours. Elle peut être prise en charge même quand une opération glisser n’est pas en cours.
-   La propriété [**IDropTargetProvider ::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) est requise.
-   La propriété [**IDropTargetProvider ::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) est requise lorsqu’il y a plus d’un effet de dépôt possible pour la cible.
-   L’élément doit déclencher des événements de modification de propriété pour les propriétés **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) et **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) lorsqu’elles changent.

## <a name="required-members-for-idroptargetprovider"></a>Membres requis pour **IDropTargetProvider**

Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .



| Membres nécessaires                                                                              | Type de membre | Remarques                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | Propriété    | Aucun                                                                     |
| [**DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | Propriété    | Obligatoire si la cible de déplacement prend en charge plusieurs effets de suppression possibles. |
| [**UIA \_ dropTarget \_ DragEnterEventId**](uiauto-event-ids.md) | Événement       | Aucun                                                                     |
| [**UIA \_ dropTarget \_ DragLeaveEventId**](uiauto-event-ids.md) | Événement       | Aucun                                                                     |
| [**UIA \_ dropTarget \_ DroppedEventId**](uiauto-event-ids.md)     | Événement       | Aucun                                                                     |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md)
</dt> <dt>

[Faire glisser le modèle de contrôle](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[Vue d'ensemble des modèles de contrôle UI Automation](uiauto-controlpatternsoverview.md)
</dt> <dt>

[Vue d’ensemble de l’arborescence UI Automation](uiauto-treeoverview.md)
</dt> <dt>

[Prise en charge d’UI Automation pour le glisser-déplacer](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 