---
title: TabItem (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle TabItem.
ms.assetid: 97b8c043-1ac5-4e14-be80-8687300a10a2
keywords:
- UI Automation, prise en charge du type de contrôle TabItem
- UI Automation, type de contrôle TabItem
- UI Automation, arborescence pour le type de contrôle TabItem
- UI Automation, propriétés du type de contrôle TabItem
- UI Automation, modèles de contrôle pour le type de contrôle TabItem
- UI Automation, événements pour le type de contrôle TabItem
- arborescences, type de contrôle TabItem
- Propriétés, type de contrôle TabItem
- modèles de contrôle, type de contrôle TabItem
- événements, type de contrôle TabItem
- prise en charge du type de contrôle TabItem
- TabItem (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle TabItem
- types de contrôle, modèles de contrôle pour le type de contrôle TabItem
- types de contrôles, prise en charge de TabItem
- types de contrôle, TabItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e8f9f900240318de8629048f242cd755994c78
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197207"
---
# <a name="tabitem-control-type"></a><span data-ttu-id="a8fc3-119">TabItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="a8fc3-119">TabItem Control Type</span></span>

<span data-ttu-id="a8fc3-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="a8fc3-120">This topic provides information about Microsoft UI Automation support for the **TabItem** control type.</span></span>

<span data-ttu-id="a8fc3-121">Un contrôle d’élément d’onglet est le contrôle dans un contrôle d’onglet qui permet de sélectionner une page spécifique à afficher dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-121">A tab item control is used as the control within a tab control that selects a specific page to be shown in a window.</span></span>

<span data-ttu-id="a8fc3-122">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="a8fc3-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TabItem** control type.</span></span> <span data-ttu-id="a8fc3-123">Les spécifications d’UI Automation s’appliquent à tous les contrôles d’élément d’onglet où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-123">The UI Automation requirements apply to all tab item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="a8fc3-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="a8fc3-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="a8fc3-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="a8fc3-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="a8fc3-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="a8fc3-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="a8fc3-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="a8fc3-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="a8fc3-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="a8fc3-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8fc3-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="a8fc3-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="a8fc3-130">Typical Tree Structure</span></span>

<span data-ttu-id="a8fc3-131">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles d’élément d’onglet et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="a8fc3-132">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a8fc3-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8fc3-133">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="a8fc3-133">Control View</span></span></th>
<th><span data-ttu-id="a8fc3-134">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="a8fc3-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="a8fc3-135">TabItem</span><span class="sxs-lookup"><span data-stu-id="a8fc3-135">TabItem</span></span>
<ul>
<li><span data-ttu-id="a8fc3-136">Image (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="a8fc3-136">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="a8fc3-137">Texte</span><span class="sxs-lookup"><span data-stu-id="a8fc3-137">Text</span></span></li>
<li><span data-ttu-id="a8fc3-138">Volet</span><span class="sxs-lookup"><span data-stu-id="a8fc3-138">Pane</span></span>
<ul>
<li><span data-ttu-id="a8fc3-139">Plusieurs contrôles (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="a8fc3-139">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="a8fc3-140">TabItem</span><span class="sxs-lookup"><span data-stu-id="a8fc3-140">TabItem</span></span>
<ul>
<li><span data-ttu-id="a8fc3-141">Volet</span><span class="sxs-lookup"><span data-stu-id="a8fc3-141">Pane</span></span>
<ul>
<li><span data-ttu-id="a8fc3-142">Plusieurs contrôles (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="a8fc3-142">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="a8fc3-143">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="a8fc3-143">Relevant Properties</span></span>

<span data-ttu-id="a8fc3-144">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="a8fc3-144">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TabItem** control type.</span></span> <span data-ttu-id="a8fc3-145">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="a8fc3-145">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="a8fc3-146">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="a8fc3-146">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="a8fc3-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8fc3-147">Value</span></span>       | <span data-ttu-id="a8fc3-148">Notes</span><span class="sxs-lookup"><span data-stu-id="a8fc3-148">Notes</span></span>                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|-------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8fc3-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="a8fc3-150">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-150">See notes.</span></span>  | <span data-ttu-id="a8fc3-151">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                |
| [<span data-ttu-id="a8fc3-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="a8fc3-153">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-153">See notes.</span></span>  | <span data-ttu-id="a8fc3-154">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-154">The outermost rectangle that contains the whole control.</span></span>                                                                                    |
| [<span data-ttu-id="a8fc3-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="a8fc3-156">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-156">See notes.</span></span>  | <span data-ttu-id="a8fc3-157">Le contrôle d’élément d’onglet doit avoir une zone interactive qui entraîne la sélection de l’élément.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-157">The tab item control must have a clickable point that causes the item to become selected.</span></span>                                                   |
| [<span data-ttu-id="a8fc3-158">**UIA \_ ControllerForPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-158">**UIA\_ControllerForPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="a8fc3-159">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-159">See notes.</span></span>  | <span data-ttu-id="a8fc3-160">Cette propriété peut être utilisée comme pointeur vers le volet d’onglets associé.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-160">This property can be used as pointer to the associated tab pane.</span></span> <span data-ttu-id="a8fc3-161">Cela est utile quand il ne peut pas héberger un volet enfant de l’objet élément d’onglet.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-161">This is useful when it cannot host a pane as child of the tab item object.</span></span> |
| [<span data-ttu-id="a8fc3-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="a8fc3-163">**TabItem**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-163">**TabItem**</span></span> | <span data-ttu-id="a8fc3-164">Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-164">This value is the same for all UI frameworks.</span></span>                                                                                               |
| [<span data-ttu-id="a8fc3-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a8fc3-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="a8fc3-166">TRUE</span></span>        | <span data-ttu-id="a8fc3-167">Le contrôle d’élément d’onglet est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-167">The tab item control is always included in the content view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="a8fc3-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="a8fc3-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="a8fc3-169">TRUE</span></span>        | <span data-ttu-id="a8fc3-170">Le contrôle d’élément d’onglet est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-170">The tab item control is always included in the control view of the UI Automation tree.</span></span>                                                      |
| [<span data-ttu-id="a8fc3-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="a8fc3-172">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-172">See notes.</span></span>  | <span data-ttu-id="a8fc3-173">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                   |
| [<span data-ttu-id="a8fc3-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="a8fc3-175">Null</span><span class="sxs-lookup"><span data-stu-id="a8fc3-175">Null</span></span>        | <span data-ttu-id="a8fc3-176">Le contrôle d’élément d’onglet n’a pas d’étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-176">The tab item control does not have a static text label.</span></span>                                                                                     |
| [<span data-ttu-id="a8fc3-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="a8fc3-178">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-178">See notes.</span></span>  | <span data-ttu-id="a8fc3-179">Chaîne localisée correspondant au type de contrôle **TabItem** .</span><span class="sxs-lookup"><span data-stu-id="a8fc3-179">Localized string corresponding to the **TabItem** control type.</span></span> <span data-ttu-id="a8fc3-180">La valeur par défaut est « élément d’onglet » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="a8fc3-180">The default value is "tab item" for en-US or English (United States).</span></span>       |
| [<span data-ttu-id="a8fc3-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="a8fc3-182">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-182">See notes.</span></span>  | <span data-ttu-id="a8fc3-183">Le contrôle d’élément d’onglet est étiqueté automatiquement.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-183">The tab item control self-labeled.</span></span>                                                                                                          |



 

## <a name="required-control-patterns"></a><span data-ttu-id="a8fc3-184">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="a8fc3-184">Required Control Patterns</span></span>

<span data-ttu-id="a8fc3-185">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles d’élément d’onglet.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-185">The following table lists the UI Automation control patterns required to be supported by all tab item controls.</span></span> <span data-ttu-id="a8fc3-186">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a8fc3-186">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="a8fc3-187">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="a8fc3-187">Control Pattern</span></span>                                                 | <span data-ttu-id="a8fc3-188">Support</span><span class="sxs-lookup"><span data-stu-id="a8fc3-188">Support</span></span>  | <span data-ttu-id="a8fc3-189">Notes</span><span class="sxs-lookup"><span data-stu-id="a8fc3-189">Notes</span></span>                                                                                                                    |
|-----------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8fc3-190">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-190">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) | <span data-ttu-id="a8fc3-191">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="a8fc3-191">Required</span></span> | <span data-ttu-id="a8fc3-192">Le contrôle d’élément d’onglet doit prendre en charge [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span><span class="sxs-lookup"><span data-stu-id="a8fc3-192">The tab item control must support [**IUIAutomationSelectionItemPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationselectionitempattern).</span></span> |
| [<span data-ttu-id="a8fc3-193">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-193">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)               | <span data-ttu-id="a8fc3-194">Jamais</span><span class="sxs-lookup"><span data-stu-id="a8fc3-194">Never</span></span>    | <span data-ttu-id="a8fc3-195">Le contrôle d’élément d’onglet ne prend jamais en charge [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span><span class="sxs-lookup"><span data-stu-id="a8fc3-195">The tab item control never supports [**IUIAutomationInvokePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationinvokepattern).</span></span>             |



 

## <a name="required-events"></a><span data-ttu-id="a8fc3-196">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="a8fc3-196">Required Events</span></span>

<span data-ttu-id="a8fc3-197">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’élément d’onglet.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-197">The following table lists the UI Automation events that tab item controls are required to support.</span></span> <span data-ttu-id="a8fc3-198">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="a8fc3-198">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="a8fc3-199">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="a8fc3-199">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="a8fc3-200">Notes</span><span class="sxs-lookup"><span data-stu-id="a8fc3-200">Notes</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a8fc3-201">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-201">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                            |
| <span data-ttu-id="a8fc3-202">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-202">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                            |
| <span data-ttu-id="a8fc3-203">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-203">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="a8fc3-204">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-204">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="a8fc3-205">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-205">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="a8fc3-206">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="a8fc3-206">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="a8fc3-207">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-207">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) |                                                                                                                            |
| [<span data-ttu-id="a8fc3-208">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-208">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         |                                                                                                                            |
| [<span data-ttu-id="a8fc3-209">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-209">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="a8fc3-210">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a8fc3-210">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a8fc3-211">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="a8fc3-211">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a8fc3-212">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="a8fc3-212">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="a8fc3-213">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="a8fc3-213">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




