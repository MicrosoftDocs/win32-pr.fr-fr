---
title: Tab (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Tab.
ms.assetid: 49e3f025-f49b-44b1-90ca-09f40dce8f2a
keywords:
- UI Automation, prise en charge du type de contrôle Tab
- UI Automation, type de contrôle Tab
- UI Automation, arborescence pour le type de contrôle Tab
- UI Automation, propriétés pour le type de contrôle Tab
- UI Automation, modèles de contrôle pour le type de contrôle Tab
- UI Automation, événements pour le type de contrôle Tab
- arborescences, type de contrôle Tab
- Propriétés, onglet (type de contrôle)
- modèles de contrôle, onglet (type de contrôle)
- événements, type de contrôle Tab
- prise en charge du type de contrôle Tab
- Tab (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Tab
- types de contrôles, modèles de contrôle pour le type de contrôle Tab
- types de contrôles, prise en charge de Tab
- types de contrôles, onglet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 769a03617830c33fce4a8f64c594010b2120785b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940092"
---
# <a name="tab-control-type"></a><span data-ttu-id="bc102-119">Tab (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="bc102-119">Tab Control Type</span></span>

<span data-ttu-id="bc102-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Tab** .</span><span class="sxs-lookup"><span data-stu-id="bc102-120">This topic provides information about Microsoft UI Automation support for the **Tab** control type.</span></span>

<span data-ttu-id="bc102-121">Un contrôle tab équivaut aux intercalaires dans un classeur ou aux étiquettes dans une armoire de classement.</span><span class="sxs-lookup"><span data-stu-id="bc102-121">A tab control is analogous to the dividers in a notebook or the labels in a file cabinet.</span></span> <span data-ttu-id="bc102-122">En utilisant un contrôle tab, une application peut définir plusieurs pages pour la même zone d’une fenêtre ou d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="bc102-122">By using a tab control, an application can define multiple pages for the same area of a window or dialog box.</span></span>

<span data-ttu-id="bc102-123">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Tab** .</span><span class="sxs-lookup"><span data-stu-id="bc102-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Tab** control type.</span></span> <span data-ttu-id="bc102-124">Les exigences d’UI Automation s’appliquent à tous les contrôles Tab où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="bc102-124">The UI Automation requirements apply to all tab controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="bc102-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="bc102-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="bc102-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="bc102-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="bc102-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="bc102-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="bc102-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="bc102-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="bc102-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="bc102-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="bc102-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc102-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="bc102-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="bc102-131">Typical Tree Structure</span></span>

<span data-ttu-id="bc102-132">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation qui se rapporte aux contrôles d’onglet et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="bc102-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to tab controls and describes what can be contained in each view.</span></span> <span data-ttu-id="bc102-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bc102-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc102-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc102-134">Control View</span></span></th>
<th><span data-ttu-id="bc102-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="bc102-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="bc102-136">Onglet</span><span class="sxs-lookup"><span data-stu-id="bc102-136">Tab</span></span>
<ul>
<li><span data-ttu-id="bc102-137">TabItem (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-137">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="bc102-138">ScrollBar (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="bc102-138">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="bc102-139">Button (0 ou 2)</span><span class="sxs-lookup"><span data-stu-id="bc102-139">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="bc102-140">Onglet</span><span class="sxs-lookup"><span data-stu-id="bc102-140">Tab</span></span>
<ul>
<li><span data-ttu-id="bc102-141">TabItem (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-141">TabItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="bc102-142">Les contrôles onglet possèdent des éléments UI Automation enfants basés sur le type de contrôle [TabItem](uiauto-supporttabitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="bc102-142">Tab controls have child UI Automation elements based on the [TabItem](uiauto-supporttabitemcontroltype.md) control type.</span></span> <span data-ttu-id="bc102-143">Lorsque les éléments d’onglet sont groupés (par exemple, comme dans Microsoft Office Applications), le type de contrôle **Tab** peut également héberger des types de contrôle de **groupes** pour les éléments d’onglet groupés, comme le montre l’arborescence suivante.</span><span class="sxs-lookup"><span data-stu-id="bc102-143">When tab items are grouped (for example, as in Microsoft Office applications) the **Tab** control type can also host **Groups** control types for the grouped tab items, as the following tree structure shows.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bc102-144">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="bc102-144">Control View</span></span></th>
<th><span data-ttu-id="bc102-145">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="bc102-145">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="bc102-146">Onglet</span><span class="sxs-lookup"><span data-stu-id="bc102-146">Tab</span></span>
<ul>
<li><span data-ttu-id="bc102-147">TabItem (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-147">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="bc102-148">Group (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-148">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="bc102-149">TabItem (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-149">TabItem (0 or more)</span></span></li>
</ul></li>
<li><span data-ttu-id="bc102-150">ScrollBar (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="bc102-150">ScrollBar (0 or 1)</span></span>
<ul>
<li><span data-ttu-id="bc102-151">Button (0 ou 2)</span><span class="sxs-lookup"><span data-stu-id="bc102-151">Button (0 or 2)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="bc102-152">Onglet</span><span class="sxs-lookup"><span data-stu-id="bc102-152">Tab</span></span>
<ul>
<li><span data-ttu-id="bc102-153">TabItem (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-153">TabItem (1 or more)</span></span></li>
<li><span data-ttu-id="bc102-154">Group (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-154">Group (0 or more)</span></span>
<ul>
<li><span data-ttu-id="bc102-155">TabItem (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="bc102-155">TabItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="bc102-156">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="bc102-156">Relevant Properties</span></span>

<span data-ttu-id="bc102-157">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles d’onglet.</span><span class="sxs-lookup"><span data-stu-id="bc102-157">The following table lists the UI Automation properties whose value or definition is especially relevant to tab controls.</span></span> <span data-ttu-id="bc102-158">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="bc102-158">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="bc102-159">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="bc102-159">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="bc102-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="bc102-160">Value</span></span>      | <span data-ttu-id="bc102-161">Notes</span><span class="sxs-lookup"><span data-stu-id="bc102-161">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc102-162">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-162">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="bc102-163">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="bc102-163">See notes.</span></span> | <span data-ttu-id="bc102-164">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="bc102-164">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="bc102-165">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-165">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="bc102-166">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="bc102-166">See notes.</span></span> | <span data-ttu-id="bc102-167">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="bc102-167">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="bc102-168">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-168">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="bc102-169">Non</span><span class="sxs-lookup"><span data-stu-id="bc102-169">No</span></span>         | <span data-ttu-id="bc102-170">Le contrôle onglet n’a pas de points intercliquables.</span><span class="sxs-lookup"><span data-stu-id="bc102-170">The tab control does not have clickable points.</span></span>                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="bc102-171">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-171">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="bc102-172">**Tab**</span><span class="sxs-lookup"><span data-stu-id="bc102-172">**Tab**</span></span>    |                                                                                                                                                                                                                                                                                                                                                                               |
| [<span data-ttu-id="bc102-173">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-173">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="bc102-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="bc102-174">TRUE</span></span>       | <span data-ttu-id="bc102-175">Le contrôle onglet est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="bc102-175">The tab control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bc102-176">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-176">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="bc102-177">TRUE</span><span class="sxs-lookup"><span data-stu-id="bc102-177">TRUE</span></span>       | <span data-ttu-id="bc102-178">Le contrôle onglet est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="bc102-178">The tab control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="bc102-179">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-179">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="bc102-180">TRUE</span><span class="sxs-lookup"><span data-stu-id="bc102-180">TRUE</span></span>       | <span data-ttu-id="bc102-181">Le type de contrôle Tab doit être en mesure de recevoir le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="bc102-181">The Tab control type must be able to receive keyboard focus.</span></span> <span data-ttu-id="bc102-182">En règle générale, un client UI Automation appelle [**IUIAutomationElement :: SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) sur un contrôle Tab et l’un de ses éléments transmet le focus clavier au contrôle Tab.</span><span class="sxs-lookup"><span data-stu-id="bc102-182">Typically, a UI Automation client calls [**IUIAutomationElement::SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on a tab control and one of its items will forward the keyboard focus to the tab control.</span></span> <span data-ttu-id="bc102-183">Il est possible que certains conteneurs d’onglet prennent le focus sans lui affecter l’un de ses éléments.</span><span class="sxs-lookup"><span data-stu-id="bc102-183">It is possible for some tab containers to take focus without setting focus to one of its items.</span></span> |
| [<span data-ttu-id="bc102-184">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-184">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="bc102-185">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="bc102-185">See notes.</span></span> | <span data-ttu-id="bc102-186">Les contrôles tab ont en général une étiquette de texte statique qui est exposée via cette propriété.</span><span class="sxs-lookup"><span data-stu-id="bc102-186">Tab controls typically have a static text label that is exposed through this property.</span></span>                                                                                                                                                                                                                                                                                        |
| [<span data-ttu-id="bc102-187">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-187">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="bc102-188">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="bc102-188">See notes.</span></span> | <span data-ttu-id="bc102-189">Chaîne localisée correspondant au type de contrôle **Tab** .</span><span class="sxs-lookup"><span data-stu-id="bc102-189">Localized string corresponding to the **Tab** control type.</span></span> <span data-ttu-id="bc102-190">La valeur par défaut est « Tab » pour « fr-fr » ou « anglais » (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="bc102-190">The default value is "tab" for en-US or English (United States).</span></span>                                                                                                                                                                                                                                                  |
| [<span data-ttu-id="bc102-191">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-191">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="bc102-192">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="bc102-192">See notes.</span></span> | <span data-ttu-id="bc102-193">Le contrôle Tab requiert rarement une propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="bc102-193">The tab control rarely requires a **Name** property.</span></span>                                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="bc102-194">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="bc102-194">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="bc102-195">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="bc102-195">See notes.</span></span> | <span data-ttu-id="bc102-196">Le contrôle tab doit toujours indiquer s’il est positionné horizontalement ou verticalement.</span><span class="sxs-lookup"><span data-stu-id="bc102-196">The tab control must always indicate whether it is positioned horizontally or vertically.</span></span>                                                                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="bc102-197">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="bc102-197">Required Control Patterns</span></span>

<span data-ttu-id="bc102-198">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles Tab.</span><span class="sxs-lookup"><span data-stu-id="bc102-198">The following table lists the UI Automation control patterns required to be supported by all tab controls.</span></span> <span data-ttu-id="bc102-199">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bc102-199">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="bc102-200">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="bc102-200">Control Pattern/Pattern Property</span></span>                                             | <span data-ttu-id="bc102-201">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="bc102-201">Support/Value</span></span> | <span data-ttu-id="bc102-202">Notes</span><span class="sxs-lookup"><span data-stu-id="bc102-202">Notes</span></span>                                                                                                                                                                  |
|------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc102-203">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="bc102-203">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)                      | <span data-ttu-id="bc102-204">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="bc102-204">Required</span></span>      | <span data-ttu-id="bc102-205">Tous les contrôles Tab doivent prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) .</span><span class="sxs-lookup"><span data-stu-id="bc102-205">All tab controls must support the [Selection](uiauto-implementingselection.md) control pattern.</span></span>                                                                       |
| [<span data-ttu-id="bc102-206">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="bc102-206">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) | <span data-ttu-id="bc102-207">TRUE</span><span class="sxs-lookup"><span data-stu-id="bc102-207">TRUE</span></span>          | <span data-ttu-id="bc102-208">Les contrôles tab requièrent toujours qu’une sélection soit effectuée.</span><span class="sxs-lookup"><span data-stu-id="bc102-208">Tab controls always require that a selection be made.</span></span>                                                                                                                  |
| [<span data-ttu-id="bc102-209">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="bc102-209">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)     | <span data-ttu-id="bc102-210">FALSE</span><span class="sxs-lookup"><span data-stu-id="bc102-210">FALSE</span></span>         | <span data-ttu-id="bc102-211">Les contrôles tab sont toujours des conteneurs à sélection unique.</span><span class="sxs-lookup"><span data-stu-id="bc102-211">Tab controls are always single-selection containers.</span></span>                                                                                                                   |
| [<span data-ttu-id="bc102-212">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="bc102-212">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)                            | <span data-ttu-id="bc102-213">Dépend</span><span class="sxs-lookup"><span data-stu-id="bc102-213">Depends</span></span>       | <span data-ttu-id="bc102-214">Le modèle de contrôle [Scroll](uiauto-implementingscroll.md) doit être pris en charge si le contrôle onglet possède des widgets qui permettent de faire défiler un ensemble d’éléments d’onglet.</span><span class="sxs-lookup"><span data-stu-id="bc102-214">The [Scroll](uiauto-implementingscroll.md) control pattern must be supported if the tab control has widgets that allow for a set of tab items to be scrolled through.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="bc102-215">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="bc102-215">Required Events</span></span>

<span data-ttu-id="bc102-216">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles onglet.</span><span class="sxs-lookup"><span data-stu-id="bc102-216">The following table lists the UI Automation events that tab controls are required to support.</span></span> <span data-ttu-id="bc102-217">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="bc102-217">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="bc102-218">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="bc102-218">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="bc102-219">Notes</span><span class="sxs-lookup"><span data-stu-id="bc102-219">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc102-220">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="bc102-220">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="bc102-221">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-221">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="bc102-222">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-222">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="bc102-223">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-223">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="bc102-224">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-224">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="bc102-225">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-225">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="bc102-226">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-226">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="bc102-227">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="bc102-228">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-228">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="bc102-229">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-229">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="bc102-230">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-230">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="bc102-231">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-231">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="bc102-232">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-232">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="bc102-233">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-233">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="bc102-234">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-234">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="bc102-235">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-235">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="bc102-236">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="bc102-236">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="bc102-237">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="bc102-237">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="bc102-238">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="bc102-238">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="bc102-239">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="bc102-239">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="bc102-240">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="bc102-240">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="bc102-241">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="bc102-241">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="bc102-242">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="bc102-242">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




