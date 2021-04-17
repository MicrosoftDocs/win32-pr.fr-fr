---
title: Pane (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Pane.
ms.assetid: 2a5d69dc-6880-4610-b481-4371637472ed
keywords:
- UI Automation, prise en charge du type de contrôle Pane
- UI Automation, type de contrôle Pane
- UI Automation, arborescence pour le type de contrôle Pane
- UI Automation, propriétés pour le type de contrôle Pane
- UI Automation, modèles de contrôle pour le type de contrôle Pane
- UI Automation, événements pour le type de contrôle Pane
- arborescences, type de contrôle Pane
- Propriétés, Pane (type de contrôle)
- modèles de contrôle, type de contrôle Pane
- événements, type de contrôle Pane
- prise en charge du type de contrôle Pane
- Pane (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Pane
- types de contrôles, modèles de contrôle pour le type de contrôle Pane
- types de contrôles, prise en charge pour le volet
- types de contrôles, volet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51b7f22e6fb302ebb160a174c27c61119b8f09fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559304"
---
# <a name="pane-control-type"></a><span data-ttu-id="4a984-119">Pane (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="4a984-119">Pane Control Type</span></span>

<span data-ttu-id="4a984-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Pane** .</span><span class="sxs-lookup"><span data-stu-id="4a984-120">This topic provides information about Microsoft UI Automation support for the **Pane** control type.</span></span>

<span data-ttu-id="4a984-121">Le type de contrôle **Pane** est destiné aux régions potentiellement défilantes qui ont un contenu disparate.</span><span class="sxs-lookup"><span data-stu-id="4a984-121">The **Pane** control type is for potentially scrollable regions that have disparate content.</span></span> <span data-ttu-id="4a984-122">Il est utilisé pour représenter un objet dans un frame ou une fenêtre de document.</span><span class="sxs-lookup"><span data-stu-id="4a984-122">It is used to represent an object within a frame or document window.</span></span> <span data-ttu-id="4a984-123">Les utilisateurs peuvent naviguer entre les contrôles de volet et dans le contenu du volet actuel.</span><span class="sxs-lookup"><span data-stu-id="4a984-123">Users can navigate between pane controls and within the contents of the current pane.</span></span> <span data-ttu-id="4a984-124">Les contrôles de volet représentent un niveau de regroupement inférieur à celui de Windows ou de documents, mais au-dessus des contrôles individuels.</span><span class="sxs-lookup"><span data-stu-id="4a984-124">Pane controls represent a level of grouping lower than windows or documents, but above individual controls.</span></span> <span data-ttu-id="4a984-125">L’utilisateur navigue entre les volets en appuyant sur TAB, F6 ou Ctrl+Tab, en fonction du contexte.</span><span class="sxs-lookup"><span data-stu-id="4a984-125">The user navigates between panes by pressing TAB, F6, or CTRL+TAB, depending on the context.</span></span>

<span data-ttu-id="4a984-126">Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Pane** .</span><span class="sxs-lookup"><span data-stu-id="4a984-126">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Pane** control type.</span></span> <span data-ttu-id="4a984-127">Les exigences d’UI Automation s’appliquent à tous les contrôles de volet où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="4a984-127">The UI Automation requirements apply to all pane controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="4a984-128">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="4a984-128">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="4a984-129">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="4a984-129">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="4a984-130">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="4a984-130">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="4a984-131">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="4a984-131">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="4a984-132">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="4a984-132">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="4a984-133">Exemple de type de contrôle Pane</span><span class="sxs-lookup"><span data-stu-id="4a984-133">Pane Control Type Example</span></span>](#pane-control-type-example)
-   [<span data-ttu-id="4a984-134">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a984-134">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="4a984-135">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="4a984-135">Typical Tree Structure</span></span>

<span data-ttu-id="4a984-136">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de volet et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="4a984-136">The following table depicts a typical control and content view of the UI Automation tree that pertains to pane controls and describes what can be contained in each view.</span></span> <span data-ttu-id="4a984-137">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4a984-137">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a984-138">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="4a984-138">Control View</span></span></th>
<th><span data-ttu-id="4a984-139">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="4a984-139">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4a984-140">Volet</span><span class="sxs-lookup"><span data-stu-id="4a984-140">Pane</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4a984-141">Volet</span><span class="sxs-lookup"><span data-stu-id="4a984-141">Pane</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4a984-142">Un contrôle de volet apparaît toujours dans les affichages de contrôle et de contenu.</span><span class="sxs-lookup"><span data-stu-id="4a984-142">A pane control always appears in the control and content views.</span></span> <span data-ttu-id="4a984-143">N’exposez pas un objet layout en tant que volet dans l’affichage de contrôle ou de contenu si l’objet est utilisé uniquement pour la présentation visuelle.</span><span class="sxs-lookup"><span data-stu-id="4a984-143">Do not expose a layout object as a pane in either the control or content view if the object is used only for visual presentation.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="4a984-144">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="4a984-144">Relevant Properties</span></span>

<span data-ttu-id="4a984-145">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de volet.</span><span class="sxs-lookup"><span data-stu-id="4a984-145">The following table lists the UI Automation properties whose value or definition is especially relevant to pane controls.</span></span> <span data-ttu-id="4a984-146">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="4a984-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="4a984-147">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="4a984-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="4a984-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="4a984-148">Value</span></span>      | <span data-ttu-id="4a984-149">Notes</span><span class="sxs-lookup"><span data-stu-id="4a984-149">Notes</span></span>                                                                                                                                                                                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a984-150">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-150">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4a984-151">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-151">See notes.</span></span> | <span data-ttu-id="4a984-152">Si une combinaison de touches spécifique donne le focus au volet, ces informations doivent être exposées via cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4a984-152">If a specific key combination gives focus to the pane, that information should be exposed through this property.</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="4a984-153">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-153">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="4a984-154">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-154">See notes.</span></span> | <span data-ttu-id="4a984-155">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4a984-155">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                          |
| [<span data-ttu-id="4a984-156">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-156">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="4a984-157">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-157">See notes.</span></span> | <span data-ttu-id="4a984-158">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="4a984-158">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="4a984-159">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-159">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="4a984-160">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-160">See notes.</span></span> | <span data-ttu-id="4a984-161">Cette propriété expose un point interactif du contrôle de volet qui, lorsque vous cliquez dessus, place le focus sur le volet.</span><span class="sxs-lookup"><span data-stu-id="4a984-161">This property exposes a clickable point of the pane control that causes the pane to become focused when it is clicked.</span></span>                                                                                                                                                                                                |
| [<span data-ttu-id="4a984-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="4a984-163">**Volet**</span><span class="sxs-lookup"><span data-stu-id="4a984-163">**Pane**</span></span>   |                                                                                                                                                                                                                                                                                                                       |
| [<span data-ttu-id="4a984-164">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-164">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="4a984-165">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-165">See notes.</span></span> | <span data-ttu-id="4a984-166">Le texte d’aide pour les contrôles de volet doit expliquer l’objectif du frame et sa relation avec d’autres frames.</span><span class="sxs-lookup"><span data-stu-id="4a984-166">The help text for pane controls should explain the purpose of the frame and how it relates to other frames.</span></span> <span data-ttu-id="4a984-167">Une description est nécessaire si l’objectif et la relation des frames ne sont pas clairs par rapport à la valeur de la propriété [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="4a984-167">A description is necessary if the purpose and relationship of the frames is not clear from the value of the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span> |
| [<span data-ttu-id="4a984-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4a984-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="4a984-169">TRUE</span></span>       | <span data-ttu-id="4a984-170">Le contrôle de volet est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4a984-170">The pane control is always included in the content view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4a984-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="4a984-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="4a984-172">TRUE</span></span>       | <span data-ttu-id="4a984-173">Le contrôle de volet est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="4a984-173">The pane control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="4a984-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="4a984-175">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-175">See notes.</span></span> | <span data-ttu-id="4a984-176">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4a984-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                             |
| [<span data-ttu-id="4a984-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="4a984-178">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-178">See notes.</span></span> | <span data-ttu-id="4a984-179">Les contrôles Pane n’ont pas d’étiquette statique.</span><span class="sxs-lookup"><span data-stu-id="4a984-179">Pane controls typically do not have a static label.</span></span> <span data-ttu-id="4a984-180">S’il existe une étiquette de texte statique, il doit être exposé via cette propriété.</span><span class="sxs-lookup"><span data-stu-id="4a984-180">If there is a static text label, it should be exposed through this property.</span></span>                                                                                                                                                                                      |
| [<span data-ttu-id="4a984-181">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-181">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="4a984-182">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-182">See notes.</span></span> | <span data-ttu-id="4a984-183">Chaîne localisée correspondant au type de contrôle **Pane** .</span><span class="sxs-lookup"><span data-stu-id="4a984-183">Localized string corresponding to the **Pane** control type.</span></span> <span data-ttu-id="4a984-184">La valeur par défaut est « Pane » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="4a984-184">The default value is "pane" for en-US or English (United States).</span></span>                                                                                                                                                                                        |
| [<span data-ttu-id="4a984-185">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="4a984-185">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="4a984-186">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="4a984-186">See notes.</span></span> | <span data-ttu-id="4a984-187">La valeur de cette propriété doit toujours être un titre clair, concis et explicite.</span><span class="sxs-lookup"><span data-stu-id="4a984-187">The value for this property must always be a clear, concise and meaningful title.</span></span>                                                                                                                                                                                                                                     |



 

## <a name="required-control-patterns"></a><span data-ttu-id="4a984-188">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="4a984-188">Required Control Patterns</span></span>

<span data-ttu-id="4a984-189">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de volet.</span><span class="sxs-lookup"><span data-stu-id="4a984-189">The following table lists the UI Automation control patterns required to be supported by pane controls.</span></span> <span data-ttu-id="4a984-190">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4a984-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="4a984-191">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="4a984-191">Control Pattern</span></span>                                         | <span data-ttu-id="4a984-192">Support</span><span class="sxs-lookup"><span data-stu-id="4a984-192">Support</span></span> | <span data-ttu-id="4a984-193">Notes</span><span class="sxs-lookup"><span data-stu-id="4a984-193">Notes</span></span>                                                                                                                                                                                         |
|---------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a984-194">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="4a984-194">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)           | <span data-ttu-id="4a984-195">Dépend</span><span class="sxs-lookup"><span data-stu-id="4a984-195">Depends</span></span> | <span data-ttu-id="4a984-196">Implémentez le modèle de contrôle [Dock](uiauto-implementingdock.md) si le contrôle de volet peut être ancré.</span><span class="sxs-lookup"><span data-stu-id="4a984-196">Implement the [Dock](uiauto-implementingdock.md) control pattern if the pane control can be docked.</span></span>                                                                                          |
| [<span data-ttu-id="4a984-197">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="4a984-197">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="4a984-198">Dépend</span><span class="sxs-lookup"><span data-stu-id="4a984-198">Depends</span></span> | <span data-ttu-id="4a984-199">Implémentez le modèle de contrôle [Scroll](uiauto-implementingscroll.md) si le contrôle de volet peut défiler.</span><span class="sxs-lookup"><span data-stu-id="4a984-199">Implement the [Scroll](uiauto-implementingscroll.md) control pattern if the pane control can be scrolled.</span></span>                                                                                    |
| [<span data-ttu-id="4a984-200">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="4a984-200">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) | <span data-ttu-id="4a984-201">Dépend</span><span class="sxs-lookup"><span data-stu-id="4a984-201">Depends</span></span> | <span data-ttu-id="4a984-202">Implémentez le modèle de contrôle [Transform](uiauto-implementingtransform.md) si le contrôle de volet peut être déplacé, redimensionné ou pivoté sur l’écran.</span><span class="sxs-lookup"><span data-stu-id="4a984-202">Implement the [Transform](uiauto-implementingtransform.md) control pattern if the pane control can be moved, resized, or rotated on the screen.</span></span>                                              |
| [<span data-ttu-id="4a984-203">**IWindowProvider**</span><span class="sxs-lookup"><span data-stu-id="4a984-203">**IWindowProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iwindowprovider)       | <span data-ttu-id="4a984-204">Jamais</span><span class="sxs-lookup"><span data-stu-id="4a984-204">Never</span></span>   | <span data-ttu-id="4a984-205">Si l’élément doit implémenter le modèle de contrôle [Window](uiauto-implementingwindow.md) , le contrôle doit être basé sur le type de contrôle [Window](uiauto-supportwindowcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="4a984-205">If the element needs to implement the [Window](uiauto-implementingwindow.md) control pattern, the control should be based on the [Window](uiauto-supportwindowcontroltype.md) control type.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="4a984-206">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="4a984-206">Required Events</span></span>

<span data-ttu-id="4a984-207">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de volet.</span><span class="sxs-lookup"><span data-stu-id="4a984-207">The following table lists the UI Automation events that pane controls are required to support.</span></span> <span data-ttu-id="4a984-208">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="4a984-208">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="4a984-209">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="4a984-209">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="4a984-210">Notes</span><span class="sxs-lookup"><span data-stu-id="4a984-210">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4a984-211">**UIA \_ AsyncContentLoadedEventId**</span><span class="sxs-lookup"><span data-stu-id="4a984-211">**UIA\_AsyncContentLoadedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                            |
| [<span data-ttu-id="4a984-212">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4a984-212">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="4a984-213">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-213">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="4a984-214">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="4a984-215">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4a984-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="4a984-216">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-216">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="4a984-217">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4a984-217">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a984-218">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-218">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="4a984-219">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4a984-219">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a984-220">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-220">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="4a984-221">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4a984-221">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a984-222">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-222">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="4a984-223">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4a984-223">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a984-224">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-224">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="4a984-225">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4a984-225">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="4a984-226">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="4a984-226">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="4a984-227">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="4a984-227">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="4a984-228">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="4a984-228">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |



 

## <a name="pane-control-type-example"></a><span data-ttu-id="4a984-229">Exemple de type de contrôle Pane</span><span class="sxs-lookup"><span data-stu-id="4a984-229">Pane Control Type Example</span></span>

<span data-ttu-id="4a984-230">L’image suivante illustre un contrôle qui implémente le type de contrôle **Pane** .</span><span class="sxs-lookup"><span data-stu-id="4a984-230">The following image illustrates a control that implements the **Pane** control type.</span></span>

![capture d’écran montrant un exemple de contrôle de volet](images/panexmpl.jpg)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4a984-232">Arborescence UI Automation — vue contrôle</span><span class="sxs-lookup"><span data-stu-id="4a984-232">UI Automation Tree—Control View</span></span></th>
<th><span data-ttu-id="4a984-233">Arborescence UI Automation — affichage du contenu</span><span class="sxs-lookup"><span data-stu-id="4a984-233">UI Automation Tree—Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="4a984-234">Volet</span><span class="sxs-lookup"><span data-stu-id="4a984-234">Pane</span></span>
<ul>
<li><span data-ttu-id="4a984-235">Tree (modèle Scroll)</span><span class="sxs-lookup"><span data-stu-id="4a984-235">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="4a984-236">TreeItem</span><span class="sxs-lookup"><span data-stu-id="4a984-236">TreeItem</span></span></li>
<li><span data-ttu-id="4a984-237">...</span><span class="sxs-lookup"><span data-stu-id="4a984-237">...</span></span></li>
</ul></li>
</ul></li>
<li><span data-ttu-id="4a984-238">Volet</span><span class="sxs-lookup"><span data-stu-id="4a984-238">Pane</span></span>
<ul>
<li><span data-ttu-id="4a984-239">Modifier (modèle Scroll)</span><span class="sxs-lookup"><span data-stu-id="4a984-239">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="4a984-240">Volet</span><span class="sxs-lookup"><span data-stu-id="4a984-240">Pane</span></span>
<ul>
<li><span data-ttu-id="4a984-241">Tree (modèle Scroll)</span><span class="sxs-lookup"><span data-stu-id="4a984-241">Tree (Scroll Pattern)</span></span>
<ul>
<li><span data-ttu-id="4a984-242">TreeItem</span><span class="sxs-lookup"><span data-stu-id="4a984-242">TreeItem</span></span></li>
<li><span data-ttu-id="4a984-243">...</span><span class="sxs-lookup"><span data-stu-id="4a984-243">...</span></span></li>
</ul></li>
<li><span data-ttu-id="4a984-244">Volet</span><span class="sxs-lookup"><span data-stu-id="4a984-244">Pane</span></span>
<ul>
<li><span data-ttu-id="4a984-245">Modifier (modèle Scroll)</span><span class="sxs-lookup"><span data-stu-id="4a984-245">Edit (Scroll Pattern)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="4a984-246">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4a984-246">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="4a984-247">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="4a984-247">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="4a984-248">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="4a984-248">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="4a984-249">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="4a984-249">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




