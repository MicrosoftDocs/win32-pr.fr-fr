---
title: Modèle de contrôle RangeValue
description: Fournit des instructions et des conventions pour l’implémentation de IRangeValueProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle RangeValue est utilisé pour prendre en charge les contrôles qui peuvent être définis sur une valeur comprise dans une plage.
ms.assetid: e5c1104c-4b20-4fdd-bd12-dfc27cb73ac5
keywords:
- UI Automation, implémentation du modèle de contrôle RangeValue
- UI Automation, modèle de contrôle RangeValue
- UI Automation, IRangeValueProvider
- IRangeValueProvider
- implémentation des modèles de contrôle RangeValue d’UI Automation
- Modèles de contrôle RangeValue
- modèles de contrôle, IRangeValueProvider
- modèles de contrôle, implémenter des RangeValue UI Automation
- modèles de contrôle, RangeValue
- interfaces, IRangeValueProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf426069ad88ad272fd78c521a220ba7ccf72275
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106531595"
---
# <a name="rangevalue-control-pattern"></a><span data-ttu-id="0d385-114">Modèle de contrôle RangeValue</span><span class="sxs-lookup"><span data-stu-id="0d385-114">RangeValue Control Pattern</span></span>

<span data-ttu-id="0d385-115">Fournit des instructions et des conventions pour l’implémentation de [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="0d385-115">Describes guidelines and conventions for implementing [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider), including information about properties and methods.</span></span> <span data-ttu-id="0d385-116">Le modèle de contrôle **RangeValue** est utilisé pour prendre en charge les contrôles qui peuvent être définis sur une valeur comprise dans une plage.</span><span class="sxs-lookup"><span data-stu-id="0d385-116">The **RangeValue** control pattern is used to support controls that can be set to a value within a range.</span></span>

<span data-ttu-id="0d385-117">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="0d385-117">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="0d385-118">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="0d385-118">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="0d385-119">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="0d385-119">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="0d385-120">Membres requis pour **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="0d385-120">Required Members for **IRangeValueProvider**</span></span>](#required-members-for-irangevalueprovider)
-   [<span data-ttu-id="0d385-121">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d385-121">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="0d385-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="0d385-122">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="0d385-123">Lorsque vous implémentez le modèle de contrôle **RangeValue** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="0d385-123">When implementing the **RangeValue** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="0d385-124">Les contrôles autorisent le réétalonnage de leurs propriétés prises en charge en fonction des paramètres régionaux ou des préférences de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="0d385-124">Controls allow recalibration of their supported properties based upon locale or user preference.</span></span> <span data-ttu-id="0d385-125">Par exemple, vous pouvez définir un contrôle de thermomètre pour afficher la température en degrés Fahrenheit ou Celsius.</span><span class="sxs-lookup"><span data-stu-id="0d385-125">An example of this is a thermometer control that can be set to display the temperature in Fahrenheit or Celsius.</span></span>
-   <span data-ttu-id="0d385-126">Les contrôles qui ont des valeurs de plage ambiguës, telles que les barres de progression ou les curseurs, doivent normaliser ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="0d385-126">Controls that have ambiguous range values, such as progress bars or sliders, should have those values normalized.</span></span>

## <a name="required-members-for-irangevalueprovider"></a><span data-ttu-id="0d385-127">Membres requis pour **IRangeValueProvider**</span><span class="sxs-lookup"><span data-stu-id="0d385-127">Required Members for **IRangeValueProvider**</span></span>

<span data-ttu-id="0d385-128">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) .</span><span class="sxs-lookup"><span data-stu-id="0d385-128">The following properties and methods are required for implementing the [**IRangeValueProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-irangevalueprovider) interface.</span></span>



| <span data-ttu-id="0d385-129">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="0d385-129">Required members</span></span>                                              | <span data-ttu-id="0d385-130">Type de membre</span><span class="sxs-lookup"><span data-stu-id="0d385-130">Member type</span></span> | <span data-ttu-id="0d385-131">Notes</span><span class="sxs-lookup"><span data-stu-id="0d385-131">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="0d385-132">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="0d385-132">**IsReadOnly**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_isreadonly)   | <span data-ttu-id="0d385-133">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d385-133">Property</span></span>    | <span data-ttu-id="0d385-134">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d385-134">None</span></span>  |
| [<span data-ttu-id="0d385-135">**Valeur**</span><span class="sxs-lookup"><span data-stu-id="0d385-135">**Value**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_value)             | <span data-ttu-id="0d385-136">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d385-136">Property</span></span>    | <span data-ttu-id="0d385-137">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d385-137">None</span></span>  |
| [<span data-ttu-id="0d385-138">**LargeChange**</span><span class="sxs-lookup"><span data-stu-id="0d385-138">**LargeChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_largechange) | <span data-ttu-id="0d385-139">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d385-139">Property</span></span>    | <span data-ttu-id="0d385-140">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d385-140">None</span></span>  |
| [<span data-ttu-id="0d385-141">**SmallChange**</span><span class="sxs-lookup"><span data-stu-id="0d385-141">**SmallChange**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_smallchange) | <span data-ttu-id="0d385-142">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d385-142">Property</span></span>    | <span data-ttu-id="0d385-143">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d385-143">None</span></span>  |
| [<span data-ttu-id="0d385-144">**Maximale**</span><span class="sxs-lookup"><span data-stu-id="0d385-144">**Maximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_maximum)         | <span data-ttu-id="0d385-145">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d385-145">Property</span></span>    | <span data-ttu-id="0d385-146">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d385-146">None</span></span>  |
| [<span data-ttu-id="0d385-147">**Minimum**</span><span class="sxs-lookup"><span data-stu-id="0d385-147">**Minimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-get_minimum)         | <span data-ttu-id="0d385-148">Propriété</span><span class="sxs-lookup"><span data-stu-id="0d385-148">Property</span></span>    | <span data-ttu-id="0d385-149">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d385-149">None</span></span>  |
| [<span data-ttu-id="0d385-150">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="0d385-150">**SetValue**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-irangevalueprovider-setvalue)       | <span data-ttu-id="0d385-151">Méthode</span><span class="sxs-lookup"><span data-stu-id="0d385-151">Method</span></span>      | <span data-ttu-id="0d385-152">Aucun</span><span class="sxs-lookup"><span data-stu-id="0d385-152">None</span></span>  |



 

<span data-ttu-id="0d385-153">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="0d385-153">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0d385-154">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="0d385-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0d385-155">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="0d385-155">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="0d385-156">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="0d385-156">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="0d385-157">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="0d385-157">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




