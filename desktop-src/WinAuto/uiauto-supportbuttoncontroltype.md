---
title: Button (type de contrôle)
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle Button.
ms.assetid: a2942067-461c-4281-80cf-385e3c08c874
keywords:
- UI Automation, prise en charge du type de contrôle Button
- UI Automation, type de contrôle Button
- UI Automation, arborescence pour le type de contrôle Button
- UI Automation, propriétés pour le type de contrôle Button
- UI Automation, modèles de contrôle pour le type de contrôle Button
- UI Automation, événements pour le type de contrôle Button
- arborescences, type de contrôle Button
- Propriétés, Button (type de contrôle)
- modèles de contrôle, type de contrôle Button
- événements, Button (type de contrôle)
- prise en charge du type de contrôle Button
- Button (type de contrôle)
- types de contrôles, arborescence pour le type de contrôle Button
- types de contrôles, modèles de contrôle pour le type de contrôle Button
- types de contrôles, prise en charge du bouton
- types de contrôle, bouton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def18e7094e297303a70fc0980bfdd0cb4413c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104197455"
---
# <a name="button-control-type"></a><span data-ttu-id="84134-119">Button (type de contrôle)</span><span class="sxs-lookup"><span data-stu-id="84134-119">Button Control Type</span></span>

<span data-ttu-id="84134-120">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **Button** .</span><span class="sxs-lookup"><span data-stu-id="84134-120">This topic provides information about Microsoft UI Automation support for the **Button** control type.</span></span>

<span data-ttu-id="84134-121">Un bouton est un objet avec lequel un utilisateur interagit pour effectuer une action. Tel est le cas des boutons OK et Annuler d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="84134-121">A button is an object that a user interacts with to perform an action such as the OK and Cancel buttons on a dialog box.</span></span> <span data-ttu-id="84134-122">Le contrôle button est un contrôle simple à exposer, car il correspond à une commande unique que l’utilisateur veut exécuter.</span><span class="sxs-lookup"><span data-stu-id="84134-122">The button control is a simple control to expose because it maps to a single command that the user wishes to complete.</span></span>

<span data-ttu-id="84134-123">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **Button** .</span><span class="sxs-lookup"><span data-stu-id="84134-123">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **Button** control type.</span></span> <span data-ttu-id="84134-124">Les spécifications d’UI Automation s’appliquent à tous les contrôles de bouton où l’infrastructure d’interface utilisateur/plateforme intègre la prise en charge d’UI Automation pour les types de contrôle et les modèles de contrôle.</span><span class="sxs-lookup"><span data-stu-id="84134-124">The UI Automation requirements apply to all button controls where the UI framework/platform integrates UI Automation support for control types and control patterns.</span></span>

<span data-ttu-id="84134-125">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="84134-125">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="84134-126">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="84134-126">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="84134-127">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="84134-127">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="84134-128">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="84134-128">Required Control Patterns</span></span>](#required-control-patterns)
-   [<span data-ttu-id="84134-129">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="84134-129">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="84134-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84134-130">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="84134-131">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="84134-131">Typical Tree Structure</span></span>

<span data-ttu-id="84134-132">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles Button et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="84134-132">The following table depicts a typical control and content view of the UI Automation tree that pertains to button controls and describes what can be contained in each view.</span></span> <span data-ttu-id="84134-133">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="84134-133">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="84134-134">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="84134-134">Control View</span></span></th>
<th><span data-ttu-id="84134-135">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="84134-135">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="84134-136">Bouton</span><span class="sxs-lookup"><span data-stu-id="84134-136">Button</span></span>
<ul>
<li><span data-ttu-id="84134-137">Image (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="84134-137">Image (0 or more)</span></span></li>
<li><span data-ttu-id="84134-138">Text (0 ou plus)</span><span class="sxs-lookup"><span data-stu-id="84134-138">Text (0 or more)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="84134-139">Bouton</span><span class="sxs-lookup"><span data-stu-id="84134-139">Button</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="84134-140">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="84134-140">Relevant Properties</span></span>

<span data-ttu-id="84134-141">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **Button** (tels que les contrôles Button).</span><span class="sxs-lookup"><span data-stu-id="84134-141">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **Button** control type (such as button controls).</span></span> <span data-ttu-id="84134-142">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="84134-142">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="84134-143">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="84134-143">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="84134-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="84134-144">Value</span></span>      | <span data-ttu-id="84134-145">Notes</span><span class="sxs-lookup"><span data-stu-id="84134-145">Notes</span></span>                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84134-146">**UIA \_ AcceleratorKeyPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-146">**UIA\_AcceleratorKeyPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="84134-147">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-147">See notes.</span></span> | <span data-ttu-id="84134-148">Un contrôle Button prend généralement en charge une touche accélérateur pour permettre à l’utilisateur final d’effectuer rapidement l’action représentée par le bouton à partir du clavier.</span><span class="sxs-lookup"><span data-stu-id="84134-148">A button control typically supports an accelerator key to enable the end user to quickly perform the action represented by the button from the keyboard.</span></span>                                             |
| [<span data-ttu-id="84134-149">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-149">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="84134-150">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-150">See notes.</span></span> | <span data-ttu-id="84134-151">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="84134-151">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                         |
| [<span data-ttu-id="84134-152">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-152">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="84134-153">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-153">See notes.</span></span> | <span data-ttu-id="84134-154">Rectangle externe qui contient l’ensemble du contrôle.</span><span class="sxs-lookup"><span data-stu-id="84134-154">The outermost rectangle that contains the whole control.</span></span>                                                                                                                                             |
| [<span data-ttu-id="84134-155">**UIA \_ ClickablePointPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-155">**UIA\_ClickablePointPropertyId**</span></span>](uiauto-automation-element-propids.md)             | <span data-ttu-id="84134-156">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-156">See notes.</span></span> | <span data-ttu-id="84134-157">Pris en charge s’il existe un rectangle englobant.</span><span class="sxs-lookup"><span data-stu-id="84134-157">Supported if there is a bounding rectangle.</span></span> <span data-ttu-id="84134-158">Si tous les points du rectangle englobant ne sont pas cliquables et que l’élément effectue un test de positionnement spécialisé, substituez et fournissez un point cliquable.</span><span class="sxs-lookup"><span data-stu-id="84134-158">If not every point within the bounding rectangle is clickable, and the element performs specialized hit testing, override and provide a clickable point.</span></span> |
| [<span data-ttu-id="84134-159">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-159">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="84134-160">**Button**</span><span class="sxs-lookup"><span data-stu-id="84134-160">**Button**</span></span> |                                                                                                                                                                                                      |
| [<span data-ttu-id="84134-161">**UIA \_ HelpTextPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-161">**UIA\_HelpTextPropertyId**</span></span>](uiauto-automation-element-propids.md)                         | <span data-ttu-id="84134-162">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-162">See notes.</span></span> | <span data-ttu-id="84134-163">Le texte d’aide doit indiquer ce que sera le résultat final de l’activation du bouton.</span><span class="sxs-lookup"><span data-stu-id="84134-163">The help text should indicate what the end result of activating the button will be.</span></span> <span data-ttu-id="84134-164">Il s’agit généralement du même type d’informations que celui présenté dans une info-bulle.</span><span class="sxs-lookup"><span data-stu-id="84134-164">This is typically the same type of information presented through a tooltip.</span></span>                                      |
| [<span data-ttu-id="84134-165">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-165">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="84134-166">TRUE</span><span class="sxs-lookup"><span data-stu-id="84134-166">TRUE</span></span>       | <span data-ttu-id="84134-167">Le contrôle Button doit toujours être du contenu.</span><span class="sxs-lookup"><span data-stu-id="84134-167">The button control must always be content.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="84134-168">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-168">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="84134-169">TRUE</span><span class="sxs-lookup"><span data-stu-id="84134-169">TRUE</span></span>       | <span data-ttu-id="84134-170">Le contrôle Button doit toujours être un contrôle.</span><span class="sxs-lookup"><span data-stu-id="84134-170">The button control must always be a control.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="84134-171">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-171">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="84134-172">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-172">See notes.</span></span> | <span data-ttu-id="84134-173">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="84134-173">If the control can receive keyboard focus, it must support this property.</span></span>                                                                                                                            |
| [<span data-ttu-id="84134-174">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-174">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="84134-175">Null</span><span class="sxs-lookup"><span data-stu-id="84134-175">Null</span></span>       | <span data-ttu-id="84134-176">Les contrôles Button sont étiquetés automatiquement par leur contenu.</span><span class="sxs-lookup"><span data-stu-id="84134-176">Button controls are self-labeled by their contents.</span></span>                                                                                                                                                  |
| [<span data-ttu-id="84134-177">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-177">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="84134-178">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-178">See notes.</span></span> | <span data-ttu-id="84134-179">Chaîne localisée correspondant au type de contrôle **Button** .</span><span class="sxs-lookup"><span data-stu-id="84134-179">Localized string corresponding to the **Button** control type.</span></span> <span data-ttu-id="84134-180">La valeur par défaut est « Button » pour « fr-fr » ou « anglais » (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="84134-180">The default value is "button" for en-US or English (United States).</span></span>                                                                   |
| [<span data-ttu-id="84134-181">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="84134-181">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="84134-182">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-182">See notes.</span></span> | <span data-ttu-id="84134-183">Le nom du contrôle Button est le texte utilisé pour l’étiqueter.</span><span class="sxs-lookup"><span data-stu-id="84134-183">The name of the button control is the text used to label it.</span></span> <span data-ttu-id="84134-184">Chaque fois qu’une image est utilisée pour étiqueter un bouton, un texte de remplacement doit être fourni pour la propriété **Name** du bouton.</span><span class="sxs-lookup"><span data-stu-id="84134-184">Whenever an image is used to label a button, alternate text must be supplied for the button's **Name** property.</span></span>                        |



 

## <a name="required-control-patterns"></a><span data-ttu-id="84134-185">Modèles de contrôle requis</span><span class="sxs-lookup"><span data-stu-id="84134-185">Required Control Patterns</span></span>

<span data-ttu-id="84134-186">Le tableau suivant répertorie les modèles de contrôle UI Automation qui doivent être pris en charge par tous les contrôles bouton.</span><span class="sxs-lookup"><span data-stu-id="84134-186">The following table lists the UI Automation control patterns required to be supported by all button controls.</span></span> <span data-ttu-id="84134-187">Pour plus d’informations sur les modèles de contrôle, consultez [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="84134-187">For more information on control patterns, see [UI Automation Control Patterns Overview](uiauto-controlpatternsoverview.md).</span></span>



| <span data-ttu-id="84134-188">Modèle de contrôle/Propriété de modèle</span><span class="sxs-lookup"><span data-stu-id="84134-188">Control Pattern/Pattern Property</span></span>                                  | <span data-ttu-id="84134-189">Prise en charge/valeur</span><span class="sxs-lookup"><span data-stu-id="84134-189">Support/Value</span></span> | <span data-ttu-id="84134-190">Notes</span><span class="sxs-lookup"><span data-stu-id="84134-190">Notes</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------------------------------------------|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84134-191">**IExpandCollapseProvider**</span><span class="sxs-lookup"><span data-stu-id="84134-191">**IExpandCollapseProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iexpandcollapseprovider) | <span data-ttu-id="84134-192">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-192">See notes.</span></span>    | <span data-ttu-id="84134-193">Quand un bouton est hébergé en tant qu’enfant d’un bouton partagé, le bouton enfant peut prendre en charge le modèle de contrôle [ExpandCollapse](uiauto-implementingexpandcollapse.md) à la place du modèle de contrôle [Invoke](uiauto-implementinginvoke.md) ou [Toggle](uiauto-implementingtoggle.md) .</span><span class="sxs-lookup"><span data-stu-id="84134-193">When a button is hosted as a child of a split button, the child button can support the [ExpandCollapse](uiauto-implementingexpandcollapse.md) control pattern instead of the [Invoke](uiauto-implementinginvoke.md) or [Toggle](uiauto-implementingtoggle.md) control pattern.</span></span> <span data-ttu-id="84134-194">Le modèle de contrôle ExpandCollapse peut être utilisé pour ouvrir ou fermer un menu ou une autre sous-structure associée à l’élément Button.</span><span class="sxs-lookup"><span data-stu-id="84134-194">The ExpandCollapse control pattern can be used for opening or closing a menu or other sub-structure associated with the button element.</span></span> |
| [<span data-ttu-id="84134-195">**IInvokeProvider**</span><span class="sxs-lookup"><span data-stu-id="84134-195">**IInvokeProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iinvokeprovider)                 | <span data-ttu-id="84134-196">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-196">See notes.</span></span>    | <span data-ttu-id="84134-197">Tous les boutons doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) ou le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="84134-197">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="84134-198">Le modèle de contrôle Invoke doit être pris en charge lorsque le bouton exécute une commande à la demande de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="84134-198">The Invoke control pattern must be supported when the button performs a command at the request of the user.</span></span> <span data-ttu-id="84134-199">Cette commande correspond à une seule opération, par exemple, Couper, Copier, Coller ou Supprimer.</span><span class="sxs-lookup"><span data-stu-id="84134-199">This command maps to a single operation such as Cut, Copy, Paste, or Delete.</span></span>                                                              |
| [<span data-ttu-id="84134-200">**IToggleProvider**</span><span class="sxs-lookup"><span data-stu-id="84134-200">**IToggleProvider**</span></span>](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider)                 | <span data-ttu-id="84134-201">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="84134-201">See notes.</span></span>    | <span data-ttu-id="84134-202">Tous les boutons doivent prendre en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) ou le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , mais pas les deux.</span><span class="sxs-lookup"><span data-stu-id="84134-202">All buttons should support the [Invoke](uiauto-implementinginvoke.md) control pattern or the [Toggle](uiauto-implementingtoggle.md) control pattern but not both.</span></span> <span data-ttu-id="84134-203">Le modèle de contrôle Toggle doit être pris en charge si le bouton peut parcourir une série de trois États au maximum.</span><span class="sxs-lookup"><span data-stu-id="84134-203">The Toggle control pattern must be supported if the button can cycle through a series of up to three states.</span></span> <span data-ttu-id="84134-204">En général, cela est considéré comme un commutateur d’activation/désactivation pour des fonctionnalités spécifiques.</span><span class="sxs-lookup"><span data-stu-id="84134-204">Typically this is seen as an on/off switch for specific features.</span></span>                                                                        |



 

## <a name="required-events"></a><span data-ttu-id="84134-205">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="84134-205">Required Events</span></span>

<span data-ttu-id="84134-206">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de bouton.</span><span class="sxs-lookup"><span data-stu-id="84134-206">The following table lists the UI Automation events that button controls are required to support.</span></span> <span data-ttu-id="84134-207">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="84134-207">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="84134-208">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="84134-208">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="84134-209">Notes</span><span class="sxs-lookup"><span data-stu-id="84134-209">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="84134-210">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="84134-210">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="84134-211">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="84134-211">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| [<span data-ttu-id="84134-212">**UIA \_ Invoke \_ InvokedEventId**</span><span class="sxs-lookup"><span data-stu-id="84134-212">**UIA\_Invoke\_InvokedEventId**</span></span>](uiauto-event-ids.md)                                                     | <span data-ttu-id="84134-213">Si le contrôle prend en charge le modèle de contrôle [Invoke](uiauto-implementinginvoke.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="84134-213">If the control supports the [Invoke](uiauto-implementinginvoke.md) control pattern, it must support this event.</span></span>           |
| <span data-ttu-id="84134-214">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="84134-214">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="84134-215">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="84134-215">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="84134-216">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="84134-216">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="84134-217">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="84134-217">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| <span data-ttu-id="84134-218">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété NamePropertyId.</span><span class="sxs-lookup"><span data-stu-id="84134-218">[**UIA\_NamePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                           |                                                                                                                            |
| [<span data-ttu-id="84134-219">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="84134-219">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |
| <span data-ttu-id="84134-220">[**UIA \_**](uiauto-control-pattern-propids.md) Événement de modification de propriété ToggleToggleStatePropertyId.</span><span class="sxs-lookup"><span data-stu-id="84134-220">[**UIA\_ToggleToggleStatePropertyId**](uiauto-control-pattern-propids.md) property-changed event.</span></span>    | <span data-ttu-id="84134-221">Si le contrôle prend en charge le modèle de contrôle [Toggle](uiauto-implementingtoggle.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="84134-221">If the control supports the [Toggle](uiauto-implementingtoggle.md) control pattern, it must support this event.</span></span>           |



 

## <a name="related-topics"></a><span data-ttu-id="84134-222">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="84134-222">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="84134-223">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="84134-223">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="84134-224">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="84134-224">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="84134-225">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="84134-225">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> </dl>

 

 




