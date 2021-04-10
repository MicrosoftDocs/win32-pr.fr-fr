---
title: Selection (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ISelectionProvider, y compris des informations sur les propriétés, les méthodes et les événements.
ms.assetid: 9371e656-6f93-4a43-bd0c-c6977348b16a
keywords:
- UI Automation, implémenter le modèle de contrôle Selection
- UI Automation, modèle de contrôle Selection
- UI Automation, ISelectionProvider
- ISelectionProvider
- implémentation des modèles de contrôle Selection d’UI Automation
- Modèles de contrôle de sélection
- modèles de contrôle, ISelectionProvider
- modèles de contrôle, implémenter la sélection UI Automation
- modèles de contrôle, sélection
- interfaces, ISelectionProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ad6950302373494f307c91c0aadaeab1db0132a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029269"
---
# <a name="selection-control-pattern"></a><span data-ttu-id="3a17c-113">Selection (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="3a17c-113">Selection Control Pattern</span></span>

<span data-ttu-id="3a17c-114">Fournit des instructions et des conventions pour l’implémentation de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), y compris des informations sur les propriétés, les méthodes et les événements.</span><span class="sxs-lookup"><span data-stu-id="3a17c-114">Describes guidelines and conventions for implementing [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="3a17c-115">Le modèle de contrôle **Selection** est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants sélectionnables.</span><span class="sxs-lookup"><span data-stu-id="3a17c-115">The **Selection** control pattern is used to support controls that act as containers for a collection of selectable child items.</span></span> <span data-ttu-id="3a17c-116">Les enfants de cet élément doivent implémenter [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="3a17c-116">The children of this element must implement [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

<span data-ttu-id="3a17c-117">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="3a17c-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="3a17c-118">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3a17c-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3a17c-119">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="3a17c-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="3a17c-120">Membres requis pour **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="3a17c-120">Required Members for **ISelectionProvider**</span></span>](#required-members-for-iselectionprovider)
-   [<span data-ttu-id="3a17c-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a17c-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="3a17c-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="3a17c-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="3a17c-123">Lorsque vous implémentez le modèle de contrôle **Selection** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a17c-123">When implementing the **Selection** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="3a17c-124">Les contrôles qui implémentent [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) autorisent la sélection d’un ou de plusieurs éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="3a17c-124">Controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) allow either single or multiple child items to be selected.</span></span> <span data-ttu-id="3a17c-125">Par exemple, les zones de liste, les affichages de liste et les arborescences prennent en charge les sélections multiples, alors que les zones de liste modifiable, les curseurs et les groupes de cases d’option prennent en charge la sélection unique</span><span class="sxs-lookup"><span data-stu-id="3a17c-125">For example, list boxes, list views, and tree views support multiple selections, whereas combo boxes, sliders, and radio button groups support single selection.</span></span>
-   <span data-ttu-id="3a17c-126">Les contrôles qui ont une plage minimale, maximale et continue, tels que le contrôle Slider **volume** d’un lecteur multimédia, doivent implémenter [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) au lieu de [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="3a17c-126">Controls that have a minimum, maximum, and continuous range, such as the **Volume** slider control of a media player, should implement [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) instead of [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>
-   <span data-ttu-id="3a17c-127">Les contrôles à sélection unique qui gèrent des contrôles enfants qui implémentent [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), tels que le curseur **résolution d’écran** dans la boîte de dialogue des propriétés d' **affichage** pour Windows, ou le contrôle de sélection du **Sélecteur de couleurs** de Microsoft Word (Voir l’image suivante), doivent implémenter [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); leurs enfants doivent implémenter à la fois [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) et [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="3a17c-127">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, or the **Color Picker** selection control from Microsoft Word (see the following image), should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

    ![image présentant un exemple de mappage de chaîne d’échantillons de couleurs](images/uia-valuepattern-colorpicker.jpg)

-   <span data-ttu-id="3a17c-129">Les menus ne prennent pas en charge le modèle de contrôle **Selection** .</span><span class="sxs-lookup"><span data-stu-id="3a17c-129">Menus do not support the **Selection** control pattern.</span></span> <span data-ttu-id="3a17c-130">Si vous utilisez des éléments de menu qui incluent à la fois des graphiques et du texte (tels que les éléments du **volet de visualisation** dans le menu **affichage** de Microsoft Outlook) et que vous devez communiquer l’État, vous devez implémenter [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span><span class="sxs-lookup"><span data-stu-id="3a17c-130">If you are working with menu items that include both graphics and text (such as the **Preview Pane** items in the **View** menu in Microsoft Outlook) and need to convey state, you should implement [**IToggleProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itoggleprovider).</span></span>

## <a name="required-members-for-iselectionprovider"></a><span data-ttu-id="3a17c-131">Membres requis pour **ISelectionProvider**</span><span class="sxs-lookup"><span data-stu-id="3a17c-131">Required Members for **ISelectionProvider**</span></span>

<span data-ttu-id="3a17c-132">Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) .</span><span class="sxs-lookup"><span data-stu-id="3a17c-132">The following properties, methods, and events are required for implementing the [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider) interface.</span></span>



| <span data-ttu-id="3a17c-133">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="3a17c-133">Required members</span></span>                                                                                | <span data-ttu-id="3a17c-134">Type de membre</span><span class="sxs-lookup"><span data-stu-id="3a17c-134">Member type</span></span> | <span data-ttu-id="3a17c-135">Notes</span><span class="sxs-lookup"><span data-stu-id="3a17c-135">Notes</span></span>                                                                       |
|-------------------------------------------------------------------------------------------------|-------------|-----------------------------------------------------------------------------|
| [<span data-ttu-id="3a17c-136">**CanSelectMultiple**</span><span class="sxs-lookup"><span data-stu-id="3a17c-136">**CanSelectMultiple**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple)                        | <span data-ttu-id="3a17c-137">Propriété</span><span class="sxs-lookup"><span data-stu-id="3a17c-137">Property</span></span>    | <span data-ttu-id="3a17c-138">Aucun</span><span class="sxs-lookup"><span data-stu-id="3a17c-138">None</span></span>                                                                        |
| [<span data-ttu-id="3a17c-139">**IsSelectionRequired**</span><span class="sxs-lookup"><span data-stu-id="3a17c-139">**IsSelectionRequired**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired)                    | <span data-ttu-id="3a17c-140">Propriété</span><span class="sxs-lookup"><span data-stu-id="3a17c-140">Property</span></span>    | <span data-ttu-id="3a17c-141">Aucun</span><span class="sxs-lookup"><span data-stu-id="3a17c-141">None</span></span>                                                                        |
| [<span data-ttu-id="3a17c-142">**GetSelection**</span><span class="sxs-lookup"><span data-stu-id="3a17c-142">**GetSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-getselection)                                  | <span data-ttu-id="3a17c-143">Méthode</span><span class="sxs-lookup"><span data-stu-id="3a17c-143">Method</span></span>      | <span data-ttu-id="3a17c-144">Aucun</span><span class="sxs-lookup"><span data-stu-id="3a17c-144">None</span></span>                                                                        |
| [<span data-ttu-id="3a17c-145">**\_InvalidatedEventId de sélection UIA \_**</span><span class="sxs-lookup"><span data-stu-id="3a17c-145">**UIA\_Selection\_InvalidatedEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="3a17c-146">Événement</span><span class="sxs-lookup"><span data-stu-id="3a17c-146">Event</span></span>       | <span data-ttu-id="3a17c-147">Déclenchez cet événement lorsqu’une sélection dans un conteneur a changé de manière significative.</span><span class="sxs-lookup"><span data-stu-id="3a17c-147">Raise this event when a selection in a container has changed significantly.</span></span> |



 

<span data-ttu-id="3a17c-148">Les propriétés [**ISelectionProvider :: IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) et [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) peuvent être dynamiques.</span><span class="sxs-lookup"><span data-stu-id="3a17c-148">The [**ISelectionProvider::IsSelectionRequired**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_isselectionrequired) and [**CanSelectMultiple**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionprovider-get_canselectmultiple) properties can be dynamic.</span></span> <span data-ttu-id="3a17c-149">Par exemple, l’état initial d’un contrôle peut ne pas avoir d’éléments sélectionnés par défaut, ce qui indique que **IsSelectionRequired** a la valeur false.</span><span class="sxs-lookup"><span data-stu-id="3a17c-149">For example, the initial state of a control might not have any items selected by default, indicating that **IsSelectionRequired** is false.</span></span> <span data-ttu-id="3a17c-150">Toutefois, une fois qu’un élément a été sélectionné, le contrôle doit toujours avoir au moins un élément sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3a17c-150">However, after an item is selected, the control must always have at least one item selected.</span></span> <span data-ttu-id="3a17c-151">De la même façon, dans quelques cas rares, un contrôle peut autoriser la sélection de plusieurs éléments lors de l’initialisation, mais n’autoriser par la suite que des sélections uniques.</span><span class="sxs-lookup"><span data-stu-id="3a17c-151">Similarly, in rare cases, a control might allow multiple items to be selected on initialization, but subsequently allow only single selections to be made.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3a17c-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a17c-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a17c-153">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="3a17c-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="3a17c-154">Modèle de contrôle SelectionItem</span><span class="sxs-lookup"><span data-stu-id="3a17c-154">SelectionItem Control Pattern</span></span>](uiauto-implementingselectionitem.md)
</dt> <dt>

[<span data-ttu-id="3a17c-155">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="3a17c-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="3a17c-156">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="3a17c-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




