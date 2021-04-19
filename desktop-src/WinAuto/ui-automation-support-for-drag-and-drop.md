---
title: Prise en charge d’UI Automation pour le glisser-déplacer
description: Cette rubrique décrit les modèles de contrôle qui exposent des informations sur la fonctionnalité de glisser-déplacer d’un élément.
ms.assetid: FFF5A296-C9FF-4B47-AAF8-A9DD581D9DBE
keywords:
- UI Automation, prise en charge du glisser-déplacer
- UI Automation, vue d’ensemble du modèle Drag
- UI Automation, vue d’ensemble du modèle DropTarget
- UI Automation, vue d’ensemble du glisser-déplacer
- modèles glisser-déplacer, à propos de
- Faire glisser le modèle de contrôle
- Modèle de contrôle DropTarget
- modèles de contrôle, faites glisser
- modèles de contrôle, DropTarget
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4194613d15aadac4a925303ef2322d4cf53c341c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106543618"
---
# <a name="ui-automation-support-for-drag-and-drop"></a>Prise en charge d’UI Automation pour le glisser-déplacer

Microsoft UI Automation définit deux modèles de contrôle pour la prise en charge des scénarios de glisser-déplacer, le modèle de contrôle [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) et le modèle de contrôle [dropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) . Vous implémentez le modèle de contrôle Drag pour un élément qui peut être glissé, et le modèle de contrôle DropTarget pour un élément qui peut recevoir un élément glissé ; autrement dit, une cible de déplacement. Les deux modèles de contrôle exposent des informations qu’une technologie d’assistance peut utiliser pour aider un utilisateur d’accessibilité à effectuer une opération de glisser-déplacer.

-   [Faire glisser des styles](#dragging-styles)
    -   [Style source/cible](#sourcetarget-style)
    -   [Style source uniquement](#source-only-style)
-   [Faire glisser plusieurs éléments](#dragging-multiple-items)
-   [Interfaces clientes pour le glisser-déplacer](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a>Faire glisser des styles

Lorsque vous implémentez le modèle de contrôle [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) pour un élément déplaçable, vous devez décider s’il faut implémenter le style de glissement *source/cible* , ou le style de glissement *source uniquement* .

### <a name="sourcetarget-style"></a>Style source/cible

Dans le style source/cible de glisser-déplacer, l’élément déplacé (la « source ») et l’élément cible (« cible ») sont distincts et chacun d’eux déclenche un ensemble d’événements distincts. Voici le cycle de vie d’une opération glisser qui utilise le style source/cible : <dl> Lorsque l’utilisateur démarre une opération glisser :

-   La source déclenche l’événement DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   La source définit la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) sur **true**.
-   Les cibles mettent à jour leurs propriétés [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .

  
Lorsque l’opération glisser entre dans une région cible :

-   La cible déclenche l’événement DragEnter ([**UIA \_ dropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).

  
Lorsque l’opération glisser quitte une région cible :

-   La cible déclenche l’événement DragLeave ([**UIA \_ dropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).

  
Lorsque l’utilisateur relâche l’élément déplacé sur une non-cible :

-   La source déclenche l’événement DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).
-   La source affecte la **valeur false** à la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) .

  
Lorsque l’utilisateur relâche l’élément déplacé sur une cible :

-   La source déclenche l’événement DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   La source affecte la **valeur false** à la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) .
-   La cible définit la propriété [**IDropTargetProvider ::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) pour indiquer l’effet qui s’est produit.
-   La cible déclenche l’événement supprimé ([**UIA \_ dropTarget \_ DroppedEventId**](uiauto-event-ids.md)).

  
</dl>

Les événements des objets source et cible sont étroitement liés, mais distincts. Les données relatives à ce qui est glissé proviennent de la source, tandis que les données relatives à « ce qui pourrait se produire » et à « ce qui se passe » proviennent de la cible.

Quand une opération glisser est en cours, l’élément déplacé peut être glissé dans et hors des régions cibles, le nombre de fois où l’opération se termine.

Toute cible de déplacement qui doit mettre à jour sa propriété [**IDropTargetProvider ::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) à la volée doit déclencher un événement de modification de propriété supplémentaire sur cette propriété.

### <a name="source-only-style"></a>Style source uniquement

Le style de glissement source uniquement permet à un fournisseur d’éviter d’implémenter des cibles de dépôt. Le fait de ne pas implémenter des cibles de dépôt réduit le coût d’implémentation, mais ne donne pas aux applications clientes d’accessibilité des informations sur l’objet qui a reçu la suppression. Voici le cycle de vie d’une opération glisser qui utilise le style source uniquement : <dl> Lorsque l’utilisateur démarre une opération glisser :

-   La source déclenche l’événement DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   La source définit la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) sur **true**.

  
Lorsque l’opération glisser entre dans une région cible :

-   La source définit la propriété [**IDragProvider ::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sur la valeur appropriée.

  
Lorsque l’opération glisser quitte une région cible :

-   La source définit la propriété [**IDragProvider ::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sur la valeur appropriée.

  
Lorsque l’utilisateur relâche l’élément déplacé sur une non-cible :

-   La source déclenche l’événement DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).
-   La source affecte la **valeur false** à la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) .

  
Lorsque l’utilisateur relâche l’élément déplacé sur une cible :

-   La source déclenche l’événement DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).
-   La source définit la propriété [**IDragProvider ::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) pour indiquer l’effet qui a eu lieu quand l’élément a été supprimé.

  
</dl>

## <a name="dragging-multiple-items"></a>Faire glisser plusieurs éléments

Si un fournisseur implémente des opérations de glisser-déplacer où l’utilisateur peut faire glisser plusieurs objets en même temps, le fournisseur utilise les styles source/cible ou source uniquement comme décrit dans la section précédente, mais avec une petite différence. Lorsque l’utilisateur commence l’opération glisser, le fournisseur crée un élément source maître qui représente le jeu complet d’éléments qui sont glissés. L’élément source maître déclenche tous les événements pour le compte du jeu d’éléments déplacés ; les éléments ne déclenchent aucun événement propre.<dl> Lorsque l’utilisateur démarre une opération glisser :

-   Le fournisseur crée l’élément source maître.
-   L’élément source maître déclenche l’événement DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).
-   L’élément source maître définit la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) sur **true**.
-   L’élément source maître met à jour la liste des éléments récupérés pour inclure tous les éléments déplacés afin que la méthode [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) puisse récupérer la liste.

  
</dl>

Pour ce point, l’élément source maître remplit le même rôle que celui de l’élément source, comme décrit dans la section précédente.

## <a name="client-interfaces-for-drag-and-drop"></a>Interfaces clientes pour le glisser-déplacer

Les applications clientes UI Automation utilisent les interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) et [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) pour accéder aux informations de glisser-déplacer à partir d’éléments d’interface utilisateur.

 

 