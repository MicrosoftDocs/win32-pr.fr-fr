---
title: Spreadsheet (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ISpreadsheetProvider, y compris des informations sur les méthodes.
ms.assetid: 4004D867-8367-486A-96ED-DE5B41D24935
keywords:
- UI Automation, implémenter le modèle de contrôle Spreadsheet
- UI Automation, modèle de contrôle Spreadsheet
- UI Automation, ISpreadsheetProvider
- ISpreadsheetProvider
- implémentation du modèle de contrôle Spreadsheet d’UI Automation
- Spreadsheet (modèle de contrôle)
- modèles de contrôle, ISpreadsheetProvider
- modèles de contrôle, implémenter une feuille de calcul UI Automation
- modèles de contrôle, feuille de calcul
- interfaces, ISpreadsheetProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be34174745ccf91435db92665b98eb387f7241a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315774"
---
# <a name="spreadsheet-control-pattern"></a><span data-ttu-id="0a63b-113">Spreadsheet (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="0a63b-113">Spreadsheet Control Pattern</span></span>

<span data-ttu-id="0a63b-114">Fournit des instructions et des conventions pour l’implémentation de [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), y compris des informations sur les méthodes.</span><span class="sxs-lookup"><span data-stu-id="0a63b-114">Describes guidelines and conventions for implementing [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider), including information about methods.</span></span> <span data-ttu-id="0a63b-115">Des liens vers des références supplémentaires sont répertoriés à la fin de la rubrique.</span><span class="sxs-lookup"><span data-stu-id="0a63b-115">Links to additional references are listed at the end of the topic.</span></span> <span data-ttu-id="0a63b-116">Le modèle de contrôle **Spreadsheet** est utilisé pour exposer le contenu d’une feuille de calcul ou d’un autre document basé sur la grille.</span><span class="sxs-lookup"><span data-stu-id="0a63b-116">The **Spreadsheet** control pattern is used to expose the contents of a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="0a63b-117">Le modèle de contrôle **Spreadsheet** est étroitement lié au modèle de contrôle [Grid](uiauto-implementinggrid.md) ; les contrôles qui implémentent le modèle de contrôle **Spreadsheet** doivent également implémenter le modèle de contrôle Grid.</span><span class="sxs-lookup"><span data-stu-id="0a63b-117">The **Spreadsheet** control pattern is closely related to the [Grid](uiauto-implementinggrid.md) control pattern; controls that implement the **Spreadsheet** control pattern should also implement the Grid control pattern.</span></span> <span data-ttu-id="0a63b-118">Les contrôles peuvent également implémenter le modèle de contrôle [table](uiauto-implementingtable.md) , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="0a63b-118">Controls can also implement the [Table](uiauto-implementingtable.md) control pattern, if appropriate.</span></span> <span data-ttu-id="0a63b-119">Pour obtenir des exemples de contrôles qui implémentent ces modèles de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="0a63b-119">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="0a63b-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="0a63b-120">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="0a63b-121">Lorsque vous implémentez le modèle de contrôle **Spreadsheet** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0a63b-121">When implementing the **Spreadsheet** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="0a63b-122">Si une feuille de calcul implémente l’interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) , ses cellules doivent implémenter l’interface [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="0a63b-122">If a spreadsheet implements the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface, its cells must implement the [**ISpreadsheetItemProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>
-   <span data-ttu-id="0a63b-123">La méthode [**ISpreadsheetProvider :: GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) est destinée à fournir le même type de navigation qu’une application peut fournir avec une fonctionnalité de **saut à étiquette** .</span><span class="sxs-lookup"><span data-stu-id="0a63b-123">The [**ISpreadsheetProvider::GetItemByName**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) method is intended to provide the same kind of navigation that an application might supply with a **Jump to Label** feature.</span></span> <span data-ttu-id="0a63b-124">De nombreux feuilles de calcul permettent à des cellules spécifiques de recevoir un nom convivial ou une étiquette.</span><span class="sxs-lookup"><span data-stu-id="0a63b-124">Many spreadsheet programs let specific cells be given a friendly name or label.</span></span> <span data-ttu-id="0a63b-125">**GetItemByName** permet au client de rechercher une cellule en fonction de son nom convivial.</span><span class="sxs-lookup"><span data-stu-id="0a63b-125">**GetItemByName** enables the client to look up a cell based on its friendly name.</span></span> <span data-ttu-id="0a63b-126">Cette méthode ne doit pas récupérer de cellules qui contiennent le texte de nom, car les résultats peuvent être très ambigus.</span><span class="sxs-lookup"><span data-stu-id="0a63b-126">This method should not retrieve any cells that contain the name text because the results can be highly ambiguous.</span></span> <span data-ttu-id="0a63b-127">Si le programme de feuille de calcul permet à plusieurs cellules d’une même feuille de calcul d’avoir le même nom convivial ou étiquette, le comportement d’automatisation de l’interface utilisateur de Microsoft n’est pas défini.</span><span class="sxs-lookup"><span data-stu-id="0a63b-127">If the spreadsheet program allows multiple cells in the same a spreadsheet to have the same friendly name or label, the Microsoft UI Automation behavior is undefined.</span></span>

## <a name="required-members-for-ispreadsheetprovider"></a><span data-ttu-id="0a63b-128">Membres requis pour **ISpreadsheetProvider**</span><span class="sxs-lookup"><span data-stu-id="0a63b-128">Required Members for **ISpreadsheetProvider**</span></span>

<span data-ttu-id="0a63b-129">La méthode suivante est requise pour l’implémentation de l’interface [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) .</span><span class="sxs-lookup"><span data-stu-id="0a63b-129">The following method is required for implementing the [**ISpreadsheetProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-ispreadsheetprovider) interface.</span></span>



| <span data-ttu-id="0a63b-130">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="0a63b-130">Required members</span></span>                                                       | <span data-ttu-id="0a63b-131">Type de membre</span><span class="sxs-lookup"><span data-stu-id="0a63b-131">Member type</span></span> | <span data-ttu-id="0a63b-132">Notes</span><span class="sxs-lookup"><span data-stu-id="0a63b-132">Notes</span></span> |
|------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="0a63b-133">**GetItemByName**</span><span class="sxs-lookup"><span data-stu-id="0a63b-133">**GetItemByName**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetprovider-getitembyname) | <span data-ttu-id="0a63b-134">Méthode</span><span class="sxs-lookup"><span data-stu-id="0a63b-134">Method</span></span>      | <span data-ttu-id="0a63b-135">Aucun</span><span class="sxs-lookup"><span data-stu-id="0a63b-135">None</span></span>  |



 

<span data-ttu-id="0a63b-136">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="0a63b-136">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0a63b-137">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0a63b-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0a63b-138">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a63b-138">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="0a63b-139">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="0a63b-139">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="0a63b-140">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="0a63b-140">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 