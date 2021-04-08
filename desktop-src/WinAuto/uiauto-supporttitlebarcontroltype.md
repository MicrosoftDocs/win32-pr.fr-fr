---
title: TitleBar (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle TitleBar. Un contrôle de barre de titre représente un titre ou une barre de légende dans une fenêtre.
ms.assetid: dc707198-ceb6-4fbf-ace4-8fec88c92b98
keywords:
- UI Automation, prise en charge du type de contrôle TitleBar
- UI Automation, type de contrôle TitleBar
- UI Automation, arborescence pour le type de contrôle TitleBar
- UI Automation, propriétés du type de contrôle TitleBar
- UI Automation, modèles de contrôle pour le type de contrôle TitleBar
- UI Automation, événements pour le type de contrôle TitleBar
- arborescences, type de contrôle TitleBar
- Propriétés, TitleBar (type de contrôle)
- modèles de contrôle, type de contrôle TitleBar
- événements, type de contrôle TitleBar
- prise en charge du type de contrôle TitleBar
- TitleBar (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle TitleBar
- types de contrôle, modèles de contrôle pour le type de contrôle TitleBar
- types de contrôles, prise en charge de TitleBar
- types de contrôles, TitleBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9471d08479345bf8c1df118f720bf273d4d89d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940292"
---
# <a name="titlebar-control-type"></a><span data-ttu-id="aa73e-120">TitleBar (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="aa73e-120">TitleBar Control Type</span></span>

<span data-ttu-id="aa73e-121">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="aa73e-121">This topic provides information about Microsoft UI Automation support for the **TitleBar** control type.</span></span> <span data-ttu-id="aa73e-122">Un contrôle de barre de titre représente un titre ou une barre de légende dans une fenêtre.</span><span class="sxs-lookup"><span data-stu-id="aa73e-122">A title bar control represents a title or caption bar in a window.</span></span>

<span data-ttu-id="aa73e-123">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="aa73e-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **TitleBar** control type.</span></span> <span data-ttu-id="aa73e-124">Les exigences d’UI Automation s’appliquent à tous les contrôles de barre de titre dans lesquels l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="aa73e-124">The UI Automation requirements apply to all title bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="aa73e-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="aa73e-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="aa73e-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="aa73e-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="aa73e-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="aa73e-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="aa73e-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="aa73e-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="aa73e-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="aa73e-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="aa73e-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa73e-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="aa73e-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="aa73e-131">Typical Tree Structure</span></span>

<span data-ttu-id="aa73e-132">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de barre de titre et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="aa73e-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to title bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="aa73e-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="aa73e-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="aa73e-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="aa73e-134">Control View</span></span></th>
<th><span data-ttu-id="aa73e-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="aa73e-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="aa73e-136">TitleBar</span><span class="sxs-lookup"><span data-stu-id="aa73e-136">TitleBar</span></span>
<ul>
<li><span data-ttu-id="aa73e-137">Menu (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="aa73e-137">Menu (0 or 1)</span></span></li>
<li><span data-ttu-id="aa73e-138">Button (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="aa73e-138">Button (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="aa73e-139">(Non applicable ; le contrôle de barre de titre n’a pas de contenu)</span><span class="sxs-lookup"><span data-stu-id="aa73e-139">(Not applicable; the title bar control has no content)</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="aa73e-140">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="aa73e-140">Relevant Properties</span></span>

<span data-ttu-id="aa73e-141">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **TitleBar** .</span><span class="sxs-lookup"><span data-stu-id="aa73e-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the **TitleBar** control type.</span></span> <span data-ttu-id="aa73e-142">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="aa73e-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="aa73e-143">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="aa73e-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="aa73e-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="aa73e-144">Value</span></span>        | <span data-ttu-id="aa73e-145">Notes</span><span class="sxs-lookup"><span data-stu-id="aa73e-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa73e-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="aa73e-147">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="aa73e-147">See notes.</span></span>   | <span data-ttu-id="aa73e-148">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="aa73e-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="aa73e-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="aa73e-150">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="aa73e-150">See notes.</span></span>   | <span data-ttu-id="aa73e-151">La valeur exposée par cette propriété doit inclure tous les contrôles qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="aa73e-151">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                             |
| [<span data-ttu-id="aa73e-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="aa73e-153">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="aa73e-153">See notes.</span></span>   | <span data-ttu-id="aa73e-154">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="aa73e-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="aa73e-155">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="aa73e-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="aa73e-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="aa73e-157">**Spreadsheet**</span><span class="sxs-lookup"><span data-stu-id="aa73e-157">**TitleBar**</span></span> | <span data-ttu-id="aa73e-158">Cette valeur est identique pour toutes les infrastructures d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="aa73e-158">This value is the same for all UI frameworks.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="aa73e-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="aa73e-160">FALSE</span><span class="sxs-lookup"><span data-stu-id="aa73e-160">FALSE</span></span>        | <span data-ttu-id="aa73e-161">Le contrôle de barre de titre n’est jamais inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="aa73e-161">The title bar control is never included in the content view of the UI Automation tree.</span></span>                                                                                                               |
| [<span data-ttu-id="aa73e-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="aa73e-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="aa73e-163">TRUE</span></span>         | <span data-ttu-id="aa73e-164">Le contrôle de barre de titre est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="aa73e-164">The title bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                              |
| [<span data-ttu-id="aa73e-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="aa73e-166">FALSE</span><span class="sxs-lookup"><span data-stu-id="aa73e-166">FALSE</span></span>        | <span data-ttu-id="aa73e-167">Un contrôle de barre de titre n’a jamais le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="aa73e-167">A title bar control never has keyboard focus.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="aa73e-168">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-168">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="aa73e-169">Dépend</span><span class="sxs-lookup"><span data-stu-id="aa73e-169">Depends</span></span>      | <span data-ttu-id="aa73e-170">Un contrôle de barre de titre retourne une valeur selon qu’elle est visible à l’écran.</span><span class="sxs-lookup"><span data-stu-id="aa73e-170">A title bar control returns a value depending on whether it is visible on the screen.</span></span>                                                                                                                |
| [<span data-ttu-id="aa73e-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="aa73e-172">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="aa73e-172">See notes.</span></span>   | <span data-ttu-id="aa73e-173">Un contrôle de barre de titre n’a généralement pas d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="aa73e-173">A title bar control typically does not have a label.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="aa73e-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="aa73e-175">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="aa73e-175">See notes.</span></span>   | <span data-ttu-id="aa73e-176">Chaîne localisée correspondant au type de contrôle TitleBar.</span><span class="sxs-lookup"><span data-stu-id="aa73e-176">Localized string corresponding to the TitleBar control type.</span></span> <span data-ttu-id="aa73e-177">La valeur par défaut est « barre de titre » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="aa73e-177">The default value is "title bar" for en-US or English (United States).</span></span>                                                                  |
| [<span data-ttu-id="aa73e-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="aa73e-179">""</span><span class="sxs-lookup"><span data-stu-id="aa73e-179">""</span></span>           | <span data-ttu-id="aa73e-180">La barre de titre ne comporte pas de contenu ; ses informations textuelles sont exposées par le nom de la fenêtre parente.</span><span class="sxs-lookup"><span data-stu-id="aa73e-180">A title bar is not content; its textual information is exposed by the name of the parent window.</span></span>                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="aa73e-181">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="aa73e-181">Required Control Patterns</span></span>

<span data-ttu-id="aa73e-182">Le type de contrôle **TitleBar** n’est pas requis pour prendre en charge les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="aa73e-182">The **TitleBar** control type is not required to support any control patterns.</span></span> <span data-ttu-id="aa73e-183">Ses fonctionnalités sont exposées via le modèle de contrôle [Window](uiauto-implementingwindow.md) sur le type de contrôle [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="aa73e-183">Its functionality is exposed through the [Window](uiauto-implementingwindow.md) control pattern on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="aa73e-184">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="aa73e-184">Required Events</span></span>

<span data-ttu-id="aa73e-185">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de barre de titre.</span><span class="sxs-lookup"><span data-stu-id="aa73e-185">The following table lists the UI Automation events that title bar controls are required to support.</span></span> <span data-ttu-id="aa73e-186">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="aa73e-186">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="aa73e-187">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="aa73e-187">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="aa73e-188">Notes</span><span class="sxs-lookup"><span data-stu-id="aa73e-188">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="aa73e-189">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-189">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="aa73e-190">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="aa73e-190">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="aa73e-191">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="aa73e-191">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="aa73e-192">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="aa73e-192">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="aa73e-193">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="aa73e-193">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="aa73e-194">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="aa73e-194">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="aa73e-195">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="aa73e-195">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="aa73e-196">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="aa73e-196">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="aa73e-197">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="aa73e-197">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="aa73e-198">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="aa73e-198">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="aa73e-199">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="aa73e-199">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




