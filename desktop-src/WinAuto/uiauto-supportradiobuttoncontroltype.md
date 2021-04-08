---
title: RadioButton (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle RadioButton.
ms.assetid: 6fc4a6a3-f5c0-402b-b9e7-870dfaa3370d
keywords:
- UI Automation, prise en charge du type de contrôle RadioButton
- UI Automation, type de contrôle RadioButton
- UI Automation, arborescence pour le type de contrôle RadioButton
- UI Automation, propriétés du type de contrôle RadioButton
- UI Automation, modèles de contrôle pour le type de contrôle RadioButton
- UI Automation, événements pour le type de contrôle RadioButton
- arborescences, type de contrôle RadioButton
- Propriétés, RadioButton (type de contrôle)
- modèles de contrôle, RadioButton (type de contrôle)
- événements, type de contrôle RadioButton
- prise en charge du type de contrôle RadioButton
- RadioButton (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle RadioButton
- types de contrôle, modèles de contrôle pour le type de contrôle RadioButton
- types de contrôles, prise en charge de RadioButton
- types de contrôles, RadioButton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702a2227a5164ff694378c82fa3b7cde33f9823
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674669"
---
# <a name="radiobutton-control-type"></a><span data-ttu-id="9fa9c-119">RadioButton (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="9fa9c-119">RadioButton Control Type</span></span>

<span data-ttu-id="9fa9c-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="9fa9c-120">This topic provides information about Microsoft UI Automation support for the **RadioButton** control type.</span></span>

<span data-ttu-id="9fa9c-121">Une case d’option se compose d’un bouton rond et d’un texte défini par l’application (étiquette), d’une icône ou d’une image bitmap qui indique un choix que l’utilisateur peut faire en sélectionnant le bouton.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-121">A radio button consists of a round button and application-defined text (a label), an icon, or a bitmap that indicates a choice the user can make by selecting the button.</span></span> <span data-ttu-id="9fa9c-122">Une application utilise généralement des cases d’option dans une zone de groupe pour permettre à l’utilisateur de choisir parmi un ensemble d’options connexes mais s’excluant mutuellement.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-122">An application typically uses radio buttons in a group box to permit the user to choose from a set of related, but mutually exclusive options.</span></span> <span data-ttu-id="9fa9c-123">Par exemple, l’application peut présenter un groupe de cases d’option parmi lesquelles l’utilisateur peut sélectionner une préférence de format pour le texte sélectionné dans la zone cliente.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-123">For example, the application might present a group of radio buttons from which the user can select a format preference for text selected in the client area.</span></span> <span data-ttu-id="9fa9c-124">L’utilisateur peut sélectionner un format aligné à gauche, aligné à droite ou centré en cochant la case d’option correspondante.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-124">The user could select a left-aligned, right-aligned, or centered format by selecting the corresponding radio button.</span></span> <span data-ttu-id="9fa9c-125">En règle générale, l’utilisateur peut sélectionner une seule option à la fois parmi un ensemble de cases d’option.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-125">Typically, the user can select only one option at a time from a set of radio buttons.</span></span>

> [!Note]  
> <span data-ttu-id="9fa9c-126">Une autre généralisation de contrôle pour les boutons dans lesquels une seule partie d’un groupe peut être sélectionnée est le contenu d’un bouton bascule.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-126">Another control generalization for buttons where only one in a group can be selected is the content of a toggle button.</span></span> <span data-ttu-id="9fa9c-127">Certaines infrastructures d’interface utilisateur considèrent qu’une case d’option est un bouton bascule spécialisé.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-127">Some UI frameworks consider a radio button to be a specialized toggle button.</span></span>

 

<span data-ttu-id="9fa9c-128">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="9fa9c-128">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **RadioButton** control type.</span></span> <span data-ttu-id="9fa9c-129">Les spécifications d’UI Automation s’appliquent à tous les contrôles de bouton où l’infrastructure d’interface utilisateur/plateforme intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-129">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="9fa9c-130">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-130">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="9fa9c-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="9fa9c-131">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="9fa9c-132">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-132">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="9fa9c-133">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="9fa9c-133">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="9fa9c-134">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="9fa9c-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="9fa9c-135">Remarques</span><span class="sxs-lookup"><span data-stu-id="9fa9c-135">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="9fa9c-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="9fa9c-137">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="9fa9c-137">Typical Tree Structure</span></span>

<span data-ttu-id="9fa9c-138">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de case d’option et décrit ce que peut contenir chaque vue.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to radio button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="9fa9c-139">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9c-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9fa9c-140">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="9fa9c-140">Control View</span></span></th>
<th><span data-ttu-id="9fa9c-141">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="9fa9c-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="9fa9c-142">RadioButton</span><span class="sxs-lookup"><span data-stu-id="9fa9c-142">RadioButton</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="9fa9c-143">RadioButton</span><span class="sxs-lookup"><span data-stu-id="9fa9c-143">RadioButton</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="9fa9c-144">Aucun enfant ne figure dans la vue de contrôle ni dans la vue de contenu.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-144">There are no children in the control view or the content view.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="9fa9c-145">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-145">Relevant Properties</span></span>

<span data-ttu-id="9fa9c-146">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **RadioButton** (tels que les contrôles Button).</span><span class="sxs-lookup"><span data-stu-id="9fa9c-146">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **RadioButton** control type (such as button controls).</span></span> <span data-ttu-id="9fa9c-147">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9c-147">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="9fa9c-148">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="9fa9c-148">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="9fa9c-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fa9c-149">Value</span></span>           | <span data-ttu-id="9fa9c-150">Notes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-150">Notes</span></span>                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fa9c-151">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-151">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="9fa9c-152">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-152">See notes.</span></span>      | <span data-ttu-id="9fa9c-153">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-153">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                  |
| [<span data-ttu-id="9fa9c-154">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-154">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="9fa9c-155">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-155">See notes.</span></span>      | <span data-ttu-id="9fa9c-156">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-156">The outermost rectangle that contains the whole control.</span></span>                                                                                      |
| [<span data-ttu-id="9fa9c-157">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-157">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="9fa9c-158">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-158">See notes.</span></span>      | <span data-ttu-id="9fa9c-159">Le point cliquable doit être un point qui, lorsque vous cliquez dessus, sélectionne la case d’option.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-159">The clickable point must be a point that, when clicked, selects the radio button.</span></span>                                                             |
| [<span data-ttu-id="9fa9c-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="9fa9c-161">**RadioButton**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-161">**RadioButton**</span></span> |                                                                                                                                               |
| [<span data-ttu-id="9fa9c-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9fa9c-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="9fa9c-163">TRUE</span></span>            | <span data-ttu-id="9fa9c-164">Le contrôle de case d’option est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-164">The radio button control is always included in the content view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="9fa9c-165">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-165">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="9fa9c-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="9fa9c-166">TRUE</span></span>            | <span data-ttu-id="9fa9c-167">Le contrôle de case d’option est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-167">The radio button control is always included in the control view of the UI Automation tree.</span></span>                                                    |
| [<span data-ttu-id="9fa9c-168">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-168">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="9fa9c-169">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-169">See notes.</span></span>      | <span data-ttu-id="9fa9c-170">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-170">If the control can receive keyboard focus, it must support this property.</span></span>                                                                     |
| [<span data-ttu-id="9fa9c-171">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-171">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="9fa9c-172">NULL</span><span class="sxs-lookup"><span data-stu-id="9fa9c-172">NULL</span></span>            | <span data-ttu-id="9fa9c-173">Les contrôles de cases d’option sont étiquetés automatiquement par leur contenu.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-173">Radio button controls are self-labeled by their contents.</span></span>                                                                                     |
| [<span data-ttu-id="9fa9c-174">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-174">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="9fa9c-175">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-175">See notes.</span></span>      | <span data-ttu-id="9fa9c-176">Chaîne localisée correspondant au type de contrôle **RadioButton** .</span><span class="sxs-lookup"><span data-stu-id="9fa9c-176">Localized string corresponding to the **RadioButton** control type.</span></span> <span data-ttu-id="9fa9c-177">La valeur par défaut est « case d’option » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="9fa9c-177">The default value is "radio button" for en-US or English (United States).</span></span> |
| [<span data-ttu-id="9fa9c-178">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-178">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="9fa9c-179">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-179">See notes.</span></span>      | <span data-ttu-id="9fa9c-180">Le nom du contrôle de case d’option est le texte qui s’affiche en regard du bouton qui maintient l’état de sélection.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-180">The name of the radio button control is the text that is displayed beside the button that maintains the selection state.</span></span>                      |



 

## <a name="required-control-patterns"></a><span data-ttu-id="9fa9c-181">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="9fa9c-181">Required Control Patterns</span></span>

<span data-ttu-id="9fa9c-182">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de case d’option.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-182">The following table lists the UI Automation control patterns required to be supported by all radio button controls.</span></span> <span data-ttu-id="9fa9c-183">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9c-183">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="9fa9c-184">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="9fa9c-184">Control Pattern/Pattern Property</span></span>                                               | <span data-ttu-id="9fa9c-185">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="9fa9c-185">Support/Value</span></span> | <span data-ttu-id="9fa9c-186">Notes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-186">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------|---------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fa9c-187">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-187">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)                | <span data-ttu-id="9fa9c-188">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="9fa9c-188">Required</span></span>      | <span data-ttu-id="9fa9c-189">Tous les contrôles de case d’option doivent prendre en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) pour pouvoir être sélectionnés.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-189">All radio button controls must support the [SelectionItem](uiauto-implementingselectionitem.md) control pattern to enable themselves to be selected.</span></span>                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="9fa9c-190">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-190">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) | <span data-ttu-id="9fa9c-191">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-191">See notes.</span></span>    | <span data-ttu-id="9fa9c-192">La propriété [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) doit toujours être terminée afin qu’un client UI Automation puisse déterminer quelles autres cases d’option dans un contexte spécifique sont liées les unes aux autres.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-192">The [**SelectionContainer**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer) property must always be completed so that a UI Automation client can determine what other radio buttons within a specific context relate to one another.</span></span> <span data-ttu-id="9fa9c-193">Pour la version Microsoft Win32 de la case d’option, cette propriété n’est pas prise en charge, car il n’est pas possible d’obtenir ces informations à partir de cette infrastructure héritée.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-193">For the Microsoft Win32 version of the radio button, this property is not supported because it is not possible to obtain this information from that legacy framework.</span></span> |
| [<span data-ttu-id="9fa9c-194">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-194">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                              | <span data-ttu-id="9fa9c-195">Jamais</span><span class="sxs-lookup"><span data-stu-id="9fa9c-195">Never</span></span>         | <span data-ttu-id="9fa9c-196">La case d’option ne peut pas passer d’un état à un autre une fois qu’elle a été définie.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-196">The radio button cannot cycle through its state once it has been set.</span></span> <span data-ttu-id="9fa9c-197">Le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) ne doit jamais être pris en charge sur une case d’option.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-197">The [Toggle](uiauto-implementingtoggle.md) control pattern must never be supported on a radio button.</span></span>                                                                                                                                                                                                                                      |



 

## <a name="required-events"></a><span data-ttu-id="9fa9c-198">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="9fa9c-198">Required Events</span></span>

<span data-ttu-id="9fa9c-199">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de bouton.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-199">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="9fa9c-200">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="9fa9c-200">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="9fa9c-201">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="9fa9c-201">UI Automation Event</span></span>                                                                                                                     | <span data-ttu-id="9fa9c-202">Notes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-202">Notes</span></span>                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9fa9c-203">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-203">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                        |                                                                                                                                |
| <span data-ttu-id="9fa9c-204">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-204">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>   |                                                                                                                                |
| <span data-ttu-id="9fa9c-205">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-205">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                   | <span data-ttu-id="9fa9c-206">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-206">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="9fa9c-207">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-207">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>               | <span data-ttu-id="9fa9c-208">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-208">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>     |
| [<span data-ttu-id="9fa9c-209">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-209">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="9fa9c-210">Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-210">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="9fa9c-211">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-211">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="9fa9c-212">Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-212">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="9fa9c-213">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-213">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="9fa9c-214">Notes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-214">Remarks</span></span>

<span data-ttu-id="9fa9c-215">Une case d’option représente une option sélectionnable unique parmi un groupe de cases d’option homologues.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-215">A radio button represents a single selectable option among a group of peer radio buttons.</span></span> <span data-ttu-id="9fa9c-216">Dans l’idéal, les cases d’option doivent avoir un élément de regroupement qui clarifie les limites des cases d’option homologues.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-216">Ideally, radio buttons should have a grouping element that clarifies the boundaries of the peer radio buttons.</span></span> <span data-ttu-id="9fa9c-217">Toutefois, il arrive souvent que la limite soit impliquée par la structure de l’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-217">Often, however, the boundary is implied by the UI element structure.</span></span> <span data-ttu-id="9fa9c-218">Par exemple, un menu peut contenir un ensemble de cases d’option consécutives à la place d’éléments de menu, ou un ensemble de cases d’option qui se produisent après une étiquette de groupe, mais avant un élément actionnable tel que Button.</span><span class="sxs-lookup"><span data-stu-id="9fa9c-218">For example, a menu might contain a set of consecutive radio buttons instead of menu items, or a set of radio buttons that occur after a group label, but before an actionable element such as button.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9fa9c-219">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9fa9c-219">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9fa9c-220">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9fa9c-220">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9fa9c-221">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="9fa9c-221">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="9fa9c-222">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="9fa9c-222">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




