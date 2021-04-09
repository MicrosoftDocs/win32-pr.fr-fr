---
title: Dock (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IDockProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Dock est utilisé pour exposer les propriétés d’ancrage d’un contrôle dans un conteneur d’ancrage.
ms.assetid: a6ea269b-632e-48ce-ac3b-edd7cc34d986
keywords:
- UI Automation, implémenter le modèle de contrôle Dock
- UI Automation, modèle de contrôle Dock
- UI Automation, IDockProvider
- IDockProvider
- implémentation des modèles de contrôle Dock UI Automation
- modèles de contrôle d’ancrage
- modèles de contrôle, IDockProvider
- modèles de contrôle, implémenter Dock UI Automation
- modèles de contrôle, ancrer
- interfaces, IDockProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87381669889ca7dd33811a030a718448f4b79cb5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839874"
---
# <a name="dock-control-pattern"></a><span data-ttu-id="f57ab-114">Dock (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="f57ab-114">Dock Control Pattern</span></span>

<span data-ttu-id="f57ab-115">Fournit des instructions et des conventions pour l’implémentation de [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="f57ab-115">Describes guidelines and conventions for implementing [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider), including information about properties and methods.</span></span> <span data-ttu-id="f57ab-116">Le modèle de contrôle **Dock** est utilisé pour exposer les propriétés d’ancrage d’un contrôle dans un conteneur d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="f57ab-116">The **Dock** control pattern is used to expose the dock properties of a control within a docking container.</span></span>

<span data-ttu-id="f57ab-117">Un conteneur d’ancrage est un contrôle qui vous permet de réorganiser des éléments enfants horizontalement et verticalement, les uns par rapport aux autres.</span><span class="sxs-lookup"><span data-stu-id="f57ab-117">A docking container is a control that allows you to arrange child elements horizontally and vertically, relative to each other.</span></span> <span data-ttu-id="f57ab-118">L’illustration suivante montre un conteneur d’ancrage avec deux éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="f57ab-118">The following image shows a docking container with two child elements.</span></span> <span data-ttu-id="f57ab-119">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="f57ab-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![capture d’écran montrant un conteneur d’ancrage avec deux enfants ancrés](images/dockxmpl.jpg)

<span data-ttu-id="f57ab-121">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="f57ab-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f57ab-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="f57ab-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="f57ab-123">Membres requis pour **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="f57ab-123">Required Members for **IDockProvider**</span></span>](#required-members-for-idockprovider)
-   [<span data-ttu-id="f57ab-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f57ab-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="f57ab-125">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="f57ab-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="f57ab-126">Lorsque vous implémentez le modèle de contrôle **Dock** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f57ab-126">When implementing the **Dock** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="f57ab-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) n’expose aucune propriété du conteneur d’ancrage ni aucune propriété des contrôles qui sont ancrés adjacents au contrôle actuel dans le conteneur d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="f57ab-127">[**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) does not expose any properties of the docking container or any properties of controls that are docked adjacent to the current control within the docking container.</span></span>
-   <span data-ttu-id="f57ab-128">Les contrôles sont ancrés les uns par rapport aux autres selon leur ordre de plan actuel ; plus leur positionnement dans l’ordre de plan est haut, plus ils sont placés loin du bord spécifié du conteneur d’ancrage.</span><span class="sxs-lookup"><span data-stu-id="f57ab-128">Controls are docked relative to each other based on their current z-order; the higher their z-order placement, the farther they are placed from the specified edge of the docking container.</span></span>
-   <span data-ttu-id="f57ab-129">Si le conteneur d’ancrage est redimensionné, tout contrôle ancré dans le conteneur est repositionné sur le même bord que celui auquel il était ancré à l’origine.</span><span class="sxs-lookup"><span data-stu-id="f57ab-129">If the docking container is resized, any docked controls within the container will be repositioned flush to the same edge to which they were originally docked.</span></span> <span data-ttu-id="f57ab-130">Les contrôles ancrés sont également redimensionnés pour remplir tout l’espace dans le conteneur d’après le comportement d’ancrage de leur propriété [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) .</span><span class="sxs-lookup"><span data-stu-id="f57ab-130">The docked controls will also resize to fill any space within the container according to the docking behavior of their [**DockPosition**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition) property.</span></span> <span data-ttu-id="f57ab-131">Par exemple, si **DockPosition \_ Top** est spécifié, les côtés gauche et droit du contrôle sont développés pour remplir tout l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="f57ab-131">For example, if **DockPosition\_Top** is specified, the left and right sides of the control will expand to fill any available space.</span></span> <span data-ttu-id="f57ab-132">Si **DockPosition \_ Fill** est spécifié, les quatre côtés du contrôle sont développés pour remplir tout l’espace disponible.</span><span class="sxs-lookup"><span data-stu-id="f57ab-132">If **DockPosition\_Fill** is specified, all four sides of the control will expand to fill any available space.</span></span>
-   <span data-ttu-id="f57ab-133">Sur un système à écrans multiples, les contrôles doivent être ancrés au côté gauche ou droit de l’écran actif.</span><span class="sxs-lookup"><span data-stu-id="f57ab-133">On a multi-monitor system, controls should dock to the left or right side of the current monitor.</span></span> <span data-ttu-id="f57ab-134">Si ce n’est pas possible, ils doivent être ancrés au côté gauche de l’écran le plus à gauche ou au côté droit de l’écran le plus à droite.</span><span class="sxs-lookup"><span data-stu-id="f57ab-134">If that is not possible, they should dock to the left side of the leftmost monitor or the right side of the rightmost monitor.</span></span>

## <a name="required-members-for-idockprovider"></a><span data-ttu-id="f57ab-135">Membres requis pour **IDockProvider**</span><span class="sxs-lookup"><span data-stu-id="f57ab-135">Required Members for **IDockProvider**</span></span>

<span data-ttu-id="f57ab-136">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) .</span><span class="sxs-lookup"><span data-stu-id="f57ab-136">The following properties and methods are required for implementing the [**IDockProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-idockprovider) interface.</span></span>



| <span data-ttu-id="f57ab-137">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="f57ab-137">Required members</span></span>                                                | <span data-ttu-id="f57ab-138">Type de membre</span><span class="sxs-lookup"><span data-stu-id="f57ab-138">Member type</span></span> | <span data-ttu-id="f57ab-139">Notes</span><span class="sxs-lookup"><span data-stu-id="f57ab-139">Notes</span></span> |
|-----------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="f57ab-140">**DockPosition**</span><span class="sxs-lookup"><span data-stu-id="f57ab-140">**DockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-get_dockposition)       | <span data-ttu-id="f57ab-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="f57ab-141">Property</span></span>    | <span data-ttu-id="f57ab-142">Aucun</span><span class="sxs-lookup"><span data-stu-id="f57ab-142">None</span></span>  |
| [<span data-ttu-id="f57ab-143">**SetDockPosition**</span><span class="sxs-lookup"><span data-stu-id="f57ab-143">**SetDockPosition**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-idockprovider-setdockposition) | <span data-ttu-id="f57ab-144">Méthode</span><span class="sxs-lookup"><span data-stu-id="f57ab-144">Method</span></span>      | <span data-ttu-id="f57ab-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="f57ab-145">None</span></span>  |



 

<span data-ttu-id="f57ab-146">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="f57ab-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f57ab-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f57ab-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f57ab-148">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="f57ab-148">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="f57ab-149">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="f57ab-149">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="f57ab-150">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="f57ab-150">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




