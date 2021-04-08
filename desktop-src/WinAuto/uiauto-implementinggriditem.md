---
title: GridItem (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IGridItemProvider, y compris des informations sur les propriétés. Le modèle de contrôle GridItem est utilisé pour prendre en charge les contrôles enfants individuels des conteneurs qui implémentent IGridProvider.
ms.assetid: ae4b9021-1800-485b-99a2-54ddf9c21f93
keywords:
- UI Automation, implémentation du modèle de contrôle GridItem
- UI Automation, modèle de contrôle GridItem
- UI Automation, IGridItemProvider
- IGridItemProvider
- implémentation des modèles de contrôle GridItem d’UI Automation
- Modèles de contrôle GridItem
- modèles de contrôle, IGridItemProvider
- modèles de contrôle, implémentation de GridItem UI Automation
- modèles de contrôle, GridItem
- interfaces, IGridItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ef45b5f655e3ef09350c508271233de49f964a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103672662"
---
# <a name="griditem-control-pattern"></a><span data-ttu-id="2cd92-114">GridItem (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="2cd92-114">GridItem Control Pattern</span></span>

<span data-ttu-id="2cd92-115">Fournit des instructions et des conventions pour l’implémentation de [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), y compris des informations sur les propriétés.</span><span class="sxs-lookup"><span data-stu-id="2cd92-115">Describes guidelines and conventions for implementing [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider), including information about properties.</span></span> <span data-ttu-id="2cd92-116">Le modèle de contrôle **GridItem** est utilisé pour prendre en charge les contrôles enfants individuels des conteneurs qui implémentent [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="2cd92-116">The **GridItem** control pattern is used to support individual child controls of containers that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>

<span data-ttu-id="2cd92-117">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="2cd92-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="2cd92-118">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="2cd92-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="2cd92-119">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="2cd92-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="2cd92-120">Membres requis pour **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="2cd92-120">Required Members for **IGridItemProvider**</span></span>](#required-members-for-igriditemprovider)
-   [<span data-ttu-id="2cd92-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2cd92-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="2cd92-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="2cd92-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="2cd92-123">Lorsque vous implémentez le modèle de contrôle **GridItem** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="2cd92-123">When implementing the **GridItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="2cd92-124">Les coordonnées de grille ont une base zéro et la cellule supérieure gauche possède les coordonnées (0, 0).</span><span class="sxs-lookup"><span data-stu-id="2cd92-124">Grid coordinates are zero-based with the upper left cell having coordinates (0, 0).</span></span>
-   <span data-ttu-id="2cd92-125">Les cellules fusionnées signalent leurs propriétés de [**ligne**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) et de [**colonne**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) en fonction de leur cellule d’ancrage sous-jacente, tel que défini par le fournisseur Microsoft UI Automation.</span><span class="sxs-lookup"><span data-stu-id="2cd92-125">Merged cells will report their [**Row**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row) and [**Column**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column) properties based on their underlying anchor cell as defined by the Microsoft UI Automation provider.</span></span> <span data-ttu-id="2cd92-126">En règle générale, il s’agit de la ligne la plus haute ou de la colonne la plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="2cd92-126">Typically, it will be the topmost and leftmost row or column.</span></span>
-   <span data-ttu-id="2cd92-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) ne fournit pas de manipulation active de la grille telle que la fusion ou le fractionnement des cellules.</span><span class="sxs-lookup"><span data-stu-id="2cd92-127">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not provide for active manipulation of the grid such as merging or splitting cells.</span></span>
-   <span data-ttu-id="2cd92-128">Les contrôles qui implémentent [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) peuvent généralement être parcourus (autrement dit, un client UI Automation peut se déplacer vers des contrôles adjacents) à l’aide du clavier.</span><span class="sxs-lookup"><span data-stu-id="2cd92-128">Controls that implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) can typically be traversed (that is, a UI Automation client can move to adjacent controls) by using the keyboard.</span></span>

## <a name="required-members-for-igriditemprovider"></a><span data-ttu-id="2cd92-129">Membres requis pour **IGridItemProvider**</span><span class="sxs-lookup"><span data-stu-id="2cd92-129">Required Members for **IGridItemProvider**</span></span>

<span data-ttu-id="2cd92-130">Les propriétés suivantes sont requises pour implémenter l’interface [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) .</span><span class="sxs-lookup"><span data-stu-id="2cd92-130">The following properties are required for implementing the [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) interface.</span></span>



| <span data-ttu-id="2cd92-131">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="2cd92-131">Required members</span></span>                                                  | <span data-ttu-id="2cd92-132">Type de membre</span><span class="sxs-lookup"><span data-stu-id="2cd92-132">Member type</span></span> | <span data-ttu-id="2cd92-133">Notes</span><span class="sxs-lookup"><span data-stu-id="2cd92-133">Notes</span></span> |
|-------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="2cd92-134">**Haut**</span><span class="sxs-lookup"><span data-stu-id="2cd92-134">**Row**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_row)                       | <span data-ttu-id="2cd92-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="2cd92-135">Property</span></span>    | <span data-ttu-id="2cd92-136">Aucun</span><span class="sxs-lookup"><span data-stu-id="2cd92-136">None</span></span>  |
| [<span data-ttu-id="2cd92-137">**Chronique**</span><span class="sxs-lookup"><span data-stu-id="2cd92-137">**Column**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_column)                 | <span data-ttu-id="2cd92-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="2cd92-138">Property</span></span>    | <span data-ttu-id="2cd92-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="2cd92-139">None</span></span>  |
| [<span data-ttu-id="2cd92-140">**RowSpan**</span><span class="sxs-lookup"><span data-stu-id="2cd92-140">**RowSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_rowspan)               | <span data-ttu-id="2cd92-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="2cd92-141">Property</span></span>    | <span data-ttu-id="2cd92-142">Aucun</span><span class="sxs-lookup"><span data-stu-id="2cd92-142">None</span></span>  |
| [<span data-ttu-id="2cd92-143">**ColumnSpan**</span><span class="sxs-lookup"><span data-stu-id="2cd92-143">**ColumnSpan**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_columnspan)         | <span data-ttu-id="2cd92-144">Propriété</span><span class="sxs-lookup"><span data-stu-id="2cd92-144">Property</span></span>    | <span data-ttu-id="2cd92-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="2cd92-145">None</span></span>  |
| [<span data-ttu-id="2cd92-146">**ContainingGrid**</span><span class="sxs-lookup"><span data-stu-id="2cd92-146">**ContainingGrid**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) | <span data-ttu-id="2cd92-147">Propriété</span><span class="sxs-lookup"><span data-stu-id="2cd92-147">Property</span></span>    | <span data-ttu-id="2cd92-148">Aucun</span><span class="sxs-lookup"><span data-stu-id="2cd92-148">None</span></span>  |



 

<span data-ttu-id="2cd92-149">Ce modèle de contrôle n’est associé à aucune méthode ou aucun événement.</span><span class="sxs-lookup"><span data-stu-id="2cd92-149">This control pattern has no associated methods or events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2cd92-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2cd92-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2cd92-151">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="2cd92-151">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="2cd92-152">Grid (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="2cd92-152">Grid Control Pattern</span></span>](uiauto-implementinggrid.md)
</dt> <dt>

[<span data-ttu-id="2cd92-153">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="2cd92-153">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="2cd92-154">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="2cd92-154">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




