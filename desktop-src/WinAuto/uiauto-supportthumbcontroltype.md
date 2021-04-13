---
title: Thumb (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Thumb.
ms.assetid: 3b1d6802-cfd4-4b07-80a0-2950ca7f4e96
keywords:
- UI Automation, prise en charge du type de contrôle Thumb
- UI Automation, type de contrôle Thumb
- UI Automation, arborescence pour le type de contrôle Thumb
- UI Automation, propriétés du type de contrôle Thumb
- UI Automation, modèles de contrôle pour le type de contrôle Thumb
- UI Automation, événements pour le type de contrôle Thumb
- arborescences, type de contrôle Thumb
- Propriétés, type de contrôle Thumb
- modèles de contrôle, type de contrôle Thumb
- événements, type de contrôle Thumb
- prise en charge du type de contrôle Thumb
- Thumb (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Thumb
- types de contrôles, modèles de contrôle pour le type de contrôle Thumb
- types de contrôles, prise en charge de Thumb
- types de contrôles, Thumb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8faf60fab30f54d3ed3e4b5a9f49628a3a35be5b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380322"
---
# <a name="thumb-control-type"></a><span data-ttu-id="01ad5-119">Thumb (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="01ad5-119">Thumb Control Type</span></span>

<span data-ttu-id="01ad5-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="01ad5-120">This topic provides information about Microsoft UI Automation support for the **Thumb** control type.</span></span>

<span data-ttu-id="01ad5-121">Les contrôles curseur de position fournissent des fonctionnalités qui permettent de déplacer ou de faire glisser un contrôle, par exemple un bouton de barre de défilement, ou de le redimensionner, par exemple un widget de redimensionnement de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="01ad5-121">Thumb controls provide the functionality that enables a control to be moved (or dragged), such as a scroll bar button, or resized, such as a window resizing widget.</span></span> <span data-ttu-id="01ad5-122">Notez qu’un contrôle Thumb ne fournit pas de fonctionnalité de glisser-déplacer.</span><span class="sxs-lookup"><span data-stu-id="01ad5-122">Note that a thumb control does not provide drag-and-drop functionality.</span></span> <span data-ttu-id="01ad5-123">Les contrôles Thumb peuvent recevoir le focus de souris, mais pas le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="01ad5-123">Thumb controls can receive mouse focus but not keyboard focus.</span></span> <span data-ttu-id="01ad5-124">Le développeur du contrôle doit implémenter ce dernier pour qu’il se comporte de manière appropriée (déplacement ou redimensionnement).</span><span class="sxs-lookup"><span data-stu-id="01ad5-124">The control developer must implement the control so that it acts appropriately (can be dragged or resized).</span></span>

<span data-ttu-id="01ad5-125">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="01ad5-125">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Thumb** control type.</span></span> <span data-ttu-id="01ad5-126">Les exigences d’UI Automation appliquent tous les contrôles Thumb où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="01ad5-126">The UI Automation requirements apply all thumb controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="01ad5-127">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="01ad5-127">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="01ad5-128">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="01ad5-128">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="01ad5-129">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="01ad5-129">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="01ad5-130">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="01ad5-130">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="01ad5-131">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="01ad5-131">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="01ad5-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01ad5-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="01ad5-133">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="01ad5-133">Typical Tree Structure</span></span>

<span data-ttu-id="01ad5-134">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles Thumb et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="01ad5-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to thumb controls and describes what can be contained in each view.</span></span> <span data-ttu-id="01ad5-135">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="01ad5-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01ad5-136">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="01ad5-136">Control View</span></span></th>
<th><span data-ttu-id="01ad5-137">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="01ad5-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="01ad5-138">Thumb</span><span class="sxs-lookup"><span data-stu-id="01ad5-138">Thumb</span></span></li>
</ul></td>
<td><span data-ttu-id="01ad5-139">(Non applicable)</span><span class="sxs-lookup"><span data-stu-id="01ad5-139">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="01ad5-140">Les contrôles Thumb n’apparaissent jamais dans l’affichage de contenu, car ils n’existent que pour être manipulés avec une souris.</span><span class="sxs-lookup"><span data-stu-id="01ad5-140">Thumb controls never appear in the content view because they exist only to be manipulated with a mouse.</span></span> <span data-ttu-id="01ad5-141">Ils sont exposés via un autre modèle de contrôle, tel que le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , le modèle de contrôle [Transform](uiauto-implementingtransform.md) ou le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , pris en charge sur le conteneur du contrôle Thumb.</span><span class="sxs-lookup"><span data-stu-id="01ad5-141">They are exposed though another control pattern, such as the [Scroll](uiauto-implementingscroll.md) control pattern, [Transform](uiauto-implementingtransform.md) control pattern, or [RangeValue](uiauto-implementingrangevalue.md) control pattern, being supported on the thumb control's container.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="01ad5-142">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="01ad5-142">Relevant Properties</span></span>

<span data-ttu-id="01ad5-143">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Thumb.</span><span class="sxs-lookup"><span data-stu-id="01ad5-143">The following table lists the UI Automation properties whose value or definition is especially relevant to thumb controls.</span></span> <span data-ttu-id="01ad5-144">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="01ad5-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="01ad5-145">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="01ad5-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="01ad5-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="01ad5-146">Value</span></span>      | <span data-ttu-id="01ad5-147">Notes</span><span class="sxs-lookup"><span data-stu-id="01ad5-147">Notes</span></span>                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01ad5-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="01ad5-149">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="01ad5-149">See notes.</span></span> | <span data-ttu-id="01ad5-150">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="01ad5-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="01ad5-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="01ad5-152">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="01ad5-152">See notes.</span></span> | <span data-ttu-id="01ad5-153">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="01ad5-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                     |
| [<span data-ttu-id="01ad5-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="01ad5-155">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="01ad5-155">See notes.</span></span> | <span data-ttu-id="01ad5-156">Point dans la zone cliente visible du contrôle Thumb.</span><span class="sxs-lookup"><span data-stu-id="01ad5-156">A point within the visible client area of the thumb control.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="01ad5-157">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-157">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="01ad5-158">**Flash**</span><span class="sxs-lookup"><span data-stu-id="01ad5-158">**Thumb**</span></span>  |                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="01ad5-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="01ad5-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="01ad5-160">FALSE</span></span>      | <span data-ttu-id="01ad5-161">Le contrôle Thumb n’est jamais inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="01ad5-161">The thumb control is never included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="01ad5-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="01ad5-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="01ad5-163">TRUE</span></span>       | <span data-ttu-id="01ad5-164">Le contrôle Thumb est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="01ad5-164">The thumb control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="01ad5-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="01ad5-166">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="01ad5-166">See notes.</span></span> | <span data-ttu-id="01ad5-167">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="01ad5-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="01ad5-168">Un contrôle Thumb peut recevoir le focus s’il est utilisé comme un objet de « pincement » pour le dimensionnement d’une fenêtre ou d’un volet.</span><span class="sxs-lookup"><span data-stu-id="01ad5-168">A thumb control can receive the focus if it is used as a "gripper" object for sizing a window or a pane.</span></span> <span data-ttu-id="01ad5-169">Un contrôle Thumb dans un curseur ou une barre de défilement ne doit jamais recevoir le focus.</span><span class="sxs-lookup"><span data-stu-id="01ad5-169">A thumb control in a slider or scroll bar should never receive the focus.</span></span> |
| [<span data-ttu-id="01ad5-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="01ad5-171">NULL</span><span class="sxs-lookup"><span data-stu-id="01ad5-171">NULL</span></span>       | <span data-ttu-id="01ad5-172">Les contrôles curseur de position n’ont jamais d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="01ad5-172">Thumb controls never have a label.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="01ad5-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="01ad5-174">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="01ad5-174">See notes.</span></span> | <span data-ttu-id="01ad5-175">Chaîne localisée correspondant au type de contrôle **Thumb** .</span><span class="sxs-lookup"><span data-stu-id="01ad5-175">Localized string corresponding to the **Thumb** control type.</span></span> <span data-ttu-id="01ad5-176">La valeur par défaut est « Thumb » pour « fr-fr » ou « anglais » (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="01ad5-176">The default value is "thumb" for en-US or English (United States).</span></span>                                                                                                                             |
| [<span data-ttu-id="01ad5-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="01ad5-178">NULL</span><span class="sxs-lookup"><span data-stu-id="01ad5-178">NULL</span></span>       | <span data-ttu-id="01ad5-179">Étant donné que le contrôle Thumb n’est pas disponible dans l’affichage de contenu de l’arborescence UI Automation, il ne nécessite pas de nom.</span><span class="sxs-lookup"><span data-stu-id="01ad5-179">Because the thumb control is not available in the content view of the UI Automation tree, it does not require a name.</span></span>                                                                                                                                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="01ad5-180">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="01ad5-180">Required Control Patterns</span></span>

<span data-ttu-id="01ad5-181">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles Thumb.</span><span class="sxs-lookup"><span data-stu-id="01ad5-181">The following table lists the UI Automation control patterns required to be supported by thumb controls.</span></span> <span data-ttu-id="01ad5-182">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="01ad5-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="01ad5-183">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="01ad5-183">Control Pattern</span></span>                                         | <span data-ttu-id="01ad5-184">Support</span><span class="sxs-lookup"><span data-stu-id="01ad5-184">Support</span></span>  | <span data-ttu-id="01ad5-185">Notes</span><span class="sxs-lookup"><span data-stu-id="01ad5-185">Notes</span></span>                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01ad5-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="01ad5-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="01ad5-187">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="01ad5-187">Required</span></span> | <span data-ttu-id="01ad5-188">Permet de déplacer le contrôle curseur de position à l’écran.</span><span class="sxs-lookup"><span data-stu-id="01ad5-188">Enables the thumb control to be moved on the screen.</span></span> <span data-ttu-id="01ad5-189">Étant donné que le contrôle Thumb ne peut généralement pas être redimensionné ou pivoté, le modèle de contrôle [Transform](uiauto-implementingtransform.md) prend principalement en charge la fonction [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) .</span><span class="sxs-lookup"><span data-stu-id="01ad5-189">Because the thumb control typically cannot be resized or rotated, the [Transform](uiauto-implementingtransform.md) control pattern primarily supports the [**Move**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move) function.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="01ad5-190">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="01ad5-190">Required Events</span></span>

<span data-ttu-id="01ad5-191">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles Thumb.</span><span class="sxs-lookup"><span data-stu-id="01ad5-191">The following table lists the UI Automation events that thumb controls are required to support.</span></span> <span data-ttu-id="01ad5-192">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="01ad5-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="01ad5-193">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="01ad5-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="01ad5-194">Notes</span><span class="sxs-lookup"><span data-stu-id="01ad5-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="01ad5-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="01ad5-196">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="01ad5-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="01ad5-197">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="01ad5-197">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="01ad5-198">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="01ad5-198">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="01ad5-199">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="01ad5-199">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="01ad5-200">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="01ad5-200">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="01ad5-201">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="01ad5-201">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="01ad5-202">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="01ad5-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="01ad5-203">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="01ad5-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="01ad5-204">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="01ad5-204">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="01ad5-205">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="01ad5-205">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




