---
title: SplitButton (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle SplitButton.
ms.assetid: ca4f8e45-7487-4a8b-9df5-edc2b0e56663
keywords:
- UI Automation, prise en charge du type de contrôle SplitButton
- UI Automation, type de contrôle SplitButton
- UI Automation, arborescence pour le type de contrôle SplitButton
- UI Automation, propriétés du type de contrôle SplitButton
- UI Automation, modèles de contrôle pour le type de contrôle SplitButton
- UI Automation, événements pour le type de contrôle SplitButton
- arborescences, type de contrôle SplitButton
- Propriétés, type de contrôle SplitButton
- modèles de contrôle, type de contrôle SplitButton
- événements, type de contrôle SplitButton
- prise en charge du type de contrôle SplitButton
- SplitButton (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle SplitButton
- types de contrôles, modèles de contrôle pour le type de contrôle SplitButton
- types de contrôles, prise en charge du SplitButton
- types de contrôles, SplitButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c56cd6b22838dfa92ba25ce05e74d228f4173ac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674665"
---
# <a name="splitbutton-control-type"></a><span data-ttu-id="53a7a-119">SplitButton (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="53a7a-119">SplitButton Control Type</span></span>

<span data-ttu-id="53a7a-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="53a7a-120">This topic provides information about Microsoft UI Automation support for the **SplitButton** control type.</span></span>

<span data-ttu-id="53a7a-121">Le contrôle bouton partagé permet d’effectuer une action sur un contrôle et de développer le contrôle pour afficher la liste des autres actions possibles qui peuvent être effectuées.</span><span class="sxs-lookup"><span data-stu-id="53a7a-121">The split button control enables an action to be performed on a control, and to expand the control to see a list of other possible actions that can be performed.</span></span>

<span data-ttu-id="53a7a-122">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="53a7a-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SplitButton** control type.</span></span> <span data-ttu-id="53a7a-123">Les exigences d’UI Automation s’appliquent à tous les contrôles bouton partagé où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="53a7a-123">The UI Automation requirements apply to all split button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="53a7a-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="53a7a-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="53a7a-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="53a7a-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="53a7a-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="53a7a-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="53a7a-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="53a7a-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="53a7a-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="53a7a-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="53a7a-129">Exemple de type de contrôle SplitButton</span><span class="sxs-lookup"><span data-stu-id="53a7a-129">SplitButton Control Type Example</span></span>](#splitbutton-control-type-example)
-   [<span data-ttu-id="53a7a-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53a7a-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="53a7a-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="53a7a-131">Typical Tree Structure</span></span>

<span data-ttu-id="53a7a-132">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles bouton partagé et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="53a7a-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to split button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="53a7a-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="53a7a-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53a7a-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="53a7a-134">Control View</span></span></th>
<th><span data-ttu-id="53a7a-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="53a7a-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="53a7a-136">SplitButton</span><span class="sxs-lookup"><span data-stu-id="53a7a-136">SplitButton</span></span>
<ul>
<li><span data-ttu-id="53a7a-137">Image (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="53a7a-137">Image (0 or 1)</span></span></li>
<li><span data-ttu-id="53a7a-138">Text (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="53a7a-138">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="53a7a-139">Button (1 ou 2)</span><span class="sxs-lookup"><span data-stu-id="53a7a-139">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="53a7a-140">Menu (0 ou 1 ; apparaît en tant qu’enfant d’un sous-bouton qui prend en charge le modèle ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="53a7a-140">Menu (0 or 1; appears as a child of a sub-button that supports the ExpandCollapse pattern)</span></span>
<ul>
<li><span data-ttu-id="53a7a-141">MenuItem (1 et plus)</span><span class="sxs-lookup"><span data-stu-id="53a7a-141">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="53a7a-142">SplitButton</span><span class="sxs-lookup"><span data-stu-id="53a7a-142">SplitButton</span></span>
<ul>
<li><span data-ttu-id="53a7a-143">Button (1 ou 2)</span><span class="sxs-lookup"><span data-stu-id="53a7a-143">Button (1 or 2)</span></span>
<ul>
<li><span data-ttu-id="53a7a-144">MenuItem (1 et plus)</span><span class="sxs-lookup"><span data-stu-id="53a7a-144">MenuItem (1 to many)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="53a7a-145">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="53a7a-145">Relevant Properties</span></span>

<span data-ttu-id="53a7a-146">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="53a7a-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the **SplitButton** control type.</span></span> <span data-ttu-id="53a7a-147">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="53a7a-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="53a7a-148">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="53a7a-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="53a7a-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="53a7a-149">Value</span></span>           | <span data-ttu-id="53a7a-150">Notes</span><span class="sxs-lookup"><span data-stu-id="53a7a-150">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53a7a-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="53a7a-152">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a7a-152">See notes.</span></span>      | <span data-ttu-id="53a7a-153">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="53a7a-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="53a7a-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="53a7a-155">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a7a-155">See notes.</span></span>      | <span data-ttu-id="53a7a-156">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="53a7a-156">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="53a7a-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="53a7a-158">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a7a-158">See notes.</span></span>      | <span data-ttu-id="53a7a-159">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="53a7a-159">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="53a7a-160">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="53a7a-160">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="53a7a-161">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-161">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="53a7a-162">**SplitButton**</span><span class="sxs-lookup"><span data-stu-id="53a7a-162">**SplitButton**</span></span> | <span data-ttu-id="53a7a-163">Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="53a7a-163">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="53a7a-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="53a7a-165">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a7a-165">See notes.</span></span>      | <span data-ttu-id="53a7a-166">Le texte d’aide peut indiquer le résultat de l’activation du bouton partagé, qui contient généralement le même type d’informations que celles présentées via une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="53a7a-166">The help text can indicate the result of activating the split button, which is typically the same type of information presented through a tooltip.</span></span>                                                   |
| [<span data-ttu-id="53a7a-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="53a7a-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="53a7a-168">TRUE</span></span>            | <span data-ttu-id="53a7a-169">Le contrôle bouton partagé contient des informations pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="53a7a-169">The split button control contains information for the end user.</span></span>                                                                                                                                      |
| [<span data-ttu-id="53a7a-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="53a7a-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="53a7a-171">TRUE</span></span>            | <span data-ttu-id="53a7a-172">Le contrôle bouton partagé est visible par l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="53a7a-172">The split button control is visible to the end user.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="53a7a-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="53a7a-174">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a7a-174">See notes.</span></span>      | <span data-ttu-id="53a7a-175">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="53a7a-175">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="53a7a-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="53a7a-177">NULL</span><span class="sxs-lookup"><span data-stu-id="53a7a-177">NULL</span></span>            | <span data-ttu-id="53a7a-178">Les contrôles bouton partagé n’ont pas d’étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="53a7a-178">Split button controls do not have a static text label.</span></span>                                                                                                                                               |
| [<span data-ttu-id="53a7a-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="53a7a-180">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a7a-180">See notes.</span></span>      | <span data-ttu-id="53a7a-181">Chaîne localisée correspondant au type de contrôle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="53a7a-181">Localized string corresponding to the **SplitButton** control type.</span></span> <span data-ttu-id="53a7a-182">La valeur par défaut est « fractionner le bouton » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="53a7a-182">The default value is "split button" for en-US or English (United States).</span></span>                                                        |
| [<span data-ttu-id="53a7a-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="53a7a-184">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="53a7a-184">See notes.</span></span>      | <span data-ttu-id="53a7a-185">Texte utilisé pour étiqueter le bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="53a7a-185">The text that is used to label the split button.</span></span> <span data-ttu-id="53a7a-186">Chaque fois qu’une image est utilisée pour étiqueter un bouton partagé, un texte de remplacement doit être fourni pour la propriété nom du bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="53a7a-186">Whenever an image is used to label a split button, alternate text must be supplied for the split button Name property.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="53a7a-187">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="53a7a-187">Required Control Patterns</span></span>

<span data-ttu-id="53a7a-188">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles bouton partagé.</span><span class="sxs-lookup"><span data-stu-id="53a7a-188">The following table lists the UI Automation control patterns required to be supported by all split button controls.</span></span> <span data-ttu-id="53a7a-189">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="53a7a-189">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="53a7a-190">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="53a7a-190">Control Pattern</span></span>                                                   | <span data-ttu-id="53a7a-191">Support</span><span class="sxs-lookup"><span data-stu-id="53a7a-191">Support</span></span>  | <span data-ttu-id="53a7a-192">Notes</span><span class="sxs-lookup"><span data-stu-id="53a7a-192">Notes</span></span>                                                                                                                                                                                                                          |
|-------------------------------------------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53a7a-193">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="53a7a-193">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="53a7a-194">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="53a7a-194">Required</span></span> | <span data-ttu-id="53a7a-195">Étant donné que les boutons partagés ont toujours la possibilité de développer une liste d’options, ils doivent prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="53a7a-195">Because split buttons always have the ability to expand a list of options, they must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span>                                                      |
| [<span data-ttu-id="53a7a-196">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="53a7a-196">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="53a7a-197">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="53a7a-197">Required</span></span> | <span data-ttu-id="53a7a-198">Étant donné que les boutons partagés ont toujours une action par défaut associée à la méthode [**IInvokeProvider :: Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) , ils doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="53a7a-198">Because split buttons always have a default action associated with the [**IInvokeProvider::Invoke**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iinvokeprovider-invoke) method, they must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="53a7a-199">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="53a7a-199">Required Events</span></span>

<span data-ttu-id="53a7a-200">Le tableau suivant répertorie les événements UI Automation qui doivent être pris en charge par les contrôles bouton Split.</span><span class="sxs-lookup"><span data-stu-id="53a7a-200">The following table lists the UI Automation events that split button controls are required to support.</span></span> <span data-ttu-id="53a7a-201">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="53a7a-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="53a7a-202">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="53a7a-202">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="53a7a-203">Notes</span><span class="sxs-lookup"><span data-stu-id="53a7a-203">Notes</span></span>                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53a7a-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| <span data-ttu-id="53a7a-205">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="53a7a-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                            |
| <span data-ttu-id="53a7a-206">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="53a7a-206">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="53a7a-207">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-207">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  |                                                                                                                            |
| <span data-ttu-id="53a7a-208">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="53a7a-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="53a7a-209">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="53a7a-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="53a7a-210">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="53a7a-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="53a7a-211">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="53a7a-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="53a7a-212">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="53a7a-212">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                            |



 

## <a name="splitbutton-control-type-example"></a><span data-ttu-id="53a7a-213">Exemple de type de contrôle SplitButton</span><span class="sxs-lookup"><span data-stu-id="53a7a-213">SplitButton Control Type Example</span></span>

<span data-ttu-id="53a7a-214">L’image suivante illustre un contrôle qui implémente le type de contrôle **SplitButton** .</span><span class="sxs-lookup"><span data-stu-id="53a7a-214">The following image illustrates a control that implements the **SplitButton** control type.</span></span>

![capture d’écran montrant un exemple de contrôle SplitButton](images/splitbuttonxmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="53a7a-216">Arborescence UI Automation — vue contrôle</span><span class="sxs-lookup"><span data-stu-id="53a7a-216">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="53a7a-217">Arborescence UI Automation — affichage du contenu</span><span class="sxs-lookup"><span data-stu-id="53a7a-217">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="53a7a-218">Nom du SplitButton &quot; &quot; (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="53a7a-218">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="53a7a-219">Bouton &quot; plus &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="53a7a-219">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="53a7a-220">Menu</span><span class="sxs-lookup"><span data-stu-id="53a7a-220">Menu</span></span>
<ul>
<li><span data-ttu-id="53a7a-221">MenuItem</span><span class="sxs-lookup"><span data-stu-id="53a7a-221">MenuItem</span></span></li>
<li><span data-ttu-id="53a7a-222">...</span><span class="sxs-lookup"><span data-stu-id="53a7a-222">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="53a7a-223">Nom du SplitButton &quot; &quot; (Invoke, ExpandCollapse)</span><span class="sxs-lookup"><span data-stu-id="53a7a-223">SplitButton &quot;Name&quot; (Invoke, ExpandCollapse)</span></span>
<ul>
<li><span data-ttu-id="53a7a-224">Bouton &quot; plus &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="53a7a-224">Button &quot;More option&quot; (Invoke)</span></span>
<ul>
<li><span data-ttu-id="53a7a-225">Menu</span><span class="sxs-lookup"><span data-stu-id="53a7a-225">Menu</span></span>
<ul>
<li><span data-ttu-id="53a7a-226">MenuItem</span><span class="sxs-lookup"><span data-stu-id="53a7a-226">MenuItem</span></span></li>
<li><span data-ttu-id="53a7a-227">...</span><span class="sxs-lookup"><span data-stu-id="53a7a-227">...</span></span></li>
</ul></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="53a7a-228">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="53a7a-228">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="53a7a-229">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="53a7a-229">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="53a7a-230">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="53a7a-230">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="53a7a-231">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="53a7a-231">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




