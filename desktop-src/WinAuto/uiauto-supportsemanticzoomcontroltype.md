---
title: Type de contrôle SemanticZoom
description: Cette rubrique fournit des informations sur la prise en charge d’UI Automation pour le type de contrôle SemanticZoom.
ms.assetid: 37C14610-431F-46BF-97B6-CB476EA1642D
keywords:
- UI Automation, prise en charge du type de contrôle SemanticZoom
- UI Automation, type de contrôle SemanticZoom
- UI Automation, arborescence pour le type de contrôle SemanticZoom
- UI Automation, propriétés du type de contrôle SemanticZoom
- UI Automation, modèles de contrôle pour le type de contrôle SemanticZoom
- UI Automation, événements pour le type de contrôle SemanticZoom
- arborescences, type de contrôle SemanticZoom
- Propriétés, type de contrôle SemanticZoom
- modèles de contrôle, type de contrôle SemanticZoom
- événements, type de contrôle SemanticZoom
- prise en charge du type de contrôle SemanticZoom
- Type de contrôle SemanticZoom
- types de contrôles, arborescence pour le type de contrôle SemanticZoom
- types de contrôle, modèles de contrôle pour le type de contrôle SemanticZoom
- types de contrôle, prise en charge de SemanticZoom
- types de contrôles, SemanticZoom
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17d4712aa4f10489081b1b5d0f69fed849080bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101681"
---
# <a name="semanticzoom-control-type"></a><span data-ttu-id="2affa-119">Type de contrôle SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="2affa-119">SemanticZoom Control Type</span></span>

<span data-ttu-id="2affa-120">Cette rubrique fournit des informations sur la prise en charge d’UI Automation pour le type de contrôle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="2affa-120">This topic provides information about UI Automation support for the **SemanticZoom** control type.</span></span>

<span data-ttu-id="2affa-121">Le zoom sémantique est une technique introduite dans Windows 8 pour la présentation et la navigation dans de grands ensembles de données ou de contenu connexes dans une seule vue, par exemple un album photo, une liste d’applications ou un carnet d’adresses.</span><span class="sxs-lookup"><span data-stu-id="2affa-121">Semantic Zoom is a technique introduced in Windows 8 for presenting and navigating large sets of related data or content within a single view, such as a photo album, app list, or address book.</span></span> <span data-ttu-id="2affa-122">Le zoom sémantique utilise deux modes distincts de classification, ou *niveaux de zoom*, pour l’organisation et la présentation du contenu.</span><span class="sxs-lookup"><span data-stu-id="2affa-122">Semantic Zoom uses two distinct modes of classification, or *zoom levels*, for organizing and presenting the content.</span></span> <span data-ttu-id="2affa-123">Le mode de bas niveau (ou *Zoom avant*) affiche les éléments dans une structure « tout-en-un » plat. et le mode de haut niveau (ou *Zoom arrière*) affiche des éléments dans des groupes, ce qui permet à l’utilisateur de parcourir rapidement le contenu.</span><span class="sxs-lookup"><span data-stu-id="2affa-123">The low-level (or *zoomed in*) mode displays items in a flat, "all-up" structure; and the high-level (or *zoomed out*) mode displays items in groups, enabling the user to quickly navigate and browse through the content.</span></span> <span data-ttu-id="2affa-124">Par exemple, le zoom d’une liste de villes peut passer à une liste d’États contenant ces villes.</span><span class="sxs-lookup"><span data-stu-id="2affa-124">For example, zooming a list of cities might change to a list of states containing those cities.</span></span> <span data-ttu-id="2affa-125">Le zoom d’une liste de programmes peut être modifié en une liste de groupes de programmes logiques.</span><span class="sxs-lookup"><span data-stu-id="2affa-125">Zooming a list of programs might change to a list of logical program groups.</span></span>

<span data-ttu-id="2affa-126">Pour plus d’informations sur le zoom sémantique spécifiquement utilisé pour les applications du Windows Store, consultez [instructions pour le zoom sémantique](/windows/uwp/controls-and-patterns/semantic-zoom).</span><span class="sxs-lookup"><span data-stu-id="2affa-126">For more information about Semantic Zoom specifically as used for Windows Store apps, see [Guidelines for Semantic Zoom](/windows/uwp/controls-and-patterns/semantic-zoom).</span></span>

<span data-ttu-id="2affa-127">Le modèle d’utilisation pour le type de contrôle **SemanticZoom** est inhabituel, car il existe principalement pour l’accès par programme.</span><span class="sxs-lookup"><span data-stu-id="2affa-127">The usage model for the **SemanticZoom** control type is unusual in that it exists mainly for programmatic access.</span></span> <span data-ttu-id="2affa-128">Les clients UI Automation de Microsoft peuvent surveiller et manipuler le contrôle de zoom sémantique pour contrôler l’état de zoom de la liste.</span><span class="sxs-lookup"><span data-stu-id="2affa-128">Microsoft UI Automation clients can monitor and manipulate the Semantic Zoom control to control the zoomed-in state of the list.</span></span> <span data-ttu-id="2affa-129">Les utilisateurs qui n’utilisent pas la technologie d’assistance manipulent généralement le contrôle de zoom sémantique directement par le biais de gestes tactiles ou de raccourcis clavier.</span><span class="sxs-lookup"><span data-stu-id="2affa-129">Users who are not using assistive technology would typically manipulate the Semantic Zoom control directly through touch gestures or keyboard shortcuts.</span></span>

<span data-ttu-id="2affa-130">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="2affa-130">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **SemanticZoom** control type.</span></span> <span data-ttu-id="2affa-131">Les spécifications d’UI Automation s’appliquent à tous les contrôles de zoom sémantique où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="2affa-131">The UI Automation requirements apply to all Semantic Zoom controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="2affa-132">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="2affa-132">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2affa-133">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="2affa-133">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="2affa-134">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="2affa-134">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="2affa-135">Modèles de contrôle et propriétés obligatoires</span><span class="sxs-lookup"><span data-stu-id="2affa-135">Required Control Patterns and Properties</span></span>](#required-control-patterns-and-properties)
-   [<span data-ttu-id="2affa-136">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="2affa-136">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="2affa-137">Remarques</span><span class="sxs-lookup"><span data-stu-id="2affa-137">Remarks</span></span>](#remarks)
-   [<span data-ttu-id="2affa-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2affa-138">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="2affa-139">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="2affa-139">Typical Tree Structure</span></span>

<span data-ttu-id="2affa-140">Le tableau suivant représente un contrôle classique et un affichage de contenu de l’arborescence UI Automation qui se rapporte au type de contrôle **SemanticZoom** et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="2affa-140">The following table depicts a typical control and content view of the UI Automation tree that pertains to the **SemanticZoom** control type and describes what can be contained in each view.</span></span> <span data-ttu-id="2affa-141">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2affa-141">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2affa-142">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="2affa-142">Control View</span></span></th>
<th><span data-ttu-id="2affa-143">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="2affa-143">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2affa-144">List</span><span class="sxs-lookup"><span data-stu-id="2affa-144">List</span></span>
<ul>
<li><span data-ttu-id="2affa-145">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="2affa-145">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="2affa-146">ListItem (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="2affa-146">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2affa-147">List</span><span class="sxs-lookup"><span data-stu-id="2affa-147">List</span></span>
<ul>
<li><span data-ttu-id="2affa-148">ListItem (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="2affa-148">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="2affa-149">Ou :</span><span class="sxs-lookup"><span data-stu-id="2affa-149">Or:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2affa-150">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="2affa-150">Control View</span></span></th>
<th><span data-ttu-id="2affa-151">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="2affa-151">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="2affa-152">SemanticZoom</span><span class="sxs-lookup"><span data-stu-id="2affa-152">[SemanticZoom]</span></span>
<ul>
<li><span data-ttu-id="2affa-153">List</span><span class="sxs-lookup"><span data-stu-id="2affa-153">List</span></span>
<ul>
<li><span data-ttu-id="2affa-154">ListItem (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="2affa-154">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="2affa-155">List</span><span class="sxs-lookup"><span data-stu-id="2affa-155">List</span></span>
<ul>
<li><span data-ttu-id="2affa-156">ListItem (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="2affa-156">ListItem (0 or more)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="2affa-157">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="2affa-157">Relevant Properties</span></span>

<span data-ttu-id="2affa-158">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="2affa-158">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **SemanticZoom** control type.</span></span> <span data-ttu-id="2affa-159">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="2affa-159">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2affa-160">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="2affa-160">UI Automation Property</span></span></th>
<th><span data-ttu-id="2affa-161">Valeur</span><span class="sxs-lookup"><span data-stu-id="2affa-161">Value</span></span></th>
<th><span data-ttu-id="2affa-162">Notes</span><span class="sxs-lookup"><span data-stu-id="2affa-162">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2affa-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-163"><a href="uiauto-automation-element-propids.md"><strong>UIA_AutomationIdPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-164">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="2affa-164">See notes.</span></span></td>
<td><span data-ttu-id="2affa-165">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="2affa-165">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2affa-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-166"><a href="uiauto-automation-element-propids.md"><strong>UIA_BoundingRectanglePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-167">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="2affa-167">See notes.</span></span></td>
<td><span data-ttu-id="2affa-168">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="2affa-168">The outermost rectangle that contains the whole control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2affa-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-169"><a href="uiauto-automation-element-propids.md"><strong>UIA_ClickablePointPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-170">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="2affa-170">See notes.</span></span></td>
<td><span data-ttu-id="2affa-171">Si le contrôle de liste a un point interactif (point sur lequel vous pouvez cliquer pour que la liste prenne le focus), ce point doit être exposé via cette propriété.</span><span class="sxs-lookup"><span data-stu-id="2affa-171">If the list control has a clickable point (a point that can be clicked to cause the list to take focus), that point must be exposed through this property.</span></span> <span data-ttu-id="2affa-172">Si la valeur de la propriété <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> a la valeur <strong>true</strong>, la tentative d’extraction de cette propriété entraîne l’erreur <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="2affa-172">If the value of the <a href="uiauto-automation-element-propids.md"><strong>UIA_IsOffscreenPropertyId</strong></a> property is <strong>TRUE</strong>, attempting to retrieve this property results in the <a href="uiauto-error-codes.md"><strong>UIA_E_NOCLICKABLEPOINT</strong></a> error.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2affa-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-173"><a href="uiauto-automation-element-propids.md"><strong>UIA_ControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-174"><strong>SemanticZoom</strong></span><span class="sxs-lookup"><span data-stu-id="2affa-174"><strong>SemanticZoom</strong></span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2affa-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-175"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsContentElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-176">TRUE</span><span class="sxs-lookup"><span data-stu-id="2affa-176">TRUE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2affa-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-177"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsControlElementPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-178">TRUE</span><span class="sxs-lookup"><span data-stu-id="2affa-178">TRUE</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="2affa-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-179"><a href="uiauto-automation-element-propids.md"><strong>UIA_IsKeyboardFocusablePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-180">FALSE</span><span class="sxs-lookup"><span data-stu-id="2affa-180">FALSE</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="2affa-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-181"><a href="uiauto-automation-element-propids.md"><strong>UIA_LabeledByPropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-182">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="2affa-182">See notes.</span></span></td>
<td><span data-ttu-id="2affa-183">S’il existe une étiquette de texte statique, cette propriété doit exposer une référence à ce contrôle.</span><span class="sxs-lookup"><span data-stu-id="2affa-183">If there is a static text label, this property must expose a reference to that control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="2affa-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-184"><a href="uiauto-automation-element-propids.md"><strong>UIA_LocalizedControlTypePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-185">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="2affa-185">See notes.</span></span></td>
<td><span data-ttu-id="2affa-186">Chaîne localisée correspondant au type de contrôle <strong>SemanticZoom</strong> .</span><span class="sxs-lookup"><span data-stu-id="2affa-186">A localized string corresponding to the <strong>SemanticZoom</strong> control type.</span></span> <span data-ttu-id="2affa-187">La valeur par défaut est &quot; Zoom sémantique &quot; pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="2affa-187">The default value is &quot;semantic zoom&quot; for en-US or English (United States).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="2affa-188">Certaines infrastructures ont été concaténées comme &quot; semanticzoom &quot; .</span><span class="sxs-lookup"><span data-stu-id="2affa-188">Some frameworks concatenated this as &quot;semanticzoom&quot;.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="2affa-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span><span class="sxs-lookup"><span data-stu-id="2affa-189"><a href="uiauto-automation-element-propids.md"><strong>UIA_NamePropertyId</strong></a></span></span></td>
<td><span data-ttu-id="2affa-190">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="2affa-190">See notes.</span></span></td>
<td><span data-ttu-id="2affa-191">Une chaîne vide est acceptable, ou un nom plus utile peut être fourni, à condition qu’elle ne contienne pas le terme zoom sémantique, ce qui rendrait la combinaison du type de contrôle et du nom déroutante.</span><span class="sxs-lookup"><span data-stu-id="2affa-191">An empty string is acceptable, or a more useful name could be provided, as long as it does not contain the term  semantic zoom , which would make the combination of control type and name confusing.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="required-control-patterns-and-properties"></a><span data-ttu-id="2affa-192">Modèles de contrôle et propriétés obligatoires</span><span class="sxs-lookup"><span data-stu-id="2affa-192">Required Control Patterns and Properties</span></span>

<span data-ttu-id="2affa-193">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles de zoom sémantique.</span><span class="sxs-lookup"><span data-stu-id="2affa-193">The following table lists the UI Automation control patterns required to be supported by all Semantic Zoom controls.</span></span> <span data-ttu-id="2affa-194">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2affa-194">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="2affa-195">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="2affa-195">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="2affa-196">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="2affa-196">Support/Value</span></span> | <span data-ttu-id="2affa-197">Notes</span><span class="sxs-lookup"><span data-stu-id="2affa-197">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                          |
|---------------------------------------------------|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2affa-198">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="2affa-198">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider) | <span data-ttu-id="2affa-199">Dépend</span><span class="sxs-lookup"><span data-stu-id="2affa-199">Depends</span></span>       | <span data-ttu-id="2affa-200">Les contrôles de zoom sémantique prennent en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) pour permettre l’activation ou la désactivation du zoom.</span><span class="sxs-lookup"><span data-stu-id="2affa-200">Semantic Zoom controls support the [Toggle](uiauto-implementingtoggle.md) control pattern to allow the zoom to be enabled or disabled.</span></span> <span data-ttu-id="2affa-201">[**ToggleState \_ OFF**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) correspond à l’État Flat, All-up, et [**ToggleState \_ on**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) correspond à la vue de niveau supérieur, zoom arrière.</span><span class="sxs-lookup"><span data-stu-id="2affa-201">[**ToggleState\_Off**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the flat, all-up state, and [**ToggleState\_On**](/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-togglestate) corresponds to the high level, zoomed-out view.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="2affa-202">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="2affa-202">Required Events</span></span>

<span data-ttu-id="2affa-203">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de zoom sémantique.</span><span class="sxs-lookup"><span data-stu-id="2affa-203">The following table lists the UI Automation events that Semantic Zoom controls are required to support.</span></span> <span data-ttu-id="2affa-204">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="2affa-204">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="2affa-205">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="2affa-205">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="2affa-206">Notes</span><span class="sxs-lookup"><span data-stu-id="2affa-206">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2affa-207">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2affa-207">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="2affa-208">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="2affa-208">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="2affa-209">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="2affa-209">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="2affa-210">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="2affa-210">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="2affa-211">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="2affa-211">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="2affa-212">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="2affa-212">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    |                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="2affa-213">Notes</span><span class="sxs-lookup"><span data-stu-id="2affa-213">Remarks</span></span>

<span data-ttu-id="2affa-214">Si une interface utilisateur a un bouton visible pour activer/désactiver le comportement du contrôle de zoom sémantique, ce bouton ne doit pas avoir de type de contrôle **SemanticZoom** .</span><span class="sxs-lookup"><span data-stu-id="2affa-214">If a UI has a visible button to toggle Semantic Zoom control behavior, this button should not have a **SemanticZoom** control type.</span></span> <span data-ttu-id="2affa-215">Il s’agit d’un compteur intuitif, mais le type de contrôle **SemanticZoom** caractérise le conteneur du contenu de zoom, pas un bouton qui contrôle le zoom.</span><span class="sxs-lookup"><span data-stu-id="2affa-215">This is counter-intuitive, but the **SemanticZoom** control type characterizes the container of the zooming content, not a button that controls the zoom.</span></span> <span data-ttu-id="2affa-216">(Un bouton peut être représenté simplement sous la forme d’un type de contrôle [Button](uiauto-supportbuttoncontroltype.md) avec le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) .)</span><span class="sxs-lookup"><span data-stu-id="2affa-216">(Such a button could be represented simply as a [Button](uiauto-supportbuttoncontroltype.md) control type with the [Toggle](uiauto-implementingtoggle.md) control pattern.)</span></span>

## <a name="related-topics"></a><span data-ttu-id="2affa-217">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2affa-217">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2affa-218">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="2affa-218">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="2affa-219">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="2affa-219">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

