---
title: Table (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ITableProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle table est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.
ms.assetid: 81a1a316-cdd6-4490-8de2-1b6db52d84e6
keywords:
- UI Automation, implémenter le modèle de contrôle table
- UI Automation, modèle de contrôle table
- UI Automation, ITableProvider
- ITableProvider
- implémentation de modèles de contrôle de table UI Automation
- Modèles de contrôle de table
- modèles de contrôle, ITableProvider
- modèles de contrôle, implémenter une table UI Automation
- modèles de contrôle, table
- interfaces, ITableProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9879d1589985df0257a1dd7805f474c013b93732
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104570999"
---
# <a name="table-control-pattern"></a><span data-ttu-id="b0a3f-114">Table (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="b0a3f-114">Table Control Pattern</span></span>

<span data-ttu-id="b0a3f-115">Fournit des instructions et des conventions pour l’implémentation de [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-115">Describes guidelines and conventions for implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider), including information about properties and methods.</span></span> <span data-ttu-id="b0a3f-116">Le modèle de contrôle **table** est utilisé pour prendre en charge les contrôles qui jouent le rôle de conteneurs pour une collection d’éléments enfants.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-116">The **Table** control pattern is used to support controls that act as containers for a collection of child elements.</span></span>

<span data-ttu-id="b0a3f-117">Les enfants de l’élément conteneur doivent implémenter [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) et être organisés dans un système de coordonnées logiques à deux dimensions qui peut être parcouru par ligne et par colonne.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-117">The children of the container element must implement [**ITableItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableitemprovider) and be organized in a two-dimensional logical coordinate system that can be traversed by row and column.</span></span> <span data-ttu-id="b0a3f-118">Ce modèle de contrôle est analogue à [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) , à la différence que tout contrôle qui implémente [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) doit également exposer une relation d’en-tête de colonne et/ou de ligne pour chaque élément enfant.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-118">This control pattern is analogous to [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider) with the distinction that any control implementing [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) must also expose a column and/or row header relationship for each child element.</span></span> <span data-ttu-id="b0a3f-119">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="b0a3f-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="b0a3f-120">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-120">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b0a3f-121">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b0a3f-121">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="b0a3f-122">Membres requis pour **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="b0a3f-122">Required Members for **ITableProvider**</span></span>](#required-members-for-itableprovider)
-   [<span data-ttu-id="b0a3f-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0a3f-123">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b0a3f-124">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b0a3f-124">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="b0a3f-125">Lorsque vous implémentez le modèle de contrôle **table** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b0a3f-125">When implementing the **Table** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="b0a3f-126">L’accès au contenu de cellules individuelles s’effectue par le biais d’un système de coordonnées logiques à deux dimensions ou d’un tableau fourni par l’implémentation simultanée requise de [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span><span class="sxs-lookup"><span data-stu-id="b0a3f-126">Access to the content of individual cells is through a two-dimensional logical coordinate system or array provided by the required, concurrent implementation of [**IGridProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-igridprovider).</span></span>
-   <span data-ttu-id="b0a3f-127">Un en-tête de colonne ou de ligne peut figurer dans un objet table ou être un objet d’en-tête séparé, associé à un objet table.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-127">A column or row header can be contained within a table object or be a separate header object that is associated with a table object.</span></span>
-   <span data-ttu-id="b0a3f-128">Les en-têtes de colonne et de ligne peuvent inclure un en-tête principal et des en-têtes de prise en charge quelconques.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-128">Column and row headers may include both a primary header as well as any supporting headers.</span></span>
    > [!Note]  
    > <span data-ttu-id="b0a3f-129">Ce concept devient évident dans une feuille de calcul Microsoft Excel où un utilisateur a défini une colonne **First Name** .</span><span class="sxs-lookup"><span data-stu-id="b0a3f-129">This concept becomes evident in a Microsoft Excel spreadsheet where a user has defined a **First name** column.</span></span> <span data-ttu-id="b0a3f-130">Cette colonne contient maintenant deux en-têtes, y compris l’en-tête de **prénom** défini par l’utilisateur, et la désignation alphanumérique pour cette colonne assignée par l’application.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-130">This column now has two headers, including the **First name** header defined by the user, and the alphanumeric designation for that column assigned by the application.</span></span>

     

-   <span data-ttu-id="b0a3f-131">Consultez [modèle de contrôle Grid](uiauto-implementinggrid.md) pour obtenir des fonctionnalités de grille associées.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-131">See [Grid Control Pattern](uiauto-implementinggrid.md) for related grid functionality.</span></span>

    <span data-ttu-id="b0a3f-132">L’illustration suivante montre un tableau avec des en-têtes de colonnes complexes.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-132">The following image shows a table with complex column headers.</span></span>

    ![table avec en-têtes de colonnes complexes](images/uia-valuepattern-colorpicker.jpg)

    <span data-ttu-id="b0a3f-134">L’illustration suivante montre une table avec une propriété [**ITableProvider :: RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) ambiguë.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-134">The following image shows a table with an ambiguous [**ITableProvider::RowOrColumnMajor**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) property.</span></span>

    ![table avec une propriété RowOrColumnMajor ambiguë](images/uia-tablepattern-roworcolumnmajorproperty.jpg)

## <a name="required-members-for-itableprovider"></a><span data-ttu-id="b0a3f-136">Membres requis pour **ITableProvider**</span><span class="sxs-lookup"><span data-stu-id="b0a3f-136">Required Members for **ITableProvider**</span></span>

<span data-ttu-id="b0a3f-137">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) .</span><span class="sxs-lookup"><span data-stu-id="b0a3f-137">The following properties and methods are required for implementing the [**ITableProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itableprovider) interface.</span></span>



| <span data-ttu-id="b0a3f-138">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="b0a3f-138">Required members</span></span>                                                   | <span data-ttu-id="b0a3f-139">Type de membre</span><span class="sxs-lookup"><span data-stu-id="b0a3f-139">Member type</span></span> | <span data-ttu-id="b0a3f-140">Notes</span><span class="sxs-lookup"><span data-stu-id="b0a3f-140">Notes</span></span> |
|--------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="b0a3f-141">**RowOrColumnMajor**</span><span class="sxs-lookup"><span data-stu-id="b0a3f-141">**RowOrColumnMajor**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-get_roworcolumnmajor) | <span data-ttu-id="b0a3f-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="b0a3f-142">Property</span></span>    | <span data-ttu-id="b0a3f-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="b0a3f-143">None</span></span>  |
| [<span data-ttu-id="b0a3f-144">**GetColumnHeaders**</span><span class="sxs-lookup"><span data-stu-id="b0a3f-144">**GetColumnHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getcolumnheaders) | <span data-ttu-id="b0a3f-145">Méthode</span><span class="sxs-lookup"><span data-stu-id="b0a3f-145">Method</span></span>      | <span data-ttu-id="b0a3f-146">Aucun</span><span class="sxs-lookup"><span data-stu-id="b0a3f-146">None</span></span>  |
| [<span data-ttu-id="b0a3f-147">**GetRowHeaders**</span><span class="sxs-lookup"><span data-stu-id="b0a3f-147">**GetRowHeaders**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itableprovider-getrowheaders)       | <span data-ttu-id="b0a3f-148">Méthode</span><span class="sxs-lookup"><span data-stu-id="b0a3f-148">Method</span></span>      | <span data-ttu-id="b0a3f-149">Aucun</span><span class="sxs-lookup"><span data-stu-id="b0a3f-149">None</span></span>  |



 

<span data-ttu-id="b0a3f-150">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="b0a3f-150">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b0a3f-151">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b0a3f-151">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b0a3f-152">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="b0a3f-152">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b0a3f-153">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0a3f-153">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="b0a3f-154">Modèle de contrôle TableItem</span><span class="sxs-lookup"><span data-stu-id="b0a3f-154">TableItem Control Pattern</span></span>](uiauto-implementingtableitem.md)
</dt> <dt>

[<span data-ttu-id="b0a3f-155">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="b0a3f-155">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="b0a3f-156">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="b0a3f-156">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




