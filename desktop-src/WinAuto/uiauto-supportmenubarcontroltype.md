---
title: BarreMenus (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle MenuBar.
ms.assetid: e93a92ce-7c98-4e8f-8a6a-a365ccb705d6
keywords:
- UI Automation, prise en charge du type de contrôle MenuBar
- UI Automation, type de contrôle MenuBar
- UI Automation, arborescence pour le type de contrôle MenuBar
- UI Automation, propriétés pour le type de contrôle MenuBar
- UI Automation, modèles de contrôle pour le type de contrôle MenuBar
- UI Automation, événements pour le type de contrôle MenuBar
- arborescences, type de contrôle MenuBar
- Propriétés, BarreMenus (type de contrôle)
- modèles de contrôle, type de contrôle MenuBar
- événements, type de contrôle MenuBar
- prise en charge du type de contrôle MenuBar
- BarreMenus (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle MenuBar
- types de contrôle, modèles de contrôle pour le type de contrôle MenuBar
- types de contrôles, prise en charge de MenuBar
- types de contrôles, BarreMenus
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b94bb60c13b5999bc8020eb70b84f6c932a2fb94
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106531186"
---
# <a name="menubar-control-type"></a><span data-ttu-id="b4607-119">BarreMenus (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="b4607-119">MenuBar Control Type</span></span>

<span data-ttu-id="b4607-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="b4607-120">This topic provides information about Microsoft UI Automation support for the **MenuBar** control type.</span></span>

<span data-ttu-id="b4607-121">Les contrôles de barre de menus sont un exemple de contrôles qui implémentent le type de contrôle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="b4607-121">Menu bar controls are an example of controls that implement the **MenuBar** control type.</span></span> <span data-ttu-id="b4607-122">Les barres de menus permettent aux utilisateurs d’activer les commandes et les options contenues dans une application.</span><span class="sxs-lookup"><span data-stu-id="b4607-122">Menu bars provide a means for users to activate commands and options contained in an application.</span></span>

<span data-ttu-id="b4607-123">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="b4607-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **MenuBar** control type.</span></span> <span data-ttu-id="b4607-124">Les spécifications d’UI Automation s’appliquent à tous les contrôles de barre de menus où l’infrastructure d’interface utilisateur/plateforme intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="b4607-124">The UI Automation requirements apply to all menu bar controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="b4607-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b4607-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b4607-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="b4607-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="b4607-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="b4607-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="b4607-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="b4607-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="b4607-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="b4607-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="b4607-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4607-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="b4607-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="b4607-131">Typical Tree Structure</span></span>

<span data-ttu-id="b4607-132">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de barre de menus, et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="b4607-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu bar controls and describes what can be contained in each view.</span></span> <span data-ttu-id="b4607-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b4607-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b4607-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="b4607-134">Control View</span></span></th>
<th><span data-ttu-id="b4607-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="b4607-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="b4607-136">MenuBar</span><span class="sxs-lookup"><span data-stu-id="b4607-136">MenuBar</span></span>
<ul>
<li><span data-ttu-id="b4607-137">MenuItem (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="b4607-137">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="b4607-138">Autres contrôles (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="b4607-138">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="b4607-139">Non applicable</span><span class="sxs-lookup"><span data-stu-id="b4607-139">Not applicable</span></span>
<ul>
<li><span data-ttu-id="b4607-140">MenuItem (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="b4607-140">MenuItem (1 or more)</span></span></li>
<li><span data-ttu-id="b4607-141">Autres contrôles (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="b4607-141">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="b4607-142">Un contrôle de barre de menus apparaît toujours dans l’affichage de contrôle, mais pas dans l’affichage de contenu, car il ne transmet généralement pas d’informations significatives à l’utilisateur final (sauf si l’application contient plus d’une barre de menus).</span><span class="sxs-lookup"><span data-stu-id="b4607-142">A menu bar control always appears in the control view, but not in content view because it usually does not convey meaningful information to the end user (unless the application contains more than one menu bar).</span></span>

<span data-ttu-id="b4607-143">Les clients UI Automation peuvent écouter l’événement [**UIA \_ MenuModeStartEventId**](uiauto-event-ids.md) pour s’assurer qu’ils sont régulièrement avertis lorsque l’interface utilisateur passe en mode de menu.</span><span class="sxs-lookup"><span data-stu-id="b4607-143">UI Automation clients can listen for the [**UIA\_MenuModeStartEventId**](uiauto-event-ids.md) event to ensure that they are consistently notified when the UI enters menu mode.</span></span> <span data-ttu-id="b4607-144">Quand l’application est en mode de menu, toutes les entrées au clavier peuvent être capturées pour la navigation dans les menus (par exemple, l’entrée peut appeler le menu **Enregistrer** au lieu de taper le caractère dans la zone cliente de l’application).</span><span class="sxs-lookup"><span data-stu-id="b4607-144">When the application is in menu mode, all of the keyboard input may be captured for menu navigation (for example, typing 's' might invoke the **Save** menu instead of typing the character on the application client area).</span></span> <span data-ttu-id="b4607-145">L’événement **UIA \_ MenuModeStartEventId** doit précéder le premier événement [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) pour garantir la cohérence logique.</span><span class="sxs-lookup"><span data-stu-id="b4607-145">The **UIA\_MenuModeStartEventId** event must precede the first [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event to ensure logical consistency.</span></span> <span data-ttu-id="b4607-146">L’événement [**UIA \_ MenuModeEndEventId**](uiauto-event-ids.md) suit le dernier événement [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) .</span><span class="sxs-lookup"><span data-stu-id="b4607-146">The [**UIA\_MenuModeEndEventId**](uiauto-event-ids.md) event follows the last [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event.</span></span> <span data-ttu-id="b4607-147">Un clic sur un élément de menu peut également déclencher immédiatement l’événement **UIA \_ MenuModeStartEventId** , suivi d’un événement **UIA \_ MenuOpenedEventId** .</span><span class="sxs-lookup"><span data-stu-id="b4607-147">Clicking a menu item may also immediately trigger the **UIA\_MenuModeStartEventId** event, followed by a **UIA\_MenuOpenedEventId** event.</span></span>

<span data-ttu-id="b4607-148">Un contrôle de barre de menus peut contenir d’autres contrôles, tels que des contrôles d’édition et des zones de liste déroulante, au sein de sa structure.</span><span class="sxs-lookup"><span data-stu-id="b4607-148">A menu bar control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="b4607-149">Ces contrôles supplémentaires correspondent aux « autres contrôles » répertoriés ci-dessus dans les affichages de contrôle et de contenu.</span><span class="sxs-lookup"><span data-stu-id="b4607-149">These additional controls correspond to the "other controls" listed above in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="b4607-150">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="b4607-150">Relevant Properties</span></span>

<span data-ttu-id="b4607-151">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="b4607-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **MenuBar** control type.</span></span> <span data-ttu-id="b4607-152">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="b4607-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="b4607-153">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="b4607-153">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="b4607-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4607-154">Value</span></span>       | <span data-ttu-id="b4607-155">Notes</span><span class="sxs-lookup"><span data-stu-id="b4607-155">Notes</span></span>                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4607-156">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-156">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="b4607-157">NULL</span><span class="sxs-lookup"><span data-stu-id="b4607-157">NULL</span></span>        | <span data-ttu-id="b4607-158">Les barres de menus n’ont généralement pas de touches accélérateur.</span><span class="sxs-lookup"><span data-stu-id="b4607-158">Menu bars usually do not have accelerator keys.</span></span>                                                                                                                                                                                          |
| [<span data-ttu-id="b4607-159">**UIA \_ AccessKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-159">**UIA\_AccessKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="b4607-160">« ALT »</span><span class="sxs-lookup"><span data-stu-id="b4607-160">"ALT"</span></span>       | <span data-ttu-id="b4607-161">En appuyant sur la touche ALT, vous devez généralement mettre le focus sur la barre de menus de l’application.</span><span class="sxs-lookup"><span data-stu-id="b4607-161">Pressing the ALT key should usually bring focus to the menu bar within the application.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="b4607-162">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-162">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="b4607-163">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b4607-163">See notes.</span></span>  | <span data-ttu-id="b4607-164">La valeur exposée par cette propriété doit inclure tous les contrôles qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="b4607-164">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="b4607-165">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-165">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b4607-166">**MenuBar**</span><span class="sxs-lookup"><span data-stu-id="b4607-166">**MenuBar**</span></span> |                                                                                                                                                                                                                                          |
| [<span data-ttu-id="b4607-167">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-167">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b4607-168">FALSE</span><span class="sxs-lookup"><span data-stu-id="b4607-168">FALSE</span></span>       | <span data-ttu-id="b4607-169">Le contrôle de barre de menus n’est pas inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b4607-169">The menu bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="b4607-170">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-170">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="b4607-171">TRUE</span><span class="sxs-lookup"><span data-stu-id="b4607-171">TRUE</span></span>        | <span data-ttu-id="b4607-172">Le contrôle de barre de menus est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="b4607-172">The menu bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                                   |
| [<span data-ttu-id="b4607-173">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-173">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="b4607-174">TRUE</span><span class="sxs-lookup"><span data-stu-id="b4607-174">TRUE</span></span>        | <span data-ttu-id="b4607-175">Les contrôles de barre de menus sont actifs via le clavier, car les contrôles qu’ils contiennent peuvent recevoir le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="b4607-175">Menu bar controls are keyboard-focusable because the controls they contain can take keyboard focus.</span></span>                                                                                                                                      |
| [<span data-ttu-id="b4607-176">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-176">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b4607-177">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b4607-177">See notes.</span></span>  | <span data-ttu-id="b4607-178">La valeur de cette propriété varie selon que le contrôle est visible ou non à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b4607-178">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                                     |
| [<span data-ttu-id="b4607-179">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-179">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="b4607-180">NULL</span><span class="sxs-lookup"><span data-stu-id="b4607-180">NULL</span></span>        | <span data-ttu-id="b4607-181">Les contrôles de barre de menus n’ont généralement pas d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="b4607-181">Menu bar controls usually do not have a label.</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="b4607-182">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-182">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="b4607-183">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b4607-183">See notes.</span></span>  | <span data-ttu-id="b4607-184">Chaîne localisée correspondant au type de contrôle **MenuBar** .</span><span class="sxs-lookup"><span data-stu-id="b4607-184">Localized string corresponding to the **MenuBar** control type.</span></span> <span data-ttu-id="b4607-185">La valeur par défaut est « barre de menus » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="b4607-185">The default value is "menu bar" for en-US or English (United States).</span></span>                                                                                                    |
| [<span data-ttu-id="b4607-186">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-186">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="b4607-187">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="b4607-187">See notes.</span></span>  | <span data-ttu-id="b4607-188">Le contrôle de barre de menus n’a pas besoin d’un nom, sauf si une application contient plusieurs barres de menus.</span><span class="sxs-lookup"><span data-stu-id="b4607-188">The menu bar control does not need a name unless an application has more than one menu bar.</span></span> <span data-ttu-id="b4607-189">S’il existe plusieurs barres de menus dans une application, utilisez cette propriété pour exposer des noms distinctifs, tels que « mise en forme » ou « mode plan ».</span><span class="sxs-lookup"><span data-stu-id="b4607-189">If there is more than one menu bar in an application, use this property to expose distinguishing names, such as "Formatting" or "Outlining".</span></span> |
| [<span data-ttu-id="b4607-190">**UIA \_ OrientationPropertyId**</span><span class="sxs-lookup"><span data-stu-id="b4607-190">**UIA\_OrientationPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="b4607-191">Dépend</span><span class="sxs-lookup"><span data-stu-id="b4607-191">Depends</span></span>     | <span data-ttu-id="b4607-192">Cette propriété indique si le contrôle de barre de menus est horizontal ou vertical.</span><span class="sxs-lookup"><span data-stu-id="b4607-192">This property exposes whether the menu bar control is horizontal or vertical.</span></span>                                                                                                                                                            |



 

## <a name="required-control-patterns"></a><span data-ttu-id="b4607-193">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="b4607-193">Required Control Patterns</span></span>

<span data-ttu-id="b4607-194">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de barre de menus.</span><span class="sxs-lookup"><span data-stu-id="b4607-194">The following table lists the UI Automation control patterns required to be supported by menu bar controls.</span></span> <span data-ttu-id="b4607-195">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b4607-195">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="b4607-196">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="b4607-196">Control Pattern</span></span>                                                   | <span data-ttu-id="b4607-197">Support</span><span class="sxs-lookup"><span data-stu-id="b4607-197">Support</span></span> | <span data-ttu-id="b4607-198">Notes</span><span class="sxs-lookup"><span data-stu-id="b4607-198">Notes</span></span>                                                                                                                                       |
|-------------------------------------------------------------------|---------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4607-199">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="b4607-199">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="b4607-200">Dépend</span><span class="sxs-lookup"><span data-stu-id="b4607-200">Depends</span></span> | <span data-ttu-id="b4607-201">Si le contrôle peut être développé ou réduit, il doit implémenter le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) .</span><span class="sxs-lookup"><span data-stu-id="b4607-201">If the control can be expanded or collapsed, it must implement the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern.</span></span> |
| [<span data-ttu-id="b4607-202">**IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="b4607-202">**IDockProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider)                     | <span data-ttu-id="b4607-203">Dépend</span><span class="sxs-lookup"><span data-stu-id="b4607-203">Depends</span></span> | <span data-ttu-id="b4607-204">Si le contrôle peut être ancré à différentes parties de l’écran, il doit implémenter le modèle de contrôle [Dock](uiauto-implementingdock.md) .</span><span class="sxs-lookup"><span data-stu-id="b4607-204">If the control can be docked to different parts of the screen, it must implement the [Dock](uiauto-implementingdock.md) control pattern.</span></span>   |
| [<span data-ttu-id="b4607-205">**ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="b4607-205">**ITransformProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider)           | <span data-ttu-id="b4607-206">Dépend</span><span class="sxs-lookup"><span data-stu-id="b4607-206">Depends</span></span> | <span data-ttu-id="b4607-207">Si le contrôle peut être redimensionné, pivoté ou déplacé, il doit implémenter le modèle de contrôle [Transform](uiauto-implementingtransform.md) .</span><span class="sxs-lookup"><span data-stu-id="b4607-207">If the control can be resized, rotated, or moved, it must implement the [Transform](uiauto-implementingtransform.md) control pattern.</span></span>      |



 

## <a name="required-events"></a><span data-ttu-id="b4607-208">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="b4607-208">Required Events</span></span>

<span data-ttu-id="b4607-209">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de barre de menus.</span><span class="sxs-lookup"><span data-stu-id="b4607-209">The following table lists the UI Automation events that menu bar controls are required to support.</span></span> <span data-ttu-id="b4607-210">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="b4607-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="b4607-211">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="b4607-211">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="b4607-212">Notes</span><span class="sxs-lookup"><span data-stu-id="b4607-212">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b4607-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b4607-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="b4607-214">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b4607-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="b4607-215">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="b4607-215">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="b4607-216">Si le contrôle prend en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="b4607-216">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="b4607-217">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b4607-217">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="b4607-218">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="b4607-218">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="b4607-219">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="b4607-219">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="b4607-220">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="b4607-220">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| [<span data-ttu-id="b4607-221">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="b4607-221">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |



 

## <a name="related-topics"></a><span data-ttu-id="b4607-222">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4607-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b4607-223">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b4607-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b4607-224">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="b4607-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="b4607-225">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="b4607-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




