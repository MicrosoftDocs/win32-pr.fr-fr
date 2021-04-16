---
title: ToolBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle ToolBar. Les contrôles de barre d’outils permettent aux utilisateurs finaux d’activer les commandes et les outils contenus dans une application.
ms.assetid: e2a72ce3-5263-43f8-be4d-715a78224b68
keywords:
- UI Automation, prise en charge du type de contrôle ToolBar
- UI Automation, type de contrôle ToolBar
- UI Automation, arborescence pour le type de contrôle ToolBar
- UI Automation, propriétés du type de contrôle ToolBar
- UI Automation, modèles de contrôle pour le type de contrôle ToolBar
- UI Automation, événements pour le type de contrôle ToolBar
- arborescences, type de contrôle ToolBar
- Propriétés, type de contrôle ToolBar
- modèles de contrôle, type de contrôle ToolBar
- événements, type de contrôle ToolBar
- prise en charge du type de contrôle ToolBar
- ToolBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle ToolBar
- types de contrôles, modèles de contrôle pour le type de contrôle ToolBar
- types de contrôles, prise en charge pour la barre d’outils
- types de contrôles, barre d’outils
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4327c187a86ace6f02b93082675c345eae4d4edf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380321"
---
# <a name="toolbar-control-type"></a><span data-ttu-id="66516-120">ToolBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="66516-120">ToolBar Control Type</span></span>

<span data-ttu-id="66516-121">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="66516-121">This topic provides information about Microsoft UI Automation support for the **ToolBar** control type.</span></span> <span data-ttu-id="66516-122">Les contrôles de barre d’outils permettent aux utilisateurs finaux d’activer les commandes et les outils contenus dans une application.</span><span class="sxs-lookup"><span data-stu-id="66516-122">Toolbar controls enable end users to activate commands and tools contained within a application.</span></span>

<span data-ttu-id="66516-123">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="66516-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **ToolBar** control type.</span></span> <span data-ttu-id="66516-124">Les exigences d’UI Automation s’appliquent à tous les contrôles ToolBar où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="66516-124">The UI Automation requirements apply to all toolbar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="66516-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="66516-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="66516-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="66516-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="66516-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="66516-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="66516-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="66516-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="66516-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="66516-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="66516-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66516-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="66516-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="66516-131">Typical Tree Structure</span></span>

<span data-ttu-id="66516-132">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles ToolBar et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="66516-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to toolbar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="66516-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="66516-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66516-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="66516-134">Control View</span></span></th>
<th><span data-ttu-id="66516-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="66516-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="66516-136">ToolBar</span><span class="sxs-lookup"><span data-stu-id="66516-136">ToolBar</span></span>
<ul>
<li><span data-ttu-id="66516-137">Plusieurs contrôles (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="66516-137">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="66516-138">ToolBar</span><span class="sxs-lookup"><span data-stu-id="66516-138">ToolBar</span></span>
<ul>
<li><span data-ttu-id="66516-139">Plusieurs contrôles (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="66516-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="66516-140">Un contrôle ToolBar peut contenir n’importe quel type de contrôle dans sa sous-arborescence.</span><span class="sxs-lookup"><span data-stu-id="66516-140">A toolbar control can contain any type of control within its subtree.</span></span> <span data-ttu-id="66516-141">Le plus souvent, ils contiennent des boutons, des zones de liste modifiables et des boutons partagés.</span><span class="sxs-lookup"><span data-stu-id="66516-141">They most often contain buttons, combo boxes, and split buttons.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="66516-142">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="66516-142">Relevant Properties</span></span>

<span data-ttu-id="66516-143">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="66516-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the **ToolBar** control type.</span></span> <span data-ttu-id="66516-144">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="66516-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="66516-145">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="66516-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="66516-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="66516-146">Value</span></span>       | <span data-ttu-id="66516-147">Notes</span><span class="sxs-lookup"><span data-stu-id="66516-147">Notes</span></span>                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66516-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="66516-149">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="66516-149">See notes.</span></span>  | <span data-ttu-id="66516-150">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="66516-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                               |
| [<span data-ttu-id="66516-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="66516-152">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="66516-152">See notes.</span></span>  | <span data-ttu-id="66516-153">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="66516-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="66516-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="66516-155">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="66516-155">See notes.</span></span>  | <span data-ttu-id="66516-156">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="66516-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="66516-157">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="66516-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>       |
| [<span data-ttu-id="66516-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="66516-159">**Barre**</span><span class="sxs-lookup"><span data-stu-id="66516-159">**ToolBar**</span></span> | <span data-ttu-id="66516-160">Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="66516-160">This value is the same for all UI frameworks.</span></span>                                                                                                                                                              |
| [<span data-ttu-id="66516-161">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-161">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="66516-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="66516-162">TRUE</span></span>        | <span data-ttu-id="66516-163">Le contrôle ToolBar est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="66516-163">The toolbar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="66516-164">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-164">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="66516-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="66516-165">TRUE</span></span>        | <span data-ttu-id="66516-166">Le contrôle ToolBar est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="66516-166">The toolbar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="66516-167">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-167">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="66516-168">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="66516-168">See notes.</span></span>  | <span data-ttu-id="66516-169">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="66516-169">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                  |
| [<span data-ttu-id="66516-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="66516-171">NULL</span><span class="sxs-lookup"><span data-stu-id="66516-171">NULL</span></span>        | <span data-ttu-id="66516-172">Un contrôle ToolBar n’a jamais d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="66516-172">A toolbar control never has a label.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="66516-173">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-173">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="66516-174">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="66516-174">See notes.</span></span>  | <span data-ttu-id="66516-175">Chaîne localisée correspondant au type de contrôle **Toolbar** .</span><span class="sxs-lookup"><span data-stu-id="66516-175">Localized string corresponding to the **ToolBar** control type.</span></span> <span data-ttu-id="66516-176">La valeur par défaut est « barre d’outils » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="66516-176">The default value is "tool bar" for en-US or English (United States).</span></span>                                                                      |
| [<span data-ttu-id="66516-177">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="66516-177">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="66516-178">Dépend</span><span class="sxs-lookup"><span data-stu-id="66516-178">Depends</span></span>     | <span data-ttu-id="66516-179">Le contrôle ToolBar n’a pas besoin d’un nom, sauf si plusieurs sont utilisés dans une application.</span><span class="sxs-lookup"><span data-stu-id="66516-179">The toolbar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="66516-180">S’il en existe plusieurs, chacun doit avoir un nom distinctif (par exemple, « mise en forme » ou « mode plan »).</span><span class="sxs-lookup"><span data-stu-id="66516-180">If more than one is present, each must have a distinguishing name (for example, "Formatting" or "Outlining").</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="66516-181">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="66516-181">Required Control Patterns</span></span>

<span data-ttu-id="66516-182">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles ToolBar.</span><span class="sxs-lookup"><span data-stu-id="66516-182">The following table lists the UI Automation control patterns required to be supported by toolbar controls.</span></span> <span data-ttu-id="66516-183">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="66516-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="66516-184">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="66516-184">Control Pattern</span></span>                                                   | <span data-ttu-id="66516-185">Support</span><span class="sxs-lookup"><span data-stu-id="66516-185">Support</span></span> | <span data-ttu-id="66516-186">Notes</span><span class="sxs-lookup"><span data-stu-id="66516-186">Notes</span></span>                                                                                                                                                         |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66516-187">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="66516-187">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="66516-188">Dépend</span><span class="sxs-lookup"><span data-stu-id="66516-188">Depends</span></span> | <span data-ttu-id="66516-189">Si la barre d’outils peut être ancrée à différentes parties de l’écran, elle doit prendre en charge le modèle de contrôle [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="66516-189">If the toolbar can be docked to different parts of the screen, it must support the [Dock](uiauto-implementingdock.md) control pattern.</span></span>                       |
| [<span data-ttu-id="66516-190">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="66516-190">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="66516-191">Dépend</span><span class="sxs-lookup"><span data-stu-id="66516-191">Depends</span></span> | <span data-ttu-id="66516-192">Si la barre d’outils peut être développée et réduite pour afficher davantage d’éléments, elle doit prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="66516-192">If the toolbar can be expanded and collapsed to show more items, it must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="66516-193">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="66516-193">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="66516-194">Dépend</span><span class="sxs-lookup"><span data-stu-id="66516-194">Depends</span></span> | <span data-ttu-id="66516-195">Si la barre d’outils peut être redimensionnée, pivotée ou déplacée, elle doit prendre en charge le modèle de contrôle [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="66516-195">If the toolbar can be resized, rotated, or moved, it must support the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>                          |



 

## <a name="required-events"></a><span data-ttu-id="66516-196">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="66516-196">Required Events</span></span>

<span data-ttu-id="66516-197">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles ToolBar.</span><span class="sxs-lookup"><span data-stu-id="66516-197">The following table lists the UI Automation events that toolbar controls are required to support.</span></span> <span data-ttu-id="66516-198">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="66516-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="66516-199">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="66516-199">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="66516-200">Notes</span><span class="sxs-lookup"><span data-stu-id="66516-200">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="66516-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="66516-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="66516-202">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="66516-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="66516-203">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="66516-203">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="66516-204">Si le contrôle prend en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="66516-204">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="66516-205">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="66516-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="66516-206">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="66516-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="66516-207">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="66516-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="66516-208">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="66516-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="66516-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="66516-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="66516-210">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="66516-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="66516-211">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="66516-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="66516-212">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="66516-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="66516-213">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="66516-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




