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
ms.openlocfilehash: fd03d219ce8b26a0ac01806ebab09892a027fbd1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315671"
---
# <a name="droptarget-control-pattern"></a><span data-ttu-id="83328-113">Modèle de contrôle DropTarget</span><span class="sxs-lookup"><span data-stu-id="83328-113">DropTarget Control Pattern</span></span>

<span data-ttu-id="83328-114">Fournit des recommandations et des conventions pour implémenter le modèle de contrôle **dropTarget** à l’aide de [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="83328-114">Provides guidelines and conventions for implementing the **DropTarget** control pattern by using [**IDropTargetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-idroptargetprovider), including information about properties and methods.</span></span> <span data-ttu-id="83328-115">Le modèle de contrôle **dropTarget** est utilisé pour prendre en charge les contrôles qui peuvent être la cible d’une opération de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="83328-115">The **DropTarget** control pattern is used to support controls that can be the target of a drag-and-drop operation.</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="83328-116">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="83328-116">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="83328-117">Lorsque vous implémentez le modèle de contrôle **dropTarget** , utilisez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="83328-117">When implementing the **DropTarget** control pattern, use the following guidelines and conventions:</span></span>

-   <span data-ttu-id="83328-118">Le modèle **dropTarget** doit être pris en charge lorsqu’une opération glisser est en cours.</span><span class="sxs-lookup"><span data-stu-id="83328-118">The **DropTarget** pattern must be supported while a drag operation is in progress.</span></span> <span data-ttu-id="83328-119">Elle peut être prise en charge même quand une opération glisser n’est pas en cours.</span><span class="sxs-lookup"><span data-stu-id="83328-119">It can be supported even when a drag operation is not in progress.</span></span>
-   <span data-ttu-id="83328-120">La propriété [**IDropTargetProvider ::D roptargeteffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) est requise.</span><span class="sxs-lookup"><span data-stu-id="83328-120">The [**IDropTargetProvider::DropTargetEffect**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect) property is required.</span></span>
-   <span data-ttu-id="83328-121">La propriété [**IDropTargetProvider ::D roptargeteffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) est requise lorsqu’il y a plus d’un effet de dépôt possible pour la cible.</span><span class="sxs-lookup"><span data-stu-id="83328-121">The [**IDropTargetProvider::DropTargetEffects**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects) property is required when there is more than one possible drop effect for the target.</span></span>
-   <span data-ttu-id="83328-122">L’élément doit déclencher des événements de modification de propriété pour les propriétés **DropTargetEffect** ([**UIA \_ DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) et **DropTargetEffects** ([**UIA \_ DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) lorsqu’elles changent.</span><span class="sxs-lookup"><span data-stu-id="83328-122">The element must raise property changed events for the **DropTargetEffect** ([**UIA\_DropTargetDropTargetEffectPropertyId**](uiauto-control-pattern-propids.md)) and **DropTargetEffects** ([**UIA\_DropTargetDropTargetEffectsPropertyId**](uiauto-control-pattern-propids.md)) properties when they change.</span></span>

## <a name="required-members-for-idroptargetprovider"></a><span data-ttu-id="83328-123">Membres requis pour **IDropTargetProvider**</span><span class="sxs-lookup"><span data-stu-id="83328-123">Required Members for **IDropTargetProvider**</span></span>

<span data-ttu-id="83328-124">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) .</span><span class="sxs-lookup"><span data-stu-id="83328-124">The following properties and methods are required for implementing the [**IDropTargetProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idroptargetprovider) interface.</span></span>



| <span data-ttu-id="83328-125">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="83328-125">Required members</span></span>                                                                              | <span data-ttu-id="83328-126">Type de membre</span><span class="sxs-lookup"><span data-stu-id="83328-126">Member type</span></span> | <span data-ttu-id="83328-127">Notes</span><span class="sxs-lookup"><span data-stu-id="83328-127">Notes</span></span>                                                                    |
|-----------------------------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="83328-128">**DropTargetEffect**</span><span class="sxs-lookup"><span data-stu-id="83328-128">**DropTargetEffect**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffect)                       | <span data-ttu-id="83328-129">Propriété</span><span class="sxs-lookup"><span data-stu-id="83328-129">Property</span></span>    | <span data-ttu-id="83328-130">Aucun</span><span class="sxs-lookup"><span data-stu-id="83328-130">None</span></span>                                                                     |
| [<span data-ttu-id="83328-131">**DropTargetEffects**</span><span class="sxs-lookup"><span data-stu-id="83328-131">**DropTargetEffects**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idroptargetprovider-get_droptargeteffects)                     | <span data-ttu-id="83328-132">Propriété</span><span class="sxs-lookup"><span data-stu-id="83328-132">Property</span></span>    | <span data-ttu-id="83328-133">Obligatoire si la cible de déplacement prend en charge plusieurs effets de suppression possibles.</span><span class="sxs-lookup"><span data-stu-id="83328-133">Required if the drop target supports more than one possible drop effect.</span></span> |
| [<span data-ttu-id="83328-134">**UIA \_ dropTarget \_ DragEnterEventId**</span><span class="sxs-lookup"><span data-stu-id="83328-134">**UIA\_DropTarget\_DragEnterEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="83328-135">Événement</span><span class="sxs-lookup"><span data-stu-id="83328-135">Event</span></span>       | <span data-ttu-id="83328-136">Aucun</span><span class="sxs-lookup"><span data-stu-id="83328-136">None</span></span>                                                                     |
| [<span data-ttu-id="83328-137">**UIA \_ dropTarget \_ DragLeaveEventId**</span><span class="sxs-lookup"><span data-stu-id="83328-137">**UIA\_DropTarget\_DragLeaveEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="83328-138">Événement</span><span class="sxs-lookup"><span data-stu-id="83328-138">Event</span></span>       | <span data-ttu-id="83328-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="83328-139">None</span></span>                                                                     |
| [<span data-ttu-id="83328-140">**UIA \_ dropTarget \_ DroppedEventId**</span><span class="sxs-lookup"><span data-stu-id="83328-140">**UIA\_DropTarget\_DroppedEventId**</span></span>](uiauto-event-ids.md)     | <span data-ttu-id="83328-141">Événement</span><span class="sxs-lookup"><span data-stu-id="83328-141">Event</span></span>       | <span data-ttu-id="83328-142">Aucun</span><span class="sxs-lookup"><span data-stu-id="83328-142">None</span></span>                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="83328-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="83328-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="83328-144">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="83328-144">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="83328-145">Faire glisser le modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="83328-145">Drag Control Pattern</span></span>](/windows/desktop/WinAuto/uiauto-implementingdrag)
</dt> <dt>

[<span data-ttu-id="83328-146">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="83328-146">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="83328-147">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="83328-147">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> <dt>

[<span data-ttu-id="83328-148">Prise en charge d’UI Automation pour le glisser-déplacer</span><span class="sxs-lookup"><span data-stu-id="83328-148">UI Automation Support for Drag-and-Drop</span></span>](ui-automation-support-for-drag-and-drop.md)
</dt> </dl>

 

 