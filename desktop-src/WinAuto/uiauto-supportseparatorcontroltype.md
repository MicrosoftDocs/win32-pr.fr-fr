---
title: Separator (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Separator.
ms.assetid: 4987b05a-101e-48b1-aed2-bd7206146f70
keywords:
- UI Automation, prise en charge du type de contrôle Separator
- UI Automation, type de contrôle Separator
- UI Automation, arborescence pour le type de contrôle Separator
- UI Automation, propriétés du type de contrôle Separator
- UI Automation, modèles de contrôle pour le type de contrôle Separator
- UI Automation, événements pour le type de contrôle Separator
- arborescences, type de contrôle Separator
- Propriétés, Separator (type de contrôle)
- modèles de contrôle, Separator (type de contrôle)
- événements, type de contrôle Separator
- prise en charge du type de contrôle Separator
- Separator (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Separator
- types de contrôle, modèles de contrôle pour le type de contrôle Separator
- types de contrôles, prise en charge du séparateur
- types de contrôles, séparateur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92cdf6c15dbe461e78877c6b93f0ff4b52f67fc8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507343"
---
# <a name="separator-control-type"></a><span data-ttu-id="6735f-119">Separator (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="6735f-119">Separator Control Type</span></span>

<span data-ttu-id="6735f-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **separator** .</span><span class="sxs-lookup"><span data-stu-id="6735f-120">This topic provides information about Microsoft UI Automation support for the **Separator** control type.</span></span>

<span data-ttu-id="6735f-121">Les contrôles Separator permettent de diviser visuellement un espace en deux zones.</span><span class="sxs-lookup"><span data-stu-id="6735f-121">Separator controls are used to visually divide a space into two regions.</span></span> <span data-ttu-id="6735f-122">Une barre définissant deux volets dans une fenêtre est un exemple de contrôle Separator.</span><span class="sxs-lookup"><span data-stu-id="6735f-122">For example, a separator control can be a bar that defines two panes in a window.</span></span> <span data-ttu-id="6735f-123">Si le séparateur peut être déplacé, le contrôle doit être exposé en tant que Thumb (curseur de défilement) dans le type de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6735f-123">If the separator can be moved, the control should be exposed as Thumb in control type.</span></span>

<span data-ttu-id="6735f-124">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **separator** .</span><span class="sxs-lookup"><span data-stu-id="6735f-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Separator** control type.</span></span> <span data-ttu-id="6735f-125">Les exigences d’UI Automation s’appliquent à tous les contrôles Separator où l’infrastructure ou la plateforme de l’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6735f-125">The UI Automation requirements apply to all separator controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="6735f-126">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6735f-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6735f-127">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="6735f-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="6735f-128">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="6735f-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="6735f-129">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="6735f-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="6735f-130">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="6735f-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="6735f-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6735f-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="6735f-132">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="6735f-132">Typical Tree Structure</span></span>

<span data-ttu-id="6735f-133">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles separator et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="6735f-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to separator controls and describes what can be contained in each view.</span></span> <span data-ttu-id="6735f-134">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6735f-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6735f-135">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="6735f-135">Control View</span></span></th>
<th><span data-ttu-id="6735f-136">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="6735f-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="6735f-137">Séparateur</span><span class="sxs-lookup"><span data-stu-id="6735f-137">Separator</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="6735f-138">Le type de contrôle <strong>separator</strong> n’a jamais de contenu.</span><span class="sxs-lookup"><span data-stu-id="6735f-138">The <strong>Separator</strong> control type never has content.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="6735f-139">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="6735f-139">Relevant Properties</span></span>

<span data-ttu-id="6735f-140">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Separator.</span><span class="sxs-lookup"><span data-stu-id="6735f-140">The following table lists the UI Automation properties whose value or definition is especially relevant to separator controls.</span></span> <span data-ttu-id="6735f-141">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="6735f-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="6735f-142">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="6735f-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="6735f-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="6735f-143">Value</span></span>         | <span data-ttu-id="6735f-144">Notes</span><span class="sxs-lookup"><span data-stu-id="6735f-144">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6735f-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="6735f-146">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="6735f-146">See notes.</span></span>    | <span data-ttu-id="6735f-147">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="6735f-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="6735f-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="6735f-149">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="6735f-149">See notes.</span></span>    | <span data-ttu-id="6735f-150">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="6735f-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="6735f-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="6735f-152">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="6735f-152">See notes.</span></span>    | <span data-ttu-id="6735f-153">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="6735f-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="6735f-154">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="6735f-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="6735f-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="6735f-156">**Séparateur**</span><span class="sxs-lookup"><span data-stu-id="6735f-156">**Separator**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="6735f-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6735f-158">FALSE</span><span class="sxs-lookup"><span data-stu-id="6735f-158">FALSE</span></span>         | <span data-ttu-id="6735f-159">Le contrôle de séparateur ne correspond jamais à du contenu.</span><span class="sxs-lookup"><span data-stu-id="6735f-159">The separator control is never content.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="6735f-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="6735f-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="6735f-161">TRUE</span></span>          | <span data-ttu-id="6735f-162">Le contrôle de séparateur doit toujours être un contrôle.</span><span class="sxs-lookup"><span data-stu-id="6735f-162">The separator control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="6735f-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="6735f-164">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="6735f-164">See notes.</span></span>    | <span data-ttu-id="6735f-165">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="6735f-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="6735f-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="6735f-167">NULL</span><span class="sxs-lookup"><span data-stu-id="6735f-167">NULL</span></span>          | <span data-ttu-id="6735f-168">Le contrôle de séparateur n’a pas d’étiquette statique.</span><span class="sxs-lookup"><span data-stu-id="6735f-168">The separator control does not have a static label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="6735f-169">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-169">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="6735f-170">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="6735f-170">See notes.</span></span>    | <span data-ttu-id="6735f-171">Chaîne localisée correspondant au type de contrôle **separator** .</span><span class="sxs-lookup"><span data-stu-id="6735f-171">Localized string corresponding to the **Separator** control type.</span></span> <span data-ttu-id="6735f-172">La valeur par défaut est « Separator » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="6735f-172">The default value is "Separator" for en-US or English (United States).</span></span>                                                             |
| [<span data-ttu-id="6735f-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="6735f-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="6735f-174">""</span><span class="sxs-lookup"><span data-stu-id="6735f-174">""</span></span>            | <span data-ttu-id="6735f-175">Le contrôle Separator ne nécessite pas de propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="6735f-175">The separator control does not require a **Name** property.</span></span>                                                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="6735f-176">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="6735f-176">Required Control Patterns</span></span>

<span data-ttu-id="6735f-177">Le contrôle de séparateur n’est pas requis pour la prise en charge des modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="6735f-177">The separator control is not required to support any control patterns.</span></span> <span data-ttu-id="6735f-178">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6735f-178">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>

## <a name="required-events"></a><span data-ttu-id="6735f-179">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="6735f-179">Required Events</span></span>

<span data-ttu-id="6735f-180">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles Separator.</span><span class="sxs-lookup"><span data-stu-id="6735f-180">The following table lists the UI Automation events that separator controls are required to support.</span></span> <span data-ttu-id="6735f-181">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="6735f-181">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="6735f-182">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="6735f-182">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="6735f-183">Notes</span><span class="sxs-lookup"><span data-stu-id="6735f-183">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6735f-184">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6735f-184">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="6735f-185">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="6735f-185">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="6735f-186">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6735f-186">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="6735f-187">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="6735f-187">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="6735f-188">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="6735f-188">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="6735f-189">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="6735f-189">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="6735f-190">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="6735f-190">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="6735f-191">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6735f-191">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6735f-192">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6735f-192">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6735f-193">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="6735f-193">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="6735f-194">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="6735f-194">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




