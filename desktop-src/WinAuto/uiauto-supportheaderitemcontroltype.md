---
title: Type de contrôle HeaderItem
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle HeaderItem.
ms.assetid: c70420d6-d9f3-47c8-a09f-35ed170f815f
keywords:
- UI Automation, prise en charge du type de contrôle HeaderItem
- UI Automation, type de contrôle HeaderItem
- UI Automation, arborescence pour le type de contrôle HeaderItem
- UI Automation, propriétés du type de contrôle HeaderItem
- UI Automation, modèles de contrôle pour le type de contrôle HeaderItem
- UI Automation, événements pour le type de contrôle HeaderItem
- arborescences, type de contrôle HeaderItem
- Propriétés, type de contrôle HeaderItem
- modèles de contrôle, type de contrôle HeaderItem
- événements, type de contrôle HeaderItem
- prise en charge du type de contrôle HeaderItem
- Type de contrôle HeaderItem
- types de contrôles, arborescence pour le type de contrôle HeaderItem
- types de contrôle, modèles de contrôle pour le type de contrôle HeaderItem
- types de contrôle, prise en charge de HeaderItem
- types de contrôles, HeaderItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bab61f92a6ab4db221810f9f083279ade4bf353
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513665"
---
# <a name="headeritem-control-type"></a><span data-ttu-id="b07af-119">Type de contrôle HeaderItem</span><span class="sxs-lookup"><span data-stu-id="b07af-119">HeaderItem Control Type</span></span>

<span data-ttu-id="b07af-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="b07af-120">This topic provides information about Microsoft UI Automation support for the **HeaderItem** control type.</span></span>

<span data-ttu-id="b07af-121">Le type de contrôle **HeaderItem** fournit une étiquette visuelle pour une ligne ou une colonne d’informations.</span><span class="sxs-lookup"><span data-stu-id="b07af-121">The **HeaderItem** control type provides a visual label for a row or column of information.</span></span>

<span data-ttu-id="b07af-122">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="b07af-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **HeaderItem** control type.</span></span> <span data-ttu-id="b07af-123">Les exigences d’UI Automation s’appliquent à tous les contrôles d’élément d’en-tête où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b07af-123">The UI Automation requirements apply to all header item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="b07af-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b07af-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b07af-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="b07af-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="b07af-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="b07af-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="b07af-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="b07af-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="b07af-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="b07af-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="b07af-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b07af-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="b07af-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="b07af-130">Typical Tree Structure</span></span>

<span data-ttu-id="b07af-131">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles d’élément d’en-tête et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="b07af-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="b07af-132">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b07af-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b07af-133">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="b07af-133">Control View</span></span></th>
<th><span data-ttu-id="b07af-134">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="b07af-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b07af-135">HeaderItem</span><span class="sxs-lookup"><span data-stu-id="b07af-135">HeaderItem</span></span></li>
</ul></td>
<td><span data-ttu-id="b07af-136">(Non applicable)</span><span class="sxs-lookup"><span data-stu-id="b07af-136">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="b07af-137">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="b07af-137">Relevant Properties</span></span>

<span data-ttu-id="b07af-138">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="b07af-138">The following table lists the UI Automation properties whose value or definition is especially relevant to the **HeaderItem** control type.</span></span> <span data-ttu-id="b07af-139">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="b07af-139">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="b07af-140">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="b07af-140">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="b07af-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="b07af-141">Value</span></span>          | <span data-ttu-id="b07af-142">Notes</span><span class="sxs-lookup"><span data-stu-id="b07af-142">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b07af-143">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-143">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="b07af-144">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b07af-144">See notes.</span></span>     | <span data-ttu-id="b07af-145">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b07af-145">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="b07af-146">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-146">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="b07af-147">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b07af-147">See notes.</span></span>     | <span data-ttu-id="b07af-148">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="b07af-148">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="b07af-149">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-149">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="b07af-150">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b07af-150">See notes.</span></span>     | <span data-ttu-id="b07af-151">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="b07af-151">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="b07af-152">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="b07af-152">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="b07af-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b07af-154">**HeaderItem**</span><span class="sxs-lookup"><span data-stu-id="b07af-154">**HeaderItem**</span></span> | <span data-ttu-id="b07af-155">Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b07af-155">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="b07af-156">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-156">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b07af-157">FALSE</span><span class="sxs-lookup"><span data-stu-id="b07af-157">FALSE</span></span>          | <span data-ttu-id="b07af-158">Le contrôle header Item n’est pas inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b07af-158">The header item control is not included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="b07af-159">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-159">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b07af-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="b07af-160">TRUE</span></span>           | <span data-ttu-id="b07af-161">Le contrôle header Item est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b07af-161">The header item control is always included in the control view of the UI Automation tree.</span></span>                                                                                                            |
| [<span data-ttu-id="b07af-162">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-162">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="b07af-163">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b07af-163">See notes.</span></span>     | <span data-ttu-id="b07af-164">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="b07af-164">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="b07af-165">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-165">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="b07af-166">Voir les remarques</span><span class="sxs-lookup"><span data-stu-id="b07af-166">See notes</span></span>      | <span data-ttu-id="b07af-167">Cette propriété fournit des informations pour les ordres de tri par élément d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="b07af-167">This property provides information for sort orders by the header item.</span></span>                                                                                                                               |
| [<span data-ttu-id="b07af-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="b07af-169">NULL</span><span class="sxs-lookup"><span data-stu-id="b07af-169">NULL</span></span>           | <span data-ttu-id="b07af-170">Les contrôles Header Item n’ont pas d’étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="b07af-170">Header item controls do not have a static text label.</span></span>                                                                                                                                                |
| [<span data-ttu-id="b07af-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="b07af-172">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b07af-172">See notes.</span></span>     | <span data-ttu-id="b07af-173">Chaîne localisée correspondant au type de contrôle **HeaderItem** .</span><span class="sxs-lookup"><span data-stu-id="b07af-173">Localized string corresponding to the **HeaderItem** control type.</span></span> <span data-ttu-id="b07af-174">La valeur par défaut est « élément d’en-tête » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="b07af-174">The default value is "header item" for en-US or English (United States).</span></span>                                                          |
| [<span data-ttu-id="b07af-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b07af-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="b07af-176">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b07af-176">See notes.</span></span>     | <span data-ttu-id="b07af-177">Le contrôle header item est toujours à étiquetage automatique.</span><span class="sxs-lookup"><span data-stu-id="b07af-177">The header item control is always self-labeling.</span></span>                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="b07af-178">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="b07af-178">Required Control Patterns</span></span>

<span data-ttu-id="b07af-179">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles Header Item.</span><span class="sxs-lookup"><span data-stu-id="b07af-179">The following table lists the UI Automation control patterns required to be supported by all header item controls.</span></span> <span data-ttu-id="b07af-180">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b07af-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="b07af-181">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="b07af-181">Control Pattern</span></span>                                         | <span data-ttu-id="b07af-182">Support</span><span class="sxs-lookup"><span data-stu-id="b07af-182">Support</span></span> | <span data-ttu-id="b07af-183">Notes</span><span class="sxs-lookup"><span data-stu-id="b07af-183">Notes</span></span>                                                                                                                             |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b07af-184">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="b07af-184">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)       | <span data-ttu-id="b07af-185">Dépend</span><span class="sxs-lookup"><span data-stu-id="b07af-185">Depends</span></span> | <span data-ttu-id="b07af-186">Implémentez le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) si vous pouvez cliquer sur le contrôle header Item pour trier les données.</span><span class="sxs-lookup"><span data-stu-id="b07af-186">Implement the [Invoke](uiauto-implementinginvoke.md) control pattern if the header item control can be clicked to sort the data.</span></span> |
| [<span data-ttu-id="b07af-187">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="b07af-187">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="b07af-188">Dépend</span><span class="sxs-lookup"><span data-stu-id="b07af-188">Depends</span></span> | <span data-ttu-id="b07af-189">Implémentez le modèle de contrôle [Transform](uiauto-implementingtransform.md) si le contrôle header Item peut être redimensionné.</span><span class="sxs-lookup"><span data-stu-id="b07af-189">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header item control can be resized.</span></span>            |



 

## <a name="required-events"></a><span data-ttu-id="b07af-190">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="b07af-190">Required Events</span></span>

<span data-ttu-id="b07af-191">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’élément d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="b07af-191">The following table lists the UI Automation events that header item controls are required to support.</span></span> <span data-ttu-id="b07af-192">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b07af-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="b07af-193">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="b07af-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="b07af-194">Notes</span><span class="sxs-lookup"><span data-stu-id="b07af-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b07af-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b07af-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="b07af-196">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b07af-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="b07af-197">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="b07af-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="b07af-198">Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="b07af-198">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="b07af-199">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b07af-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="b07af-200">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="b07af-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="b07af-201">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b07af-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="b07af-202">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="b07af-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="b07af-203">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b07af-203">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="b07af-204">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b07af-204">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b07af-205">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b07af-205">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b07af-206">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="b07af-206">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="b07af-207">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="b07af-207">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




