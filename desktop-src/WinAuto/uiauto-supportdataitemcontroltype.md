---
title: DataItem (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle DataItem.
ms.assetid: def52fe7-9f05-4cd0-8a46-af4e2e3ba03e
keywords:
- UI Automation, prise en charge du type de contrôle DataItem
- UI Automation, type de contrôle DataItem
- UI Automation, arborescence pour le type de contrôle DataItem
- UI Automation, propriétés du type de contrôle DataItem
- UI Automation, modèles de contrôle pour le type de contrôle DataItem
- UI Automation, événements pour le type de contrôle DataItem
- UI Automation, grandes listes et le type de contrôle DataItem
- arborescences, type de contrôle DataItem
- Propriétés, DataItem (type de contrôle)
- modèles de contrôle, type de contrôle DataItem
- événements, type de contrôle DataItem
- grandes listes
- prise en charge du type de contrôle DataItem
- DataItem (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle DataItem
- types de contrôles, modèles de contrôle pour le type de contrôle DataItem
- types de contrôles, listes de grande taille et type de contrôle DataItem
- types de contrôles, prise en charge de DataItem
- types de contrôles, DataItem
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0902cc593ec7f9104ed27031caa2785b7cb9756
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029105"
---
# <a name="dataitem-control-type"></a><span data-ttu-id="54345-122">DataItem (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="54345-122">DataItem Control Type</span></span>

<span data-ttu-id="54345-123">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="54345-123">This topic provides information about Microsoft UI Automation support for the **DataItem** control type.</span></span>

<span data-ttu-id="54345-124">Une entrée dans une liste de contacts est un exemple de contrôle d’élément de données.</span><span class="sxs-lookup"><span data-stu-id="54345-124">An entry in a Contacts list is an example of a data item control.</span></span> <span data-ttu-id="54345-125">Un contrôle d’élément de données contient des informations intéressantes pour l’utilisateur final.</span><span class="sxs-lookup"><span data-stu-id="54345-125">A data item control contains information that is of interest to an end user.</span></span> <span data-ttu-id="54345-126">Il est plus complexe que l’élément de liste simple, car il contient des informations plus détaillées.</span><span class="sxs-lookup"><span data-stu-id="54345-126">It is more complicated than the simple list item because it contains richer information.</span></span>

<span data-ttu-id="54345-127">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="54345-127">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataItem** control type.</span></span> <span data-ttu-id="54345-128">Les exigences d’UI Automation s’appliquent à tous les contrôles d’élément de données où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="54345-128">The UI Automation requirements apply to all data item controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="54345-129">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="54345-129">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="54345-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="54345-130">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="54345-131">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="54345-131">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="54345-132">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="54345-132">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="54345-133">Utilisation de DataItems dans des listes volumineuses</span><span class="sxs-lookup"><span data-stu-id="54345-133">Working with DataItems in Large Lists</span></span>](#working-with-dataitems-in-large-lists)
-   [<span data-ttu-id="54345-134">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="54345-134">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="54345-135">Exemple de type de contrôle DataItem</span><span class="sxs-lookup"><span data-stu-id="54345-135">DataItem Control Type Example</span></span>](#dataitem-control-type-example)
-   [<span data-ttu-id="54345-136">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54345-136">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="54345-137">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="54345-137">Typical Tree Structure</span></span>

<span data-ttu-id="54345-138">Le tableau suivant représente un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles d’élément de données et décrit ce que peut contenir chaque vue.</span><span class="sxs-lookup"><span data-stu-id="54345-138">The following table depicts a typical control and content view of the UI Automation tree that pertains to data item controls and describes what can be contained in each view.</span></span> <span data-ttu-id="54345-139">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="54345-139">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54345-140">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="54345-140">Control View</span></span></th>
<th><span data-ttu-id="54345-141">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="54345-141">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="54345-142">DataItem</span><span class="sxs-lookup"><span data-stu-id="54345-142">DataItem</span></span>
<ul>
<li><span data-ttu-id="54345-143">Selon le cas (0 ou plus. Peut être structuré dans une hiérarchie)</span><span class="sxs-lookup"><span data-stu-id="54345-143">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="54345-144">DataItem</span><span class="sxs-lookup"><span data-stu-id="54345-144">DataItem</span></span>
<ul>
<li><span data-ttu-id="54345-145">Selon le cas (0 ou plus. Peut être structuré dans une hiérarchie)</span><span class="sxs-lookup"><span data-stu-id="54345-145">Varies (0 or more; can be structured in hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="54345-146">Un élément de données dans une grille de données peut héberger divers objets, notamment une autre couche d’éléments de données ou des éléments de grille spécifiques tels que du texte, des images ou des contrôles d’édition.</span><span class="sxs-lookup"><span data-stu-id="54345-146">A data item element in a data grid can host a variety of objects, including another layer of data items, or specific grid elements such as text, images, or edit controls.</span></span> <span data-ttu-id="54345-147">Si l’élément de données a un rôle d’objet spécifique, l’élément doit être exposé en tant que type de contrôle spécifique ; par exemple, un type de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) pour un élément de données sélectionnable dans la grille.</span><span class="sxs-lookup"><span data-stu-id="54345-147">If the data item element has a specific object role, the element should be exposed as a specific control type; for example, a [ListItem](uiauto-supportlistitemcontroltype.md) control type for a selectable data item in the grid.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="54345-148">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="54345-148">Relevant Properties</span></span>

<span data-ttu-id="54345-149">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle DataItem.</span><span class="sxs-lookup"><span data-stu-id="54345-149">The following table lists the UI Automation properties whose value or definition is especially relevant to the DataItem control type.</span></span> <span data-ttu-id="54345-150">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="54345-150">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="54345-151">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="54345-151">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="54345-152">Valeur</span><span class="sxs-lookup"><span data-stu-id="54345-152">Value</span></span>        | <span data-ttu-id="54345-153">Notes</span><span class="sxs-lookup"><span data-stu-id="54345-153">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54345-154">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-154">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="54345-155">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-155">See notes.</span></span>   | <span data-ttu-id="54345-156">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="54345-156">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="54345-157">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-157">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="54345-158">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-158">See notes.</span></span>   | <span data-ttu-id="54345-159">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="54345-159">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="54345-160">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-160">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="54345-161">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-161">See notes.</span></span>   | <span data-ttu-id="54345-162">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="54345-162">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="54345-163">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="54345-163">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="54345-164">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-164">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="54345-165">**DataItem**</span><span class="sxs-lookup"><span data-stu-id="54345-165">**DataItem**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="54345-166">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-166">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="54345-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="54345-167">TRUE</span></span>         | <span data-ttu-id="54345-168">Le contrôle d’élément de données doit toujours être du contenu.</span><span class="sxs-lookup"><span data-stu-id="54345-168">The data item control must always be content.</span></span>                                                                                                                                                        |
| [<span data-ttu-id="54345-169">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-169">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="54345-170">TRUE</span><span class="sxs-lookup"><span data-stu-id="54345-170">TRUE</span></span>         | <span data-ttu-id="54345-171">Le contrôle d’élément de données doit toujours être un contrôle.</span><span class="sxs-lookup"><span data-stu-id="54345-171">The data item control must always be a control.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="54345-172">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-172">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="54345-173">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-173">See notes.</span></span>   | <span data-ttu-id="54345-174">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="54345-174">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="54345-175">**UIA \_ ItemStatusPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-175">**UIA\_ItemStatusPropertyId**</span></span>](uiauto-automation-element-propids.md)                     | <span data-ttu-id="54345-176">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-176">See notes.</span></span>   | <span data-ttu-id="54345-177">Si le contrôle contient l’État mis à jour dynamiquement, cette propriété doit être prise en charge afin qu’une technologie d’assistance puisse recevoir des mises à jour lorsque l’état de l’élément change.</span><span class="sxs-lookup"><span data-stu-id="54345-177">If the control contains status that is being updated dynamically, this property must be supported so that an assistive technology can receive updates when the status of the element changes.</span></span>        |
| [<span data-ttu-id="54345-178">**UIA \_ ItemTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-178">**UIA\_ItemTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="54345-179">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-179">See notes.</span></span>   | <span data-ttu-id="54345-180">Il s’agit de la valeur de chaîne qui transmet à l’utilisateur final l’objet sous-jacent représenté par l’élément.</span><span class="sxs-lookup"><span data-stu-id="54345-180">This is the string value that conveys to the end user the underlying object that the item represents.</span></span> <span data-ttu-id="54345-181">Exemples : « fichier multimédia » et « contact ».</span><span class="sxs-lookup"><span data-stu-id="54345-181">Examples include "Media File" and "Contact".</span></span>                                                   |
| [<span data-ttu-id="54345-182">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-182">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="54345-183">Null</span><span class="sxs-lookup"><span data-stu-id="54345-183">Null</span></span>         | <span data-ttu-id="54345-184">Les contrôles d’élément de données n’ont pas d’étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="54345-184">Data item controls do not have a static text label.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="54345-185">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-185">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="54345-186">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-186">See notes.</span></span>   | <span data-ttu-id="54345-187">Chaîne localisée correspondant au type de contrôle **DataItem** .</span><span class="sxs-lookup"><span data-stu-id="54345-187">Localized string corresponding to the **DataItem** control type.</span></span> <span data-ttu-id="54345-188">La valeur par défaut est « Data Item » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="54345-188">The default value is "data item" for en-US or English (United States).</span></span>                                                              |
| [<span data-ttu-id="54345-189">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="54345-189">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="54345-190">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="54345-190">See notes.</span></span>   | <span data-ttu-id="54345-191">Le contrôle d’élément de données contient toujours un élément de texte principal que l’utilisateur reconnaît comme identificateur pour l’élément.</span><span class="sxs-lookup"><span data-stu-id="54345-191">The data item control always contains a primary text element that the user would recognize as the identifier for the item.</span></span>                                                                           |



 

## <a name="required-control-patterns"></a><span data-ttu-id="54345-192">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="54345-192">Required Control Patterns</span></span>

<span data-ttu-id="54345-193">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles d’élément de données.</span><span class="sxs-lookup"><span data-stu-id="54345-193">The following table lists the UI Automation control patterns required to be supported by all data item controls.</span></span> <span data-ttu-id="54345-194">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="54345-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="54345-195">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="54345-195">Control Pattern</span></span>                                                   | <span data-ttu-id="54345-196">Support</span><span class="sxs-lookup"><span data-stu-id="54345-196">Support</span></span> | <span data-ttu-id="54345-197">Notes</span><span class="sxs-lookup"><span data-stu-id="54345-197">Notes</span></span>                                                                                                                                                                                                                 |
|-------------------------------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54345-198">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="54345-198">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="54345-199">Dépend</span><span class="sxs-lookup"><span data-stu-id="54345-199">Depends</span></span> | <span data-ttu-id="54345-200">Si l’élément de données peut être développé ou réduit pour afficher et masquer des informations, le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) doit être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="54345-200">If the data item can be expanded or collapsed to show and hide information, the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern must be supported.</span></span>                                            |
| [<span data-ttu-id="54345-201">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="54345-201">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)             | <span data-ttu-id="54345-202">Dépend</span><span class="sxs-lookup"><span data-stu-id="54345-202">Depends</span></span> | <span data-ttu-id="54345-203">Les éléments de données prennent en charge le modèle de contrôle [GridItem](uiauto-implementinggriditem.md) quand une collection d’éléments de données est disponible dans un conteneur qui peut faire l’objet d’une navigation spatiale d’un élément à l’élément.</span><span class="sxs-lookup"><span data-stu-id="54345-203">Data items will support the [GridItem](uiauto-implementinggriditem.md) control pattern when a collection of data items is available within a container that can be spatially navigated item-to-item.</span></span>                 |
| [<span data-ttu-id="54345-204">**IScrollItemProvider**</span><span class="sxs-lookup"><span data-stu-id="54345-204">**IScrollItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider)         | <span data-ttu-id="54345-205">Dépend</span><span class="sxs-lookup"><span data-stu-id="54345-205">Depends</span></span> | <span data-ttu-id="54345-206">Tous les éléments de données prennent en charge la possibilité de faire défiler la vue avec le modèle de contrôle [ScrollItem](uiauto-implementingscrollitem.md) quand leur conteneur de données contient plus d’éléments que l’écran ne peut en contenir.</span><span class="sxs-lookup"><span data-stu-id="54345-206">All data items support the ability to be scrolled into view with the [ScrollItem](uiauto-implementingscrollitem.md) control pattern when their data container has more items than can fit on the screen.</span></span>             |
| [<span data-ttu-id="54345-207">**ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="54345-207">**ISelectionItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider)   | <span data-ttu-id="54345-208">Dépend</span><span class="sxs-lookup"><span data-stu-id="54345-208">Depends</span></span> | <span data-ttu-id="54345-209">La possibilité de sélectionner les éléments de données dépend du contenu.</span><span class="sxs-lookup"><span data-stu-id="54345-209">The ability to select the data items depends on the content.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="54345-210">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="54345-210">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider)           | <span data-ttu-id="54345-211">Dépend</span><span class="sxs-lookup"><span data-stu-id="54345-211">Depends</span></span> | <span data-ttu-id="54345-212">Si l’élément de données est contenu dans un type de contrôle [DataGrid](uiauto-supportdatagridcontroltype.md) qui a un élément d’en-tête, il doit prendre en charge le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="54345-212">If the data item is contained within a [DataGrid](uiauto-supportdatagridcontroltype.md) control type that has a header element, it should support the [TableItem](uiauto-implementingtableitem.md) control pattern.</span></span> |
| [<span data-ttu-id="54345-213">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="54345-213">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="54345-214">Dépend</span><span class="sxs-lookup"><span data-stu-id="54345-214">Depends</span></span> | <span data-ttu-id="54345-215">Si l’élément de données contient un État qui peut être parcouru, il doit prendre en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="54345-215">If the data item contains a state that can be cycled through, it should support the [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span>                                                                          |
| [<span data-ttu-id="54345-216">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="54345-216">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)                   | <span data-ttu-id="54345-217">Dépend</span><span class="sxs-lookup"><span data-stu-id="54345-217">Depends</span></span> | <span data-ttu-id="54345-218">Si le texte principal de l’élément de données est modifiable, le modèle de contrôle [value](uiauto-implementingvalue.md) doit être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="54345-218">If the data item's primary text is editable, the [Value](uiauto-implementingvalue.md) control pattern must be supported.</span></span>                                                                                             |



 

## <a name="working-with-dataitems-in-large-lists"></a><span data-ttu-id="54345-219">Utilisation de DataItems dans des listes volumineuses</span><span class="sxs-lookup"><span data-stu-id="54345-219">Working with DataItems in Large Lists</span></span>

<span data-ttu-id="54345-220">Étant donné que les listes volumineuses sont souvent virtualisées dans des infrastructures d’interface utilisateur pour aider à améliorer les performances, un client UI Automation ne peut pas utiliser la fonctionnalité de requête UI Automation pour rechercher le contenu de l’arborescence complète de la même façon que dans d’autres conteneurs d’éléments.</span><span class="sxs-lookup"><span data-stu-id="54345-220">Because large lists are often virtualized within UI frameworks to assist in performance, a UI Automation client cannot use the UI Automation query feature to search the contents of the full tree in the same way that it can in other item containers.</span></span> <span data-ttu-id="54345-221">Un client doit faire défiler l’élément dans l’affichage (ou développer le contrôle pour afficher toutes les options disponibles) avant d’accéder à l’ensemble complet d’informations de l’élément de données.</span><span class="sxs-lookup"><span data-stu-id="54345-221">A client should scroll the item into view (or expand the control to show all available options) prior to accessing the full set of information from the data item.</span></span>

<span data-ttu-id="54345-222">Lors de l’appel de [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) sur l’élément UI Automation pour l’élément de données, l’Explorateur Microsoft Windows est retourné avec succès et a pour effet de définir le focus sur le contrôle d’édition dans la sous-arborescence d’éléments de données.</span><span class="sxs-lookup"><span data-stu-id="54345-222">When calling [**SetFocus**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-setfocus) on the UI Automation element for the data item, Microsoft Windows Explorer returns successfully and causes focus to be set to the Edit control within the data item subtree.</span></span>

## <a name="required-events"></a><span data-ttu-id="54345-223">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="54345-223">Required Events</span></span>

<span data-ttu-id="54345-224">Le tableau suivant répertorie les événements UI Automation que les contrôles d’élément de données doivent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="54345-224">The following table lists the UI Automation events that data item controls are required to support.</span></span> <span data-ttu-id="54345-225">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="54345-225">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="54345-226">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="54345-226">UI Automation Event</span></span>                                                                                                                                                | <span data-ttu-id="54345-227">Notes</span><span class="sxs-lookup"><span data-stu-id="54345-227">Notes</span></span>                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="54345-228">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="54345-228">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                                   |                                                                                                                                  |
| <span data-ttu-id="54345-229">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-229">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                              |                                                                                                                                  |
| <span data-ttu-id="54345-230">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ExpandCollapseExpandCollapseStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-230">[**UIA\_ExpandCollapseExpandCollapseStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="54345-231">Si le contrôle prend en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-231">If the control supports the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern, it must support this event.</span></span> |
| [<span data-ttu-id="54345-232">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="54345-232">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                                                  | <span data-ttu-id="54345-233">Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-233">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="54345-234">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-234">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                              | <span data-ttu-id="54345-235">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-235">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>         |
| <span data-ttu-id="54345-236">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-236">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                          | <span data-ttu-id="54345-237">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-237">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>       |
| <span data-ttu-id="54345-238">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété ItemStatusPropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-238">[**UIA\_ItemStatusPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                            | <span data-ttu-id="54345-239">Si le contrôle prend en charge la propriété [**ItemStatus**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-239">If the control supports the [**ItemStatus**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>        |
| <span data-ttu-id="54345-240">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-240">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                                        |                                                                                                                                  |
| [<span data-ttu-id="54345-241">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="54345-241">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)                                    | <span data-ttu-id="54345-242">Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-242">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="54345-243">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="54345-243">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="54345-244">Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-244">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="54345-245">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="54345-245">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                                                    | <span data-ttu-id="54345-246">Si le contrôle prend en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-246">If the control supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern, it must support this event.</span></span>   |
| [<span data-ttu-id="54345-247">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="54345-247">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                               |                                                                                                                                  |
| <span data-ttu-id="54345-248">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-248">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                 | <span data-ttu-id="54345-249">Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-249">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>                 |
| <span data-ttu-id="54345-250">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="54345-250">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                               | <span data-ttu-id="54345-251">Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="54345-251">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>                   |



 

## <a name="dataitem-control-type-example"></a><span data-ttu-id="54345-252">Exemple de type de contrôle DataItem</span><span class="sxs-lookup"><span data-stu-id="54345-252">DataItem Control Type Example</span></span>

<span data-ttu-id="54345-253">L’image suivante illustre un type de contrôle DataItem dans un contrôle List-View.</span><span class="sxs-lookup"><span data-stu-id="54345-253">The following image illustrates a DataItem control type in a list-view control.</span></span>

![capture d’écran du contrôle List-View avec le type de contrôle DataItem](images/dataitemxmpl.jpg)

<span data-ttu-id="54345-255">L’affichage de contrôle et l’affichage de contenu de l’arborescence UI Automation relative au contrôle d’élément de données sont affichés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="54345-255">The control view and the content view of the UI Automation tree that pertains to the data item control is displayed below.</span></span> <span data-ttu-id="54345-256">Les modèles de contrôle de chaque élément Automation sont indiqués entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="54345-256">The control patterns for each automation element are shown in parentheses.</span></span> <span data-ttu-id="54345-257">Le **groupe** « contoso » fait également partie de la grille du contrôle hôte de grille de données.</span><span class="sxs-lookup"><span data-stu-id="54345-257">The **Group** "Contoso" is also part of the grid of the data grid host control.</span></span> <span data-ttu-id="54345-258">Pour obtenir un exemple d’une structure de grille de niveau supérieur, consultez [type de contrôle DataGrid](uiauto-supportdatagridcontroltype.md).</span><span class="sxs-lookup"><span data-stu-id="54345-258">For an example of a higher level grid structure, see [DataGrid Control Type](uiauto-supportdatagridcontroltype.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="54345-259">Arborescence UI Automation-vue de contrôle</span><span class="sxs-lookup"><span data-stu-id="54345-259">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="54345-260">Arborescence UI Automation-affichage du contenu</span><span class="sxs-lookup"><span data-stu-id="54345-260">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="54345-261">Groupe &quot; Contoso &quot; (table, grille)</span><span class="sxs-lookup"><span data-stu-id="54345-261">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="54345-262">&quot;Receivable.docde comptes DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="54345-262">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="54345-263">Comptes d’images &quot; Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="54345-263">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="54345-264">Modifier le &quot; nom &quot; (TableItem, GridItem, value &quot; Accounts Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="54345-264">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="54345-265">Modifier la &quot; date &quot; de modification (TableItem, GridItem, valeur &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="54345-265">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="54345-266">Modifier la &quot; taille &quot; (GridItem, TableItem, valeur &quot; 11,0 Ko &quot; )</span><span class="sxs-lookup"><span data-stu-id="54345-266">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="54345-267">&quot;Payable.docde comptes DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="54345-267">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="54345-268">...</span><span class="sxs-lookup"><span data-stu-id="54345-268">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="54345-269">Groupe &quot; Contoso &quot; (table, grille)</span><span class="sxs-lookup"><span data-stu-id="54345-269">Group &quot;Contoso&quot; (Table, Grid)</span></span>
<ul>
<li><span data-ttu-id="54345-270">&quot;Receivable.docde comptes DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="54345-270">DataItem &quot;Accounts Receivable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="54345-271">Comptes d’images &quot; Receivable.doc&quot;</span><span class="sxs-lookup"><span data-stu-id="54345-271">Image &quot;Accounts Receivable.doc&quot;</span></span></li>
<li><span data-ttu-id="54345-272">Modifier le &quot; nom &quot; (TableItem, GridItem, value &quot; Accounts Receivable.doc&quot; )</span><span class="sxs-lookup"><span data-stu-id="54345-272">Edit &quot;Name&quot; (TableItem, GridItem, Value &quot;Accounts Receivable.doc&quot;)</span></span></li>
<li><span data-ttu-id="54345-273">Modifier la &quot; date &quot; de modification (TableItem, GridItem, valeur &quot; 8/25/2006 3:29 PM &quot; )</span><span class="sxs-lookup"><span data-stu-id="54345-273">Edit &quot;Date modified&quot; (TableItem, GridItem, Value &quot;8/25/2006 3:29 PM&quot;)</span></span></li>
<li><span data-ttu-id="54345-274">Modifier la &quot; taille &quot; (GridItem, TableItem, valeur &quot; 11,0 Ko &quot; )</span><span class="sxs-lookup"><span data-stu-id="54345-274">Edit &quot;Size&quot; (GridItem, TableItem, Value &quot;11.0 KB&quot;)</span></span></li>
</ul></li>
<li><span data-ttu-id="54345-275">&quot;Payable.docde comptes DataItem &quot; (TableItem, GridItem, SelectionItem, Invoke)</span><span class="sxs-lookup"><span data-stu-id="54345-275">DataItem &quot;Accounts Payable.doc&quot; (TableItem, GridItem, SelectionItem, Invoke)</span></span>
<ul>
<li><span data-ttu-id="54345-276">...</span><span class="sxs-lookup"><span data-stu-id="54345-276">...</span></span></li>
</ul></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="54345-277">Si une grille représente une liste d’éléments sélectionnables, les éléments d’interface utilisateur sélectionnables correspondants peuvent être exposés avec le type de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) au lieu du type de contrôle DataItem.</span><span class="sxs-lookup"><span data-stu-id="54345-277">If a grid represents a list of selectable items, the corresponding selectable UI elements can be exposed with the [ListItem](uiauto-supportlistitemcontroltype.md) control type instead of the DataItem control type.</span></span> <span data-ttu-id="54345-278">Dans l’exemple précédent, les éléments **DataItem** (« accounts Receivable.doc » et « accounts Payable.doc ») sous **Group** (« contoso ») peuvent être améliorés en les exposant en tant que types de contrôle ListItem, car ce type prend déjà en charge le modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) .</span><span class="sxs-lookup"><span data-stu-id="54345-278">In the preceding example, the **DataItem** elements ("Accounts Receivable.doc" and "Accounts Payable.doc") under **Group** ("Contoso") can be improved by exposing them as ListItem control types because that type already supports the [SelectionItem](uiauto-implementingselectionitem.md) control pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="54345-279">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="54345-279">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="54345-280">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="54345-280">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="54345-281">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="54345-281">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="54345-282">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="54345-282">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




