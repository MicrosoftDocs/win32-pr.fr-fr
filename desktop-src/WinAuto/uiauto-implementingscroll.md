---
title: Scroll (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de IScrollProvider, y compris des informations sur les propriétés et les méthodes. Le modèle de contrôle Scroll est utilisé pour prendre en charge un contrôle qui agit comme un conteneur à défilement pour une collection d’objets enfants.
ms.assetid: baf8012a-52d5-4465-b26d-aa3d7f550b54
keywords:
- UI Automation, implémenter le modèle de contrôle Scroll
- UI Automation, modèle de contrôle Scroll
- UI Automation, IScrollProvider
- IScrollProvider
- implémentation des modèles de contrôle Scroll d’UI Automation
- Modèles de contrôle Scroll
- modèles de contrôle, IScrollProvider
- modèles de contrôle, implémenter le défilement d’UI Automation
- modèles de contrôle, défilement
- interfaces, IScrollProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b525c77a7f89f7adc95a3d90d999f8b243cfcdb6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674314"
---
# <a name="scroll-control-pattern"></a><span data-ttu-id="946b9-114">Scroll (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="946b9-114">Scroll Control Pattern</span></span>

<span data-ttu-id="946b9-115">Fournit des instructions et des conventions pour l’implémentation de [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="946b9-115">Describes guidelines and conventions for implementing [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider), including information about properties and methods.</span></span> <span data-ttu-id="946b9-116">Le modèle de contrôle **Scroll** est utilisé pour prendre en charge un contrôle qui agit comme un conteneur à défilement pour une collection d’objets enfants.</span><span class="sxs-lookup"><span data-stu-id="946b9-116">The **Scroll** control pattern is used to support a control that acts as a scrollable container for a collection of child objects.</span></span>

<span data-ttu-id="946b9-117">Le contrôle n’est pas obligatoire pour utiliser des barres de défilement pour prendre en charge la fonctionnalité de défilement, bien que cela le fasse couramment.</span><span class="sxs-lookup"><span data-stu-id="946b9-117">The control is not required to use scroll bars to support the scrolling functionality, although it commonly does.</span></span> <span data-ttu-id="946b9-118">L’illustration suivante montre un contrôle de défilement qui n’utilise pas de barres de défilement.</span><span class="sxs-lookup"><span data-stu-id="946b9-118">The following image shows a scrolling control that does not use scroll bars.</span></span> <span data-ttu-id="946b9-119">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="946b9-119">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

![capture d’écran montrant un contrôle de défilement sans barres de défilement](images/uia-scrollpattern-without-scrollbars.jpg)

<span data-ttu-id="946b9-121">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="946b9-121">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="946b9-122">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="946b9-122">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="946b9-123">Membres requis pour **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="946b9-123">Required Members for **IScrollProvider**</span></span>](#required-members-for-iscrollprovider)
-   [<span data-ttu-id="946b9-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="946b9-124">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="946b9-125">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="946b9-125">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="946b9-126">Lorsque vous implémentez le modèle de contrôle **Scroll** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="946b9-126">When implementing the **Scroll** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="946b9-127">Les enfants de ce contrôle doivent implémenter [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span><span class="sxs-lookup"><span data-stu-id="946b9-127">The children of this control must implement [**IScrollItemProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollitemprovider).</span></span>
-   <span data-ttu-id="946b9-128">Les barres de défilement d’un contrôle conteneur ne prennent pas en charge le modèle de contrôle **Scroll** .</span><span class="sxs-lookup"><span data-stu-id="946b9-128">The scroll bars of a container control do not support the **Scroll** control pattern.</span></span> <span data-ttu-id="946b9-129">Ils doivent prendre en charge le modèle de contrôle [RangeValue](uiauto-implementingrangevalue.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="946b9-129">They must support the [RangeValue](uiauto-implementingrangevalue.md) control pattern instead.</span></span>
-   <span data-ttu-id="946b9-130">Lorsque le défilement est mesuré sous forme de pourcentage, toutes les valeurs ou quantités liées à la graduation du défilement doivent être normalisées dans une plage de 0 à 100.</span><span class="sxs-lookup"><span data-stu-id="946b9-130">When scrolling is measured in percentages, all values or amounts related to scroll graduation must be normalized to a range of 0 to 100.</span></span>
-   <span data-ttu-id="946b9-131">La propriété [**IScrollProvider :: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) et la propriété [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) sont indépendantes de la propriété **IsEnabled** .</span><span class="sxs-lookup"><span data-stu-id="946b9-131">The [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property and [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property are independent of the **IsEnabled** property.</span></span>
-   <span data-ttu-id="946b9-132">Si la propriété [**IScrollProvider :: HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) a la **valeur false**, la propriété [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) doit avoir la valeur 100 (100%) la propriété [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) doit être définie sur **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="946b9-132">If the [**IScrollProvider::HorizontallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable) property is **FALSE**, the [**HorizontalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize) property should be set to 100 (100%) and [**HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="946b9-133">De même, si la propriété [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) a la **valeur false**, la propriété [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) doit avoir la valeur 100 (100%) la propriété [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) doit être définie sur **UIA \_ ScrollPatternNoScroll** (-1).</span><span class="sxs-lookup"><span data-stu-id="946b9-133">Likewise, if the [**VerticallyScrollable**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable) property is **FALSE**, the [**VerticalViewSize**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize) property should be set to 100 (100%) and [**VerticalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent) property should be set to **UIA\_ScrollPatternNoScroll** (-1).</span></span> <span data-ttu-id="946b9-134">Cela permet à un client Microsoft UI Automation d’utiliser ces valeurs de propriété dans la méthode [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) tout en évitant une condition de concurrence critique si une direction dans laquelle le client n’est pas intéressé par le défilement est activée.</span><span class="sxs-lookup"><span data-stu-id="946b9-134">This allows a Microsoft UI Automation client to use these property values within the [**SetScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent) method while avoiding a race condition if a direction the client is not interested in scrolling becomes activated.</span></span>
-   <span data-ttu-id="946b9-135">La propriété [**IScrollProvider :: HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) est spécifique aux paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="946b9-135">The [**IScrollProvider::HorizontalScrollPercent**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) property is locale-specific.</span></span> <span data-ttu-id="946b9-136">La définition de **HorizontalScrollPercent** sur 100 doit définir l’emplacement de défilement du contrôle sur l’équivalent de sa position la plus à droite pour les langues telles que l’anglais qui sont lues de gauche à droite.</span><span class="sxs-lookup"><span data-stu-id="946b9-136">Setting **HorizontalScrollPercent** to 100 must set the scrolling location of the control to the equivalent of its rightmost position for languages such as English that read left to right.</span></span> <span data-ttu-id="946b9-137">Sinon, pour les langues telles que l’arabe, qui sont lues de droite à gauche, la définition de **HorizontalScrollPercent** sur 100 doit définir l’emplacement de défilement à la position la plus à gauche.</span><span class="sxs-lookup"><span data-stu-id="946b9-137">Alternately, for languages such as Arabic that read right to left, setting **HorizontalScrollPercent** to 100 must set the scroll location to the leftmost position.</span></span>

## <a name="required-members-for-iscrollprovider"></a><span data-ttu-id="946b9-138">Membres requis pour **IScrollProvider**</span><span class="sxs-lookup"><span data-stu-id="946b9-138">Required Members for **IScrollProvider**</span></span>

<span data-ttu-id="946b9-139">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) .</span><span class="sxs-lookup"><span data-stu-id="946b9-139">The following properties and methods are required for implementing the [**IScrollProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-iscrollprovider) interface.</span></span>



| <span data-ttu-id="946b9-140">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="946b9-140">Required members</span></span>                                                                  | <span data-ttu-id="946b9-141">Type de membre</span><span class="sxs-lookup"><span data-stu-id="946b9-141">Member type</span></span> | <span data-ttu-id="946b9-142">Notes</span><span class="sxs-lookup"><span data-stu-id="946b9-142">Notes</span></span> |
|-----------------------------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="946b9-143">**HorizontalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="946b9-143">**HorizontalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalscrollpercent) | <span data-ttu-id="946b9-144">Propriété</span><span class="sxs-lookup"><span data-stu-id="946b9-144">Property</span></span>    | <span data-ttu-id="946b9-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-145">None</span></span>  |
| [<span data-ttu-id="946b9-146">**VerticalScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="946b9-146">**VerticalScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalscrollpercent)     | <span data-ttu-id="946b9-147">Propriété</span><span class="sxs-lookup"><span data-stu-id="946b9-147">Property</span></span>    | <span data-ttu-id="946b9-148">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-148">None</span></span>  |
| [<span data-ttu-id="946b9-149">**HorizontalViewSize**</span><span class="sxs-lookup"><span data-stu-id="946b9-149">**HorizontalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontalviewsize)           | <span data-ttu-id="946b9-150">Propriété</span><span class="sxs-lookup"><span data-stu-id="946b9-150">Property</span></span>    | <span data-ttu-id="946b9-151">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-151">None</span></span>  |
| [<span data-ttu-id="946b9-152">**VerticalViewSize**</span><span class="sxs-lookup"><span data-stu-id="946b9-152">**VerticalViewSize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticalviewsize)               | <span data-ttu-id="946b9-153">Propriété</span><span class="sxs-lookup"><span data-stu-id="946b9-153">Property</span></span>    | <span data-ttu-id="946b9-154">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-154">None</span></span>  |
| [<span data-ttu-id="946b9-155">**HorizontallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="946b9-155">**HorizontallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_horizontallyscrollable)   | <span data-ttu-id="946b9-156">Propriété</span><span class="sxs-lookup"><span data-stu-id="946b9-156">Property</span></span>    | <span data-ttu-id="946b9-157">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-157">None</span></span>  |
| [<span data-ttu-id="946b9-158">**VerticallyScrollable**</span><span class="sxs-lookup"><span data-stu-id="946b9-158">**VerticallyScrollable**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-get_verticallyscrollable)       | <span data-ttu-id="946b9-159">Propriété</span><span class="sxs-lookup"><span data-stu-id="946b9-159">Property</span></span>    | <span data-ttu-id="946b9-160">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-160">None</span></span>  |
| [<span data-ttu-id="946b9-161">**Scroll**</span><span class="sxs-lookup"><span data-stu-id="946b9-161">**Scroll**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-scroll)                                   | <span data-ttu-id="946b9-162">Méthode</span><span class="sxs-lookup"><span data-stu-id="946b9-162">Method</span></span>      | <span data-ttu-id="946b9-163">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-163">None</span></span>  |
| [<span data-ttu-id="946b9-164">**SetScrollPercent**</span><span class="sxs-lookup"><span data-stu-id="946b9-164">**SetScrollPercent**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iscrollprovider-setscrollpercent)               | <span data-ttu-id="946b9-165">Méthode</span><span class="sxs-lookup"><span data-stu-id="946b9-165">Method</span></span>      | <span data-ttu-id="946b9-166">Aucun</span><span class="sxs-lookup"><span data-stu-id="946b9-166">None</span></span>  |



 

<span data-ttu-id="946b9-167">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="946b9-167">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="946b9-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="946b9-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="946b9-169">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="946b9-169">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="946b9-170">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="946b9-170">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="946b9-171">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="946b9-171">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 




