---
title: Slider (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Slider.
ms.assetid: dc7bef7a-b68c-4184-a9e7-745bb41b592e
keywords:
- UI Automation, prise en charge du type de contrôle Slider
- UI Automation, type de contrôle Slider
- UI Automation, arborescence pour le type de contrôle Slider
- UI Automation, propriétés pour le type de contrôle Slider
- UI Automation, modèles de contrôle pour le type de contrôle Slider
- UI Automation, événements pour le type de contrôle Slider
- arborescences, type de contrôle Slider
- Propriétés, type de contrôle Slider
- modèles de contrôle, curseur, type de contrôle
- événements, type de contrôle Slider
- prise en charge du type de contrôle Slider
- Slider (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Slider
- types de contrôles, modèles de contrôle pour le type de contrôle Slider
- types de contrôles, prise en charge du curseur
- types de contrôles, Slider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be8e82dfc8f011363086745368ed1693c45a6aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940093"
---
# <a name="slider-control-type"></a><span data-ttu-id="f4389-119">Slider (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="f4389-119">Slider Control Type</span></span>

<span data-ttu-id="f4389-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Slider** .</span><span class="sxs-lookup"><span data-stu-id="f4389-120">This topic provides information about Microsoft UI Automation support for the **Slider** control type.</span></span>

<span data-ttu-id="f4389-121">Un contrôle Slider est un contrôle composite avec des boutons qui permettent à un utilisateur de définir une plage numérique ou de sélectionner un ensemble d’éléments.</span><span class="sxs-lookup"><span data-stu-id="f4389-121">A slider control is a composite control with buttons that enable a user to set a numerical range or select from a set of items.</span></span>

<span data-ttu-id="f4389-122">Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Slider** .</span><span class="sxs-lookup"><span data-stu-id="f4389-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Slider** control type.</span></span> <span data-ttu-id="f4389-123">Les exigences d’UI Automation s’appliquent à tous les contrôles Slider où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="f4389-123">The UI Automation requirements apply to all slider controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="f4389-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="f4389-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f4389-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="f4389-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="f4389-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="f4389-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="f4389-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="f4389-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="f4389-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="f4389-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="f4389-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4389-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="f4389-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="f4389-130">Typical Tree Structure</span></span>

<span data-ttu-id="f4389-131">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles Slider et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="f4389-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to slider controls and describes what can be contained in each view.</span></span> <span data-ttu-id="f4389-132">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f4389-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f4389-133">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="f4389-133">Control View</span></span></th>
<th><span data-ttu-id="f4389-134">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="f4389-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="f4389-135">Curseur</span><span class="sxs-lookup"><span data-stu-id="f4389-135">Slider</span></span>
<ul>
<li><span data-ttu-id="f4389-136">Bouton (2 ou 4)</span><span class="sxs-lookup"><span data-stu-id="f4389-136">Button (2 or 4)</span></span></li>
<li><span data-ttu-id="f4389-137">Thumb (1)</span><span class="sxs-lookup"><span data-stu-id="f4389-137">Thumb (1)</span></span></li>
<li><span data-ttu-id="f4389-138">Élément de liste (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="f4389-138">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="f4389-139">Curseur</span><span class="sxs-lookup"><span data-stu-id="f4389-139">Slider</span></span>
<ul>
<li><span data-ttu-id="f4389-140">Élément de liste (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="f4389-140">List Item (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="f4389-141">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="f4389-141">Relevant Properties</span></span>

<span data-ttu-id="f4389-142">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles Slider.</span><span class="sxs-lookup"><span data-stu-id="f4389-142">The following table lists the UI Automation properties whose value or definition is especially relevant to slider controls.</span></span> <span data-ttu-id="f4389-143">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="f4389-143">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="f4389-144">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="f4389-144">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="f4389-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4389-145">Value</span></span>      | <span data-ttu-id="f4389-146">Notes</span><span class="sxs-lookup"><span data-stu-id="f4389-146">Notes</span></span>                                                                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4389-147">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-147">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="f4389-148">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="f4389-148">See notes.</span></span> | <span data-ttu-id="f4389-149">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="f4389-149">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                   |
| [<span data-ttu-id="f4389-150">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-150">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="f4389-151">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="f4389-151">See notes.</span></span> | <span data-ttu-id="f4389-152">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="f4389-152">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="f4389-153">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-153">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="f4389-154">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="f4389-154">See notes.</span></span> | <span data-ttu-id="f4389-155">La majorité des contrôles Slider doivent retourner l’erreur [**UIA \_ E \_ NOCLICKABLEPOINT**](uiauto-error-codes.md) , car l’intégralité du rectangle englobant du contrôle Slider est occupée par les contrôles enfants.</span><span class="sxs-lookup"><span data-stu-id="f4389-155">The majority of slider controls must return the [**UIA\_E\_NOCLICKABLEPOINT**](uiauto-error-codes.md) error because the entire bounding rectangle of the slider control is occupied by child controls.</span></span> |
| [<span data-ttu-id="f4389-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="f4389-157">**Curseur**</span><span class="sxs-lookup"><span data-stu-id="f4389-157">**Slider**</span></span> | <span data-ttu-id="f4389-158">Cette valeur est la même pour toutes les infrastructures.</span><span class="sxs-lookup"><span data-stu-id="f4389-158">This value is the same for all frameworks.</span></span>                                                                                                                                                                                     |
| [<span data-ttu-id="f4389-159">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-159">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f4389-160">TRUE</span><span class="sxs-lookup"><span data-stu-id="f4389-160">TRUE</span></span>       | <span data-ttu-id="f4389-161">Le contrôle Slider est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="f4389-161">The slider control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="f4389-162">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-162">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="f4389-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="f4389-163">TRUE</span></span>       | <span data-ttu-id="f4389-164">Le contrôle Slider est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="f4389-164">The slider control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="f4389-165">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-165">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="f4389-166">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="f4389-166">See notes.</span></span> | <span data-ttu-id="f4389-167">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="f4389-167">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="f4389-168">Les enfants (boutons et Thumb) d’un contrôle Slider ne doivent jamais prendre le focus.</span><span class="sxs-lookup"><span data-stu-id="f4389-168">The children (buttons and thumb) of a slider control should never take the focus.</span></span> <span data-ttu-id="f4389-169">Le focus doit toujours rester sur le contrôle Slider lui-même.</span><span class="sxs-lookup"><span data-stu-id="f4389-169">The focus should always remain on the slider control itself.</span></span>       |
| [<span data-ttu-id="f4389-170">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-170">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="f4389-171">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="f4389-171">See notes.</span></span> | <span data-ttu-id="f4389-172">Si une étiquette de texte statique est associée au contrôle, cette propriété doit exposer une référence à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="f4389-172">If there is a static text label associated with the control, this property must expose a reference to that control.</span></span> <span data-ttu-id="f4389-173">Si le contrôle de texte est un sous-composant d’un autre contrôle, il n’aura pas de propriété **LabeledBy** définie.</span><span class="sxs-lookup"><span data-stu-id="f4389-173">If the text control is a subcomponent of another control, it will not have a **LabeledBy** property set.</span></span>   |
| [<span data-ttu-id="f4389-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="f4389-175">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="f4389-175">See notes.</span></span> | <span data-ttu-id="f4389-176">Chaîne localisée correspondant au type de contrôle **Slider** .</span><span class="sxs-lookup"><span data-stu-id="f4389-176">Localized string corresponding to the **Slider** control type.</span></span> <span data-ttu-id="f4389-177">La valeur par défaut est « Slider » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="f4389-177">The default value is "slider" for en-US or English (United States).</span></span>                                                                                             |
| [<span data-ttu-id="f4389-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="f4389-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="f4389-179">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="f4389-179">See notes.</span></span> | <span data-ttu-id="f4389-180">Le nom du contrôle Slider est généralement généré à partir d’une étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="f4389-180">The name of the slider control is typically generated from a static text label.</span></span> <span data-ttu-id="f4389-181">S’il n’y a pas d’étiquette de texte statique, une valeur de propriété pour le **nom** doit être affectée par le développeur de l’application.</span><span class="sxs-lookup"><span data-stu-id="f4389-181">If there is not a static text label, a property value for **Name** must be assigned by the application developer.</span></span>                              |



 

## <a name="required-control-patterns"></a><span data-ttu-id="f4389-182">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="f4389-182">Required Control Patterns</span></span>

<span data-ttu-id="f4389-183">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles Slider.</span><span class="sxs-lookup"><span data-stu-id="f4389-183">The following table lists the UI Automation control patterns required to be supported by all slider controls.</span></span> <span data-ttu-id="f4389-184">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f4389-184">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="f4389-185">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="f4389-185">Control Pattern/Pattern Property</span></span>                          | <span data-ttu-id="f4389-186">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="f4389-186">Support/Value</span></span> | <span data-ttu-id="f4389-187">Notes</span><span class="sxs-lookup"><span data-stu-id="f4389-187">Notes</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4389-188">**IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="f4389-188">**IRangeValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) | <span data-ttu-id="f4389-189">Dépend</span><span class="sxs-lookup"><span data-stu-id="f4389-189">Depends</span></span>       | <span data-ttu-id="f4389-190">Un curseur doit prendre en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) si le contenu peut être défini sur une valeur comprise dans une plage numérique.</span><span class="sxs-lookup"><span data-stu-id="f4389-190">A slider should support the [RangeValue](uiauto-implementingrangevalue.md) control pattern if the content can be set to a value within a numerical range.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="f4389-191">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="f4389-191">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider)   | <span data-ttu-id="f4389-192">Dépend</span><span class="sxs-lookup"><span data-stu-id="f4389-192">Depends</span></span>       | <span data-ttu-id="f4389-193">Un curseur doit prendre en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) si le contenu représente une valeur parmi un ensemble discret d’options.</span><span class="sxs-lookup"><span data-stu-id="f4389-193">A slider should support the [Selection](uiauto-implementingselection.md) control pattern if the content represents one value among a discrete set of options.</span></span> <span data-ttu-id="f4389-194">Quand le modèle de contrôle Selection est pris en charge, la sélection correspondante doit être exposée sous la forme d’un ou plusieurs éléments de liste enfants du curseur.</span><span class="sxs-lookup"><span data-stu-id="f4389-194">When the Selection control pattern is supported, the corresponding selection must be exposed as one or more child list items of the slider.</span></span> |
| [<span data-ttu-id="f4389-195">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="f4389-195">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)           | <span data-ttu-id="f4389-196">Dépend</span><span class="sxs-lookup"><span data-stu-id="f4389-196">Depends</span></span>       | <span data-ttu-id="f4389-197">Un curseur doit prendre en charge le modèle de contrôle [value](uiauto-implementingvalue.md) si le contenu représente une valeur parmi un ensemble discret d’options.</span><span class="sxs-lookup"><span data-stu-id="f4389-197">A slider should support the [Value](uiauto-implementingvalue.md) control pattern if the content represents one value among a discrete set of options.</span></span>                                                                                                                                                     |



 

## <a name="required-events"></a><span data-ttu-id="f4389-198">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="f4389-198">Required Events</span></span>

<span data-ttu-id="f4389-199">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles Slider.</span><span class="sxs-lookup"><span data-stu-id="f4389-199">The following table lists the UI Automation events that slider controls are required to support.</span></span> <span data-ttu-id="f4389-200">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="f4389-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="f4389-201">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="f4389-201">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="f4389-202">Notes</span><span class="sxs-lookup"><span data-stu-id="f4389-202">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f4389-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f4389-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="f4389-204">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f4389-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="f4389-205">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f4389-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="f4389-206">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="f4389-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="f4389-207">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="f4389-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="f4389-208">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="f4389-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="f4389-209">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété RangeValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f4389-209">[**UIA\_RangeValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>        | <span data-ttu-id="f4389-210">Si le contrôle prend en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="f4389-210">If the control supports the [RangeValue](uiauto-implementingrangevalue.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="f4389-211">**\_InvalidatedEventId de sélection UIA \_**</span><span class="sxs-lookup"><span data-stu-id="f4389-211">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                       | <span data-ttu-id="f4389-212">Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="f4389-212">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="f4389-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="f4389-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="f4389-214">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="f4389-214">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                  | <span data-ttu-id="f4389-215">Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="f4389-215">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="f4389-216">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f4389-216">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="f4389-217">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="f4389-217">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="f4389-218">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="f4389-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="f4389-219">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="f4389-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




