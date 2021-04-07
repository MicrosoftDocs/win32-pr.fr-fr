---
title: DataGrid (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle DataGrid.
ms.assetid: 2381b302-37d6-4159-bb7d-862ae41af695
keywords:
- UI Automation, prise en charge du type de contrôle DataGrid
- UI Automation, type de contrôle DataGrid
- UI Automation, arborescence pour le type de contrôle DataGrid
- UI Automation, propriétés du type de contrôle DataGrid
- UI Automation, modèles de contrôle pour le type de contrôle DataGrid
- UI Automation, événements pour le type de contrôle DataGrid
- arborescences, type de contrôle DataGrid
- Propriétés, DataGrid (type de contrôle)
- modèles de contrôle, type de contrôle DataGrid
- événements, type de contrôle DataGrid
- prise en charge du type de contrôle DataGrid
- DataGrid (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle DataGrid
- types de contrôles, modèles de contrôle pour le type de contrôle DataGrid
- types de contrôles, prise en charge de DataGrid
- types de contrôles, DataGrid
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8af1e35e062c778285d1cb7edcca9ac6192792b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939899"
---
# <a name="datagrid-control-type"></a><span data-ttu-id="c1f72-119">DataGrid (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="c1f72-119">DataGrid Control Type</span></span>

<span data-ttu-id="c1f72-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="c1f72-120">This topic provides information about Microsoft UI Automation support for the **DataGrid** control type.</span></span>

<span data-ttu-id="c1f72-121">Le type de contrôle **DataGrid** permet à un utilisateur de travailler facilement avec des éléments qui contiennent des données ou des éléments d’automatisation présentés dans des colonnes ou des lignes.</span><span class="sxs-lookup"><span data-stu-id="c1f72-121">The **DataGrid** control type lets a user easily work with items that contain data or automation elements presented in columns or rows.</span></span> <span data-ttu-id="c1f72-122">Les contrôles de grille de données présentent des lignes d’éléments et des colonnes d’informations sur ces éléments.</span><span class="sxs-lookup"><span data-stu-id="c1f72-122">Data grid controls have rows of items and columns of information about those items.</span></span> <span data-ttu-id="c1f72-123">Un contrôle List-View dans l’Explorateur Windows Vista est un exemple qui prend en charge le type de contrôle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="c1f72-123">A list-view control in Windows Vista Explorer is an example that supports the **DataGrid** control type.</span></span>

<span data-ttu-id="c1f72-124">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="c1f72-124">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **DataGrid** control type.</span></span> <span data-ttu-id="c1f72-125">Les exigences d’UI Automation s’appliquent à tous les contrôles de grille de données où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="c1f72-125">The UI Automation requirements apply to all data grid controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="c1f72-126">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="c1f72-126">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="c1f72-127">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="c1f72-127">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="c1f72-128">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="c1f72-128">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="c1f72-129">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="c1f72-129">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="c1f72-130">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="c1f72-130">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="c1f72-131">Exemple de type de contrôle DataGrid</span><span class="sxs-lookup"><span data-stu-id="c1f72-131">DataGrid Control Type Example</span></span>](#datagrid-control-type-example)
-   [<span data-ttu-id="c1f72-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1f72-132">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="c1f72-133">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="c1f72-133">Typical Tree Structure</span></span>

<span data-ttu-id="c1f72-134">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation relative aux contrôles de grille de données, et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="c1f72-134">The following table depicts a typical control and content view of the UI Automation tree that pertains to data grid controls and describes what can be contained in each view.</span></span> <span data-ttu-id="c1f72-135">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c1f72-135">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1f72-136">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="c1f72-136">Control View</span></span></th>
<th><span data-ttu-id="c1f72-137">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="c1f72-137">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="c1f72-138">DataGrid</span><span class="sxs-lookup"><span data-stu-id="c1f72-138">DataGrid</span></span>
<ul>
<li><span data-ttu-id="c1f72-139">Header (0, 1 ou 2)</span><span class="sxs-lookup"><span data-stu-id="c1f72-139">Header (0, 1, or 2)</span></span>
<ul>
<li><span data-ttu-id="c1f72-140">HeaderItem (nombre de lignes ou colonnes)</span><span class="sxs-lookup"><span data-stu-id="c1f72-140">HeaderItem (number of columns or rows)</span></span></li>
</ul></li>
<li><span data-ttu-id="c1f72-141">DataItem (0 ou plus ; peut être structuré dans une hiérarchie)</span><span class="sxs-lookup"><span data-stu-id="c1f72-141">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="c1f72-142">DataGrid</span><span class="sxs-lookup"><span data-stu-id="c1f72-142">DataGrid</span></span>
<ul>
<li><span data-ttu-id="c1f72-143">DataItem (0 ou plus ; peut être structuré dans une hiérarchie)</span><span class="sxs-lookup"><span data-stu-id="c1f72-143">DataItem (0 or more; can be structured in a hierarchy)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="c1f72-144">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="c1f72-144">Relevant Properties</span></span>

<span data-ttu-id="c1f72-145">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour le type de contrôle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="c1f72-145">The following table lists the UI Automation properties whose value or definition is especially relevant to the **DataGrid** control type.</span></span> <span data-ttu-id="c1f72-146">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="c1f72-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="c1f72-147">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="c1f72-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="c1f72-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="c1f72-148">Value</span></span>        | <span data-ttu-id="c1f72-149">Notes</span><span class="sxs-lookup"><span data-stu-id="c1f72-149">Notes</span></span>                                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1f72-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="c1f72-151">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="c1f72-151">See notes.</span></span>   | <span data-ttu-id="c1f72-152">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c1f72-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                 |
| [<span data-ttu-id="c1f72-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="c1f72-154">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="c1f72-154">See notes.</span></span>   | <span data-ttu-id="c1f72-155">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="c1f72-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="c1f72-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="c1f72-157">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="c1f72-157">See notes.</span></span>   | <span data-ttu-id="c1f72-158">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="c1f72-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="c1f72-159">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="c1f72-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                         |
| [<span data-ttu-id="c1f72-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="c1f72-161">**DataGrid**</span><span class="sxs-lookup"><span data-stu-id="c1f72-161">**DataGrid**</span></span> |                                                                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="c1f72-162">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-162">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c1f72-163">TRUE</span><span class="sxs-lookup"><span data-stu-id="c1f72-163">TRUE</span></span>         | <span data-ttu-id="c1f72-164">La valeur de cette propriété doit toujours être **true**.</span><span class="sxs-lookup"><span data-stu-id="c1f72-164">The value of this property must always be **TRUE**.</span></span> <span data-ttu-id="c1f72-165">Cela signifie que le contrôle de grille de données doit toujours être dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c1f72-165">This means that the data grid control must always be in the content view of the UI Automation tree.</span></span>                                                                                                                                                      |
| [<span data-ttu-id="c1f72-166">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-166">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="c1f72-167">TRUE</span><span class="sxs-lookup"><span data-stu-id="c1f72-167">TRUE</span></span>         | <span data-ttu-id="c1f72-168">La valeur de cette propriété doit toujours être **true**.</span><span class="sxs-lookup"><span data-stu-id="c1f72-168">The value of this property must always **TRUE**.</span></span> <span data-ttu-id="c1f72-169">Cela signifie que le contrôle de grille de données doit toujours être inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="c1f72-169">This means that the data grid control must always be included in the control view of the UI Automation tree.</span></span>                                                                                                                                                |
| [<span data-ttu-id="c1f72-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="c1f72-171">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="c1f72-171">See notes.</span></span>   | <span data-ttu-id="c1f72-172">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="c1f72-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                    |
| [<span data-ttu-id="c1f72-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="c1f72-174">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="c1f72-174">See notes.</span></span>   | <span data-ttu-id="c1f72-175">S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="c1f72-175">If there is a static text label, this property must expose a reference to that control.</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="c1f72-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="c1f72-177">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="c1f72-177">See notes.</span></span>   | <span data-ttu-id="c1f72-178">Chaîne localisée correspondant au type de contrôle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="c1f72-178">Localized string corresponding to the **DataGrid** control type.</span></span> <span data-ttu-id="c1f72-179">La valeur par défaut est « Data Grid » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="c1f72-179">The default value is "data grid" for en-US or English (United States).</span></span>                                                                                                                                                                      |
| [<span data-ttu-id="c1f72-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="c1f72-181">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="c1f72-181">See notes.</span></span>   | <span data-ttu-id="c1f72-182">Le contrôle de grille de données obtient généralement la valeur de sa propriété **Name** à partir d’une étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="c1f72-182">The data grid control typically gets the value for its **Name** property from a static text label.</span></span> <span data-ttu-id="c1f72-183">S’il n’y a pas d’étiquette de texte statique, un développeur d’applications doit attribuer une valeur à pour la propriété **Name** .</span><span class="sxs-lookup"><span data-stu-id="c1f72-183">If there is not a static text label an application developer must assign a value to for the **Name** property.</span></span> <span data-ttu-id="c1f72-184">La valeur de la propriété **Name** ne doit jamais être le contenu textuel du contrôle d’édition.</span><span class="sxs-lookup"><span data-stu-id="c1f72-184">The value of the **Name** property must never be the textual contents of the edit control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="c1f72-185">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="c1f72-185">Required Control Patterns</span></span>

<span data-ttu-id="c1f72-186">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de grille de données.</span><span class="sxs-lookup"><span data-stu-id="c1f72-186">The following table lists the UI Automation control patterns required to be supported by all data grid controls.</span></span> <span data-ttu-id="c1f72-187">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c1f72-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="c1f72-188">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="c1f72-188">Control Pattern</span></span>                                         | <span data-ttu-id="c1f72-189">Support</span><span class="sxs-lookup"><span data-stu-id="c1f72-189">Support</span></span>  | <span data-ttu-id="c1f72-190">Notes</span><span class="sxs-lookup"><span data-stu-id="c1f72-190">Notes</span></span>                                                                                                                                                                             |
|---------------------------------------------------------|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1f72-191">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="c1f72-191">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="c1f72-192">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="c1f72-192">Required</span></span> | <span data-ttu-id="c1f72-193">Le contrôle de grille de données lui-même prend toujours en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) , car les éléments qu’il contient ont des métadonnées disposées dans une grille.</span><span class="sxs-lookup"><span data-stu-id="c1f72-193">The data grid control itself always supports the [Grid](uiauto-implementinggrid.md) control pattern because the items that it contains have metadata that is laid out in a grid.</span></span> |
| [<span data-ttu-id="c1f72-194">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="c1f72-194">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider)       | <span data-ttu-id="c1f72-195">Dépend</span><span class="sxs-lookup"><span data-stu-id="c1f72-195">Depends</span></span>  | <span data-ttu-id="c1f72-196">La possibilité de faire défiler la grille de données dépend du contenu et de la présence de barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-196">The ability to scroll the data grid depends on content and whether scroll bars are present.</span></span>                                                                                       |
| [<span data-ttu-id="c1f72-197">**ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="c1f72-197">**ISelectionProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) | <span data-ttu-id="c1f72-198">Dépend</span><span class="sxs-lookup"><span data-stu-id="c1f72-198">Depends</span></span>  | <span data-ttu-id="c1f72-199">La possibilité de sélectionner la grille de données dépend du contenu.</span><span class="sxs-lookup"><span data-stu-id="c1f72-199">The ability to select the data grid depends on content.</span></span>                                                                                                                           |
| [<span data-ttu-id="c1f72-200">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="c1f72-200">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="c1f72-201">Dépend</span><span class="sxs-lookup"><span data-stu-id="c1f72-201">Depends</span></span>  | <span data-ttu-id="c1f72-202">Un contrôle de grille de données qui possède un en-tête doit prendre en charge le modèle de contrôle [table](uiauto-implementingtable.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f72-202">A data grid control that has a header should support the [Table](uiauto-implementingtable.md) control pattern.</span></span>                                                                   |



 

<span data-ttu-id="c1f72-203">Les éléments de données dans les conteneurs de grille de données prennent en charge au minimum ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="c1f72-203">Data items within the data grid containers will support at a minimum:</span></span>

-   <span data-ttu-id="c1f72-204">Modèle de contrôle [SelectionItem](uiauto-implementingselectionitem.md) (si la grille de données est sélectionnable)</span><span class="sxs-lookup"><span data-stu-id="c1f72-204">[SelectionItem](uiauto-implementingselectionitem.md) control pattern (if the data grid is selectable)</span></span>
-   <span data-ttu-id="c1f72-205">Modèle de contrôle [ScrollItem](uiauto-implementingscrollitem.md) (si la grille de données est défilante)</span><span class="sxs-lookup"><span data-stu-id="c1f72-205">[ScrollItem](uiauto-implementingscrollitem.md) control pattern (if the data grid is scrollable)</span></span>
-   <span data-ttu-id="c1f72-206">[GridItem](uiauto-implementinggriditem.md) (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="c1f72-206">[GridItem](uiauto-implementinggriditem.md) control pattern</span></span>
-   <span data-ttu-id="c1f72-207">Modèle de contrôle [TableItem](uiauto-implementingtableitem.md) (si la grille de données a un en-tête)</span><span class="sxs-lookup"><span data-stu-id="c1f72-207">[TableItem](uiauto-implementingtableitem.md) control pattern (if the data grid has a header)</span></span>

## <a name="required-events"></a><span data-ttu-id="c1f72-208">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="c1f72-208">Required Events</span></span>

<span data-ttu-id="c1f72-209">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de grille de données.</span><span class="sxs-lookup"><span data-stu-id="c1f72-209">The following table lists the UI Automation events that data grid controls are required to support.</span></span> <span data-ttu-id="c1f72-210">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="c1f72-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="c1f72-211">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="c1f72-211">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="c1f72-212">Notes</span><span class="sxs-lookup"><span data-stu-id="c1f72-212">Notes</span></span>                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c1f72-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                                                          |
| <span data-ttu-id="c1f72-214">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                                                          |
| <span data-ttu-id="c1f72-215">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="c1f72-216">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                                 |
| <span data-ttu-id="c1f72-217">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="c1f72-218">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>                               |
| [<span data-ttu-id="c1f72-219">**UIA \_ LayoutInvalidatedEventId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-219">**UIA\_LayoutInvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                                     |                                                                                                                                                          |
| [<span data-ttu-id="c1f72-220">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="c1f72-220">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                                                          |
| <span data-ttu-id="c1f72-221">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété MultipleViewCurrentViewPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-221">[**UIA\_MultipleViewCurrentViewPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>             | <span data-ttu-id="c1f72-222">Si le contrôle prend en charge la propriété CurrentView du modèle de contrôle [MultipleView](uiauto-implementingmultipleview.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-222">If the control supports the CurrentView property of the [MultipleView](uiauto-implementingmultipleview.md) control pattern, it must support this event.</span></span> |
| <span data-ttu-id="c1f72-223">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-223">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="c1f72-224">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-224">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="c1f72-225">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-225">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="c1f72-226">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-226">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="c1f72-227">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-227">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="c1f72-228">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-228">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="c1f72-229">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-229">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="c1f72-230">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-230">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="c1f72-231">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-231">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="c1f72-232">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-232">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| <span data-ttu-id="c1f72-233">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="c1f72-233">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="c1f72-234">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="c1f72-234">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>                                         |
| [<span data-ttu-id="c1f72-235">**\_InvalidatedEventId de sélection UIA \_**</span><span class="sxs-lookup"><span data-stu-id="c1f72-235">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            |                                                                                                                                                          |



 

## <a name="datagrid-control-type-example"></a><span data-ttu-id="c1f72-236">Exemple de type de contrôle DataGrid</span><span class="sxs-lookup"><span data-stu-id="c1f72-236">DataGrid Control Type Example</span></span>

<span data-ttu-id="c1f72-237">L’image suivante illustre un contrôle List-View qui implémente le type de contrôle **DataGrid** .</span><span class="sxs-lookup"><span data-stu-id="c1f72-237">The following image illustrates a list-view control that implements the **DataGrid** control type.</span></span>

![capture d’écran du contrôle List-View avec le type de contrôle DataGrid](images/datagridxmpl.jpg)

<span data-ttu-id="c1f72-239">L’affichage de contrôle et l’affichage de contenu de l’arborescence UI Automation relative au contrôle d’affichage de liste sont affichés ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="c1f72-239">The control view and the content view of the UI Automation tree that pertains to the list-view control is displayed below.</span></span> <span data-ttu-id="c1f72-240">Les modèles de contrôle de chaque élément Automation sont indiqués entre parenthèses.</span><span class="sxs-lookup"><span data-stu-id="c1f72-240">The control patterns for each automation element are shown in parentheses.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1f72-241">Arborescence UI Automation-vue de contrôle</span><span class="sxs-lookup"><span data-stu-id="c1f72-241">UI Automation Tree - Control View</span></span></th>
<th><span data-ttu-id="c1f72-242">Arborescence UI Automation-affichage du contenu</span><span class="sxs-lookup"><span data-stu-id="c1f72-242">UI Automation Tree - Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1f72-243">DataGrid (tri, table, sélection, grille)</span><span class="sxs-lookup"><span data-stu-id="c1f72-243">DataGrid (Sort, Table, Selection, Grid)</span></span>
<ul>
<li><span data-ttu-id="c1f72-244">En-tête</span><span class="sxs-lookup"><span data-stu-id="c1f72-244">Header</span></span>
<ul>
<li><span data-ttu-id="c1f72-245">&quot;Nom &quot; de HeaderItem (Invoke)</span><span class="sxs-lookup"><span data-stu-id="c1f72-245">HeaderItem &quot;Name&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="c1f72-246">HeaderItem &quot; date &quot; de modification (Invoke)</span><span class="sxs-lookup"><span data-stu-id="c1f72-246">HeaderItem &quot;Date Modified&quot; (Invoke)</span></span></li>
<li><span data-ttu-id="c1f72-247">&quot;Taille HeaderItem &quot; (Invoke)</span><span class="sxs-lookup"><span data-stu-id="c1f72-247">HeaderItem &quot;Size&quot; (Invoke)</span></span></li>
</ul></li>
<li><span data-ttu-id="c1f72-248">Groupe &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, table *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="c1f72-248">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="c1f72-249">&quot;Receivable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="c1f72-249">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="c1f72-250">&quot;Payable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="c1f72-250">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
<td><span data-ttu-id="c1f72-251">DataGrid (Table, Grid, Selection)</span><span class="sxs-lookup"><span data-stu-id="c1f72-251">DataGrid (Table, Grid, Selection)</span></span>
<ul>
<li><span data-ttu-id="c1f72-252">Groupe &quot; Contoso &quot; (TableItem, GridItem, SelectionItem, table *, Grid*)</span><span class="sxs-lookup"><span data-stu-id="c1f72-252">Group &quot;Contoso&quot; (TableItem, GridItem, SelectionItem, Table *, Grid*)</span></span>
<ul>
<li><span data-ttu-id="c1f72-253">&quot;Receivable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="c1f72-253">DataItem &quot;Accounts Receivable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
<li><span data-ttu-id="c1f72-254">&quot;Payable.docde comptes DataItem &quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span><span class="sxs-lookup"><span data-stu-id="c1f72-254">DataItem &quot;Accounts Payable.doc&quot; (SelectionItem, Invoke, TableItem *, GridItem*)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c1f72-255">\*L’exemple précédent montre une grille de données qui contient plusieurs niveaux de contrôles.</span><span class="sxs-lookup"><span data-stu-id="c1f72-255">\*The preceding example shows a data grid that contains multiple levels of controls.</span></span> <span data-ttu-id="c1f72-256">Le contrôle **Group** (« contoso ») contient deux contrôles **DataItem** (« Accounts Receivable.doc » et « Accounts Payable.doc »).</span><span class="sxs-lookup"><span data-stu-id="c1f72-256">The **Group** ("Contoso") control contains two **DataItem** controls ("Accounts Receivable.doc" and "Accounts Payable.doc").</span></span> <span data-ttu-id="c1f72-257">Une paire **DataGrid de DataGrid** /  est indépendante d’une paire à un autre niveau.</span><span class="sxs-lookup"><span data-stu-id="c1f72-257">A **DataGrid**/**GridItem** pair is independent of a pair at another level.</span></span> <span data-ttu-id="c1f72-258">Les contrôles **DataItem** sous un **groupe** peuvent également être exposés en tant que type de contrôle [ListItem](uiauto-supportlistitemcontroltype.md) , ce qui leur permet d’être présentés plus clairement comme des objets sélectionnables, plutôt que comme des éléments de données simples.</span><span class="sxs-lookup"><span data-stu-id="c1f72-258">The **DataItem** controls under a **Group** can also be exposed as a [ListItem](uiauto-supportlistitemcontroltype.md) control type, enabling them to be presented more clearly as selectable objects, rather than as simple data elements.</span></span> <span data-ttu-id="c1f72-259">Cet exemple n’inclut pas les sous-éléments des éléments de données groupés.</span><span class="sxs-lookup"><span data-stu-id="c1f72-259">This example does not include the sub-elements of the grouped data items.</span></span> <span data-ttu-id="c1f72-260">Pour un autre exemple de plusieurs niveaux de contrôles, consultez le type de contrôle [DataItem](uiauto-supportdataitemcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="c1f72-260">For another example of multiple levels of controls, see the [DataItem](uiauto-supportdataitemcontroltype.md) control type.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c1f72-261">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c1f72-261">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c1f72-262">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="c1f72-262">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c1f72-263">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="c1f72-263">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="c1f72-264">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="c1f72-264">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




