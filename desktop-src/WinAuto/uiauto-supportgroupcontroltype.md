---
title: Group (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Group.
ms.assetid: f8363c2f-dbff-43a3-831f-d30151829ef9
keywords:
- UI Automation, prise en charge du type de contrôle de groupe
- UI Automation, type de contrôle de groupe
- UI Automation, arborescence pour le type de contrôle Group
- UI Automation, propriétés du type de contrôle de groupe
- UI Automation, modèles de contrôle pour le type de contrôle Group
- UI Automation, événements pour le type de contrôle Group
- arborescences, type de contrôle de groupe
- Propriétés, groupe de contrôles (type)
- modèles de contrôle, type de contrôle de groupe
- événements, type de contrôle de groupe
- prise en charge du type de contrôle Group
- Group (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Group
- types de contrôles, modèles de contrôle pour le type de contrôle Group
- types de contrôle, prise en charge du groupe
- types de contrôles, groupe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44b630d0ef736d937e4f024c8131adc4c843b6e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379879"
---
# <a name="group-control-type"></a><span data-ttu-id="9d94b-119">Group (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="9d94b-119">Group Control Type</span></span>

<span data-ttu-id="9d94b-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Group** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-120">This topic provides information about Microsoft UI Automation support for the **Group** control type.</span></span>

<span data-ttu-id="9d94b-121">Un contrôle de groupe représente un nœud dans une hiérarchie.</span><span class="sxs-lookup"><span data-stu-id="9d94b-121">A group control represents a node within a hierarchy.</span></span> <span data-ttu-id="9d94b-122">Le type de contrôle **Group** crée une séparation dans l’arborescence UI Automation de sorte que les éléments regroupés ont une division logique dans l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9d94b-122">The **Group** control type creates a separation in the UI Automation tree so items that are grouped together have a logical division within the UI Automation tree.</span></span>

<span data-ttu-id="9d94b-123">Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Group** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Group** control type.</span></span> <span data-ttu-id="9d94b-124">Les exigences d’UI Automation s’appliquent à tous les contrôles de groupe où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="9d94b-124">The UI Automation requirements apply to all group controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9d94b-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9d94b-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9d94b-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="9d94b-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9d94b-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="9d94b-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9d94b-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="9d94b-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9d94b-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="9d94b-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9d94b-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d94b-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9d94b-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="9d94b-131">Typical Tree Structure</span></span>

<span data-ttu-id="9d94b-132">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de groupe et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="9d94b-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to group controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9d94b-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9d94b-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d94b-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="9d94b-134">Control View</span></span></th>
<th><span data-ttu-id="9d94b-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="9d94b-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9d94b-136">Group</span><span class="sxs-lookup"><span data-stu-id="9d94b-136">Group</span></span>
<ul>
<li><span data-ttu-id="9d94b-137">0 ou plusieurs contrôles</span><span class="sxs-lookup"><span data-stu-id="9d94b-137">0 or many controls</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9d94b-138">Group</span><span class="sxs-lookup"><span data-stu-id="9d94b-138">Group</span></span>
<ul>
<li><span data-ttu-id="9d94b-139">0 ou plusieurs contrôles</span><span class="sxs-lookup"><span data-stu-id="9d94b-139">0 or many controls</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9d94b-140">Les contrôles de groupe incluent généralement la prise en charge d’UI Automation pour les types de contrôle trouvés sous ceux-ci dans la sous-arborescence, y compris les types de contrôle [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md)et [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="9d94b-140">Group controls typically include UI Automation support for control types found below them in the subtree, including the [ListItem](uiauto-supportlistitemcontroltype.md), [TreeItem](uiauto-supporttreeitemcontroltype.md), and [DataItem](uiauto-supportdataitemcontroltype.md) control types.</span></span> <span data-ttu-id="9d94b-141">Étant donné qu’un contrôle de groupe est un conteneur générique, tout type de contrôle peut être sous le contrôle de groupe dans l’arborescence.</span><span class="sxs-lookup"><span data-stu-id="9d94b-141">Because a group control is a generic container, it is possible for any type of control to be under the group control in the tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="9d94b-142">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="9d94b-142">Relevant Properties</span></span>

<span data-ttu-id="9d94b-143">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de groupe.</span><span class="sxs-lookup"><span data-stu-id="9d94b-143">The following table lists the UI Automation properties whose value or definition is especially relevant to the group controls.</span></span> <span data-ttu-id="9d94b-144">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9d94b-144">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9d94b-145">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="9d94b-145">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9d94b-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d94b-146">Value</span></span>      | <span data-ttu-id="9d94b-147">Notes</span><span class="sxs-lookup"><span data-stu-id="9d94b-147">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d94b-148">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-148">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9d94b-149">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9d94b-149">See notes.</span></span> | <span data-ttu-id="9d94b-150">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9d94b-150">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="9d94b-151">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-151">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9d94b-152">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9d94b-152">See notes.</span></span> | <span data-ttu-id="9d94b-153">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9d94b-153">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="9d94b-154">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-154">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9d94b-155">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9d94b-155">See notes.</span></span> | <span data-ttu-id="9d94b-156">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="9d94b-156">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="9d94b-157">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="9d94b-157">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="9d94b-158">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-158">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9d94b-159">**Groupe**</span><span class="sxs-lookup"><span data-stu-id="9d94b-159">**Group**</span></span>  |                                                                                                                                                                                                      |
| [<span data-ttu-id="9d94b-160">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-160">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9d94b-161">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9d94b-161">**TRUE**</span></span>   | <span data-ttu-id="9d94b-162">Le contrôle de groupe est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9d94b-162">The group control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="9d94b-163">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-163">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9d94b-164">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="9d94b-164">**TRUE**</span></span>   | <span data-ttu-id="9d94b-165">Le contrôle de groupe est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9d94b-165">The group control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                  |
| [<span data-ttu-id="9d94b-166">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-166">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9d94b-167">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9d94b-167">See notes.</span></span> | <span data-ttu-id="9d94b-168">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9d94b-168">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="9d94b-169">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-169">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9d94b-170">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9d94b-170">See notes.</span></span> | <span data-ttu-id="9d94b-171">En général, les contrôles de groupe créent eux-mêmes leurs étiquettes.</span><span class="sxs-lookup"><span data-stu-id="9d94b-171">Group controls are typically self-labeling.</span></span> <span data-ttu-id="9d94b-172">Dans ce cas, retourne **null**.</span><span class="sxs-lookup"><span data-stu-id="9d94b-172">In these cases, return **NULL**.</span></span> <span data-ttu-id="9d94b-173">Si le groupe a une étiquette de texte statique, retournez l’étiquette en tant que valeur de la propriété **LabeledBy** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-173">If the group has a static text label, return the label as the value of the **LabeledBy** property.</span></span>                      |
| [<span data-ttu-id="9d94b-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9d94b-175">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9d94b-175">See notes.</span></span> | <span data-ttu-id="9d94b-176">Chaîne localisée correspondant au type de contrôle **Group** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-176">Localized string corresponding to the **Group** control type.</span></span> <span data-ttu-id="9d94b-177">La valeur par défaut est « Group » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="9d94b-177">The default value is "group" for en-US or English (United States).</span></span>                                                                     |
| [<span data-ttu-id="9d94b-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9d94b-179">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9d94b-179">See notes.</span></span> | <span data-ttu-id="9d94b-180">Le contrôle de groupe tire généralement son nom du texte qui sert d’étiquette au contrôle.</span><span class="sxs-lookup"><span data-stu-id="9d94b-180">The group control typically gets its name from the text that labels the control.</span></span>                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9d94b-181">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="9d94b-181">Required Control Patterns</span></span>

<span data-ttu-id="9d94b-182">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge pour le type de contrôle **Group** .</span><span class="sxs-lookup"><span data-stu-id="9d94b-182">The following table lists the UI Automation control patterns required to be supported for the **Group** control type.</span></span> <span data-ttu-id="9d94b-183">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9d94b-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9d94b-184">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="9d94b-184">Control Pattern</span></span>                                                   | <span data-ttu-id="9d94b-185">Support</span><span class="sxs-lookup"><span data-stu-id="9d94b-185">Support</span></span> | <span data-ttu-id="9d94b-186">Notes</span><span class="sxs-lookup"><span data-stu-id="9d94b-186">Notes</span></span>                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d94b-187">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="9d94b-187">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="9d94b-188">Dépend</span><span class="sxs-lookup"><span data-stu-id="9d94b-188">Depends</span></span> | <span data-ttu-id="9d94b-189">Les contrôles de groupe qui peuvent être utilisés pour afficher ou masquer des informations doivent prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="9d94b-189">Group controls that can be used to show or hide information must support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="9d94b-190">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="9d94b-190">Required Events</span></span>

<span data-ttu-id="9d94b-191">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de groupe.</span><span class="sxs-lookup"><span data-stu-id="9d94b-191">The following table lists the UI Automation events that group controls are required to support.</span></span> <span data-ttu-id="9d94b-192">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9d94b-192">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9d94b-193">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="9d94b-193">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="9d94b-194">Notes</span><span class="sxs-lookup"><span data-stu-id="9d94b-194">Notes</span></span>                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d94b-195">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-195">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                                  |
| <span data-ttu-id="9d94b-196">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9d94b-196">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                                  |
| <span data-ttu-id="9d94b-197">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9d94b-197">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="9d94b-198">Si le contrôle prend en charge le modèle de contrôle du modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9d94b-198">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern control pattern, it must support this event.</span></span> |
| <span data-ttu-id="9d94b-199">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9d94b-199">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="9d94b-200">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9d94b-200">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                         |
| <span data-ttu-id="9d94b-201">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9d94b-201">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="9d94b-202">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9d94b-202">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                       |
| <span data-ttu-id="9d94b-203">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9d94b-203">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="9d94b-204">Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9d94b-204">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                                 |
| [<span data-ttu-id="9d94b-205">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9d94b-205">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="9d94b-206">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9d94b-206">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9d94b-207">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9d94b-207">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9d94b-208">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="9d94b-208">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9d94b-209">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="9d94b-209">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




