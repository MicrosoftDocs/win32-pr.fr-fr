---
title: Header (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle header.
ms.assetid: 032fc3a1-f939-40db-abbb-532afe309ba3
keywords:
- UI Automation, prise en charge du type de contrôle header
- UI Automation, type de contrôle header
- UI Automation, arborescence pour le type de contrôle header
- UI Automation, propriétés du type de contrôle header
- UI Automation, modèles de contrôle pour le type de contrôle header
- UI Automation, événements pour le type de contrôle header
- arborescences, type de contrôle header
- Propriétés, type de contrôle header
- modèles de contrôle, type de contrôle header
- événements, type de contrôle header
- prise en charge du type de contrôle header
- Header (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle header
- types de contrôle, modèles de contrôle pour le type de contrôle header
- types de contrôles, prise en charge de l’en-tête
- types de contrôles, en-tête
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c38ee0a00749888c624b627db247f2d01d24ff1c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379877"
---
# <a name="header-control-type"></a><span data-ttu-id="5266e-119">Header (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="5266e-119">Header Control Type</span></span>

<span data-ttu-id="5266e-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **header** .</span><span class="sxs-lookup"><span data-stu-id="5266e-120">This topic provides information about Microsoft UI Automation support for the **Header** control type.</span></span>

<span data-ttu-id="5266e-121">Le contrôle header fournit un conteneur visuel pour les étiquettes des lignes ou colonnes d’informations.</span><span class="sxs-lookup"><span data-stu-id="5266e-121">The header control provides a visual container for the labels for rows or columns of information.</span></span>

<span data-ttu-id="5266e-122">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **header** .</span><span class="sxs-lookup"><span data-stu-id="5266e-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Header** control type.</span></span> <span data-ttu-id="5266e-123">Les exigences d’UI Automation s’appliquent à tous les contrôles Header où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="5266e-123">The UI Automation requirements apply to all header controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="5266e-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="5266e-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="5266e-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="5266e-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="5266e-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="5266e-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="5266e-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="5266e-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="5266e-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="5266e-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="5266e-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5266e-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="5266e-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="5266e-130">Typical Tree Structure</span></span>

<span data-ttu-id="5266e-131">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles Header et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="5266e-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to header controls and describes what can be contained in each view.</span></span> <span data-ttu-id="5266e-132">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5266e-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5266e-133">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="5266e-133">Control View</span></span></th>
<th><span data-ttu-id="5266e-134">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="5266e-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="5266e-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="5266e-135">Header</span></span>
<ul>
<li><span data-ttu-id="5266e-136">HeaderItem (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="5266e-136">HeaderItem (1 or more)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="5266e-137">(Non applicable)</span><span class="sxs-lookup"><span data-stu-id="5266e-137">(Not applicable)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5266e-138">Les contrôles Header ont toujours un ou plusieurs enfants dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5266e-138">Header controls always have one or more children in the control view of the UI Automation tree.</span></span>

<span data-ttu-id="5266e-139">Les contrôles Header n’ont aucun enfant dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5266e-139">Header controls have zero children in the content view of the UI Automation tree.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="5266e-140">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="5266e-140">Relevant Properties</span></span>

<span data-ttu-id="5266e-141">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Header.</span><span class="sxs-lookup"><span data-stu-id="5266e-141">The following table lists the UI Automation properties whose value or definition is especially relevant to header controls.</span></span> <span data-ttu-id="5266e-142">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="5266e-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="5266e-143">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="5266e-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="5266e-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="5266e-144">Value</span></span>                                                            | <span data-ttu-id="5266e-145">Notes</span><span class="sxs-lookup"><span data-stu-id="5266e-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5266e-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="5266e-147">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5266e-147">See notes.</span></span>                                                       | <span data-ttu-id="5266e-148">La valeur de cette propriété doit être unique pour tous les contrôles d’une application.</span><span class="sxs-lookup"><span data-stu-id="5266e-148">The value of this property must be unique across all controls in an application.</span></span>                                                                                                                     |
| [<span data-ttu-id="5266e-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="5266e-150">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5266e-150">See notes.</span></span>                                                       | <span data-ttu-id="5266e-151">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="5266e-151">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="5266e-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="5266e-153">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5266e-153">See notes.</span></span>                                                       | <span data-ttu-id="5266e-154">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="5266e-154">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="5266e-155">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="5266e-155">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="5266e-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5266e-157">**En-tête**</span><span class="sxs-lookup"><span data-stu-id="5266e-157">**Header**</span></span>                                                       |                                                                                                                                                                                                      |
| [<span data-ttu-id="5266e-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5266e-159">FALSE</span><span class="sxs-lookup"><span data-stu-id="5266e-159">FALSE</span></span>                                                            | <span data-ttu-id="5266e-160">Le contrôle header n’est pas inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5266e-160">The header control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                    |
| [<span data-ttu-id="5266e-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="5266e-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="5266e-162">TRUE</span></span>                                                             | <span data-ttu-id="5266e-163">Le contrôle header est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="5266e-163">The header control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                 |
| [<span data-ttu-id="5266e-164">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-164">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="5266e-165">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5266e-165">See notes.</span></span>                                                       | <span data-ttu-id="5266e-166">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="5266e-166">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="5266e-167">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-167">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="5266e-168">NULL</span><span class="sxs-lookup"><span data-stu-id="5266e-168">NULL</span></span>                                                             | <span data-ttu-id="5266e-169">Les contrôles header n’ont pas d’étiquette statique.</span><span class="sxs-lookup"><span data-stu-id="5266e-169">Header controls do not have a static label.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="5266e-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="5266e-171">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5266e-171">See notes.</span></span>                                                       | <span data-ttu-id="5266e-172">La valeur par défaut est « Header » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="5266e-172">The default value is "header" for en-US or English (United States).</span></span>                                                                                                                                  |
| [<span data-ttu-id="5266e-173">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-173">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="5266e-174">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="5266e-174">See notes.</span></span>                                                       | <span data-ttu-id="5266e-175">Le contrôle header a besoin d’un nom s’il existe plusieurs en-têtes de lignes ou plusieurs en-têtes de colonnes.</span><span class="sxs-lookup"><span data-stu-id="5266e-175">The header control needs a name if there is more than one row header or more than one column header.</span></span> <span data-ttu-id="5266e-176">Cela identifie les informations présentes dans l’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5266e-176">This identifies the information within the header.</span></span>                                              |
| [<span data-ttu-id="5266e-177">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="5266e-177">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="5266e-178">**OrientationType \_** **\_ Vertical** ou horizontal OrientationType</span><span class="sxs-lookup"><span data-stu-id="5266e-178">**OrientationType\_Horizontal** or **OrientationType\_Vertical**</span></span> | <span data-ttu-id="5266e-179">La valeur de cette propriété expose la position du contrôle header, qu’il s’agisse d’un en-tête de ligne (**OrientationType \_ horizontal**) ou d’un en-tête de colonne (**OrientationType \_ vertical**).</span><span class="sxs-lookup"><span data-stu-id="5266e-179">The value of this property exposes the position of the header control—whether it is a row header (**OrientationType\_Horizontal**) or column header (**OrientationType\_Vertical**).</span></span>                 |



 

## <a name="required-control-patterns"></a><span data-ttu-id="5266e-180">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="5266e-180">Required Control Patterns</span></span>

<span data-ttu-id="5266e-181">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge pour les contrôles Header.</span><span class="sxs-lookup"><span data-stu-id="5266e-181">The following table lists the UI Automation control patterns required to be supported for header controls.</span></span> <span data-ttu-id="5266e-182">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5266e-182">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="5266e-183">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="5266e-183">Control Pattern</span></span>                                         | <span data-ttu-id="5266e-184">Support</span><span class="sxs-lookup"><span data-stu-id="5266e-184">Support</span></span> | <span data-ttu-id="5266e-185">Notes</span><span class="sxs-lookup"><span data-stu-id="5266e-185">Notes</span></span>                                                                                                             |
|---------------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5266e-186">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="5266e-186">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="5266e-187">Dépend</span><span class="sxs-lookup"><span data-stu-id="5266e-187">Depends</span></span> | <span data-ttu-id="5266e-188">Implémentez le modèle de contrôle [Transform](uiauto-implementingtransform.md) si le contrôle header peut être redimensionné.</span><span class="sxs-lookup"><span data-stu-id="5266e-188">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the header control can be resized.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="5266e-189">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="5266e-189">Required Events</span></span>

<span data-ttu-id="5266e-190">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles d’en-tête.</span><span class="sxs-lookup"><span data-stu-id="5266e-190">The following table lists the UI Automation events that header controls are required to support.</span></span> <span data-ttu-id="5266e-191">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="5266e-191">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="5266e-192">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="5266e-192">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="5266e-193">Notes</span><span class="sxs-lookup"><span data-stu-id="5266e-193">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5266e-194">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5266e-194">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="5266e-195">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="5266e-195">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="5266e-196">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="5266e-196">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="5266e-197">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="5266e-197">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="5266e-198">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="5266e-198">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="5266e-199">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="5266e-199">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="5266e-200">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="5266e-200">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="5266e-201">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5266e-201">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5266e-202">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="5266e-202">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="5266e-203">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="5266e-203">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="5266e-204">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="5266e-204">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




