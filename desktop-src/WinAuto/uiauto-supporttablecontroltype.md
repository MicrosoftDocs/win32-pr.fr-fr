---
title: Table (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle table.
ms.assetid: 508db2af-1ca3-4003-8e1f-6e225cf79b7a
keywords:
- UI Automation, prise en charge du type de contrôle table
- UI Automation, type de contrôle table
- UI Automation, arborescence pour le type de contrôle table
- UI Automation, propriétés du type de contrôle table
- UI Automation, modèles de contrôle pour le type de contrôle table
- UI Automation, événements pour le type de contrôle table
- arborescences, type de contrôle table
- Propriétés, table (type de contrôle)
- modèles de contrôle, table (type de contrôle)
- événements, type de contrôle table
- prise en charge du type de contrôle table
- Table (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle table
- types de contrôle, modèles de contrôle pour le type de contrôle table
- types de contrôles, prise en charge de table
- types de contrôles, table
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb4ee709bd16156a62882aeee014b4744dab2214
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507339"
---
# <a name="table-control-type"></a><span data-ttu-id="55122-119">Table (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="55122-119">Table Control Type</span></span>

<span data-ttu-id="55122-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **table** .</span><span class="sxs-lookup"><span data-stu-id="55122-120">This topic provides information about Microsoft UI Automation support for the **Table** control type.</span></span>

<span data-ttu-id="55122-121">Les contrôles de table contiennent des lignes et des colonnes de texte et, éventuellement, des en-têtes de ligne et des en-têtes de colonnes.</span><span class="sxs-lookup"><span data-stu-id="55122-121">Table controls contain rows and columns of text and, optionally, row headers and column headers.</span></span>

<span data-ttu-id="55122-122">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **table** .</span><span class="sxs-lookup"><span data-stu-id="55122-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Table** control type.</span></span> <span data-ttu-id="55122-123">Les exigences d’UI Automation s’appliquent à tous les contrôles de table où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="55122-123">The UI Automation requirements apply to all table controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="55122-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="55122-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="55122-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="55122-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="55122-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="55122-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="55122-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="55122-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="55122-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="55122-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="55122-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55122-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="55122-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="55122-130">Typical Tree Structure</span></span>

<span data-ttu-id="55122-131">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de table, et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="55122-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to table controls and describes what can be contained in each view.</span></span> <span data-ttu-id="55122-132">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55122-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55122-133">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="55122-133">Control View</span></span></th>
<th><span data-ttu-id="55122-134">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="55122-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="55122-135">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="55122-135">Table</span></span>
<ul>
<li><span data-ttu-id="55122-136">Text (0 ou 1)</span><span class="sxs-lookup"><span data-stu-id="55122-136">Text (0 or 1)</span></span></li>
<li><span data-ttu-id="55122-137">En-tête (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="55122-137">Header (0 or more)</span></span></li>
<li><span data-ttu-id="55122-138">Plusieurs contrôles (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="55122-138">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="55122-139">Table de charge de travail</span><span class="sxs-lookup"><span data-stu-id="55122-139">Table</span></span>
<ul>
<li><span data-ttu-id="55122-140">Texte (1 ou plus)</span><span class="sxs-lookup"><span data-stu-id="55122-140">Text (1 or more)</span></span></li>
<li><span data-ttu-id="55122-141">Plusieurs contrôles (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="55122-141">Various controls (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="55122-142">Si un contrôle de table possède des en-têtes de lignes ou de colonnes, ceux-ci doivent être exposés dans la vue de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="55122-142">If a table control has row or column headers, they must be exposed in the control view of the UI Automation tree.</span></span> <span data-ttu-id="55122-143">L’affichage du contenu n’a pas besoin d’exposer ces informations, car elles sont accessibles à l’aide de [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span><span class="sxs-lookup"><span data-stu-id="55122-143">The content view does not need to expose this information because it can be accessed using [**IUIAutomationTablePattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtablepattern).</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="55122-144">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="55122-144">Relevant Properties</span></span>

<span data-ttu-id="55122-145">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de table.</span><span class="sxs-lookup"><span data-stu-id="55122-145">The following table lists the UI Automation properties whose value or definition is especially relevant to table controls.</span></span> <span data-ttu-id="55122-146">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="55122-146">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="55122-147">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="55122-147">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="55122-148">Valeur</span><span class="sxs-lookup"><span data-stu-id="55122-148">Value</span></span>      | <span data-ttu-id="55122-149">Notes</span><span class="sxs-lookup"><span data-stu-id="55122-149">Notes</span></span>                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55122-150">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-150">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="55122-151">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-151">See notes.</span></span> | <span data-ttu-id="55122-152">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="55122-152">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                      |
| [<span data-ttu-id="55122-153">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-153">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="55122-154">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-154">See notes.</span></span> | <span data-ttu-id="55122-155">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="55122-155">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                          |
| [<span data-ttu-id="55122-156">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-156">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="55122-157">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-157">See notes.</span></span> | <span data-ttu-id="55122-158">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="55122-158">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="55122-159">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="55122-159">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                              |
| [<span data-ttu-id="55122-160">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-160">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="55122-161">**Table**</span><span class="sxs-lookup"><span data-stu-id="55122-161">**Table**</span></span>  |                                                                                                                                                                                                                                   |
| [<span data-ttu-id="55122-162">**UIA \_ DescribedByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-162">**UIA\_DescribedByPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="55122-163">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-163">See notes.</span></span> | <span data-ttu-id="55122-164">Si la table est annotée par un autre élément d’interface utilisateur (par exemple, un élément de texte contenant la description de la table), la propriété DescribedBy doit exposer une référence à l’élément Automation du contrôle de texte.</span><span class="sxs-lookup"><span data-stu-id="55122-164">If the table is annotated by other UI element (for example, a text element that holds the description for the table), the DescribedBy property should expose a reference to the automation element of the text control.</span></span>           |
| [<span data-ttu-id="55122-165">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-165">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="55122-166">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-166">See notes.</span></span> | <span data-ttu-id="55122-167">Des détails supplémentaires sur l’objectif de la table doivent être exposés via cette propriété si elle n’est pas suffisamment expliquée par la propriété [**UIA \_ NamePropertyId**](uiauto-automation-element-propids.md) .</span><span class="sxs-lookup"><span data-stu-id="55122-167">More details about the purpose of the table should be exposed through this property if it is not sufficiently explained by the [**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property.</span></span>      |
| [<span data-ttu-id="55122-168">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-168">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="55122-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="55122-169">TRUE</span></span>       | <span data-ttu-id="55122-170">Le contrôle de table doit toujours apparaître dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="55122-170">The table control must always appear in the content view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="55122-171">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-171">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="55122-172">TRUE</span><span class="sxs-lookup"><span data-stu-id="55122-172">TRUE</span></span>       | <span data-ttu-id="55122-173">Le contrôle de table doit toujours apparaître dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="55122-173">The table control must always appear in the control view of the UI Automation tree.</span></span>                                                                                                                                               |
| [<span data-ttu-id="55122-174">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-174">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="55122-175">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-175">See notes.</span></span> | <span data-ttu-id="55122-176">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="55122-176">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="55122-177">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-177">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="55122-178">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-178">See notes.</span></span> | <span data-ttu-id="55122-179">S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à l’élément Automation du contrôle.</span><span class="sxs-lookup"><span data-stu-id="55122-179">If there is a static text label, this property should expose a reference to the automation element of the control.</span></span>                                                                                                                |
| [<span data-ttu-id="55122-180">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-180">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="55122-181">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-181">See notes.</span></span> | <span data-ttu-id="55122-182">Chaîne localisée correspondant au type de contrôle **table** .</span><span class="sxs-lookup"><span data-stu-id="55122-182">Localized string corresponding to the **Table** control type.</span></span> <span data-ttu-id="55122-183">La valeur par défaut est « table » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="55122-183">The default value is "table" for en-US or English (United States).</span></span>                                                                                                  |
| [<span data-ttu-id="55122-184">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="55122-184">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="55122-185">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="55122-185">See notes.</span></span> | <span data-ttu-id="55122-186">Le contrôle de table obtient généralement la valeur de son nom à partir d’une étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="55122-186">The table control typically gets the value for its name from a static text label.</span></span> <span data-ttu-id="55122-187">S’il n’y a pas d’étiquette de texte statique, l’élément doit affecter une propriété Name qui doit toujours être disponible pour expliquer l’objectif de la table.</span><span class="sxs-lookup"><span data-stu-id="55122-187">If there is not a static text label, the element must assign a Name property that must always be available to explain the purpose of the table.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="55122-188">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="55122-188">Required Control Patterns</span></span>

<span data-ttu-id="55122-189">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de table.</span><span class="sxs-lookup"><span data-stu-id="55122-189">The following table lists the UI Automation control patterns required to be supported by all table controls.</span></span> <span data-ttu-id="55122-190">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55122-190">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="55122-191">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="55122-191">Control Pattern</span></span>                                         | <span data-ttu-id="55122-192">Support</span><span class="sxs-lookup"><span data-stu-id="55122-192">Support</span></span>                     | <span data-ttu-id="55122-193">Notes</span><span class="sxs-lookup"><span data-stu-id="55122-193">Notes</span></span>                                                                                                                                                                                                                                                                                        |
|---------------------------------------------------------|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55122-194">**IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="55122-194">**IGridProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider)           | <span data-ttu-id="55122-195">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="55122-195">Required</span></span>                    | <span data-ttu-id="55122-196">Étant donné que le contrôle table contient des éléments présentés dans une grille, il prend toujours en charge le modèle de contrôle [Grid](uiauto-implementinggrid.md) .</span><span class="sxs-lookup"><span data-stu-id="55122-196">Because the table control contains items presented in a grid, it always supports the [Grid](uiauto-implementinggrid.md) control pattern.</span></span>                                                                                                                                                    |
| [<span data-ttu-id="55122-197">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="55122-197">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="55122-198">Obligatoire avec les objets enfants</span><span class="sxs-lookup"><span data-stu-id="55122-198">Required with child objects</span></span> | <span data-ttu-id="55122-199">Les objets internes d’une table doivent prendre en charge les modèles de contrôle [GridItem](uiauto-implementinggriditem.md) et [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="55122-199">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="55122-200">La table elle-même n’a pas besoin de prendre en charge le modèle de contrôle GridItem ou TableItem, sauf si la table fait partie d’une autre table.</span><span class="sxs-lookup"><span data-stu-id="55122-200">The table itself need not support the GridItem or TableItem control pattern unless the table is part of another table.</span></span>  |
| [<span data-ttu-id="55122-201">**ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="55122-201">**ITableProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider)         | <span data-ttu-id="55122-202">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="55122-202">Required</span></span>                    | <span data-ttu-id="55122-203">Le contrôle de table peut toujours avoir des en-têtes associés au contenu.</span><span class="sxs-lookup"><span data-stu-id="55122-203">The table control can always have headers associated with the content.</span></span>                                                                                                                                                                                                                       |
| [<span data-ttu-id="55122-204">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="55122-204">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="55122-205">Obligatoire avec les objets enfants</span><span class="sxs-lookup"><span data-stu-id="55122-205">Required with child objects</span></span> | <span data-ttu-id="55122-206">Les objets internes d’une table doivent prendre en charge les modèles de contrôle [GridItem](uiauto-implementinggriditem.md) et [TableItem](uiauto-implementingtableitem.md) .</span><span class="sxs-lookup"><span data-stu-id="55122-206">The inner objects of a table should support both the [GridItem](uiauto-implementinggriditem.md) and [TableItem](uiauto-implementingtableitem.md) control patterns.</span></span> <span data-ttu-id="55122-207">La table elle-même n’a pas besoin de prendre en charge les modèles de contrôle GridItem et TableItem, à moins que la table fasse partie d’une autre table.</span><span class="sxs-lookup"><span data-stu-id="55122-207">The table itself need not support the GridItem or TableItem control patterns unless the table is part of another table.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="55122-208">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="55122-208">Required Events</span></span>

<span data-ttu-id="55122-209">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de table.</span><span class="sxs-lookup"><span data-stu-id="55122-209">The following table lists the UI Automation events that table controls are required to support.</span></span> <span data-ttu-id="55122-210">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="55122-210">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="55122-211">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="55122-211">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="55122-212">Notes</span><span class="sxs-lookup"><span data-stu-id="55122-212">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="55122-213">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="55122-213">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="55122-214">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="55122-214">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="55122-215">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="55122-215">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="55122-216">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="55122-216">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="55122-217">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="55122-217">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="55122-218">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="55122-218">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="55122-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="55122-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="related-topics"></a><span data-ttu-id="55122-220">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="55122-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="55122-221">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="55122-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="55122-222">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="55122-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="55122-223">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="55122-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




