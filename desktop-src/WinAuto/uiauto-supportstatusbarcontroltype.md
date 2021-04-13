---
title: StatusBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle StatusBar.
ms.assetid: a28df0a1-95a8-4941-a00d-1f5570589626
keywords:
- UI Automation, prise en charge du type de contrôle StatusBar
- UI Automation, type de contrôle StatusBar
- UI Automation, arborescence pour le type de contrôle StatusBar
- UI Automation, propriétés pour le type de contrôle StatusBar
- UI Automation, modèles de contrôle pour le type de contrôle StatusBar
- UI Automation, événements pour le type de contrôle StatusBar
- arborescences, type de contrôle StatusBar
- Propriétés, type de contrôle StatusBar
- modèles de contrôle, type de contrôle StatusBar
- événements, type de contrôle StatusBar
- prise en charge du type de contrôle StatusBar
- StatusBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle StatusBar
- types de contrôle, modèles de contrôle pour le type de contrôle StatusBar
- types de contrôles, prise en charge de StatusBar
- types de contrôles, StatusBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65ace64d34429a6d381dfdef2d99d82a3693fca2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310593"
---
# <a name="statusbar-control-type"></a><span data-ttu-id="15c0a-119">StatusBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="15c0a-119">StatusBar Control Type</span></span>

<span data-ttu-id="15c0a-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="15c0a-120">This topic provides information about Microsoft UI Automation support for the **StatusBar** control type.</span></span>

<span data-ttu-id="15c0a-121">Un contrôle de barre d’état affiche des informations sur un objet affiché dans une fenêtre d’une application, le composant de l’objet ou des informations contextuelles relatives au fonctionnement de cet objet dans votre application.</span><span class="sxs-lookup"><span data-stu-id="15c0a-121">A status bar control displays information about an object being viewed in a window of an application, the object's component, or contextual information that relates to that object's operation within your application.</span></span>

<span data-ttu-id="15c0a-122">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="15c0a-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **StatusBar** control type.</span></span> <span data-ttu-id="15c0a-123">Les exigences d’UI Automation s’appliquent à tous les contrôles de barre d’État où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="15c0a-123">The UI Automation requirements apply to all status bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="15c0a-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="15c0a-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="15c0a-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="15c0a-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="15c0a-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="15c0a-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="15c0a-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="15c0a-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="15c0a-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="15c0a-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="15c0a-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="15c0a-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="15c0a-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15c0a-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="15c0a-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="15c0a-131">Typical Tree Structure</span></span>

<span data-ttu-id="15c0a-132">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de barre d’État et décrit ce que peut contenir chaque vue.</span><span class="sxs-lookup"><span data-stu-id="15c0a-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to status bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="15c0a-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="15c0a-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15c0a-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="15c0a-134">Control View</span></span></th>
<th><span data-ttu-id="15c0a-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="15c0a-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="15c0a-136">StatusBar</span><span class="sxs-lookup"><span data-stu-id="15c0a-136">StatusBar</span></span>
<ul>
<li><span data-ttu-id="15c0a-137">Edition (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="15c0a-137">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="15c0a-138">ProgressBar (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="15c0a-138">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="15c0a-139">Image (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="15c0a-139">Image (0 or many)</span></span></li>
<li><span data-ttu-id="15c0a-140">Bouton (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="15c0a-140">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="15c0a-141">StatusBar</span><span class="sxs-lookup"><span data-stu-id="15c0a-141">StatusBar</span></span>
<ul>
<li><span data-ttu-id="15c0a-142">Edition (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="15c0a-142">Edit (0 or more)</span></span></li>
<li><span data-ttu-id="15c0a-143">ProgressBar (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="15c0a-143">ProgressBar (0 or many)</span></span></li>
<li><span data-ttu-id="15c0a-144">Image (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="15c0a-144">Image (0 or many)</span></span></li>
<li><span data-ttu-id="15c0a-145">Bouton (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="15c0a-145">Button (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="15c0a-146">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="15c0a-146">Relevant Properties</span></span>

<span data-ttu-id="15c0a-147">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de barre d’État.</span><span class="sxs-lookup"><span data-stu-id="15c0a-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the status bar controls.</span></span> <span data-ttu-id="15c0a-148">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="15c0a-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="15c0a-149">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="15c0a-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="15c0a-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="15c0a-150">Value</span></span>         | <span data-ttu-id="15c0a-151">Notes</span><span class="sxs-lookup"><span data-stu-id="15c0a-151">Notes</span></span>                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15c0a-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="15c0a-153">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="15c0a-153">See notes.</span></span>    | <span data-ttu-id="15c0a-154">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="15c0a-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                        |
| [<span data-ttu-id="15c0a-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="15c0a-156">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="15c0a-156">See notes.</span></span>    | <span data-ttu-id="15c0a-157">Le rectangle englobant d’une barre d’état doit englober tous les contrôles qu’il contient.</span><span class="sxs-lookup"><span data-stu-id="15c0a-157">The bounding rectangle of a status bar must encompass all of the controls contained within it.</span></span>                                                                                                                      |
| [<span data-ttu-id="15c0a-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="15c0a-159">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="15c0a-159">See notes.</span></span>    | <span data-ttu-id="15c0a-160">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="15c0a-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="15c0a-161">Si des zones du rectangle englobant ne sont pas interdépendantes et que l’élément effectue un test de positionnement spécialisé, substituez-le et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="15c0a-161">If there are areas within the bounding rectangle that are not clickable, and the element performs specialized hit testing, override this and provide a clickable point.</span></span> |
| [<span data-ttu-id="15c0a-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="15c0a-163">**StatusBar**</span><span class="sxs-lookup"><span data-stu-id="15c0a-163">**StatusBar**</span></span> |                                                                                                                                                                                                                     |
| [<span data-ttu-id="15c0a-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="15c0a-165">TRUE</span><span class="sxs-lookup"><span data-stu-id="15c0a-165">TRUE</span></span>          | <span data-ttu-id="15c0a-166">Le contrôle de barre d’État est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="15c0a-166">The status bar control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="15c0a-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="15c0a-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="15c0a-168">TRUE</span></span>          | <span data-ttu-id="15c0a-169">Le contrôle de barre d’État est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="15c0a-169">The status bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                            |
| [<span data-ttu-id="15c0a-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="15c0a-171">Dépend</span><span class="sxs-lookup"><span data-stu-id="15c0a-171">Depends</span></span>       | <span data-ttu-id="15c0a-172">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="15c0a-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                           |
| [<span data-ttu-id="15c0a-173">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-173">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="15c0a-174">Dépend</span><span class="sxs-lookup"><span data-stu-id="15c0a-174">Depends</span></span>       | <span data-ttu-id="15c0a-175">Si un contrôle de barre d’État n’est pas actuellement visible, il retourne la valeur TRUE pour cette propriété.</span><span class="sxs-lookup"><span data-stu-id="15c0a-175">If a status bar control is not currently visible, it will return TRUE for this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="15c0a-176">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-176">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="15c0a-177">NULL</span><span class="sxs-lookup"><span data-stu-id="15c0a-177">NULL</span></span>          | <span data-ttu-id="15c0a-178">Le contrôle de barre d’État n’a généralement pas d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="15c0a-178">The status bar control typically does not have a label.</span></span>                                                                                                                                                             |
| [<span data-ttu-id="15c0a-179">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-179">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="15c0a-180">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="15c0a-180">See notes.</span></span>    | <span data-ttu-id="15c0a-181">Chaîne localisée correspondant au type de contrôle **StatusBar** .</span><span class="sxs-lookup"><span data-stu-id="15c0a-181">Localized string corresponding to the **StatusBar** control type.</span></span> <span data-ttu-id="15c0a-182">La valeur par défaut est « barre d’État » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="15c0a-182">The default value is "status bar" for en-US or English (United States).</span></span>                                                                           |
| [<span data-ttu-id="15c0a-183">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-183">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="15c0a-184">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="15c0a-184">See notes.</span></span>    | <span data-ttu-id="15c0a-185">Le contrôle de barre d’état n’a pas besoin d’un nom sauf si plusieurs contrôles sont utilisés dans une application.</span><span class="sxs-lookup"><span data-stu-id="15c0a-185">The status bar control does not need a name unless more than one is used within an application.</span></span> <span data-ttu-id="15c0a-186">Dans ce cas, distinguez chaque barre par des noms tels que « État Internet » ou « état de l’application ».</span><span class="sxs-lookup"><span data-stu-id="15c0a-186">In this case, distinguish each bar with names such as "Internet Status" or "Application Status".</span></span>                    |
| [<span data-ttu-id="15c0a-187">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-187">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="15c0a-188">Dépend</span><span class="sxs-lookup"><span data-stu-id="15c0a-188">Depends</span></span>       | <span data-ttu-id="15c0a-189">Valeur indiquant l’orientation du contrôle : horizontale ou verticale.</span><span class="sxs-lookup"><span data-stu-id="15c0a-189">A value indicating the control's orientation: horizontal or vertical.</span></span>                                                                                                                                               |



 

## <a name="required-control-patterns"></a><span data-ttu-id="15c0a-190">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="15c0a-190">Required Control Patterns</span></span>

<span data-ttu-id="15c0a-191">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge pour les contrôles de barre d’État.</span><span class="sxs-lookup"><span data-stu-id="15c0a-191">The following table lists the UI Automation control patterns required to be supported for status bar controls.</span></span> <span data-ttu-id="15c0a-192">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="15c0a-192">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="15c0a-193">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="15c0a-193">Control Pattern</span></span>                               | <span data-ttu-id="15c0a-194">Support</span><span class="sxs-lookup"><span data-stu-id="15c0a-194">Support</span></span>  | <span data-ttu-id="15c0a-195">Notes</span><span class="sxs-lookup"><span data-stu-id="15c0a-195">Notes</span></span>                                                                                                                                                                        |
|-----------------------------------------------|----------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15c0a-196">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="15c0a-196">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) | <span data-ttu-id="15c0a-197">Facultatif</span><span class="sxs-lookup"><span data-stu-id="15c0a-197">Optional</span></span> | <span data-ttu-id="15c0a-198">Les contrôles de barre d’État doivent prendre en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) pour que les éléments individuels puissent être surveillés et facilement référencés pour les informations.</span><span class="sxs-lookup"><span data-stu-id="15c0a-198">Status bar controls should support the [Grid](uiauto-implementinggrid.md) control pattern so that individual pieces can be monitored and easily referenced for information.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="15c0a-199">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="15c0a-199">Required Events</span></span>

<span data-ttu-id="15c0a-200">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de barre d’État.</span><span class="sxs-lookup"><span data-stu-id="15c0a-200">The following table lists the UI Automation events that status bar controls are required to support.</span></span> <span data-ttu-id="15c0a-201">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="15c0a-201">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="15c0a-202">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="15c0a-202">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="15c0a-203">Notes</span><span class="sxs-lookup"><span data-stu-id="15c0a-203">Notes</span></span>                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="15c0a-204">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-204">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                   |
| <span data-ttu-id="15c0a-205">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="15c0a-205">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                   |
| <span data-ttu-id="15c0a-206">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="15c0a-206">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="15c0a-207">Si le contrôle prend en charge la propriété **IsEnabled** , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="15c0a-207">If the control supports the **IsEnabled** property, it must support this event.</span></span>   |
| <span data-ttu-id="15c0a-208">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="15c0a-208">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="15c0a-209">Si le contrôle prend en charge la propriété **IsOffscreen** , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="15c0a-209">If the control supports the **IsOffscreen** property, it must support this event.</span></span> |
| [<span data-ttu-id="15c0a-210">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="15c0a-210">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="15c0a-211">Notes</span><span class="sxs-lookup"><span data-stu-id="15c0a-211">Remarks</span></span>

<span data-ttu-id="15c0a-212">Nous vous recommandons d’utiliser des contrôles d’édition comme éléments de grille enfants dans une barre d’État.</span><span class="sxs-lookup"><span data-stu-id="15c0a-212">We recommend that edit controls be used as child grid elements in a status bar.</span></span> <span data-ttu-id="15c0a-213">Grâce aux contrôles d’édition, il est plus facile d’associer l’objectif du champ d’État à sa valeur à l’aide de la propriété nom et valeur de l’élément.</span><span class="sxs-lookup"><span data-stu-id="15c0a-213">Using edit controls makes it easier to associate the purpose of the status field with its value by using the element name and value property.</span></span> <span data-ttu-id="15c0a-214">Étant donné que les contrôles de texte ne doivent pas prendre en charge le modèle de contrôle **value** , ils ne doivent pas être utilisés en tant qu’éléments de grille enfants.</span><span class="sxs-lookup"><span data-stu-id="15c0a-214">Because text controls should not support the **Value** control pattern, they should not be used as child grid elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15c0a-215">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15c0a-215">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="15c0a-216">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="15c0a-216">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="15c0a-217">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="15c0a-217">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="15c0a-218">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="15c0a-218">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




