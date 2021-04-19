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
# <a name="ui-automation-support-for-drag-and-drop"></a><span data-ttu-id="5e177-112">Prise en charge d’UI Automation pour le glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="5e177-112">UI Automation Support for Drag-and-Drop</span></span>

<span data-ttu-id="5e177-113">Microsoft UI Automation définit deux modèles de contrôle pour la prise en charge des scénarios de glisser-déplacer, le modèle de contrôle [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) et le modèle de contrôle [dropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) .</span><span class="sxs-lookup"><span data-stu-id="5e177-113">Microsoft UI Automation defines two control patterns for supporting drag-and-drop scenarios, the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern, and the [DropTarget](/windows/desktop/WinAuto/uiauto-implementingdroptarget) control pattern.</span></span> <span data-ttu-id="5e177-114">Vous implémentez le modèle de contrôle Drag pour un élément qui peut être glissé, et le modèle de contrôle DropTarget pour un élément qui peut recevoir un élément glissé ; autrement dit, une cible de déplacement.</span><span class="sxs-lookup"><span data-stu-id="5e177-114">You implement the Drag control pattern for an element that can be dragged, and the DropTarget control pattern for an element that can receive a dragged element; that is, a drop target.</span></span> <span data-ttu-id="5e177-115">Les deux modèles de contrôle exposent des informations qu’une technologie d’assistance peut utiliser pour aider un utilisateur d’accessibilité à effectuer une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="5e177-115">The two control patterns expose information that an assistive technology can use to help an accessibility user complete a drag-and-drop operation.</span></span>

-   [<span data-ttu-id="5e177-116">Faire glisser des styles</span><span class="sxs-lookup"><span data-stu-id="5e177-116">Dragging Styles</span></span>](#dragging-styles)
    -   [<span data-ttu-id="5e177-117">Style source/cible</span><span class="sxs-lookup"><span data-stu-id="5e177-117">Source/target Style</span></span>](#sourcetarget-style)
    -   [<span data-ttu-id="5e177-118">Style source uniquement</span><span class="sxs-lookup"><span data-stu-id="5e177-118">Source-only Style</span></span>](#source-only-style)
-   [<span data-ttu-id="5e177-119">Faire glisser plusieurs éléments</span><span class="sxs-lookup"><span data-stu-id="5e177-119">Dragging Multiple Items</span></span>](#dragging-multiple-items)
-   [<span data-ttu-id="5e177-120">Interfaces clientes pour le glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="5e177-120">Client Interfaces for Drag-and-Drop</span></span>](#client-interfaces-for-drag-and-drop)

## <a name="dragging-styles"></a><span data-ttu-id="5e177-121">Faire glisser des styles</span><span class="sxs-lookup"><span data-stu-id="5e177-121">Dragging Styles</span></span>

<span data-ttu-id="5e177-122">Lorsque vous implémentez le modèle de contrôle [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) pour un élément déplaçable, vous devez décider s’il faut implémenter le style de glissement *source/cible* , ou le style de glissement *source uniquement* .</span><span class="sxs-lookup"><span data-stu-id="5e177-122">When you implement the [Drag](/windows/desktop/WinAuto/uiauto-implementingdrag) control pattern for a draggable element, you need to decide whether to implement the *source/target* dragging style, or the *source-only* dragging style.</span></span>

### <a name="sourcetarget-style"></a><span data-ttu-id="5e177-123">Style source/cible</span><span class="sxs-lookup"><span data-stu-id="5e177-123">Source/target Style</span></span>

<span data-ttu-id="5e177-124">Dans le style source/cible de glisser-déplacer, l’élément déplacé (la « source ») et l’élément cible (« cible ») sont distincts et chacun d’eux déclenche un ensemble d’événements distincts.</span><span class="sxs-lookup"><span data-stu-id="5e177-124">In the source/target style of drag-and-drop, the dragged element (the "source") and the drop-target element (the "target") are distinct, and each raises a distinct set of events.</span></span> <span data-ttu-id="5e177-125">Voici le cycle de vie d’une opération glisser qui utilise le style source/cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-125">Here's the life cycle for a drag operation that uses the source/target style:</span></span> <dl> <span data-ttu-id="5e177-126">Lorsque l’utilisateur démarre une opération glisser :</span><span class="sxs-lookup"><span data-stu-id="5e177-126">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="5e177-127">La source déclenche l’événement DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-127">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="5e177-128">La source définit la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="5e177-128">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="5e177-129">Les cibles mettent à jour leurs propriétés [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) .</span><span class="sxs-lookup"><span data-stu-id="5e177-129">Targets update their [**DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) properties.</span></span>

  
<span data-ttu-id="5e177-130">Lorsque l’opération glisser entre dans une région cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-130">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="5e177-131">La cible déclenche l’événement DragEnter ([**UIA \_ dropTarget \_ DragEnterEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-131">The target raises the DragEnter ([**UIA\_DropTarget\_DragEnterEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="5e177-132">Lorsque l’opération glisser quitte une région cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-132">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="5e177-133">La cible déclenche l’événement DragLeave ([**UIA \_ dropTarget \_ DragLeaveEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-133">The target raises the DragLeave ([**UIA\_DropTarget\_DragLeaveEventId**](uiauto-event-ids.md)) event.</span></span>

  
<span data-ttu-id="5e177-134">Lorsque l’utilisateur relâche l’élément déplacé sur une non-cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-134">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="5e177-135">La source déclenche l’événement DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-135">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="5e177-136">La source affecte la **valeur false** à la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) .</span><span class="sxs-lookup"><span data-stu-id="5e177-136">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="5e177-137">Lorsque l’utilisateur relâche l’élément déplacé sur une cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-137">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="5e177-138">La source déclenche l’événement DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-138">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="5e177-139">La source affecte la **valeur false** à la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) .</span><span class="sxs-lookup"><span data-stu-id="5e177-139">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>
-   <span data-ttu-id="5e177-140">La cible définit la propriété [**IDropTargetProvider ::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) pour indiquer l’effet qui s’est produit.</span><span class="sxs-lookup"><span data-stu-id="5e177-140">The target sets the [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property to indicate the effect that occurred.</span></span>
-   <span data-ttu-id="5e177-141">La cible déclenche l’événement supprimé ([**UIA \_ dropTarget \_ DroppedEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-141">The target raises the Dropped ([**UIA\_DropTarget\_DroppedEventId**](uiauto-event-ids.md)) event.</span></span>

  
</dl>

<span data-ttu-id="5e177-142">Les événements des objets source et cible sont étroitement liés, mais distincts.</span><span class="sxs-lookup"><span data-stu-id="5e177-142">The events from the source and target objects are closely related, but distinct.</span></span> <span data-ttu-id="5e177-143">Les données relatives à ce qui est glissé proviennent de la source, tandis que les données relatives à « ce qui pourrait se produire » et à « ce qui se passe » proviennent de la cible.</span><span class="sxs-lookup"><span data-stu-id="5e177-143">The data about what is being dragged comes from the source, while the data about "what could happen" and "what did happen" comes from the target.</span></span>

<span data-ttu-id="5e177-144">Quand une opération glisser est en cours, l’élément déplacé peut être glissé dans et hors des régions cibles, le nombre de fois où l’opération se termine.</span><span class="sxs-lookup"><span data-stu-id="5e177-144">When a drag operation is in progress, the dragged item can be dragged in and out of target regions any number of times before the operation completes.</span></span>

<span data-ttu-id="5e177-145">Toute cible de déplacement qui doit mettre à jour sa propriété [**IDropTargetProvider ::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) à la volée doit déclencher un événement de modification de propriété supplémentaire sur cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5e177-145">Any drop target that needs to update its [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property on the fly should raise an additional property changed event on that property.</span></span>

### <a name="source-only-style"></a><span data-ttu-id="5e177-146">Style source uniquement</span><span class="sxs-lookup"><span data-stu-id="5e177-146">Source-only Style</span></span>

<span data-ttu-id="5e177-147">Le style de glissement source uniquement permet à un fournisseur d’éviter d’implémenter des cibles de dépôt.</span><span class="sxs-lookup"><span data-stu-id="5e177-147">The source-only dragging style lets a provider avoid implementing drop targets.</span></span> <span data-ttu-id="5e177-148">Le fait de ne pas implémenter des cibles de dépôt réduit le coût d’implémentation, mais ne donne pas aux applications clientes d’accessibilité des informations sur l’objet qui a reçu la suppression.</span><span class="sxs-lookup"><span data-stu-id="5e177-148">Not implementing drop targets helps lower the implementation cost, but does not give accessibility client applications any information about the object that received the drop.</span></span> <span data-ttu-id="5e177-149">Voici le cycle de vie d’une opération glisser qui utilise le style source uniquement :</span><span class="sxs-lookup"><span data-stu-id="5e177-149">Here's the life cycle for a drag operation that uses the source-only style:</span></span> <dl> <span data-ttu-id="5e177-150">Lorsque l’utilisateur démarre une opération glisser :</span><span class="sxs-lookup"><span data-stu-id="5e177-150">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="5e177-151">La source déclenche l’événement DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-151">The source raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="5e177-152">La source définit la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="5e177-152">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>

  
<span data-ttu-id="5e177-153">Lorsque l’opération glisser entre dans une région cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-153">When the drag operation enters a target region:</span></span>

-   <span data-ttu-id="5e177-154">La source définit la propriété [**IDragProvider ::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sur la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="5e177-154">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="5e177-155">Lorsque l’opération glisser quitte une région cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-155">When the drag operation leaves a target region:</span></span>

-   <span data-ttu-id="5e177-156">La source définit la propriété [**IDragProvider ::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) sur la valeur appropriée.</span><span class="sxs-lookup"><span data-stu-id="5e177-156">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to the appropriate value.</span></span>

  
<span data-ttu-id="5e177-157">Lorsque l’utilisateur relâche l’élément déplacé sur une non-cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-157">When the user releases the dragged item over a non-target:</span></span>

-   <span data-ttu-id="5e177-158">La source déclenche l’événement DragCancel ([**UIA \_ Drag \_ DragCancelEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-158">The source raises the DragCancel ([**UIA\_Drag\_DragCancelEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="5e177-159">La source affecte la **valeur false** à la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) .</span><span class="sxs-lookup"><span data-stu-id="5e177-159">The source sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **FALSE**.</span></span>

  
<span data-ttu-id="5e177-160">Lorsque l’utilisateur relâche l’élément déplacé sur une cible :</span><span class="sxs-lookup"><span data-stu-id="5e177-160">When the user releases the dragged item over a target:</span></span>

-   <span data-ttu-id="5e177-161">La source déclenche l’événement DragComplete ([**UIA \_ Drag \_ DragCompleteEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-161">The source raises the DragComplete ([**UIA\_Drag\_DragCompleteEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="5e177-162">La source définit la propriété [**IDragProvider ::D ropeffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) pour indiquer l’effet qui a eu lieu quand l’élément a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="5e177-162">The source sets the [**IDragProvider::DropEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_dropeffect) property to indicate the effect that took place when the item was dropped.</span></span>

  
</dl>

## <a name="dragging-multiple-items"></a><span data-ttu-id="5e177-163">Faire glisser plusieurs éléments</span><span class="sxs-lookup"><span data-stu-id="5e177-163">Dragging Multiple Items</span></span>

<span data-ttu-id="5e177-164">Si un fournisseur implémente des opérations de glisser-déplacer où l’utilisateur peut faire glisser plusieurs objets en même temps, le fournisseur utilise les styles source/cible ou source uniquement comme décrit dans la section précédente, mais avec une petite différence.</span><span class="sxs-lookup"><span data-stu-id="5e177-164">If a provider implements drag-and-drop operations where the user can drag multiple objects at the same time, the provider uses the source/target or source-only styles as described in the previous section, but with a small difference.</span></span> <span data-ttu-id="5e177-165">Lorsque l’utilisateur commence l’opération glisser, le fournisseur crée un élément source maître qui représente le jeu complet d’éléments qui sont glissés.</span><span class="sxs-lookup"><span data-stu-id="5e177-165">When the user begins the drag operation, the provider creates a master source element that represents the full set of items that are being dragged.</span></span> <span data-ttu-id="5e177-166">L’élément source maître déclenche tous les événements pour le compte du jeu d’éléments déplacés ; les éléments ne déclenchent aucun événement propre.</span><span class="sxs-lookup"><span data-stu-id="5e177-166">The master source element raises all events on behalf of the set of dragged items; the items don't raise any events of their own.</span></span><dl> <span data-ttu-id="5e177-167">Lorsque l’utilisateur démarre une opération glisser :</span><span class="sxs-lookup"><span data-stu-id="5e177-167">When the user starts a drag operation:</span></span>

-   <span data-ttu-id="5e177-168">Le fournisseur crée l’élément source maître.</span><span class="sxs-lookup"><span data-stu-id="5e177-168">The provider creates the master source element.</span></span>
-   <span data-ttu-id="5e177-169">L’élément source maître déclenche l’événement DragStart ([**UIA \_ Drag \_ DragStartEventId**](uiauto-event-ids.md)).</span><span class="sxs-lookup"><span data-stu-id="5e177-169">The master source element raises the DragStart ([**UIA\_Drag\_DragStartEventId**](uiauto-event-ids.md)) event.</span></span>
-   <span data-ttu-id="5e177-170">L’élément source maître définit la propriété [**IDragProvider :: IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) sur **true**.</span><span class="sxs-lookup"><span data-stu-id="5e177-170">The master source element sets the [**IDragProvider::IsGrabbed**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-get_isgrabbed) property to **TRUE**.</span></span>
-   <span data-ttu-id="5e177-171">L’élément source maître met à jour la liste des éléments récupérés pour inclure tous les éléments déplacés afin que la méthode [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) puisse récupérer la liste.</span><span class="sxs-lookup"><span data-stu-id="5e177-171">The master source element updates the list of grabbed items to include all items being dragged so that the [**GetGrabbedItems**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idragprovider-getgrabbeditems) method can retrieve the list.</span></span>

  
</dl>

<span data-ttu-id="5e177-172">Pour ce point, l’élément source maître remplit le même rôle que celui de l’élément source, comme décrit dans la section précédente.</span><span class="sxs-lookup"><span data-stu-id="5e177-172">For that point on, the master source element performs the same role as that of the source element as described in the previous section.</span></span>

## <a name="client-interfaces-for-drag-and-drop"></a><span data-ttu-id="5e177-173">Interfaces clientes pour le glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="5e177-173">Client Interfaces for Drag-and-Drop</span></span>

<span data-ttu-id="5e177-174">Les applications clientes UI Automation utilisent les interfaces [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) et [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) pour accéder aux informations de glisser-déplacer à partir d’éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5e177-174">UI Automation client applications use the [**IUIAutomationDragPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdragpattern) and [**IUIAutomationDropTargetPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationdroptargetpattern) interfaces to access drag-and-drop information from UI elements.</span></span>

 

 