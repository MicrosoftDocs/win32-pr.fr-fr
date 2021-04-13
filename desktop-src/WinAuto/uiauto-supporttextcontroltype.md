---
title: Text (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Text.
ms.assetid: 69a3b243-8ee5-48e4-a01e-c7ad69b9a3aa
keywords:
- UI Automation, prise en charge du type de contrôle Text
- UI Automation, type de contrôle Text
- UI Automation, arborescence pour le type de contrôle Text
- UI Automation, propriétés du type de contrôle Text
- UI Automation, modèles de contrôle pour le type de contrôle Text
- UI Automation, événements pour le type de contrôle Text
- arborescences, type de contrôle Text
- Propriétés, type de contrôle Text
- modèles de contrôle, type de contrôle Text
- événements, type de contrôle Text
- prise en charge du type de contrôle Text
- Text (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Text
- types de contrôles, modèles de contrôle pour le type de contrôle Text
- types de contrôles, prise en charge du texte
- types de contrôles, texte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 902b3c7c523417abde2c60e1f8039ad9f2c322b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310590"
---
# <a name="text-control-type"></a><span data-ttu-id="d727a-119">Text (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="d727a-119">Text Control Type</span></span>

<span data-ttu-id="d727a-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Text** .</span><span class="sxs-lookup"><span data-stu-id="d727a-120">This topic provides information about Microsoft UI Automation support for the **Text** control type.</span></span>

<span data-ttu-id="d727a-121">Un contrôle de texte est un élément d’interface utilisateur de base qui représente une partie du texte à l’écran.</span><span class="sxs-lookup"><span data-stu-id="d727a-121">A text control is a basic user interface item that represents a piece of text on the screen.</span></span>

<span data-ttu-id="d727a-122">Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **Text** .</span><span class="sxs-lookup"><span data-stu-id="d727a-122">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Text** control type.</span></span> <span data-ttu-id="d727a-123">Les exigences d’UI Automation s’appliquent à tous les contrôles d’arborescence où l’infrastructure/plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="d727a-123">The UI Automation requirements apply to all tree controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="d727a-124">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="d727a-124">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="d727a-125">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="d727a-125">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="d727a-126">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="d727a-126">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="d727a-127">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="d727a-127">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="d727a-128">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="d727a-128">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="d727a-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d727a-129">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="d727a-130">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="d727a-130">Typical Tree Structure</span></span>

<span data-ttu-id="d727a-131">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de texte et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="d727a-131">The following table depicts a typical control and content view of the UI Automation tree that pertains to text controls and describes what can be contained in each view.</span></span> <span data-ttu-id="d727a-132">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d727a-132">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d727a-133">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="d727a-133">Control View</span></span></th>
<th><span data-ttu-id="d727a-134">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="d727a-134">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="d727a-135">Texte</span><span class="sxs-lookup"><span data-stu-id="d727a-135">Text</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="d727a-136">Text (s’il s’agit de contenu)</span><span class="sxs-lookup"><span data-stu-id="d727a-136">Text (if content)</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d727a-137">Un contrôle de texte peut être utilisé seul comme étiquette ou texte statique dans un formulaire.</span><span class="sxs-lookup"><span data-stu-id="d727a-137">A text control can be used alone as a label or as static text on a form.</span></span> <span data-ttu-id="d727a-138">Il peut également être contenu dans la structure de l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d727a-138">It can also be contained within the structure of one of the following items:</span></span>

-   [<span data-ttu-id="d727a-139">DataItem</span><span class="sxs-lookup"><span data-stu-id="d727a-139">DataItem</span></span>](uiauto-supportdataitemcontroltype.md)
-   [<span data-ttu-id="d727a-140">ListItem</span><span class="sxs-lookup"><span data-stu-id="d727a-140">ListItem</span></span>](uiauto-supportlistitemcontroltype.md)
-   [<span data-ttu-id="d727a-141">TreeItem</span><span class="sxs-lookup"><span data-stu-id="d727a-141">TreeItem</span></span>](uiauto-supporttreeitemcontroltype.md)

<span data-ttu-id="d727a-142">Les contrôles de texte peuvent ne pas apparaître dans l’affichage de contenu de l’arborescence UI Automation, car le texte est souvent affiché via la propriété **Name** d’un autre contrôle.</span><span class="sxs-lookup"><span data-stu-id="d727a-142">Text controls might not appear in the content view of the UI Automation tree because text is often displayed through the **Name** property of another control.</span></span> <span data-ttu-id="d727a-143">Par exemple, le texte utilisé pour étiqueter un contrôle de zone de liste déroulante est exposé via la propriété **Name** du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d727a-143">For example, the text used to label a combo box control is exposed through the control's **Name** property.</span></span> <span data-ttu-id="d727a-144">Étant donné que le contrôle de zone de liste déroulante se trouve dans l’affichage de contenu de l’arborescence UI Automation, le contrôle de texte n’a pas besoin d’être présent.</span><span class="sxs-lookup"><span data-stu-id="d727a-144">Because the combo box control is in the content view of the UI Automation tree, the text control need not be there.</span></span> <span data-ttu-id="d727a-145">Les contrôles de texte peuvent avoir des enfants dans l’affichage de contenu s’il existe un objet incorporé, tel qu’un lien hypertexte.</span><span class="sxs-lookup"><span data-stu-id="d727a-145">Text controls may have children in the content view if there is an embedded object such as a hyperlink.</span></span>

## <a name="relevant-properties"></a><span data-ttu-id="d727a-146">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="d727a-146">Relevant Properties</span></span>

<span data-ttu-id="d727a-147">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de texte.</span><span class="sxs-lookup"><span data-stu-id="d727a-147">The following table lists the UI Automation properties whose value or definition is especially relevant to the text controls.</span></span> <span data-ttu-id="d727a-148">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="d727a-148">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="d727a-149">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="d727a-149">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="d727a-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="d727a-150">Value</span></span>      | <span data-ttu-id="d727a-151">Notes</span><span class="sxs-lookup"><span data-stu-id="d727a-151">Notes</span></span>                                                                                                                                                                                                                                                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d727a-152">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-152">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="d727a-153">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="d727a-153">See notes.</span></span> | <span data-ttu-id="d727a-154">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="d727a-154">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                                                                                                                                        |
| [<span data-ttu-id="d727a-155">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-155">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="d727a-156">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="d727a-156">See notes.</span></span> | <span data-ttu-id="d727a-157">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="d727a-157">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                                                                                                                                                                            |
| [<span data-ttu-id="d727a-158">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-158">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="d727a-159">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="d727a-159">See notes.</span></span> | <span data-ttu-id="d727a-160">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="d727a-160">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="d727a-161">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="d727a-161">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span>                                                                                                                                                |
| [<span data-ttu-id="d727a-162">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-162">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="d727a-163">**Text**</span><span class="sxs-lookup"><span data-stu-id="d727a-163">**Text**</span></span>   |                                                                                                                                                                                                                                                                                                                                                     |
| [<span data-ttu-id="d727a-164">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-164">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d727a-165">Dépend</span><span class="sxs-lookup"><span data-stu-id="d727a-165">Depends</span></span>    | <span data-ttu-id="d727a-166">Le contrôle de texte est du contenu s’il contient des informations qui ne sont pas exposées dans la propriété Name d’un autre contrôle.</span><span class="sxs-lookup"><span data-stu-id="d727a-166">The text control is content if it contains information not exposed in another control's Name property.</span></span>                                                                                                                                                                                                                                              |
| [<span data-ttu-id="d727a-167">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-167">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="d727a-168">TRUE</span><span class="sxs-lookup"><span data-stu-id="d727a-168">TRUE</span></span>       | <span data-ttu-id="d727a-169">Le contrôle de texte doit toujours être un contrôle.</span><span class="sxs-lookup"><span data-stu-id="d727a-169">The text control must always be a control.</span></span>                                                                                                                                                                                                                                                                                                          |
| [<span data-ttu-id="d727a-170">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-170">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="d727a-171">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="d727a-171">See notes.</span></span> | <span data-ttu-id="d727a-172">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="d727a-172">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                                                                                                                                                                           |
| [<span data-ttu-id="d727a-173">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-173">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="d727a-174">NULL</span><span class="sxs-lookup"><span data-stu-id="d727a-174">NULL</span></span>       | <span data-ttu-id="d727a-175">Les contrôles de texte n’ont pas d’étiquette de texte statique.</span><span class="sxs-lookup"><span data-stu-id="d727a-175">Text controls do not have a static text label.</span></span>                                                                                                                                                                                                                                                                                                      |
| [<span data-ttu-id="d727a-176">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-176">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="d727a-177">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="d727a-177">See notes.</span></span> | <span data-ttu-id="d727a-178">Chaîne localisée correspondant au type de contrôle **Text** .</span><span class="sxs-lookup"><span data-stu-id="d727a-178">Localized string corresponding to the **Text** control type.</span></span> <span data-ttu-id="d727a-179">La valeur par défaut est « texte » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="d727a-179">The default value is "text" for en-US or English (United States).</span></span>                                                                                                                                                                                                                      |
| [<span data-ttu-id="d727a-180">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="d727a-180">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="d727a-181">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="d727a-181">See notes.</span></span> | <span data-ttu-id="d727a-182">Le nom d’un contrôle de texte peut être le texte qu’il affiche.</span><span class="sxs-lookup"><span data-stu-id="d727a-182">The name of a text control can be the text that it displays.</span></span> <span data-ttu-id="d727a-183">Toutefois, si le contrôle prend également en charge le modèle de [texte](uiauto-implementingtextandtextrange.md) et que le texte est étendu, n’utilisez pas le contenu de texte intégral comme valeur de **nom** .</span><span class="sxs-lookup"><span data-stu-id="d727a-183">However, if the control also supports the [Text](uiauto-implementingtextandtextrange.md) pattern, and the text is extensive, don't use the full text content as the **Name** value.</span></span> <span data-ttu-id="d727a-184">Au lieu de cela, fournissez une valeur de **nom** plus petite, dérivée d’autres propriétés de votre contrôle.</span><span class="sxs-lookup"><span data-stu-id="d727a-184">Instead, provide a **Name** value that is shorter, derived from other properties of your control.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="d727a-185">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="d727a-185">Required Control Patterns</span></span>

<span data-ttu-id="d727a-186">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de texte.</span><span class="sxs-lookup"><span data-stu-id="d727a-186">The following table lists the UI Automation control patterns required to be supported by text controls.</span></span> <span data-ttu-id="d727a-187">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d727a-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="d727a-188">Modèle de contrôle</span><span class="sxs-lookup"><span data-stu-id="d727a-188">Control Pattern</span></span>                                         | <span data-ttu-id="d727a-189">Support</span><span class="sxs-lookup"><span data-stu-id="d727a-189">Support</span></span> | <span data-ttu-id="d727a-190">Notes</span><span class="sxs-lookup"><span data-stu-id="d727a-190">Notes</span></span>                                                                                                                                                                                                                                                                  |
|---------------------------------------------------------|---------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d727a-191">**IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d727a-191">**IGridItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider)   | <span data-ttu-id="d727a-192">Dépend</span><span class="sxs-lookup"><span data-stu-id="d727a-192">Depends</span></span> | <span data-ttu-id="d727a-193">Si le contrôle de texte est contenu dans un contrôle de table, le modèle de contrôle [GridItem](uiauto-implementinggriditem.md) doit être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d727a-193">If the text control is contained within a table control, the [GridItem](uiauto-implementinggriditem.md) control pattern must be supported.</span></span>                                                                                                                            |
| [<span data-ttu-id="d727a-194">**ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="d727a-194">**ITableItemProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) | <span data-ttu-id="d727a-195">Dépend</span><span class="sxs-lookup"><span data-stu-id="d727a-195">Depends</span></span> | <span data-ttu-id="d727a-196">Si le contrôle de texte est contenu dans un contrôle de table, le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) doit être pris en charge.</span><span class="sxs-lookup"><span data-stu-id="d727a-196">If the text control is contained within a table control, the [TableItem](uiauto-implementingtableitem.md) control pattern must be supported.</span></span>                                                                                                                          |
| [<span data-ttu-id="d727a-197">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="d727a-197">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)           | <span data-ttu-id="d727a-198">Dépend</span><span class="sxs-lookup"><span data-stu-id="d727a-198">Depends</span></span> | <span data-ttu-id="d727a-199">Le texte doit prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) pour une meilleure accessibilité. Toutefois, ce n’est pas obligatoire.</span><span class="sxs-lookup"><span data-stu-id="d727a-199">Text should support the [Text](uiauto-implementingtextandtextrange.md) control pattern for better accessibility; however, it is not required.</span></span> <span data-ttu-id="d727a-200">Le modèle de contrôle Text est utile quand le texte possède un style complexe et des attributs (par exemple, couleur, gras et italique).</span><span class="sxs-lookup"><span data-stu-id="d727a-200">The Text control pattern is useful when the text has rich style and attributes (for example, color, bold, and italics).</span></span> |
| [<span data-ttu-id="d727a-201">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="d727a-201">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)         | <span data-ttu-id="d727a-202">Jamais</span><span class="sxs-lookup"><span data-stu-id="d727a-202">Never</span></span>   | <span data-ttu-id="d727a-203">Un contrôle de texte ne prend jamais en charge le modèle de contrôle [value](uiauto-implementingvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="d727a-203">A text control never supports the [Value](uiauto-implementingvalue.md) control pattern.</span></span> <span data-ttu-id="d727a-204">Si le texte est modifiable, il s’agit du type de contrôle [Edit](uiauto-supporteditcontroltype.md) .</span><span class="sxs-lookup"><span data-stu-id="d727a-204">If the text is editable, it is the [Edit](uiauto-supporteditcontroltype.md) control type.</span></span>                                                                                    |



 

## <a name="required-events"></a><span data-ttu-id="d727a-205">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="d727a-205">Required Events</span></span>

<span data-ttu-id="d727a-206">Le tableau suivant répertorie les événements UI Automation que les contrôles de texte doivent prendre en charge.</span><span class="sxs-lookup"><span data-stu-id="d727a-206">The following table lists the UI Automation events that text controls are required to support.</span></span> <span data-ttu-id="d727a-207">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="d727a-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="d727a-208">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="d727a-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="d727a-209">Notes</span><span class="sxs-lookup"><span data-stu-id="d727a-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d727a-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d727a-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="d727a-211">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d727a-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="d727a-212">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d727a-212">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="d727a-213">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="d727a-213">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="d727a-214">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="d727a-214">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="d727a-215">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="d727a-215">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="d727a-216">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="d727a-216">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="d727a-217">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="d727a-217">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| [<span data-ttu-id="d727a-218">**\_TextChangedEventId de texte UIA \_**</span><span class="sxs-lookup"><span data-stu-id="d727a-218">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                 | <span data-ttu-id="d727a-219">Si le contrôle prend en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="d727a-219">If the control supports the [Text](uiauto-implementingtextandtextrange.md) control pattern, it must support this event.</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="d727a-220">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d727a-220">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d727a-221">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="d727a-221">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d727a-222">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="d727a-222">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="d727a-223">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="d727a-223">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




