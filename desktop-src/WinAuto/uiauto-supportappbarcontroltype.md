---
title: Type de contrôle AppBar
description: Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle AppBar.
ms.assetid: B56F4E7A-934F-8516-9B1B-B23B80D54273
keywords:
- UI Automation, prise en charge du type de contrôle AppBar
- UI Automation, type de contrôle AppBar
- UI Automation, modèles de contrôle pour le type de contrôle AppBar
- modèles de contrôle, type de contrôle AppBar
- prise en charge du type de contrôle AppBar
- Type de contrôle AppBar
- types de contrôles, AppBar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 151aecc0f5f97878e10b59b091c4c59ec98cb26d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104463515"
---
# <a name="appbar-control-type"></a><span data-ttu-id="3ca59-110">Type de contrôle AppBar</span><span class="sxs-lookup"><span data-stu-id="3ca59-110">AppBar Control Type</span></span>

<span data-ttu-id="3ca59-111">Cette rubrique fournit des informations sur la prise en charge de Microsoft UI Automation pour le type de contrôle **appbar** .</span><span class="sxs-lookup"><span data-stu-id="3ca59-111">This topic provides information about Microsoft UI Automation support for the **AppBar** control type.</span></span>

<span data-ttu-id="3ca59-112">Une barre d’application est un élément d’interface utilisateur qui présente la navigation, les commandes et les outils à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3ca59-112">An app bar is a UI element that presents navigation, commands, and tools to the user.</span></span> <span data-ttu-id="3ca59-113">Pour les applications du Windows Store, les barres d’application pour les applications peuvent être affichées en appuyant sur la touche Windows + Z.</span><span class="sxs-lookup"><span data-stu-id="3ca59-113">For Windows Store apps, app bars for apps can be displayed by pressing Windows Key + Z.</span></span>

<span data-ttu-id="3ca59-114">Les sections suivantes définissent l’arborescence, les propriétés, les modèles de contrôle et les événements UI Automation requis pour le type de contrôle **appbar** .</span><span class="sxs-lookup"><span data-stu-id="3ca59-114">The following sections define the required UI Automation tree structure, properties, control patterns, and events for the **AppBar** control type.</span></span>

<span data-ttu-id="3ca59-115">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3ca59-115">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3ca59-116">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="3ca59-116">Typical Tree Structure</span></span>](#typical-tree-structure)
-   [<span data-ttu-id="3ca59-117">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="3ca59-117">Relevant Properties</span></span>](#relevant-properties)
-   [<span data-ttu-id="3ca59-118">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="3ca59-118">Required Events</span></span>](#required-events)
-   [<span data-ttu-id="3ca59-119">Événements pertinents</span><span class="sxs-lookup"><span data-stu-id="3ca59-119">Relevant Events</span></span>](#relevant-events)
-   [<span data-ttu-id="3ca59-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ca59-120">Related topics</span></span>](#related-topics)

## <a name="typical-tree-structure"></a><span data-ttu-id="3ca59-121">Structure d’arborescence classique</span><span class="sxs-lookup"><span data-stu-id="3ca59-121">Typical Tree Structure</span></span>

<span data-ttu-id="3ca59-122">Le tableau suivant illustre un contrôle classique et une vue de contenu de l’arborescence UI Automation relative aux contrôles **appbar** et décrit ce que peut contenir chaque affichage.</span><span class="sxs-lookup"><span data-stu-id="3ca59-122">The following table depicts a typical control and content view of the UI Automation tree that pertains to **AppBar** controls and describes what can be contained in each view.</span></span> <span data-ttu-id="3ca59-123">**Button** est l’élément le plus courant dans un **appbar** , mais les autres contrôles qui appellent des actions pour une application sont également possibles.</span><span class="sxs-lookup"><span data-stu-id="3ca59-123">**Button** is the most common element within an **AppBar** but other controls that invoke actions for an app are also possible.</span></span> <span data-ttu-id="3ca59-124">Un **appbar** peut également avoir 0 ou plusieurs séparateurs (type de contrôle **separator** ), qui apparaissent dans l’affichage de contrôle tels qu’ils sont placés entre les autres contrôles.</span><span class="sxs-lookup"><span data-stu-id="3ca59-124">An **AppBar** can also have 0 or more separators (**Separator** control type), which appear in the control view as placed between the other controls.</span></span> <span data-ttu-id="3ca59-125">Pour plus d’informations sur l’arborescence UI Automation, consultez [UI Automation Tree Overview](uiauto-treeoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3ca59-125">For more information about the UI Automation tree, see [UI Automation Tree Overview](uiauto-treeoverview.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ca59-126">Affichage de contrôle</span><span class="sxs-lookup"><span data-stu-id="3ca59-126">Control View</span></span></th>
<th><span data-ttu-id="3ca59-127">Affichage de contenu</span><span class="sxs-lookup"><span data-stu-id="3ca59-127">Content View</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><span data-ttu-id="3ca59-128">AppBar</span><span class="sxs-lookup"><span data-stu-id="3ca59-128">AppBar</span></span>
<ul>
<li><span data-ttu-id="3ca59-129">Bouton (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="3ca59-129">Button (0 or many)</span></span></li>
<li><span data-ttu-id="3ca59-130">Autres contrôles (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="3ca59-130">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="3ca59-131">Non applicable</span><span class="sxs-lookup"><span data-stu-id="3ca59-131">Not applicable</span></span>
<ul>
<li><span data-ttu-id="3ca59-132">Bouton (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="3ca59-132">Button (0 or many)</span></span></li>
<li><span data-ttu-id="3ca59-133">Autres contrôles (0 ou plusieurs)</span><span class="sxs-lookup"><span data-stu-id="3ca59-133">Other controls (0 or many)</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="relevant-properties"></a><span data-ttu-id="3ca59-134">Propriétés pertinentes</span><span class="sxs-lookup"><span data-stu-id="3ca59-134">Relevant Properties</span></span>

<span data-ttu-id="3ca59-135">Le tableau suivant répertorie les propriétés UI Automation dont la valeur ou la définition est particulièrement pertinente pour les contrôles qui implémentent le type de contrôle **appbar** .</span><span class="sxs-lookup"><span data-stu-id="3ca59-135">The following table lists the UI Automation properties whose value or definition is especially relevant to the controls that implement the **AppBar** control type.</span></span> <span data-ttu-id="3ca59-136">Pour plus d’informations sur les propriétés UI Automation, consultez [extraction de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md).</span><span class="sxs-lookup"><span data-stu-id="3ca59-136">For more information about UI Automation properties, see [Retrieving Properties from UI Automation Elements](uiauto-propertiesforclients.md).</span></span>



| <span data-ttu-id="3ca59-137">Propriété UI Automation</span><span class="sxs-lookup"><span data-stu-id="3ca59-137">UI Automation Property</span></span>                                                                                              | <span data-ttu-id="3ca59-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="3ca59-138">Value</span></span>      | <span data-ttu-id="3ca59-139">Notes</span><span class="sxs-lookup"><span data-stu-id="3ca59-139">Notes</span></span>                                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca59-140">**UIA \_ AutomationIdPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-140">**UIA\_AutomationIdPropertyId**</span></span>](uiauto-automation-element-propids.md)                 | <span data-ttu-id="3ca59-141">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3ca59-141">See notes.</span></span> | <span data-ttu-id="3ca59-142">La valeur de cette propriété doit être unique parmi tous les éléments homologues de l’affichage brut de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3ca59-142">The value of this property must be unique among all peer elements in the raw view of the UI Automation tree.</span></span>                                                                                                                |
| [<span data-ttu-id="3ca59-143">**UIA \_ BoundingRectanglePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-143">**UIA\_BoundingRectanglePropertyId**</span></span>](uiauto-automation-element-propids.md)       | <span data-ttu-id="3ca59-144">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3ca59-144">See notes.</span></span> | <span data-ttu-id="3ca59-145">La valeur exposée par cette propriété doit inclure tous les contrôles qu’elle contient.</span><span class="sxs-lookup"><span data-stu-id="3ca59-145">The value exposed by this property must include all of the controls contained within it.</span></span>                                                                                                                                    |
| [<span data-ttu-id="3ca59-146">**UIA \_ ControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-146">**UIA\_ControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="3ca59-147">**AppBar**</span><span class="sxs-lookup"><span data-stu-id="3ca59-147">**AppBar**</span></span> |                                                                                                                                                                                                                             |
| [<span data-ttu-id="3ca59-148">**UIA \_ IsContentElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-148">**UIA\_IsContentElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3ca59-149">FALSE</span><span class="sxs-lookup"><span data-stu-id="3ca59-149">FALSE</span></span>      | <span data-ttu-id="3ca59-150">Un contrôle de barre d’application n’est pas inclus dans l’affichage de contenu de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3ca59-150">An app bar control is not included in the content view of the UI Automation tree.</span></span>                                                                                                                                           |
| [<span data-ttu-id="3ca59-151">**UIA \_ IsControlElementPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-151">**UIA\_IsControlElementPropertyId**</span></span>](uiauto-automation-element-propids.md)         | <span data-ttu-id="3ca59-152">TRUE</span><span class="sxs-lookup"><span data-stu-id="3ca59-152">TRUE</span></span>       | <span data-ttu-id="3ca59-153">Un contrôle de barre d’application est toujours inclus dans l’affichage de contrôle de l’arborescence UI Automation.</span><span class="sxs-lookup"><span data-stu-id="3ca59-153">An app bar control is always included in the control view of the UI Automation tree.</span></span>                                                                                                                                        |
| [<span data-ttu-id="3ca59-154">**UIA \_ IsKeyboardFocusablePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-154">**UIA\_IsKeyboardFocusablePropertyId**</span></span>](uiauto-automation-element-propids.md)   | <span data-ttu-id="3ca59-155">Voir les remarques</span><span class="sxs-lookup"><span data-stu-id="3ca59-155">See notes</span></span>  | <span data-ttu-id="3ca59-156">Si le contrôle peut recevoir le focus clavier, il doit prendre en charge cette propriété.</span><span class="sxs-lookup"><span data-stu-id="3ca59-156">If the control can receive keyboard focus, it must support this property.</span></span> <span data-ttu-id="3ca59-157">Les contrôles dans la barre de l’application peuvent généralement prendre le focus clavier.</span><span class="sxs-lookup"><span data-stu-id="3ca59-157">Controls within the app bar typically can take keyboard focus.</span></span>                                                                                    |
| [<span data-ttu-id="3ca59-158">**UIA \_ IsOffscreenPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-158">**UIA\_IsOffscreenPropertyId**</span></span>](uiauto-automation-element-propids.md)                   | <span data-ttu-id="3ca59-159">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3ca59-159">See notes.</span></span> | <span data-ttu-id="3ca59-160">La valeur de cette propriété varie selon que le contrôle est visible ou non à l’écran.</span><span class="sxs-lookup"><span data-stu-id="3ca59-160">The value of this property depends on whether the control is viewable on the screen.</span></span>                                                                                                                                        |
| [<span data-ttu-id="3ca59-161">**UIA \_ LabeledByPropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-161">**UIA\_LabeledByPropertyId**</span></span>](uiauto-automation-element-propids.md)                       | <span data-ttu-id="3ca59-162">Null</span><span class="sxs-lookup"><span data-stu-id="3ca59-162">Null</span></span>       | <span data-ttu-id="3ca59-163">Les contrôles de la barre de l’application n’ont généralement pas d’étiquette.</span><span class="sxs-lookup"><span data-stu-id="3ca59-163">App bar controls usually do not have a label.</span></span>                                                                                                                                                                               |
| [<span data-ttu-id="3ca59-164">**UIA \_ LocalizedControlTypePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-164">**UIA\_LocalizedControlTypePropertyId**</span></span>](uiauto-automation-element-propids.md) | <span data-ttu-id="3ca59-165">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3ca59-165">See notes.</span></span> | <span data-ttu-id="3ca59-166">Chaîne localisée correspondant au type de contrôle **appbar** .</span><span class="sxs-lookup"><span data-stu-id="3ca59-166">Localized string corresponding to the **AppBar** control type.</span></span> <span data-ttu-id="3ca59-167">La valeur par défaut est « barre d’application » pour en-US ou anglais (États-Unis).</span><span class="sxs-lookup"><span data-stu-id="3ca59-167">The default value is "app bar" for en-US or English (United States).</span></span>                                                                                         |
| [<span data-ttu-id="3ca59-168">**UIA \_ NamePropertyId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-168">**UIA\_NamePropertyId**</span></span>](uiauto-automation-element-propids.md)                                 | <span data-ttu-id="3ca59-169">Consultez les remarques.</span><span class="sxs-lookup"><span data-stu-id="3ca59-169">See notes.</span></span> | <span data-ttu-id="3ca59-170">Le contrôle de la barre de l’application n’a pas besoin d’un nom, sauf si une application contient plusieurs barres de l’application.</span><span class="sxs-lookup"><span data-stu-id="3ca59-170">The app bar control does not need a name unless an application has more than one app bar.</span></span> <span data-ttu-id="3ca59-171">S’il existe plusieurs barres d’application dans une application, utilisez cette propriété pour exposer des noms distinctifs, tels que « Top » ou « Bottom ».</span><span class="sxs-lookup"><span data-stu-id="3ca59-171">If there is more than one app bar in an application, use this property to expose distinguishing names, such as "Top" or "Bottom."</span></span> |



 

## <a name="required-events"></a><span data-ttu-id="3ca59-172">Événements obligatoires</span><span class="sxs-lookup"><span data-stu-id="3ca59-172">Required Events</span></span>

<span data-ttu-id="3ca59-173">Le tableau suivant répertorie les événements UI Automation nécessaires à la prise en charge des contrôles de la barre de l’application.</span><span class="sxs-lookup"><span data-stu-id="3ca59-173">The following table lists the UI Automation events that app bar controls are required to support.</span></span> <span data-ttu-id="3ca59-174">Pour plus d’informations sur les événements, consultez [UI Automation Events Overview](uiauto-eventsoverview.md).</span><span class="sxs-lookup"><span data-stu-id="3ca59-174">For more information on events, see [UI Automation Events Overview](uiauto-eventsoverview.md).</span></span>



| <span data-ttu-id="3ca59-175">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="3ca59-175">UI Automation Event</span></span>                                                                                                                   | <span data-ttu-id="3ca59-176">Notes</span><span class="sxs-lookup"><span data-stu-id="3ca59-176">Notes</span></span>                                                                                                                      |
|---------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca59-177">**UIA \_ AutomationFocusChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-177">**UIA\_AutomationFocusChangedEventId**</span></span>](uiauto-event-ids.md)                                      |                                                                                                                            |
| <span data-ttu-id="3ca59-178">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété BoundingRectanglePropertyId.</span><span class="sxs-lookup"><span data-stu-id="3ca59-178">[**UIA\_BoundingRectanglePropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span> |                                                                                                                            |
| <span data-ttu-id="3ca59-179">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsEnabledPropertyId.</span><span class="sxs-lookup"><span data-stu-id="3ca59-179">[**UIA\_IsEnabledPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>                 | <span data-ttu-id="3ca59-180">Si le contrôle prend en charge la propriété [**IsEnabled**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="3ca59-180">If the control supports the [**IsEnabled**](uiauto-automation-element-propids.md) property, it must support this event.</span></span>   |
| <span data-ttu-id="3ca59-181">[**UIA \_**](uiauto-automation-element-propids.md) Événement de modification de propriété IsOffscreenPropertyId.</span><span class="sxs-lookup"><span data-stu-id="3ca59-181">[**UIA\_IsOffscreenPropertyId**](uiauto-automation-element-propids.md) property-changed event.</span></span>             | <span data-ttu-id="3ca59-182">Si le contrôle prend en charge la propriété [**IsOffscreen**](uiauto-automation-element-propids.md) , il doit prendre en charge cet événement.</span><span class="sxs-lookup"><span data-stu-id="3ca59-182">If the control supports the [**IsOffscreen**](uiauto-automation-element-propids.md) property, it must support this event.</span></span> |
| [<span data-ttu-id="3ca59-183">**UIA \_ StructureChangedEventId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-183">**UIA\_StructureChangedEventId**</span></span>](uiauto-event-ids.md)                                                  |                                                                                                                            |



 

## <a name="relevant-events"></a><span data-ttu-id="3ca59-184">Événements pertinents</span><span class="sxs-lookup"><span data-stu-id="3ca59-184">Relevant Events</span></span>

<span data-ttu-id="3ca59-185">Le tableau suivant répertorie les événements UI Automation qui sont particulièrement pertinents pour les contrôles qui implémentent le type de contrôle **appbar** , mais qui ne sont pas strictement requis.</span><span class="sxs-lookup"><span data-stu-id="3ca59-185">The following table lists the UI Automation events that are especially relevant to the controls that implement the **AppBar** control type but not strictly required.</span></span>



| <span data-ttu-id="3ca59-186">Événement UI Automation</span><span class="sxs-lookup"><span data-stu-id="3ca59-186">UI Automation Event</span></span>                                                                                 | <span data-ttu-id="3ca59-187">Notes</span><span class="sxs-lookup"><span data-stu-id="3ca59-187">Notes</span></span>                                                                              |
|-----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="3ca59-188">**UIA \_ MenuClosedEventId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-188">**UIA\_MenuClosedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="3ca59-189">Les implémentations de plateforme peuvent déclencher cet événement lorsque le contrôle de la barre de l’application est fermé.</span><span class="sxs-lookup"><span data-stu-id="3ca59-189">Platform implementations might fire this event when the app bar control is closed.</span></span> |
| [<span data-ttu-id="3ca59-190">**UIA \_ MenuOpenedEventId**</span><span class="sxs-lookup"><span data-stu-id="3ca59-190">**UIA\_MenuOpenedEventId**</span></span>](uiauto-event-ids.md)                            | <span data-ttu-id="3ca59-191">Les implémentations de plateforme peuvent déclencher cet événement lorsque le contrôle de la barre de l’application est ouvert.</span><span class="sxs-lookup"><span data-stu-id="3ca59-191">Platform implementations might fire this event when the app bar control is opened.</span></span> |
| [<span data-ttu-id="3ca59-192">**IUIAutomationPropertyChangedEventHandler**</span><span class="sxs-lookup"><span data-stu-id="3ca59-192">**IUIAutomationPropertyChangedEventHandler**</span></span>](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationpropertychangedeventhandler) | <span data-ttu-id="3ca59-193">Gestionnaire d’événements de modification de propriété.</span><span class="sxs-lookup"><span data-stu-id="3ca59-193">Property-changed event handler.</span></span>                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3ca59-194">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3ca59-194">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3ca59-195">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3ca59-195">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3ca59-196">Vue d'ensemble des types de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="3ca59-196">UI Automation Control Types Overview</span></span>](uiauto-controltypesoverview.md)
</dt> <dt>

[<span data-ttu-id="3ca59-197">Vue d'ensemble d'UI Automation</span><span class="sxs-lookup"><span data-stu-id="3ca59-197">UI Automation Overview</span></span>](uiauto-uiautomationoverview.md)
</dt> <dt>

<span data-ttu-id="3ca59-198">**Référence**</span><span class="sxs-lookup"><span data-stu-id="3ca59-198">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3ca59-199">**Contrôle XAML AppBar**</span><span class="sxs-lookup"><span data-stu-id="3ca59-199">**AppBar XAML control**</span></span>](/uwp/api/Windows.UI.Xaml.Controls.AppBar)
</dt> <dt>

<span data-ttu-id="3ca59-200">[**WinJS. UI. AppBar, objet**](/previous-versions/windows/apps/br229670(v=win.10))</span><span class="sxs-lookup"><span data-stu-id="3ca59-200">[**WinJS.UI.AppBar object**](/previous-versions/windows/apps/br229670(v=win.10))</span></span>
</dt> </dl>

 

 