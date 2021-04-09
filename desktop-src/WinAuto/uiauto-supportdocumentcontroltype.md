---
title: Document (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle document.
ms.assetid: 62565f16-f0d6-42ff-bc36-897a2618c867
keywords:
- UI Automation, prise en charge du type de contrôle document
- UI Automation, type de contrôle de document
- UI Automation, arborescence pour le type de contrôle document
- UI Automation, propriétés du type de contrôle document
- UI Automation, modèles de contrôle pour le type de contrôle document
- UI Automation, événements pour le type de contrôle document
- arborescences, type de contrôle document
- Propriétés, document (type de contrôle)
- modèles de contrôle, type de contrôle document
- événements, type de contrôle document
- prise en charge du type de contrôle document
- Document (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle document
- types de contrôles, modèles de contrôle pour le type de contrôle document
- types de contrôles, prise en charge du document
- types de contrôles, document
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46ca481df812e3321da7bb4bbb39bdcb5628fb98
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029104"
---
# <a name="document-control-type"></a><span data-ttu-id="23e89-119">Document (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="23e89-119">Document Control Type</span></span>

<span data-ttu-id="23e89-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **document** .</span><span class="sxs-lookup"><span data-stu-id="23e89-120">This topic provides information about Microsoft UI Automation support for the **Document** control type.</span></span>

<span data-ttu-id="23e89-121">Les contrôles de document permettent à l’utilisateur d’afficher et de manipuler plusieurs pages de texte.</span><span class="sxs-lookup"><span data-stu-id="23e89-121">Document controls let a user view and manipulate multiple pages of text.</span></span> <span data-ttu-id="23e89-122">Contrairement aux contrôles d’édition qui prennent uniquement en charge une simple ligne de texte sans mise en forme, les contrôles de document peuvent héberger du texte de style et de mise en forme enrichis</span><span class="sxs-lookup"><span data-stu-id="23e89-122">Unlike edit controls which only support a simple line of unformatted text, document controls can host text that is richly styled and formatted</span></span>

<span data-ttu-id="23e89-123">Les sections suivantes définissent l’arborescence UI Automation, les propriétés, les modèles de contrôle et les événements requis pour le type de contrôle **document** .</span><span class="sxs-lookup"><span data-stu-id="23e89-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Document** control type.</span></span> <span data-ttu-id="23e89-124">Les exigences d’UI Automation s’appliquent à tous les contrôles de document où l’infrastructure ou la plateforme d’interface utilisateur intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="23e89-124">The UI Automation requirements apply to all document controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="23e89-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="23e89-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="23e89-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="23e89-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="23e89-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="23e89-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="23e89-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="23e89-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="23e89-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="23e89-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="23e89-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23e89-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="23e89-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="23e89-131">Typical Tree Structure</span></span>

<span data-ttu-id="23e89-132">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles de document, et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="23e89-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to document controls and describes what can be contained in each view.</span></span> <span data-ttu-id="23e89-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="23e89-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23e89-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="23e89-134">Control View</span></span></th>
<th><span data-ttu-id="23e89-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="23e89-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="23e89-136">Document</span><span class="sxs-lookup"><span data-stu-id="23e89-136">Document</span></span>
<ul>
<li><span data-ttu-id="23e89-137">Variable</span><span class="sxs-lookup"><span data-stu-id="23e89-137">Varies</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="23e89-138">Document</span><span class="sxs-lookup"><span data-stu-id="23e89-138">Document</span></span>
<ul>
<li><span data-ttu-id="23e89-139">Variable</span><span class="sxs-lookup"><span data-stu-id="23e89-139">Varies</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="23e89-140">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="23e89-140">Relevant Properties</span></span>

<span data-ttu-id="23e89-141">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles de document.</span><span class="sxs-lookup"><span data-stu-id="23e89-141">The following table lists the UI Automation properties whose value or definition is especially relevant to document controls.</span></span> <span data-ttu-id="23e89-142">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="23e89-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="23e89-143">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="23e89-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="23e89-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="23e89-144">Value</span></span>        | <span data-ttu-id="23e89-145">Notes</span><span class="sxs-lookup"><span data-stu-id="23e89-145">Notes</span></span>                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23e89-146">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-146">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="23e89-147">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="23e89-147">See notes.</span></span>   | <span data-ttu-id="23e89-148">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="23e89-148">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                      |
| [<span data-ttu-id="23e89-149">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-149">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="23e89-150">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="23e89-150">See notes.</span></span>   | <span data-ttu-id="23e89-151">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="23e89-151">The outermost rectangle that contains the whole control.</span></span>                                                                                          |
| [<span data-ttu-id="23e89-152">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-152">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="23e89-153">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="23e89-153">See notes.</span></span>   | <span data-ttu-id="23e89-154">Le document comporte une zone interactive qui place le focus sur le document ou sur l’un de ses éléments dans le conteneur du document.</span><span class="sxs-lookup"><span data-stu-id="23e89-154">The document has a clickable point that will cause the document of one of its elements in the document container to have focus.</span></span>                   |
| [<span data-ttu-id="23e89-155">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-155">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="23e89-156">**Document**</span><span class="sxs-lookup"><span data-stu-id="23e89-156">**Document**</span></span> |                                                                                                                                                   |
| [<span data-ttu-id="23e89-157">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-157">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="23e89-158">TRUE</span><span class="sxs-lookup"><span data-stu-id="23e89-158">TRUE</span></span>         | <span data-ttu-id="23e89-159">Le contrôle de document est toujours inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="23e89-159">The document control is always included in the content view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="23e89-160">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-160">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="23e89-161">TRUE</span><span class="sxs-lookup"><span data-stu-id="23e89-161">TRUE</span></span>         | <span data-ttu-id="23e89-162">Le contrôle de document est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="23e89-162">The document control is always included in the control view of the UI Automation tree.</span></span>                                                            |
| [<span data-ttu-id="23e89-163">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-163">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="23e89-164">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="23e89-164">See notes.</span></span>   | <span data-ttu-id="23e89-165">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="23e89-165">If the control can receive keyboard focus, it must support this property.</span></span>                                                                         |
| [<span data-ttu-id="23e89-166">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-166">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="23e89-167">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="23e89-167">See notes.</span></span>   | <span data-ttu-id="23e89-168">La valeur de cette propriété doit être l’étiquette du contrôle de document.</span><span class="sxs-lookup"><span data-stu-id="23e89-168">The value of this property should be the label of the document control.</span></span> <span data-ttu-id="23e89-169">En général, le titre du document est utilisé.</span><span class="sxs-lookup"><span data-stu-id="23e89-169">Typically, the title of the document is used.</span></span>                             |
| [<span data-ttu-id="23e89-170">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-170">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="23e89-171">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="23e89-171">See notes.</span></span>   | <span data-ttu-id="23e89-172">Chaîne localisée correspondant au type de contrôle **document** .</span><span class="sxs-lookup"><span data-stu-id="23e89-172">Localized string corresponding to the **Document** control type.</span></span> <span data-ttu-id="23e89-173">La valeur par défaut est « document » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="23e89-173">The default value is "document" for en-US or English (United States).</span></span>            |
| [<span data-ttu-id="23e89-174">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="23e89-174">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="23e89-175">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="23e89-175">See notes.</span></span>   | <span data-ttu-id="23e89-176">Le contrôle de document obtient généralement son nom à partir du nom de fichier à partir duquel il est chargé.</span><span class="sxs-lookup"><span data-stu-id="23e89-176">The document control typically gets its name from the file name it is loaded from.</span></span> <span data-ttu-id="23e89-177">Il est souvent affiché dans le titre de la fenêtre ou du frame qui le contient.</span><span class="sxs-lookup"><span data-stu-id="23e89-177">This is often displayed in a containing window or frame title.</span></span> |



 

## <a name="required-control-patterns"></a><span data-ttu-id="23e89-178">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="23e89-178">Required Control Patterns</span></span>

<span data-ttu-id="23e89-179">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par les contrôles de document.</span><span class="sxs-lookup"><span data-stu-id="23e89-179">The following table lists the UI Automation control patterns required to be supported by document controls.</span></span> <span data-ttu-id="23e89-180">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="23e89-180">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="23e89-181">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="23e89-181">Control Pattern/Pattern Property</span></span>                  | <span data-ttu-id="23e89-182">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="23e89-182">Support/Value</span></span> | <span data-ttu-id="23e89-183">Notes</span><span class="sxs-lookup"><span data-stu-id="23e89-183">Notes</span></span>                                                                                                                                                                                                                                                                                                                  |
|---------------------------------------------------|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23e89-184">**IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="23e89-184">**IScrollProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) | <span data-ttu-id="23e89-185">Dépend</span><span class="sxs-lookup"><span data-stu-id="23e89-185">Depends</span></span>       | <span data-ttu-id="23e89-186">Le contrôle de document peut couvrir une étendue supérieure à celle de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="23e89-186">The document control can span larger than that span of the viewport.</span></span> <span data-ttu-id="23e89-187">Le contrôle doit prendre en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) si le contenu est défilant.</span><span class="sxs-lookup"><span data-stu-id="23e89-187">The control should support the [Scroll](uiauto-implementingscroll.md) control pattern if the content is scrollable.</span></span>                                                                                                                              |
| [<span data-ttu-id="23e89-188">**ITextProvider**</span><span class="sxs-lookup"><span data-stu-id="23e89-188">**ITextProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itextprovider)     | <span data-ttu-id="23e89-189">Obligatoire</span><span class="sxs-lookup"><span data-stu-id="23e89-189">Required</span></span>      | <span data-ttu-id="23e89-190">Tous les contrôles de document doivent prendre en charge le modèle de contrôle [Text](uiauto-implementingtextandtextrange.md) .</span><span class="sxs-lookup"><span data-stu-id="23e89-190">All document controls must support the [Text](uiauto-implementingtextandtextrange.md) control pattern.</span></span>                                                                                                                                                                                                                |
| [<span data-ttu-id="23e89-191">**IValueProvider**</span><span class="sxs-lookup"><span data-stu-id="23e89-191">**IValueProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ivalueprovider)   | <span data-ttu-id="23e89-192">Dépend</span><span class="sxs-lookup"><span data-stu-id="23e89-192">Depends</span></span>       | <span data-ttu-id="23e89-193">Alors que les clients UI Automation peuvent utiliser [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) pour obtenir des informations textuelles sur un document, ils ont besoin du modèle de contrôle [value](uiauto-implementingvalue.md) pour définir la valeur interne.</span><span class="sxs-lookup"><span data-stu-id="23e89-193">While UI Automation clients can use [**IUIAutomationTextPattern**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextpattern) to obtain text information about a document, they need the [Value](uiauto-implementingvalue.md) control pattern to set the inner value.</span></span> <span data-ttu-id="23e89-194">Une entrée de texte simple est possible uniquement via le modèle de contrôle value.</span><span class="sxs-lookup"><span data-stu-id="23e89-194">Simple text entry is possible only through the Value control pattern.</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="23e89-195">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="23e89-195">Required Events</span></span>

<span data-ttu-id="23e89-196">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de document.</span><span class="sxs-lookup"><span data-stu-id="23e89-196">The following table lists the UI Automation events that document controls are required to support.</span></span> <span data-ttu-id="23e89-197">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="23e89-197">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="23e89-198">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="23e89-198">UI Automation Event</span></span>                                                                                                                                        | <span data-ttu-id="23e89-199">Notes</span><span class="sxs-lookup"><span data-stu-id="23e89-199">Notes</span></span>                                                                                                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="23e89-200">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="23e89-200">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                                           |                                                                                                                            |
| <span data-ttu-id="23e89-201">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-201">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                      |                                                                                                                            |
| <span data-ttu-id="23e89-202">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-202">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                      | <span data-ttu-id="23e89-203">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-203">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="23e89-204">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-204">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                                  | <span data-ttu-id="23e89-205">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-205">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="23e89-206">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="23e89-206">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                                       |                                                                                                                            |
| <span data-ttu-id="23e89-207">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-207">[**UIA\_ScrollHorizontallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>   | <span data-ttu-id="23e89-208">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-208">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="23e89-209">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-209">[**UIA\_ScrollHorizontalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span> | <span data-ttu-id="23e89-210">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-210">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="23e89-211">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollHorizontalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-211">[**UIA\_ScrollHorizontalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>           | <span data-ttu-id="23e89-212">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-212">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="23e89-213">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticallyScrollablePropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-213">[**UIA\_ScrollVerticallyScrollablePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>       | <span data-ttu-id="23e89-214">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-214">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="23e89-215">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalScrollPercentPropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-215">[**UIA\_ScrollVerticalScrollPercentPropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>     | <span data-ttu-id="23e89-216">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-216">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="23e89-217">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ScrollVerticalViewSizePropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-217">[**UIA\_ScrollVerticalViewSizePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>               | <span data-ttu-id="23e89-218">Si le contrôle prend en charge le modèle de contrôle [Scroll](uiauto-implementingscroll.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-218">If the control supports the [Scroll](uiauto-implementingscroll.md) control pattern, it must support this event.</span></span>           |
| [<span data-ttu-id="23e89-219">**\_InvalidatedEventId de sélection UIA \_**</span><span class="sxs-lookup"><span data-stu-id="23e89-219">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md)                                                            | <span data-ttu-id="23e89-220">Si le contrôle prend en charge le modèle de contrôle [Selection](uiauto-implementingselection.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-220">If the control supports the [Selection](uiauto-implementingselection.md) control pattern, it must support this event.</span></span>     |
| [<span data-ttu-id="23e89-221">**\_TextSelectionChangedEventId de texte UIA \_**</span><span class="sxs-lookup"><span data-stu-id="23e89-221">**UIA\_Text\_TextSelectionChangedEventId**</span></span>](uiauto-event-ids.md)                                                    |                                                                                                                            |
| [<span data-ttu-id="23e89-222">**\_TextChangedEventId de texte UIA \_**</span><span class="sxs-lookup"><span data-stu-id="23e89-222">**UIA\_Text\_TextChangedEventId**</span></span>](uiauto-event-ids.md)                                                                      |                                                                                                                            |
| <span data-ttu-id="23e89-223">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ValueValuePropertyId.</span><span class="sxs-lookup"><span data-stu-id="23e89-223">[**UIA\_ValueValuePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>                                       | <span data-ttu-id="23e89-224">Si le contrôle prend en charge le modèle de contrôle [value](uiauto-implementingvalue.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="23e89-224">If the control supports the [Value](uiauto-implementingvalue.md) control pattern, it must support this event.</span></span>             |



 

## <a name="related-topics"></a><span data-ttu-id="23e89-225">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="23e89-225">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="23e89-226">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="23e89-226">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="23e89-227">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="23e89-227">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="23e89-228">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="23e89-228">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




