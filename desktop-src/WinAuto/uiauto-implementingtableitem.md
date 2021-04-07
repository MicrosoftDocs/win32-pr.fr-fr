---
title: Modèle de contrôle TableItem
description: Fournit des instructions et des conventions pour l’implémentation de ITableItemProvider, y compris des informations sur les méthodes. Le modèle de contrôle TableItem est utilisé pour prendre en charge les contrôles enfants des conteneurs qui implémentent ITableProvider.
ms.assetid: e00c7a58-410c-4818-8f61-57ee98527d6e
keywords:
- UI Automation, implémentation du modèle de contrôle TableItem
- UI Automation, modèle de contrôle TableItem
- UI Automation, ITableItemProvider
- ITableItemProvider
- implémentation des modèles de contrôle TableItem d’UI Automation
- Modèles de contrôle TableItem
- modèles de contrôle, ITableItemProvider
- modèles de contrôle, implémenter des TableItem UI Automation
- modèles de contrôle, TableItem
- interfaces, ITableItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bae3e6d5379ec9a662e31ec6181476b112631381
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672385"
---
# <a name="tableitem-control-pattern"></a><span data-ttu-id="6ee05-114">Modèle de contrôle TableItem</span><span class="sxs-lookup"><span data-stu-id="6ee05-114">TableItem Control Pattern</span></span>

<span data-ttu-id="6ee05-115">Fournit des instructions et des conventions pour l’implémentation de [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), y compris des informations sur les méthodes.</span><span class="sxs-lookup"><span data-stu-id="6ee05-115">Describes guidelines and conventions for implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider), including information about methods.</span></span> <span data-ttu-id="6ee05-116">Le modèle de contrôle **TableItem** est utilisé pour prendre en charge les contrôles enfants des conteneurs qui implémentent [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span><span class="sxs-lookup"><span data-stu-id="6ee05-116">The **TableItem** control pattern is used to support child controls of containers that implement [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider).</span></span>

<span data-ttu-id="6ee05-117">L’accès aux fonctionnalités des cellules individuelles est fourni par l’implémentation simultanée requise de [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span><span class="sxs-lookup"><span data-stu-id="6ee05-117">Access to individual cell functionality is provided by the required, concurrent implementation of [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider).</span></span> <span data-ttu-id="6ee05-118">Ce modèle de contrôle est analogue à **IGridItemProvider** , à la différence que tout contrôle qui implémente [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) doit exposer par programmation la relation entre la cellule individuelle et ses informations de ligne et de colonne.</span><span class="sxs-lookup"><span data-stu-id="6ee05-118">This control pattern is analogous to **IGridItemProvider** with the distinction that any control implementing [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) must programmatically expose the relationship between the individual cell and its row and column information.</span></span> <span data-ttu-id="6ee05-119">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="6ee05-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="6ee05-120">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="6ee05-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="6ee05-121">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="6ee05-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="6ee05-122">Membres requis pour **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="6ee05-122">Required Members for **ITableItemProvider**</span></span>](#required-members-for-itableitemprovider)
-   [<span data-ttu-id="6ee05-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ee05-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="6ee05-124">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="6ee05-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="6ee05-125">Lorsque vous implémentez le modèle de contrôle **TableItem** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="6ee05-125">When implementing the **TableItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="6ee05-126">Pour obtenir des fonctionnalités d’élément de grille associées, consultez [modèle de contrôle GridItem](uiauto-implementinggriditem.md).</span><span class="sxs-lookup"><span data-stu-id="6ee05-126">For related grid item functionality, see [GridItem Control Pattern](uiauto-implementinggriditem.md).</span></span>

## <a name="required-members-for-itableitemprovider"></a><span data-ttu-id="6ee05-127">Membres requis pour **ITableItemProvider**</span><span class="sxs-lookup"><span data-stu-id="6ee05-127">Required Members for **ITableItemProvider**</span></span>

<span data-ttu-id="6ee05-128">Les méthodes suivantes sont requises pour implémenter l’interface [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="6ee05-128">The following methods are required for implementing the [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) interface.</span></span>



| <span data-ttu-id="6ee05-129">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="6ee05-129">Required members</span></span>                                                               | <span data-ttu-id="6ee05-130">Type de membre</span><span class="sxs-lookup"><span data-stu-id="6ee05-130">Member type</span></span> | <span data-ttu-id="6ee05-131">Notes</span><span class="sxs-lookup"><span data-stu-id="6ee05-131">Notes</span></span> |
|--------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="6ee05-132">**GetColumnHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="6ee05-132">**GetColumnHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getcolumnheaderitems) | <span data-ttu-id="6ee05-133">Méthode</span><span class="sxs-lookup"><span data-stu-id="6ee05-133">Method</span></span>      | <span data-ttu-id="6ee05-134">Aucun</span><span class="sxs-lookup"><span data-stu-id="6ee05-134">None</span></span>  |
| [<span data-ttu-id="6ee05-135">**GetRowHeaderItems**</span><span class="sxs-lookup"><span data-stu-id="6ee05-135">**GetRowHeaderItems**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableitemprovider-getrowheaderitems)       | <span data-ttu-id="6ee05-136">Méthode</span><span class="sxs-lookup"><span data-stu-id="6ee05-136">Method</span></span>      | <span data-ttu-id="6ee05-137">Aucun</span><span class="sxs-lookup"><span data-stu-id="6ee05-137">None</span></span>  |



 

<span data-ttu-id="6ee05-138">Ce modèle de contrôle n’est associé à aucune propriété ni à aucun événement.</span><span class="sxs-lookup"><span data-stu-id="6ee05-138">This control pattern has no associated properties or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ee05-139">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6ee05-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="6ee05-140">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="6ee05-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="6ee05-141">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ee05-141">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="6ee05-142">Table (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="6ee05-142">Table Control Pattern</span></span>](uiauto-implementingtable.md)
</dt> <dt>

[<span data-ttu-id="6ee05-143">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="6ee05-143">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="6ee05-144">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="6ee05-144">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




