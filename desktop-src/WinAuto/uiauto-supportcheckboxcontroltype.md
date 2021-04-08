---
title: CheckBox (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle CheckBox.
ms.assetid: 5a9061bc-2eac-4839-8f2c-32b9d58fe712
keywords:
- UI Automation, prise en charge du type de contrôle CheckBox
- UI Automation, type de contrôle CheckBox
- UI Automation, arborescence pour le type de contrôle CheckBox
- UI Automation, propriétés du type de contrôle CheckBox
- UI Automation, modèles de contrôle pour le type de contrôle CheckBox
- UI Automation, événements pour le type de contrôle CheckBox
- arborescences, type de contrôle CheckBox
- Propriétés, CheckBox (type de contrôle)
- modèles de contrôle, CheckBox (type de contrôle)
- événements, CheckBox (type de contrôle)
- prise en charge du type de contrôle CheckBox
- CheckBox (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle CheckBox
- types de contrôles, modèles de contrôle pour le type de contrôle CheckBox
- types de contrôles, prise en charge de CheckBox
- types de contrôle, CheckBox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8e5bac106c8ba3bbf58c7f5b06c087ceb7b3418
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839969"
---
# <a name="checkbox-control-type"></a><span data-ttu-id="5244f-119">CheckBox (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="5244f-119">CheckBox Control Type</span></span>

<span data-ttu-id="5244f-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="5244f-120">This topic provides information about Microsoft UI Automation support for the **CheckBox** control type.</span></span>

<span data-ttu-id="5244f-121">Une case à cocher est un objet utilisé pour indiquer un état avec lequel les utilisateurs peuvent interagir pour parcourir cet état.</span><span class="sxs-lookup"><span data-stu-id="5244f-121">A check box is an object used to indicate a state that users can interact with to cycle through that state.</span></span> <span data-ttu-id="5244f-122">Les cases à cocher présentent une option binaire (oui/non), (activé/désactivé), ou tertiaire (activé, désactivé, indéterminé) à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5244f-122">Check boxes either present a binary (Yes/No), (On/Off), or tertiary (On, Off, Indeterminate) option to the user.</span></span>

<span data-ttu-id="5244f-123">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="5244f-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **CheckBox** control type.</span></span> <span data-ttu-id="5244f-124">Les exigences d’UI Automation s’appliquent à tous les contrôles de case à cocher où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="5244f-124">The UI Automation requirements apply to all check box controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="5244f-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="5244f-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5244f-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="5244f-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="5244f-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="5244f-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="5244f-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="5244f-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="5244f-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="5244f-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="5244f-130">Nœud</span><span class="sxs-lookup"><span data-stu-id="5244f-130">DefaultAction</span></span>](#defaultaction)
-   [<span data-ttu-id="5244f-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5244f-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="5244f-132">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="5244f-132">Typical Tree Structure</span></span>

<span data-ttu-id="5244f-133">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de case à cocher et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="5244f-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to check box controls and describes what can be contained in each view.</span></span> <span data-ttu-id="5244f-134">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5244f-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5244f-135">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="5244f-135">Control View</span></span></th>
<th><span data-ttu-id="5244f-136">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="5244f-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5244f-137">CheckBox</span><span class="sxs-lookup"><span data-stu-id="5244f-137">CheckBox</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="5244f-138">CheckBox</span><span class="sxs-lookup"><span data-stu-id="5244f-138">CheckBox</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="5244f-139">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="5244f-139">Relevant Properties</span></span>

<span data-ttu-id="5244f-140">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="5244f-140">The following table lists the UI Automation properties whose value or definition is especially relevant to the **CheckBox** control type.</span></span> <span data-ttu-id="5244f-141">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="5244f-141">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="5244f-142">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="5244f-142">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="5244f-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="5244f-143">Value</span></span>        | <span data-ttu-id="5244f-144">Notes</span><span class="sxs-lookup"><span data-stu-id="5244f-144">Notes</span></span>                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5244f-145">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-145">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="5244f-146">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5244f-146">See notes.</span></span>   | <span data-ttu-id="5244f-147">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5244f-147">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="5244f-148">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-148">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="5244f-149">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5244f-149">See notes.</span></span>   | <span data-ttu-id="5244f-150">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5244f-150">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                           |
| [<span data-ttu-id="5244f-151">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-151">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="5244f-152">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5244f-152">See notes.</span></span>   | <span data-ttu-id="5244f-153">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="5244f-153">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="5244f-154">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="5244f-154">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                               |
| [<span data-ttu-id="5244f-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5244f-156">**CheckBox**</span><span class="sxs-lookup"><span data-stu-id="5244f-156">**CheckBox**</span></span> |                                                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="5244f-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5244f-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="5244f-158">TRUE</span></span>         | <span data-ttu-id="5244f-159">La valeur de cette propriété doit toujours être **true**.</span><span class="sxs-lookup"><span data-stu-id="5244f-159">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="5244f-160">Cela signifie que le contrôle de case à cocher doit toujours être inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5244f-160">This means that the check box control must always be included in the content view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="5244f-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5244f-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="5244f-162">TRUE</span></span>         | <span data-ttu-id="5244f-163">La valeur de cette propriété doit toujours être **true**.</span><span class="sxs-lookup"><span data-stu-id="5244f-163">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="5244f-164">Cela signifie que le contrôle de case à cocher doit toujours être inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5244f-164">This means that the check box control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="5244f-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="5244f-166">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5244f-166">See notes.</span></span>   | <span data-ttu-id="5244f-167">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5244f-167">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="5244f-168">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-168">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="5244f-169">Null</span><span class="sxs-lookup"><span data-stu-id="5244f-169">Null</span></span>         | <span data-ttu-id="5244f-170">Les contrôles de case à cocher sont à étiquette automatique.</span><span class="sxs-lookup"><span data-stu-id="5244f-170">Check box controls are self-labeling.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="5244f-171">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-171">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="5244f-172">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5244f-172">See notes.</span></span>   | <span data-ttu-id="5244f-173">Chaîne localisée correspondant au type de contrôle **CheckBox** .</span><span class="sxs-lookup"><span data-stu-id="5244f-173">Localized string corresponding to the **CheckBox** control type.</span></span> <span data-ttu-id="5244f-174">La valeur par défaut est « case à cocher » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="5244f-174">The default value is "check box" for en-US or English (United States).</span></span>                                                                                                                                            |
| [<span data-ttu-id="5244f-175">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5244f-175">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="5244f-176">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5244f-176">See notes.</span></span>   | <span data-ttu-id="5244f-177">La valeur de la propriété [**IUIAutomationElement :: CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (ou [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) du contrôle de case à cocher est le texte qui s’affiche à côté de la zone qui maintient l’État bascule.</span><span class="sxs-lookup"><span data-stu-id="5244f-177">The value of the check box control's [**IUIAutomationElement::CurrentName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_currentname) (or [**CachedName**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-get_cachedname)) property is the text that is displayed beside the box that maintains the toggle state.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="5244f-178">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="5244f-178">Required Control Patterns</span></span>

<span data-ttu-id="5244f-179">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="5244f-179">The following table lists the UI Automation control patterns required to be supported by all check box controls.</span></span> <span data-ttu-id="5244f-180">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5244f-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="5244f-181">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="5244f-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="5244f-182">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="5244f-182">Support/Value</span></span> | <span data-ttu-id="5244f-183">Notes</span><span class="sxs-lookup"><span data-stu-id="5244f-183">Notes</span></span>                                                                                                                                                             |
|---------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5244f-184">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="5244f-184">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="5244f-185">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="5244f-185">Required</span></span>      | <span data-ttu-id="5244f-186">Les cases à cocher prennent en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) pour permettre à la case à cocher d’être recycle par programmation par le biais de ses États internes.</span><span class="sxs-lookup"><span data-stu-id="5244f-186">Check boxes support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the check box to be programmatically cycled through its internal states.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="5244f-187">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="5244f-187">Required Events</span></span>

<span data-ttu-id="5244f-188">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de case à cocher.</span><span class="sxs-lookup"><span data-stu-id="5244f-188">The following table lists the UI Automation events that check box controls are required to support.</span></span> <span data-ttu-id="5244f-189">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5244f-189">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="5244f-190">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="5244f-190">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="5244f-191">Notes</span><span class="sxs-lookup"><span data-stu-id="5244f-191">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5244f-192">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5244f-192">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="5244f-193">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="5244f-193">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="5244f-194">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="5244f-194">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="5244f-195">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="5244f-195">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="5244f-196">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="5244f-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="5244f-197">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="5244f-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| [<span data-ttu-id="5244f-198">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5244f-198">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="5244f-199">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="5244f-199">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="defaultaction"></a><span data-ttu-id="5244f-200">Nœud</span><span class="sxs-lookup"><span data-stu-id="5244f-200">DefaultAction</span></span>

<span data-ttu-id="5244f-201">L’action par défaut de la case à cocher est de placer le focus sur une case d’option et de basculer son état actuel.</span><span class="sxs-lookup"><span data-stu-id="5244f-201">The default action of the check box is to cause a radio button to become focused and toggle its current state.</span></span> <span data-ttu-id="5244f-202">Comme mentionné précédemment, les cases à cocher présentent une décision binaire (oui/non ou activé/désactivé) à l’utilisateur ou un tertiaire (activé, désactivé ou indéterminé).</span><span class="sxs-lookup"><span data-stu-id="5244f-202">As mentioned previously, check boxes either present a binary (Yes/No or On/Off) decision to the user or a tertiary (On, Off, Indeterminate).</span></span> <span data-ttu-id="5244f-203">Si la case à cocher est binaire, l’action par défaut bascule l’état « activé » vers « désactivé » ou l’état « désactivé » vers « activé ».</span><span class="sxs-lookup"><span data-stu-id="5244f-203">If the check box is binary the default action causes the "on" state to become "off" or the "off" state to become "on".</span></span> <span data-ttu-id="5244f-204">Dans une case à cocher tertiaire, l’action par défaut parcourt les États de la case à cocher dans le même ordre que si l’utilisateur a envoyé des clics de souris successifs au contrôle.</span><span class="sxs-lookup"><span data-stu-id="5244f-204">In a tertiary check box the default action cycles through the states of the check box in the same order as if the user had sent successive mouse clicks to the control.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5244f-205">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5244f-205">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5244f-206">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5244f-206">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5244f-207">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="5244f-207">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5244f-208">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="5244f-208">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




