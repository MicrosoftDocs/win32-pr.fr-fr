---
title: Grid (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IGridProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Grid est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.
ms.assetid: c50fb6f7-884a-4147-a6b2-c59d787fc04b
keywords:
- UI Automation, implémenter le modèle de contrôle Grid
- UI Automation, modèle de contrôle Grid
- UI Automation, IGridProvider
- IGridProvider
- implémentation de modèles de contrôle de grille UI Automation
- Modèles de contrôle Grid
- modèles de contrôle, IGridProvider
- modèles de contrôle, implémenter la grille UI Automation
- modèles de contrôle, grille
- interfaces, IGridProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 328d8536a367389a6d17422bd6f6476a3e82aa11
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028973"
---
# <a name="grid-control-pattern"></a><span data-ttu-id="15414-114">Grid (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="15414-114">Grid Control Pattern</span></span>

<span data-ttu-id="15414-115">Fournit des instructions et des conventions pour l’implémentation de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="15414-115">Describes guidelines and conventions for implementing [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider), including information about properties and methods.</span></span> <span data-ttu-id="15414-116">Le modèle de contrôle **Grid** est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="15414-116">The **Grid** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="15414-117">Les enfants de cet élément doivent implémenter [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) et être organisés dans un système de coordonnées logiques à deux dimensions qui peut être parcouru par ligne et par colonne.</span><span class="sxs-lookup"><span data-stu-id="15414-117">The children of this element must implement [**IGridItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igriditemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="15414-118">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="15414-118">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="15414-119">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="15414-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="15414-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="15414-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="15414-121">Membres requis pour **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="15414-121">Required Members for **IGridProvider**</span></span>](#required-members-for-igridprovider)
-   [<span data-ttu-id="15414-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15414-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="15414-123">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="15414-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="15414-124">Lorsque vous implémentez le modèle de contrôle **Grid** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="15414-124">When implementing the **Grid** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="15414-125">Les coordonnées de grille sont de base zéro avec la cellule supérieure gauche (ou supérieure droite en fonction des paramètres régionaux) qui ont des coordonnées (0, 0).</span><span class="sxs-lookup"><span data-stu-id="15414-125">Grid coordinates are zero-based with the upper left (or upper right cell depending on locale) having coordinates (0,0).</span></span>
-   <span data-ttu-id="15414-126">Si une cellule est vide, un élément Microsoft UI Automation doit être retourné pour permettre la prise en charge de la propriété [**IGridItemProvider :: ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) pour cette cellule.</span><span class="sxs-lookup"><span data-stu-id="15414-126">If a cell is empty, a Microsoft UI Automation element must still be returned in order to support the [**IGridItemProvider::ContainingGrid**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igriditemprovider-get_containinggrid) property for that cell.</span></span> <span data-ttu-id="15414-127">Cela est possible quand la disposition des éléments enfants de la grille est semblable à celle d’un tableau non justifié (consultez l’exemple ci-dessous).</span><span class="sxs-lookup"><span data-stu-id="15414-127">This is possible when the layout of child elements in the grid is similar to a ragged array (see example below).</span></span>

    ![exemple de contrôle Grid avec des coordonnées vides](images/grid.png)

-   <span data-ttu-id="15414-129">Une grille avec un seul élément est toujours nécessaire pour implémenter [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) s’il est logiquement considéré comme une grille.</span><span class="sxs-lookup"><span data-stu-id="15414-129">A grid with a single item is still required to implement [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) if it is logically considered to be a grid.</span></span> <span data-ttu-id="15414-130">Le nombre d’éléments enfants de la grille est immatériel.</span><span class="sxs-lookup"><span data-stu-id="15414-130">The number of child items in the grid is immaterial.</span></span>
-   <span data-ttu-id="15414-131">Selon l’implémentation du fournisseur, les lignes et les colonnes masquées peuvent être chargées dans l’arborescence UI Automation et sont donc reflétées dans les propriétés [**IGridProvider :: RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) et [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) .</span><span class="sxs-lookup"><span data-stu-id="15414-131">Hidden rows and columns, depending on the provider implementation, may be loaded in the UI Automation tree and will therefore be reflected in the [**IGridProvider::RowCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount) and [**ColumnCount**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) properties.</span></span> <span data-ttu-id="15414-132">Si les lignes et les colonnes masquées n’ont pas encore été chargées, elles ne doivent pas être comptabilisées.</span><span class="sxs-lookup"><span data-stu-id="15414-132">If the hidden rows and columns have not yet been loaded, they should not be counted.</span></span>
-   <span data-ttu-id="15414-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) n’active pas la manipulation active d’une grille ; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) doit être implémenté pour activer cette fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="15414-133">[**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) does not enable active manipulation of a grid; [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) must be implemented to enable this functionality.</span></span>
-   <span data-ttu-id="15414-134">Utilisez un [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) pour écouter les changements structurels ou de disposition apportés à la grille, tels que les cellules qui ont été ajoutées, supprimées ou fusionnées.</span><span class="sxs-lookup"><span data-stu-id="15414-134">Use a [**IUIAutomationStructureChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationstructurechangedeventhandler) to listen for structural or layout changes to the grid such as cells that have been added, removed, or merged.</span></span>
-   <span data-ttu-id="15414-135">Utilisez un [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) pour suivre le parcours des éléments ou des cellules d’une grille.</span><span class="sxs-lookup"><span data-stu-id="15414-135">Use a [**IUIAutomationFocusChangedEventHandler**](/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationfocuschangedeventhandler) to track traversal through the items or cells of a grid.</span></span>

## <a name="required-members-for-igridprovider"></a><span data-ttu-id="15414-136">Membres requis pour **IGridProvider**</span><span class="sxs-lookup"><span data-stu-id="15414-136">Required Members for **IGridProvider**</span></span>

<span data-ttu-id="15414-137">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) .</span><span class="sxs-lookup"><span data-stu-id="15414-137">The following properties and methods are required for implementing the [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) interface.</span></span>



| <span data-ttu-id="15414-138">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="15414-138">Required members</span></span>                                        | <span data-ttu-id="15414-139">Type de membre</span><span class="sxs-lookup"><span data-stu-id="15414-139">Member type</span></span> | <span data-ttu-id="15414-140">Notes</span><span class="sxs-lookup"><span data-stu-id="15414-140">Notes</span></span> |
|---------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="15414-141">**Stopp**</span><span class="sxs-lookup"><span data-stu-id="15414-141">**RowCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_rowcount)       | <span data-ttu-id="15414-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="15414-142">Property</span></span>    | <span data-ttu-id="15414-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="15414-143">None</span></span>  |
| [<span data-ttu-id="15414-144">**ColumnCount**</span><span class="sxs-lookup"><span data-stu-id="15414-144">**ColumnCount**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-get_columncount) | <span data-ttu-id="15414-145">Propriété</span><span class="sxs-lookup"><span data-stu-id="15414-145">Property</span></span>    | <span data-ttu-id="15414-146">Aucun</span><span class="sxs-lookup"><span data-stu-id="15414-146">None</span></span>  |
| [<span data-ttu-id="15414-147">**GetItem**</span><span class="sxs-lookup"><span data-stu-id="15414-147">**GetItem**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-igridprovider-getitem)         | <span data-ttu-id="15414-148">Méthode</span><span class="sxs-lookup"><span data-stu-id="15414-148">Method</span></span>      | <span data-ttu-id="15414-149">Aucun</span><span class="sxs-lookup"><span data-stu-id="15414-149">None</span></span>  |



 

<span data-ttu-id="15414-150">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="15414-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15414-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="15414-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15414-152">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="15414-152">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="15414-153">GridItem (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="15414-153">GridItem Control Pattern</span></span>](uiauto-implementinggriditem.md)
</dt> <dt>

[<span data-ttu-id="15414-154">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="15414-154">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="15414-155">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="15414-155">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




