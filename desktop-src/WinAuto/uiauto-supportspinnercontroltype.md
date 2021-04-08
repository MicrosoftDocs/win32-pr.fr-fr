---
title: Spinner (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Spinner.
ms.assetid: 28673ad5-645d-4314-96c4-81a951226256
keywords:
- UI Automation, prise en charge du type de contrôle Spinner
- UI Automation, type de contrôle Spinner
- UI Automation, arborescence pour le type de contrôle Spinner
- UI Automation, propriétés du type de contrôle Spinner
- UI Automation, modèles de contrôle pour le type de contrôle Spinner
- UI Automation, événements pour le type de contrôle Spinner
- arborescences, type de contrôle Spinner
- Propriétés, Spinner (type de contrôle)
- modèles de contrôle, Spinner (type de contrôle)
- événements, type de contrôle Spinner
- prise en charge du type de contrôle Spinner
- Spinner (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Spinner
- types de contrôle, modèles de contrôle pour le type de contrôle Spinner
- types de contrôles, prise en charge du compteur
- types de contrôles, Spinner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9681160bf82c9a541412bb6dde8958c603fcfe22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674666"
---
# <a name="spinner-control-type"></a><span data-ttu-id="3e12b-119">Spinner (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="3e12b-119">Spinner Control Type</span></span>

<span data-ttu-id="3e12b-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="3e12b-120">This topic provides information about Microsoft UI Automation support for the **Spinner** control type.</span></span>

<span data-ttu-id="3e12b-121">Les contrôles compteur sont utilisés pour effectuer une sélection parmi un domaine d’éléments ou une plage de nombres.</span><span class="sxs-lookup"><span data-stu-id="3e12b-121">Spinner controls are used to select from a domain of items or a range of numbers.</span></span>

<span data-ttu-id="3e12b-122">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="3e12b-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Spinner** control type.</span></span> <span data-ttu-id="3e12b-123">Les exigences d’UI Automation s’appliquent à tous les contrôles Spinner où l’infrastructure ou la plateforme de l’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="3e12b-123">The UI Automation requirements apply to all spinner controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="3e12b-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3e12b-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3e12b-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="3e12b-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="3e12b-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="3e12b-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="3e12b-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="3e12b-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="3e12b-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="3e12b-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="3e12b-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e12b-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="3e12b-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="3e12b-130">Typical Tree Structure</span></span>

<span data-ttu-id="3e12b-131">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation qui se rapporte aux contrôles Spinner lorsqu’ils prennent en charge les modèles de contrôle **RangeValue** et **Selection** et décrit ce que peut contenir chaque vue.</span><span class="sxs-lookup"><span data-stu-id="3e12b-131">The following table depicts a typical control and content view of the UI Automation tree that pertain to spinner controls when they support the **RangeValue** and **Selection** control patterns and describes what can be contained in each view.</span></span> <span data-ttu-id="3e12b-132">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3e12b-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>

<span data-ttu-id="3e12b-133">**Modèle de contrôle RangeValue**</span><span class="sxs-lookup"><span data-stu-id="3e12b-133">**RangeValue control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e12b-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="3e12b-134">Control View</span></span></th>
<th><span data-ttu-id="3e12b-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="3e12b-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3e12b-136">Spinner</span><span class="sxs-lookup"><span data-stu-id="3e12b-136">Spinner</span></span>
<ul>
<li><span data-ttu-id="3e12b-137">Edit (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="3e12b-137">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="3e12b-138">Button (2)</span><span class="sxs-lookup"><span data-stu-id="3e12b-138">Button (2)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3e12b-139">Spinner</span><span class="sxs-lookup"><span data-stu-id="3e12b-139">Spinner</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3e12b-140">**Selection (modèle de contrôle)**</span><span class="sxs-lookup"><span data-stu-id="3e12b-140">**Selection control pattern**</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e12b-141">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="3e12b-141">Control View</span></span></th>
<th><span data-ttu-id="3e12b-142">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="3e12b-142">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3e12b-143">Spinner</span><span class="sxs-lookup"><span data-stu-id="3e12b-143">Spinner</span></span>
<ul>
<li><span data-ttu-id="3e12b-144">Edit (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="3e12b-144">Edit (0 or 1)</span></span></li>
<li><span data-ttu-id="3e12b-145">Button (2)</span><span class="sxs-lookup"><span data-stu-id="3e12b-145">Button (2)</span></span></li>
<li><span data-ttu-id="3e12b-146">Élément de liste (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="3e12b-146">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3e12b-147">Spinner</span><span class="sxs-lookup"><span data-stu-id="3e12b-147">Spinner</span></span>
<ul>
<li><span data-ttu-id="3e12b-148">ListItem (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="3e12b-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3e12b-149">Pour vous assurer que les deux boutons de la sous-arborescence de la vue de contrôle peuvent être distingués par des outils de test automatisés, affectez la valeur **ScrollAmount \_ SmallIncrement** ou [**ScrollAmount \_ SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) à la propriété **AutomationId** , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3e12b-149">To ensure that the two buttons in the control view subtree can be distinguished by automated test tools, assign the **ScrollAmount\_SmallIncrement** or [**ScrollAmount\_SmallDecrement**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-scrollamount) value to the **AutomationId** property as appropriate.</span></span> <span data-ttu-id="3e12b-150">Pour certaines implémentations, le contrôle d’édition associé peut être un homologue du contrôle Spinner.</span><span class="sxs-lookup"><span data-stu-id="3e12b-150">For some implementations, the associated edit control may be a peer of the spinner control.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="3e12b-151">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="3e12b-151">Relevant Properties</span></span>

<span data-ttu-id="3e12b-152">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Spinner.</span><span class="sxs-lookup"><span data-stu-id="3e12b-152">The following table lists the UI Automation properties whose value or definition is especially relevant to spinner controls.</span></span> <span data-ttu-id="3e12b-153">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="3e12b-153">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="3e12b-154">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="3e12b-154">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="3e12b-155">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e12b-155">Value</span></span>       | <span data-ttu-id="3e12b-156">Notes</span><span class="sxs-lookup"><span data-stu-id="3e12b-156">Notes</span></span>                                                                                                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e12b-157">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-157">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="3e12b-158">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3e12b-158">See notes.</span></span>  | <span data-ttu-id="3e12b-159">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3e12b-159">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                               |
| [<span data-ttu-id="3e12b-160">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-160">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="3e12b-161">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3e12b-161">See notes.</span></span>  | <span data-ttu-id="3e12b-162">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3e12b-162">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="3e12b-163">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-163">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="3e12b-164">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3e12b-164">See notes.</span></span>  | <span data-ttu-id="3e12b-165">Le point interactif du contrôle compteur donne le focus à la partie d’édition du contrôle.</span><span class="sxs-lookup"><span data-stu-id="3e12b-165">The spinner control's clickable point gives focus to the edit portion of the control.</span></span>                                                                                                                                                                                                                                      |
| [<span data-ttu-id="3e12b-166">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-166">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="3e12b-167">**Spinner**</span><span class="sxs-lookup"><span data-stu-id="3e12b-167">**Spinner**</span></span> | <span data-ttu-id="3e12b-168">Cette valeur est la même pour toutes les infrastructures.</span><span class="sxs-lookup"><span data-stu-id="3e12b-168">This value is the same for all frameworks.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="3e12b-169">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-169">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3e12b-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="3e12b-170">TRUE</span></span>        | <span data-ttu-id="3e12b-171">Le contrôle compteur doit toujours être du contenu.</span><span class="sxs-lookup"><span data-stu-id="3e12b-171">The spinner control must always be content.</span></span>                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="3e12b-172">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-172">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3e12b-173">TRUE</span><span class="sxs-lookup"><span data-stu-id="3e12b-173">TRUE</span></span>        | <span data-ttu-id="3e12b-174">Le contrôle Spinner doit toujours être un contrôle.</span><span class="sxs-lookup"><span data-stu-id="3e12b-174">The spinner control must always be a control.</span></span>                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="3e12b-175">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-175">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="3e12b-176">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3e12b-176">See notes.</span></span>  | <span data-ttu-id="3e12b-177">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="3e12b-177">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="3e12b-178">Un contrôle Spinner prend rarement le focus, mais dans ce cas, le focus doit rester sur le contrôle Spinner lui-même, et non sur les boutons enfants.</span><span class="sxs-lookup"><span data-stu-id="3e12b-178">A spinner control rarely takes the focus, but when it does, the focus should remain on the spinner control itself, not on the child buttons.</span></span> <span data-ttu-id="3e12b-179">L’utilisateur doit être en mesure d’effectuer toutes les actions de défilement à l’aide des flèches haut et bas.</span><span class="sxs-lookup"><span data-stu-id="3e12b-179">The user should be able to perform all scrolling actions by using the UP ARROW and DOWN ARROW keys.</span></span> |
| [<span data-ttu-id="3e12b-180">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-180">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="3e12b-181">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3e12b-181">See notes.</span></span>  | <span data-ttu-id="3e12b-182">Les contrôles compteur ont une étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="3e12b-182">Spinner controls have a static text label.</span></span>                                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="3e12b-183">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-183">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="3e12b-184">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3e12b-184">See notes.</span></span>  | <span data-ttu-id="3e12b-185">Chaîne localisée correspondant au type de contrôle **Spinner** .</span><span class="sxs-lookup"><span data-stu-id="3e12b-185">Localized string corresponding to the **Spinner** control type.</span></span> <span data-ttu-id="3e12b-186">La valeur par défaut est « Spinner » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="3e12b-186">The default value is "spinner" for en-US or English (United States).</span></span>                                                                                                                                                                                       |
| [<span data-ttu-id="3e12b-187">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-187">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="3e12b-188">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3e12b-188">See notes.</span></span>  | <span data-ttu-id="3e12b-189">Le contrôle compteur tire généralement son nom d’une étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="3e12b-189">The spinner control typically gets its name from a static text label.</span></span>                                                                                                                                                                                                                                                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="3e12b-190">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="3e12b-190">Required Control Patterns</span></span>

<span data-ttu-id="3e12b-191">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles Spinner.</span><span class="sxs-lookup"><span data-stu-id="3e12b-191">The following table lists the UI Automation control patterns required to be supported by all spinner controls.</span></span> <span data-ttu-id="3e12b-192">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3e12b-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="3e12b-193">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="3e12b-193">Control Pattern/Pattern Property</span></span>                                         | <span data-ttu-id="3e12b-194">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="3e12b-194">Support/Value</span></span> | <span data-ttu-id="3e12b-195">Notes</span><span class="sxs-lookup"><span data-stu-id="3e12b-195">Notes</span></span>                                                                                                                                     |
|--------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e12b-196">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="3e12b-196">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider)                | <span data-ttu-id="3e12b-197">Dépend</span><span class="sxs-lookup"><span data-stu-id="3e12b-197">Depends</span></span>       | <span data-ttu-id="3e12b-198">Les contrôles Spinner qui couvrent une plage numérique peuvent prendre en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) .</span><span class="sxs-lookup"><span data-stu-id="3e12b-198">Spinner controls that span a numeric range can support the [RangeValue](uiauto-implementingrangevalue.md) control pattern.</span></span>               |
| [<span data-ttu-id="3e12b-199">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="3e12b-199">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                  | <span data-ttu-id="3e12b-200">Dépend</span><span class="sxs-lookup"><span data-stu-id="3e12b-200">Depends</span></span>       | <span data-ttu-id="3e12b-201">Les contrôles Spinner qui ont une liste d’éléments à sélectionner doivent prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="3e12b-201">Spinner controls that have a list of items to be selected must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span> |
| [<span data-ttu-id="3e12b-202">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="3e12b-202">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) | <span data-ttu-id="3e12b-203">FALSE</span><span class="sxs-lookup"><span data-stu-id="3e12b-203">FALSE</span></span>         | <span data-ttu-id="3e12b-204">Les contrôles compteur sont toujours des conteneurs à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="3e12b-204">Spinner controls are always single selection containers.</span></span>                                                                                  |
| [<span data-ttu-id="3e12b-205">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="3e12b-205">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                          | <span data-ttu-id="3e12b-206">Dépend</span><span class="sxs-lookup"><span data-stu-id="3e12b-206">Depends</span></span>       | <span data-ttu-id="3e12b-207">Les contrôles Spinner qui couvrent un ensemble descrete d’options ou de nombres peuvent prendre en charge le modèle de contrôle [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="3e12b-207">Spinner controls that span a descrete set of options or numbers can support the [Value](uiauto-implementingvalue.md) control pattern.</span></span>    |



 

## <a name="required-events"></a><span data-ttu-id="3e12b-208">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="3e12b-208">Required Events</span></span>

<span data-ttu-id="3e12b-209">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles Spinner.</span><span class="sxs-lookup"><span data-stu-id="3e12b-209">The following table lists the UI Automation events that spinner controls are required to support.</span></span> <span data-ttu-id="3e12b-210">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3e12b-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="3e12b-211">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="3e12b-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="3e12b-212">Notes</span><span class="sxs-lookup"><span data-stu-id="3e12b-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3e12b-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="3e12b-214">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="3e12b-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="3e12b-215">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="3e12b-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="3e12b-216">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="3e12b-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="3e12b-217">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="3e12b-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="3e12b-218">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="3e12b-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="3e12b-219">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="3e12b-219">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="3e12b-220">Si le contrôle prend en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="3e12b-220">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| <span data-ttu-id="3e12b-221">[**UIA \_ Sélection \_**](uiauto-event-ids.md) de l’événement de modification de propriété InvalidatedEventId.</span><span class="sxs-lookup"><span data-stu-id="3e12b-221">[**UIA\_Selection\_InvalidatedEventId**](uiauto-event-ids.md) property-changed event.</span></span>               | <span data-ttu-id="3e12b-222">Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="3e12b-222">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="3e12b-223">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="3e12b-223">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="3e12b-224">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="3e12b-224">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="3e12b-225">Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="3e12b-225">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="3e12b-226">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e12b-226">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3e12b-227">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3e12b-227">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3e12b-228">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="3e12b-228">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="3e12b-229">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="3e12b-229">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




