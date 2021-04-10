---
title: Modèle de contrôle SpreadsheetItem
description: Fournit des instructions et des conventions pour l’implémentation de ISpreadsheetItemProvider, y compris des informations sur les propriétés et les méthodes.
ms.assetid: AADD06C5-CF51-4A1A-9ACB-3E896050D7DD
keywords:
- UI Automation, implémentation du modèle de contrôle SpreadsheetItem
- UI Automation, modèle de contrôle SpreadsheetItem
- UI Automation, ISpreadsheetItemProvider
- ISpreadsheetItemProvider
- implémentation du modèle de contrôle SpreadsheetItem d’UI Automation
- Modèle de contrôle SpreadsheetItem
- modèles de contrôle, ISpreadsheetItemProvider
- modèles de contrôle, implémenter des SpreadsheetItem UI Automation
- modèles de contrôle, SpreadsheetItem
- interfaces, ISpreadsheetItemProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88ba050c5a5c8b10c68695fdf1a05d845353e638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031728"
---
# <a name="spreadsheetitem-control-pattern"></a><span data-ttu-id="3c68f-113">Modèle de contrôle SpreadsheetItem</span><span class="sxs-lookup"><span data-stu-id="3c68f-113">SpreadsheetItem Control Pattern</span></span>

<span data-ttu-id="3c68f-114">Fournit des instructions et des conventions pour l’implémentation de [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="3c68f-114">Describes guidelines and conventions for implementing [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider), including information about properties and methods.</span></span> <span data-ttu-id="3c68f-115">Le modèle de contrôle **SpreadsheetItem** est utilisé pour exposer les propriétés d’une cellule dans une feuille de calcul ou un autre document basé sur la grille.</span><span class="sxs-lookup"><span data-stu-id="3c68f-115">The **SpreadsheetItem** control pattern is used to expose the properties of a cell in a spreadsheet or other grid-based document.</span></span>

<span data-ttu-id="3c68f-116">Le modèle de contrôle **SpreadsheetItem** est étroitement lié au modèle de contrôle [GridItem](uiauto-implementinggriditem.md) . les contrôles qui implémentent le modèle de contrôle **SpreadsheetItem** doivent également implémenter le modèle de contrôle GridItem.</span><span class="sxs-lookup"><span data-stu-id="3c68f-116">The **SpreadsheetItem** control pattern is closely related to the [GridItem](uiauto-implementinggriditem.md) control pattern; controls that implement the **SpreadsheetItem** control pattern should also implement the GridItem control pattern.</span></span> <span data-ttu-id="3c68f-117">Les contrôles peuvent également implémenter le modèle de contrôle [TableItem](uiauto-implementingtableitem.md) , le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="3c68f-117">Controls can also implement the [TableItem](uiauto-implementingtableitem.md) control pattern, if appropriate.</span></span> <span data-ttu-id="3c68f-118">Pour obtenir des exemples de contrôles qui implémentent ces modèles de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="3c68f-118">For examples of controls that implement these control patterns, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="3c68f-119">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="3c68f-119">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3c68f-120">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="3c68f-120">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="3c68f-121">Membres requis pour **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="3c68f-121">Required Members for **ISpreadsheetItemProvider**</span></span>](#required-members-for-ispreadsheetitemprovider)
-   [<span data-ttu-id="3c68f-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c68f-122">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="3c68f-123">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="3c68f-123">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="3c68f-124">Lorsque vous implémentez le modèle de contrôle **SpreadsheetItem** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="3c68f-124">When implementing the **SpreadsheetItem** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="3c68f-125">Lorsque vous implémentez les méthodes [**ISpreadsheetItemProvider :: GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) et [**ISpreadsheetItemProvider :: GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) , reportez-vous à la documentation [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="3c68f-125">When implementing the [**ISpreadsheetItemProvider::GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) and [**ISpreadsheetItemProvider::GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) methods, please refer to the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) documentation.</span></span> <span data-ttu-id="3c68f-126">Ces méthodes retournent des tableaux pour permettre aux fournisseurs de prendre en charge plusieurs annotations sur une seule cellule.</span><span class="sxs-lookup"><span data-stu-id="3c68f-126">These methods both return arrays to enable providers to support multiple annotations on a single cell.</span></span>
-   <span data-ttu-id="3c68f-127">Certains types d’annotations ne nécessitent pas une implémentation complète de l’interface [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) .</span><span class="sxs-lookup"><span data-stu-id="3c68f-127">Some kinds of annotations do not require a full implementation of the [**IAnnotationProvider**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iannotationprovider) interface.</span></span> <span data-ttu-id="3c68f-128">Par exemple, un indicateur d’erreur d’orthographe simple peut être représenté en indiquant que [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) retourne un identificateur d’attribut de texte de [**AnnotationType \_ SpellingError**](uiauto-annotation-type-identifiers.md)et que [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) retourne une valeur null.</span><span class="sxs-lookup"><span data-stu-id="3c68f-128">For example, a simple spelling-error indicator could be represented by having [**GetAnnotationTypes**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes) return a text attribute identifier of [**AnnotationType\_SpellingError**](uiauto-annotation-type-identifiers.md), and having [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) return a null value.</span></span>

## <a name="required-members-for-ispreadsheetitemprovider"></a><span data-ttu-id="3c68f-129">Membres requis pour **ISpreadsheetItemProvider**</span><span class="sxs-lookup"><span data-stu-id="3c68f-129">Required Members for **ISpreadsheetItemProvider**</span></span>

<span data-ttu-id="3c68f-130">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) .</span><span class="sxs-lookup"><span data-stu-id="3c68f-130">The following properties and methods are required for implementing the [**ISpreadsheetItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-ispreadsheetitemprovider) interface.</span></span>



| <span data-ttu-id="3c68f-131">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="3c68f-131">Required members</span></span>                                                                         | <span data-ttu-id="3c68f-132">Type de membre</span><span class="sxs-lookup"><span data-stu-id="3c68f-132">Member type</span></span> | <span data-ttu-id="3c68f-133">Notes</span><span class="sxs-lookup"><span data-stu-id="3c68f-133">Notes</span></span>                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3c68f-134">**Formule**</span><span class="sxs-lookup"><span data-stu-id="3c68f-134">**Formula**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula)                           | <span data-ttu-id="3c68f-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="3c68f-135">Property</span></span>    | <span data-ttu-id="3c68f-136">L’implémentation d’une propriété de [**formule**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) distincte est nécessaire, car la propriété de [valeur](value-property.md) d’une cellule retourne généralement la valeur calculée de la cellule.</span><span class="sxs-lookup"><span data-stu-id="3c68f-136">Implementing a separate [**Formula**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-get_formula) property is necessary because a cell’s [Value](value-property.md) property typically returns the computed value of the cell.</span></span> <span data-ttu-id="3c68f-137">La propriété **Formula** doit avoir la **valeur null** si aucune formule n’est définie.</span><span class="sxs-lookup"><span data-stu-id="3c68f-137">The **Formula** property should be **NULL** if no formula is set.</span></span> |
| [<span data-ttu-id="3c68f-138">**GetAnnotationObjects**</span><span class="sxs-lookup"><span data-stu-id="3c68f-138">**GetAnnotationObjects**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects) | <span data-ttu-id="3c68f-139">Méthode</span><span class="sxs-lookup"><span data-stu-id="3c68f-139">Method</span></span>      | <span data-ttu-id="3c68f-140">Retourne un tableau de fournisseurs d’éléments qui font référence aux annotations liées à cette cellule.</span><span class="sxs-lookup"><span data-stu-id="3c68f-140">Returns an array of element providers that refer to the annotations linked to this cell.</span></span> <span data-ttu-id="3c68f-141">Les pointeurs dans le tableau peuvent avoir la valeur null si une annotation n’a pas de fournisseur lié.</span><span class="sxs-lookup"><span data-stu-id="3c68f-141">Pointers within the array can be null if an annotation does not have a linked provider.</span></span>                                                                                                       |
| [<span data-ttu-id="3c68f-142">**GetAnnotationTypes**</span><span class="sxs-lookup"><span data-stu-id="3c68f-142">**GetAnnotationTypes**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationtypes)     | <span data-ttu-id="3c68f-143">Méthode</span><span class="sxs-lookup"><span data-stu-id="3c68f-143">Method</span></span>      | <span data-ttu-id="3c68f-144">Retourne un tableau d’identificateurs de type d’annotation qui décrivent les annotations sur cette cellule.</span><span class="sxs-lookup"><span data-stu-id="3c68f-144">Returns an array of annotation type identifiers that describe the annotations on this cell.</span></span> <span data-ttu-id="3c68f-145">Le tableau doit avoir la même taille que le tableau retourné par [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span><span class="sxs-lookup"><span data-stu-id="3c68f-145">The array must be the same size as the array returned by [**GetAnnotationObjects**](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ispreadsheetitemprovider-getannotationobjects).</span></span>                                         |



 

<span data-ttu-id="3c68f-146">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="3c68f-146">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c68f-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3c68f-147">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="3c68f-148">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="3c68f-148">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3c68f-149">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="3c68f-149">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="3c68f-150">Spreadsheet (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="3c68f-150">Spreadsheet Control Pattern</span></span>](uiauto-implementingspreadsheet.md)
</dt> <dt>

[<span data-ttu-id="3c68f-151">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="3c68f-151">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="3c68f-152">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="3c68f-152">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 