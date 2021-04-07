---
title: Menu (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Menu.
ms.assetid: cdbb6db7-63d7-422e-952c-7b59779fefbe
keywords:
- UI Automation, prise en charge du type de contrôle Menu
- UI Automation, type de contrôle Menu
- UI Automation, arborescence pour le type de contrôle Menu
- UI Automation, propriétés du type de contrôle Menu
- UI Automation, modèles de contrôle pour le type de contrôle Menu
- UI Automation, événements pour le type de contrôle Menu
- arborescences, type de contrôle Menu
- Propriétés, type de contrôle Menu
- modèles de contrôle, type de contrôle Menu
- événements, type de contrôle Menu
- prise en charge du type de contrôle Menu
- Menu (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Menu
- types de contrôles, modèles de contrôle pour le type de contrôle Menu
- types de contrôles, prise en charge du menu
- types de contrôles, menu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: edee9f30f4d4cea123a2c7f5ff4dac235782faea
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029102"
---
# <a name="menu-control-type"></a><span data-ttu-id="50bc0-119">Menu (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="50bc0-119">Menu Control Type</span></span>

<span data-ttu-id="50bc0-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **menu** .</span><span class="sxs-lookup"><span data-stu-id="50bc0-120">This topic provides information about Microsoft UI Automation support for the **Menu** control type.</span></span>

<span data-ttu-id="50bc0-121">Un contrôle menu permet une organisation hiérarchique des éléments associés à des commandes et des gestionnaires d’événements.</span><span class="sxs-lookup"><span data-stu-id="50bc0-121">A menu control allows hierarchal organization of elements associated with commands and event handlers.</span></span> <span data-ttu-id="50bc0-122">Dans une application Microsoft Windows classique, une barre de menus contient plusieurs boutons de menu (tels que **fichier**, **Edition** et **fenêtre**) et chaque bouton de menu affiche un menu.</span><span class="sxs-lookup"><span data-stu-id="50bc0-122">In a typical Microsoft Windows application, a menu bar contains several menu buttons (such as **File**, **Edit**, and **Window**), and each menu button displays a menu.</span></span> <span data-ttu-id="50bc0-123">Un menu contient un groupe d’éléments de menu (tels que **Nouveau**, **Ouvrir** et **Fermer**), qui peuvent être développés pour afficher des éléments de menu supplémentaires ou pour exécuter une action spécifique quand vous cliquez dessus.</span><span class="sxs-lookup"><span data-stu-id="50bc0-123">A menu contains a collection of menu items (such as **New**, **Open**, and **Close**), which can be expanded to display additional menu items or to perform a specific action when clicked.</span></span>

<span data-ttu-id="50bc0-124">Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **menu** .</span><span class="sxs-lookup"><span data-stu-id="50bc0-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Menu** control type.</span></span> <span data-ttu-id="50bc0-125">Les exigences d’UI Automation s’appliquent à tous les contrôles de menu où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="50bc0-125">The UI Automation requirements apply to all menu controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="50bc0-126">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="50bc0-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="50bc0-127">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="50bc0-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="50bc0-128">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="50bc0-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="50bc0-129">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="50bc0-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="50bc0-130">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="50bc0-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="50bc0-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50bc0-131">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="50bc0-132">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="50bc0-132">Typical Tree Structure</span></span>

<span data-ttu-id="50bc0-133">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de menu et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="50bc0-133">The following table depicts a typical control and content view of the UI Automation tree that pertains to menu controls and describes what can be contained in each view.</span></span> <span data-ttu-id="50bc0-134">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="50bc0-134">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="50bc0-135">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="50bc0-135">Control View</span></span></th>
<th><span data-ttu-id="50bc0-136">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="50bc0-136">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="50bc0-137">Menu</span><span class="sxs-lookup"><span data-stu-id="50bc0-137">Menu</span></span>
<ul>
<li><span data-ttu-id="50bc0-138">MenuItem (1 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="50bc0-138">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="50bc0-139">Autres contrôles (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="50bc0-139">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="50bc0-140">Menu</span><span class="sxs-lookup"><span data-stu-id="50bc0-140">Menu</span></span>
<ul>
<li><span data-ttu-id="50bc0-141">MenuItem (1 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="50bc0-141">MenuItem (1 or many)</span></span></li>
</ul>
<ul>
<li><span data-ttu-id="50bc0-142">Autres contrôles (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="50bc0-142">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="50bc0-143">Les contrôles de menu s’affichent toujours dans l’affichage de contrôle et l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="50bc0-143">Menu controls always appear in the control view and the content view of the UI Automation tree.</span></span> <span data-ttu-id="50bc0-144">Les contrôles de menu doivent apparaître sous le contrôle auquel leurs informations font référence.</span><span class="sxs-lookup"><span data-stu-id="50bc0-144">Menu controls should appear under the control that their information is referring to.</span></span> <span data-ttu-id="50bc0-145">Les clients UI Automation peuvent écouter [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) pour s’assurer qu’ils obtiennent régulièrement les informations véhiculées par les contrôles menu.</span><span class="sxs-lookup"><span data-stu-id="50bc0-145">UI Automation clients can listen for [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) to ensure that they consistently obtain information conveyed by menu controls.</span></span> <span data-ttu-id="50bc0-146">Les contrôles de menu contextuel constituent un cas particulier.</span><span class="sxs-lookup"><span data-stu-id="50bc0-146">Context menu controls are a special case.</span></span> <span data-ttu-id="50bc0-147">Ils peuvent apparaître en tant qu’enfants du bureau ou d’une fenêtre d’application de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="50bc0-147">They may appear as children of the desktop or of a top level application window.</span></span>

<span data-ttu-id="50bc0-148">Un contrôle de menu peut contenir d’autres contrôles, tels que des contrôles d’édition et des zones de liste déroulante, au sein de sa structure.</span><span class="sxs-lookup"><span data-stu-id="50bc0-148">A menu control can contain other controls, such as edit controls and combo boxes, within its structure.</span></span> <span data-ttu-id="50bc0-149">Ces contrôles supplémentaires correspondent aux « autres contrôles » figurant dans le tableau précédent dans les affichages de contrôle et de contenu.</span><span class="sxs-lookup"><span data-stu-id="50bc0-149">These additional controls correspond to the "other controls" listed in the previous table in the control and content views.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="50bc0-150">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="50bc0-150">Relevant Properties</span></span>

<span data-ttu-id="50bc0-151">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **menu** .</span><span class="sxs-lookup"><span data-stu-id="50bc0-151">The following table lists the UI Automation properties whose value or definition is especially relevant to the **Menu** control type.</span></span> <span data-ttu-id="50bc0-152">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="50bc0-152">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="50bc0-153">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="50bc0-153">UI Automation Property</span></span>                                                                                      | <span data-ttu-id="50bc0-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="50bc0-154">Value</span></span>      | <span data-ttu-id="50bc0-155">Notes</span><span class="sxs-lookup"><span data-stu-id="50bc0-155">Notes</span></span>                                                                                                                                                                   |
|-------------------------------------------------------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50bc0-156">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-156">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)           | <span data-ttu-id="50bc0-157">**Menu**</span><span class="sxs-lookup"><span data-stu-id="50bc0-157">**Menu**</span></span>   |                                                                                                                                                                         |
| [<span data-ttu-id="50bc0-158">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-158">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="50bc0-159">TRUE</span><span class="sxs-lookup"><span data-stu-id="50bc0-159">TRUE</span></span>       | <span data-ttu-id="50bc0-160">Le contrôle Menu est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="50bc0-160">The menu control is always included in the content view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="50bc0-161">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-161">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="50bc0-162">TRUE</span><span class="sxs-lookup"><span data-stu-id="50bc0-162">TRUE</span></span>       | <span data-ttu-id="50bc0-163">Le contrôle Menu est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="50bc0-163">The menu control is always included in the control view of the UI Automation tree.</span></span>                                                                                      |
| [<span data-ttu-id="50bc0-164">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-164">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)               | <span data-ttu-id="50bc0-165">NULL</span><span class="sxs-lookup"><span data-stu-id="50bc0-165">NULL</span></span>       | <span data-ttu-id="50bc0-166">Aucune étiquette n’est censée accompagner un contrôle menu standard.</span><span class="sxs-lookup"><span data-stu-id="50bc0-166">No label is anticipated with a typical menu control.</span></span>                                                                                                                    |
| [<span data-ttu-id="50bc0-167">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-167">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="50bc0-168">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="50bc0-168">See notes.</span></span> | <span data-ttu-id="50bc0-169">Le contrôle de menu ne requiert pas la définition d’une propriété **Name** ou peut avoir le même nom que le contrôle associé, par exemple un élément de menu qui a ouvert le sous-menu.</span><span class="sxs-lookup"><span data-stu-id="50bc0-169">The menu control does not require a **Name** property to be set, or it could have the same name as the associated control, such as a menu item that opened the submenu.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="50bc0-170">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="50bc0-170">Required Control Patterns</span></span>

<span data-ttu-id="50bc0-171">Il n’existe aucun modèle de contrôle obligatoire pour le type de contrôle Menu.</span><span class="sxs-lookup"><span data-stu-id="50bc0-171">There are no required control patterns for the Menu control type.</span></span>

## <a name="required-events"></a><span data-ttu-id="50bc0-172">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="50bc0-172">Required Events</span></span>

<span data-ttu-id="50bc0-173">Les contrôles menu doivent déclencher l’événement [**UIA \_ MenuOpenedEventId**](uiauto-event-ids.md) lorsqu’ils s’affichent à l’écran.</span><span class="sxs-lookup"><span data-stu-id="50bc0-173">Menu controls must raise the [**UIA\_MenuOpenedEventId**](uiauto-event-ids.md) event when they appear on the screen.</span></span> <span data-ttu-id="50bc0-174">L’événement **UIA \_ MenuOpenedEventId** inclut le texte du contrôle.</span><span class="sxs-lookup"><span data-stu-id="50bc0-174">The **UIA\_MenuOpenedEventId** event will include the text of the control.</span></span> <span data-ttu-id="50bc0-175">L’événement [**UIA \_ MenuClosedEventId**](uiauto-event-ids.md) doit être déclenché quand un menu disparaît de l’écran.</span><span class="sxs-lookup"><span data-stu-id="50bc0-175">The [**UIA\_MenuClosedEventId**](uiauto-event-ids.md) event must be raised when a menu disappears from the screen.</span></span>

<span data-ttu-id="50bc0-176">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de menu.</span><span class="sxs-lookup"><span data-stu-id="50bc0-176">The following table lists the UI Automation events that menu controls are required to support.</span></span> <span data-ttu-id="50bc0-177">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="50bc0-177">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="50bc0-178">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="50bc0-178">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="50bc0-179">Notes</span><span class="sxs-lookup"><span data-stu-id="50bc0-179">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="50bc0-180">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-180">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="50bc0-181">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="50bc0-181">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="50bc0-182">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="50bc0-182">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="50bc0-183">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="50bc0-183">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="50bc0-184">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="50bc0-184">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="50bc0-185">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="50bc0-185">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="50bc0-186">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-186">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="50bc0-187">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-187">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                                                              |                                                                                                                            |
| [<span data-ttu-id="50bc0-188">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="50bc0-188">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="50bc0-189">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="50bc0-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="50bc0-190">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="50bc0-190">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="50bc0-191">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="50bc0-191">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="50bc0-192">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="50bc0-192">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




