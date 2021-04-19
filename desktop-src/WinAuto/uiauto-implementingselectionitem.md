---
title: Modèle de contrôle SelectionItem
description: Fournit des instructions et des conventions pour l’implémentation de ISelectionItemProvider, y compris des informations sur les propriétés, les méthodes et les événements.
ms.assetid: 9314547f-7062-42db-b6a7-8a8eaef21d4e
keywords:
- UI Automation, implémentation du modèle de contrôle SelectionItem
- UI Automation, modèle de contrôle SelectionItem
- UI Automation, ISelectionItemProvider
- ISelectionItemProvider
- implémentation des modèles de contrôle SelectionItem d’UI Automation
- Modèles de contrôle SelectionItem
- modèles de contrôle, ISelectionItemProvider
- modèles de contrôle, implémenter des SelectionItem UI Automation
- modèles de contrôle, SelectionItem
- interfaces, ISelectionItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 912be363ea8228d905a600de091d6cbe12b925fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511204"
---
# <a name="selectionitem-control-pattern"></a><span data-ttu-id="ef463-113">Modèle de contrôle SelectionItem</span><span class="sxs-lookup"><span data-stu-id="ef463-113">SelectionItem Control Pattern</span></span>

<span data-ttu-id="ef463-114">Fournit des instructions et des conventions pour l’implémentation de [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), y compris des informations sur les propriétés, les méthodes et les événements.</span><span class="sxs-lookup"><span data-stu-id="ef463-114">Describes guidelines and conventions for implementing [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider), including information about properties, methods, and events.</span></span> <span data-ttu-id="ef463-115">Le modèle de contrôle **SelectionItem** est utilisé pour prendre en charge les contrôles qui agissent en tant qu’éléments enfants individuels et sélectionnables de contrôles conteneurs qui implémentent [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span><span class="sxs-lookup"><span data-stu-id="ef463-115">The **SelectionItem** control pattern is used to support controls that act as individual, selectable child items of container controls that implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider).</span></span>

<span data-ttu-id="ef463-116">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="ef463-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="ef463-117">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="ef463-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="ef463-118">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="ef463-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="ef463-119">Membres requis pour **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ef463-119">Required Members for **ISelectionItemProvider**</span></span>](#required-members-for-iselectionitemprovider)
-   [<span data-ttu-id="ef463-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef463-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="ef463-121">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="ef463-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="ef463-122">Lorsque vous implémentez le modèle de contrôle **SelectionItem** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="ef463-122">When implementing the **SelectionItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="ef463-123">Les contrôles à sélection unique qui gèrent des contrôles enfants qui implémentent [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), tels que le curseur **résolution d’écran** dans la boîte de dialogue des **propriétés d’affichage** pour Windows, doivent implémenter [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); leurs enfants doivent implémenter à la fois [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) et [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span><span class="sxs-lookup"><span data-stu-id="ef463-123">Single-selection controls that manage child controls that implement [**IRawElementProviderFragmentRoot**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragmentroot), such as the **Screen Resolution** slider in the **Display Properties** dialog for Windows, should implement [**ISelectionProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionprovider); their children should implement both [**IRawElementProviderFragment**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irawelementproviderfragment) and [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider).</span></span>

## <a name="required-members-for-iselectionitemprovider"></a><span data-ttu-id="ef463-124">Membres requis pour **ISelectionItemProvider**</span><span class="sxs-lookup"><span data-stu-id="ef463-124">Required Members for **ISelectionItemProvider**</span></span>

<span data-ttu-id="ef463-125">Les propriétés, méthodes et événements suivants sont requis pour implémenter l’interface [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="ef463-125">The following properties, methods, and events are required for implementing the [**ISelectionItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iselectionitemprovider) interface.</span></span>



| <span data-ttu-id="ef463-126">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="ef463-126">Required members</span></span>                                                                                                                        | <span data-ttu-id="ef463-127">Type de membre</span><span class="sxs-lookup"><span data-stu-id="ef463-127">Member type</span></span> | <span data-ttu-id="ef463-128">Notes</span><span class="sxs-lookup"><span data-stu-id="ef463-128">Notes</span></span> |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="ef463-129">**AddToSelection**</span><span class="sxs-lookup"><span data-stu-id="ef463-129">**AddToSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-addtoselection)                                                                  | <span data-ttu-id="ef463-130">Méthode</span><span class="sxs-lookup"><span data-stu-id="ef463-130">Method</span></span>      | <span data-ttu-id="ef463-131">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-131">None</span></span>  |
| [<span data-ttu-id="ef463-132">**IsSelected**</span><span class="sxs-lookup"><span data-stu-id="ef463-132">**IsSelected**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_isselected)                                                                          | <span data-ttu-id="ef463-133">Propriété</span><span class="sxs-lookup"><span data-stu-id="ef463-133">Property</span></span>    | <span data-ttu-id="ef463-134">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-134">None</span></span>  |
| [<span data-ttu-id="ef463-135">**RemoveFromSelection**</span><span class="sxs-lookup"><span data-stu-id="ef463-135">**RemoveFromSelection**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-removefromselection)                                                        | <span data-ttu-id="ef463-136">Méthode</span><span class="sxs-lookup"><span data-stu-id="ef463-136">Method</span></span>      | <span data-ttu-id="ef463-137">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-137">None</span></span>  |
| [<span data-ttu-id="ef463-138">**Sélectionner**</span><span class="sxs-lookup"><span data-stu-id="ef463-138">**Select**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select)                                                                                  | <span data-ttu-id="ef463-139">Méthode</span><span class="sxs-lookup"><span data-stu-id="ef463-139">Method</span></span>      | <span data-ttu-id="ef463-140">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-140">None</span></span>  |
| [<span data-ttu-id="ef463-141">**SelectionContainer**</span><span class="sxs-lookup"><span data-stu-id="ef463-141">**SelectionContainer**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-get_selectioncontainer)                                                          | <span data-ttu-id="ef463-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="ef463-142">Property</span></span>    | <span data-ttu-id="ef463-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-143">None</span></span>  |
| [<span data-ttu-id="ef463-144">**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="ef463-144">**UIA\_SelectionItem\_ElementAddedToSelectionEventId**</span></span>](uiauto-event-ids.md)         | <span data-ttu-id="ef463-145">Événement</span><span class="sxs-lookup"><span data-stu-id="ef463-145">Event</span></span>       | <span data-ttu-id="ef463-146">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-146">None</span></span>  |
| [<span data-ttu-id="ef463-147">**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**</span><span class="sxs-lookup"><span data-stu-id="ef463-147">**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**</span></span>](uiauto-event-ids.md) | <span data-ttu-id="ef463-148">Événement</span><span class="sxs-lookup"><span data-stu-id="ef463-148">Event</span></span>       | <span data-ttu-id="ef463-149">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-149">None</span></span>  |
| [<span data-ttu-id="ef463-150">**UIA \_ SelectionItem \_ ElementSelectedEventId**</span><span class="sxs-lookup"><span data-stu-id="ef463-150">**UIA\_SelectionItem\_ElementSelectedEventId**</span></span>](uiauto-event-ids.md)                         | <span data-ttu-id="ef463-151">Événement</span><span class="sxs-lookup"><span data-stu-id="ef463-151">Event</span></span>       | <span data-ttu-id="ef463-152">Aucun</span><span class="sxs-lookup"><span data-stu-id="ef463-152">None</span></span>  |



 

<span data-ttu-id="ef463-153">Si le résultat d’une [**sélection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), d' [**un AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection)ou d’un [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) est un élément sélectionné unique, un événement **ElementSelected** ([**UIA \_ SelectionItem \_ ElementSelectedEventId**](uiauto-event-ids.md)) doit être déclenché ; sinon, déclenchez les événements **ElementAddedToSelection** ([**UIA \_ SelectionItem \_ ElementAddedToSelectionEventId**](uiauto-event-ids.md)) ou **ElementRemovedFromSelection** ([**UIA \_ SelectionItem \_ ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) selon le cas.</span><span class="sxs-lookup"><span data-stu-id="ef463-153">If the result of a [**Select**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-select), an [**AddToSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-addtoselection), or a [**RemoveFromSelection**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationselectionitempattern-removefromselection) is a single selected item, an **ElementSelected** event ([**UIA\_SelectionItem\_ElementSelectedEventId**](uiauto-event-ids.md)) should be raised; otherwise raise **ElementAddedToSelection** ([**UIA\_SelectionItem\_ElementAddedToSelectionEventId**](uiauto-event-ids.md)) or **ElementRemovedFromSelection** ([**UIA\_SelectionItem\_ElementRemovedFromSelectionEventId**](uiauto-event-ids.md)) events as appropriate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ef463-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ef463-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef463-155">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="ef463-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="ef463-156">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="ef463-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="ef463-157">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="ef463-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




