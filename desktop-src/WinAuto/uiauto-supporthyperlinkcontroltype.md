---
title: HYPERLINK (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle HyperLink.
ms.assetid: 6dd16ae6-eff0-4913-8916-5092aec34f1f
keywords:
- UI Automation, prise en charge du type de contrôle HyperLink
- UI Automation, type de contrôle HyperLink
- UI Automation, arborescence pour le type de contrôle HyperLink
- UI Automation, propriétés du type de contrôle HyperLink
- UI Automation, modèles de contrôle pour le type de contrôle HyperLink
- UI Automation, événements pour le type de contrôle HyperLink
- arborescences, type de contrôle HyperLink
- Propriétés, type de contrôle HyperLink
- modèles de contrôle, type de contrôle HyperLink
- événements, type de contrôle HyperLink
- prise en charge du type de contrôle HyperLink
- Hyperlink (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle HyperLink
- types de contrôles, modèles de contrôle pour le type de contrôle HyperLink
- types de contrôles, prise en charge du lien hypertexte
- types de contrôles, lien hypertexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71547f37380aeb029e4f73f8d9b2286b285187ff
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673074"
---
# <a name="hyperlink-control-type"></a><span data-ttu-id="4d288-119">HYPERLINK (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="4d288-119">Hyperlink Control Type</span></span>

<span data-ttu-id="4d288-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="4d288-120">This topic provides information about Microsoft UI Automation support for the **Hyperlink** control type.</span></span>

<span data-ttu-id="4d288-121">Les contrôles de lien hypertexte créent des liens qui permettent aux utilisateurs de naviguer dans la même page ou d’une page à une autre.</span><span class="sxs-lookup"><span data-stu-id="4d288-121">Hyperlink controls create links that enable users to navigate within the same page, or from one page to another.</span></span>

<span data-ttu-id="4d288-122">Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="4d288-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Hyperlink** control type.</span></span> <span data-ttu-id="4d288-123">Les exigences d’UI Automation s’appliquent à tous les contrôles de lien hypertexte où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="4d288-123">The UI Automation requirements apply to all hyperlink controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4d288-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4d288-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4d288-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="4d288-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4d288-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="4d288-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4d288-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="4d288-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4d288-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="4d288-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4d288-129">Remarques</span><span class="sxs-lookup"><span data-stu-id="4d288-129">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="4d288-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d288-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4d288-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="4d288-131">Typical Tree Structure</span></span>

<span data-ttu-id="4d288-132">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de lien hypertexte et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="4d288-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to hyperlink controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4d288-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4d288-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d288-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="4d288-134">Control View</span></span></th>
<th><span data-ttu-id="4d288-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="4d288-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4d288-136">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="4d288-136">Hyperlink</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4d288-137">Hyperlink</span><span class="sxs-lookup"><span data-stu-id="4d288-137">Hyperlink</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="4d288-138">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="4d288-138">Relevant Properties</span></span>

<span data-ttu-id="4d288-139">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="4d288-139">The following table lists the UI Automation properties whose value or definition is especially relevant to the hyperlink controls.</span></span> <span data-ttu-id="4d288-140">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4d288-140">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4d288-141">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d288-141">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4d288-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="4d288-142">Value</span></span>         | <span data-ttu-id="4d288-143">Notes</span><span class="sxs-lookup"><span data-stu-id="4d288-143">Notes</span></span>                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d288-144">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-144">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4d288-145">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4d288-145">See notes.</span></span>    | <span data-ttu-id="4d288-146">La valeur de cette propriété doit être unique pour tous les contrôles d’une application.</span><span class="sxs-lookup"><span data-stu-id="4d288-146">The value of this property must be unique across all controls in an application.</span></span>                                                         |
| [<span data-ttu-id="4d288-147">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-147">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4d288-148">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4d288-148">See notes.</span></span>    | <span data-ttu-id="4d288-149">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4d288-149">The outermost rectangle that contains the whole control.</span></span>                                                                                 |
| [<span data-ttu-id="4d288-150">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-150">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4d288-151">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4d288-151">See notes.</span></span>    | <span data-ttu-id="4d288-152">Le point cliquable du contrôle de lien hypertexte doit être un point qui lance le lien hypertexte si l’utilisateur clique dessus avec le pointeur de la souris.</span><span class="sxs-lookup"><span data-stu-id="4d288-152">The hyperlink control's clickable point must be a point that launches the hyperlink if clicked with a mouse pointer.</span></span>                     |
| [<span data-ttu-id="4d288-153">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-153">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4d288-154">**Lien hypertexte**</span><span class="sxs-lookup"><span data-stu-id="4d288-154">**Hyperlink**</span></span> |                                                                                                                                          |
| [<span data-ttu-id="4d288-155">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-155">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4d288-156">TRUE</span><span class="sxs-lookup"><span data-stu-id="4d288-156">TRUE</span></span>          | <span data-ttu-id="4d288-157">Le contrôle de lien hypertexte est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4d288-157">The hyperlink control is always included in the content view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="4d288-158">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-158">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4d288-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="4d288-159">TRUE</span></span>          | <span data-ttu-id="4d288-160">Le contrôle de lien hypertexte est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4d288-160">The hyperlink control is always included in the control view of the UI Automation tree.</span></span>                                                  |
| [<span data-ttu-id="4d288-161">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-161">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4d288-162">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4d288-162">See notes.</span></span>    | <span data-ttu-id="4d288-163">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4d288-163">If the control can receive keyboard focus, it must support this property.</span></span>                                                                |
| [<span data-ttu-id="4d288-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4d288-165">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4d288-165">See notes.</span></span>    | <span data-ttu-id="4d288-166">S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="4d288-166">If there is a static text label, this property must expose a reference to that control.</span></span>                                                  |
| [<span data-ttu-id="4d288-167">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-167">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4d288-168">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4d288-168">See notes.</span></span>    | <span data-ttu-id="4d288-169">Chaîne localisée correspondant au type de contrôle **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="4d288-169">Localized string corresponding to the **Hyperlink** control type.</span></span> <span data-ttu-id="4d288-170">La valeur par défaut est « HYPERLINK » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="4d288-170">The default value is "hyperlink" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="4d288-171">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4d288-171">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4d288-172">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4d288-172">See notes.</span></span>    | <span data-ttu-id="4d288-173">Le nom du contrôle de lien hypertexte est le texte affiché sur l’écran comme souligné.</span><span class="sxs-lookup"><span data-stu-id="4d288-173">The hyperlink control's name is the text that is displayed on the screen as underlined.</span></span>                                                  |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4d288-174">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="4d288-174">Required Control Patterns</span></span>

<span data-ttu-id="4d288-175">Le tableau suivant répertorie les modèles de contrôle UI Automation que les contrôles de lien hypertexte doivent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="4d288-175">The following table lists the UI Automation control patterns that hyperlink controls are required to support.</span></span> <span data-ttu-id="4d288-176">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4d288-176">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4d288-177">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="4d288-177">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="4d288-178">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="4d288-178">Support/Value</span></span>                | <span data-ttu-id="4d288-179">Notes</span><span class="sxs-lookup"><span data-stu-id="4d288-179">Notes</span></span>                                                                                                                                                                                                                                                  |
|---------------------------------------------------|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d288-180">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="4d288-180">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider) | <span data-ttu-id="4d288-181">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="4d288-181">Required</span></span>                     | <span data-ttu-id="4d288-182">Tous les contrôles de lien hypertexte doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) .</span><span class="sxs-lookup"><span data-stu-id="4d288-182">All hyperlink controls must support the [Invoke](uiauto-implementinginvoke.md) control pattern.</span></span>                                                                                                                                                       |
| [<span data-ttu-id="4d288-183">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="4d288-183">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="4d288-184">Dépend</span><span class="sxs-lookup"><span data-stu-id="4d288-184">Depends</span></span>                      | <span data-ttu-id="4d288-185">Les contrôles de lien hypertexte doivent prendre en charge le modèle de contrôle [value](uiauto-implementingvalue.md) quand le lien contient des informations utilisables et explicites pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4d288-185">Hyperlink controls should support the [Value](uiauto-implementingvalue.md) control pattern when the link contains information that is usable and meaningful to the user.</span></span>                                                                              |
| [<span data-ttu-id="4d288-186">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="4d288-186">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-ivalueprovider-get_value)      | <span data-ttu-id="4d288-187">Par exemple, «https://www...»</span><span class="sxs-lookup"><span data-stu-id="4d288-187">For example, "https://www..."</span></span> | <span data-ttu-id="4d288-188">Une URL pour une adresse Internet ou intranet est un exemple de lien hypertexte qui contient des informations explicites pour l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="4d288-188">A URL for an Internet or intranet address is an example of a hyperlink that contains information that is meaningful to the user.</span></span> <span data-ttu-id="4d288-189">Toutefois, un lien de programmation est significatif uniquement pour une application et n’est pas recommandé pour la propriété **value** .</span><span class="sxs-lookup"><span data-stu-id="4d288-189">A programmatic link, however, is meaningful only to an application and is not recommended for the **Value** property.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="4d288-190">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="4d288-190">Required Events</span></span>

<span data-ttu-id="4d288-191">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="4d288-191">The following table lists the UI Automation events that hyperlink controls are required to support.</span></span> <span data-ttu-id="4d288-192">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4d288-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4d288-193">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d288-193">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="4d288-194">Notes</span><span class="sxs-lookup"><span data-stu-id="4d288-194">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4d288-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4d288-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="4d288-196">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4d288-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="4d288-197">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="4d288-197">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     |                                                                                                                            |
| <span data-ttu-id="4d288-198">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4d288-198">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="4d288-199">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4d288-199">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="4d288-200">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4d288-200">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="4d288-201">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4d288-201">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="4d288-202">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4d288-202">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="4d288-203">Notes</span><span class="sxs-lookup"><span data-stu-id="4d288-203">Remarks</span></span>

<span data-ttu-id="4d288-204">Le type de contrôle HyperLink doit être appliqué uniquement à un objet qui, lorsque vous cliquez dessus, provoque l’exécution de la navigation. elle ne doit pas être appliquée au conteneur du lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="4d288-204">The Hyperlink control type should be applied only to an object that, when clicked, causes navigation to occur; it should not be applied to the container of the hyperlink.</span></span> <span data-ttu-id="4d288-205">Par exemple, seules les « zones réactives » cliquables à l’intérieur d’une image interactive doivent avoir le type de contrôle **Hyperlink** .</span><span class="sxs-lookup"><span data-stu-id="4d288-205">For example, only the clickable "hot spots" inside an image map should have the **Hyperlink** control type.</span></span> <span data-ttu-id="4d288-206">Il en va de même pour les liens hypertexte dans un champ de texte ou un conteneur de documents.</span><span class="sxs-lookup"><span data-stu-id="4d288-206">The same is true of hyperlinks in a text field or document container.</span></span> <span data-ttu-id="4d288-207">Dans ce cas, seul le texte ou l’image du lien hypertexte doit avoir le type de contrôle **Hyperlink** , et non le conteneur.</span><span class="sxs-lookup"><span data-stu-id="4d288-207">In this case, only the hyperlink text or image should have the **Hyperlink** control type, not the container.</span></span>

<span data-ttu-id="4d288-208">Le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) est idéal pour prendre en charge les liens hypertexte incorporés dans les éléments texte ou document.</span><span class="sxs-lookup"><span data-stu-id="4d288-208">The [Text](uiauto-implementingtextandtextrange.md) control pattern is ideal for supporting embedded hyperlinks in text or document elements.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d288-209">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4d288-209">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4d288-210">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4d288-210">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4d288-211">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d288-211">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4d288-212">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="4d288-212">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




