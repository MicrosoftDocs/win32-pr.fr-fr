---
title: Transform (modèle de contrôle)
description: Fournit des instructions et des conventions pour l’implémentation de ITransformProvider et ITransformProvider2, y compris des informations sur les propriétés et les méthodes.
ms.assetid: e1d862a0-8085-42b4-9710-cf11e1a467cf
keywords:
- UI Automation, implémenter le modèle de contrôle Transform
- UI Automation, transformation (modèle de contrôle)
- UI Automation, ITransformProvider
- ITransformProvider
- implémentation des modèles de contrôle Transform d’UI Automation
- Transformer les modèles de contrôle
- modèles de contrôle, ITransformProvider
- modèles de contrôle, implémenter une transformation UI Automation
- modèles de contrôle, transformer
- interfaces, ITransformProvider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1eae752b34ed0b64fd2c0a7b476377fd1142f9b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508029"
---
# <a name="transform-control-pattern"></a><span data-ttu-id="b7d78-113">Transform (modèle de contrôle)</span><span class="sxs-lookup"><span data-stu-id="b7d78-113">Transform Control Pattern</span></span>

<span data-ttu-id="b7d78-114">Fournit des instructions et des conventions pour l’implémentation de [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) et [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), y compris des informations sur les propriétés et les méthodes.</span><span class="sxs-lookup"><span data-stu-id="b7d78-114">Describes guidelines and conventions for implementing [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) and [**ITransformProvider2**](/windows/desktop/api/uiautomationcore/nn-uiautomationcore-itransformprovider2), including information about properties and methods.</span></span> <span data-ttu-id="b7d78-115">Le modèle de contrôle Transform est utilisé pour prendre en charge les contrôles qui peuvent être déplacés, redimensionnés ou pivotés dans un espace à deux dimensions.</span><span class="sxs-lookup"><span data-stu-id="b7d78-115">The Transform control pattern is used to support controls that can be moved, resized, or rotated within a two-dimensional space.</span></span>

<span data-ttu-id="b7d78-116">Pour obtenir des exemples de contrôles qui implémentent ce modèle de contrôle, consultez [types de contrôle et leurs modèles de contrôle pris en charge](uiauto-controlpatternmapping.md).</span><span class="sxs-lookup"><span data-stu-id="b7d78-116">For examples of controls that implement this control pattern, see [Control Types and Their Supported Control Patterns](uiauto-controlpatternmapping.md).</span></span>

<span data-ttu-id="b7d78-117">Cette rubrique contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="b7d78-117">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="b7d78-118">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b7d78-118">Implementation Guidelines and Conventions</span></span>](#implementation-guidelines-and-conventions)
-   [<span data-ttu-id="b7d78-119">Membres requis pour **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="b7d78-119">Required Members for **ITransformProvider**</span></span>](#required-members-for-itransformprovider)
-   [<span data-ttu-id="b7d78-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7d78-120">Related topics</span></span>](#related-topics)

## <a name="implementation-guidelines-and-conventions"></a><span data-ttu-id="b7d78-121">Conventions et directives d'implémentation</span><span class="sxs-lookup"><span data-stu-id="b7d78-121">Implementation Guidelines and Conventions</span></span>

<span data-ttu-id="b7d78-122">Lorsque vous implémentez le modèle de contrôle **Transform** , notez les conventions et recommandations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b7d78-122">When implementing the **Transform** control pattern, note the following guidelines and conventions:</span></span>

-   <span data-ttu-id="b7d78-123">La prise en charge pour ce modèle de contrôle ne se limite pas aux objets sur le bureau.</span><span class="sxs-lookup"><span data-stu-id="b7d78-123">Support for this control pattern is not limited to objects on the desktop.</span></span> <span data-ttu-id="b7d78-124">Ce modèle de contrôle doit également être pris en charge par les enfants d’un objet conteneur si les enfants peuvent être déplacés, redimensionnés et pivotés librement dans les limites du conteneur.</span><span class="sxs-lookup"><span data-stu-id="b7d78-124">This control pattern must also be supported by the children of a container object if the children can be moved, resized, or rotated freely within the boundaries of the container.</span></span>
-   <span data-ttu-id="b7d78-125">Il n’est pas possible de déplacer, redimensionner ni pivoter un objet de manière à ce que son emplacement résultant à l’écran soit complètement en dehors des coordonnées de son conteneur et, par conséquent, inaccessible via le clavier et la souris (par exemple, quand une fenêtre de niveau supérieur est déplacée hors de l’écran ou qu’un objet enfant est déplacé en dehors des limites de la fenêtre d’affichage du conteneur).</span><span class="sxs-lookup"><span data-stu-id="b7d78-125">An object cannot be moved, resized, or rotated such that its resulting screen location would be completely outside the coordinates of its container and therefore inaccessible to the keyboard or mouse (for example, when a top-level window is moved off-screen or a child object is moved outside the boundaries of the container's viewport).</span></span> <span data-ttu-id="b7d78-126">Dans ce cas, l’objet est placé le plus près possible des coordonnées d’écran demandées avec les coordonnées en haut et à gauche substituées de façon à être incluses dans les limites du conteneur.</span><span class="sxs-lookup"><span data-stu-id="b7d78-126">In these cases, the object is placed as close to the requested screen coordinates as possible with the top or left coordinates overridden to be within the container boundaries.</span></span>
-   <span data-ttu-id="b7d78-127">Pour les systèmes à plusieurs écrans, si un objet est déplacé, redimensionné ou pivoté complètement en dehors des coordonnées d’écran du bureau combiné, l’objet est placé sur le moniteur principal, aussi près que possible des coordonnées demandées.</span><span class="sxs-lookup"><span data-stu-id="b7d78-127">For multi-monitor systems, if an object is moved, resized, or rotated completely outside the combined desktop screen coordinates, the object is placed on the primary monitor as close to the requested coordinates as possible.</span></span>
-   <span data-ttu-id="b7d78-128">Tous les paramètres et valeurs de propriété sont absolus et indépendants des paramètres régionaux.</span><span class="sxs-lookup"><span data-stu-id="b7d78-128">All parameters and property values are absolute and independent of locale.</span></span>

## <a name="required-members-for-itransformprovider"></a><span data-ttu-id="b7d78-129">Membres requis pour **ITransformProvider**</span><span class="sxs-lookup"><span data-stu-id="b7d78-129">Required Members for **ITransformProvider**</span></span>

<span data-ttu-id="b7d78-130">Les propriétés et méthodes suivantes sont requises pour implémenter l’interface [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="b7d78-130">The following properties and methods are required for implementing the [**ITransformProvider**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="b7d78-131">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="b7d78-131">Required members</span></span>                                         | <span data-ttu-id="b7d78-132">Type de membre</span><span class="sxs-lookup"><span data-stu-id="b7d78-132">Member type</span></span> | <span data-ttu-id="b7d78-133">Notes</span><span class="sxs-lookup"><span data-stu-id="b7d78-133">Notes</span></span> |
|----------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="b7d78-134">**CanMove**</span><span class="sxs-lookup"><span data-stu-id="b7d78-134">**CanMove**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canmove)     | <span data-ttu-id="b7d78-135">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7d78-135">Property</span></span>    | <span data-ttu-id="b7d78-136">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-136">None</span></span>  |
| [<span data-ttu-id="b7d78-137">**CanResize**</span><span class="sxs-lookup"><span data-stu-id="b7d78-137">**CanResize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canresize) | <span data-ttu-id="b7d78-138">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7d78-138">Property</span></span>    | <span data-ttu-id="b7d78-139">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-139">None</span></span>  |
| [<span data-ttu-id="b7d78-140">**CanRotate**</span><span class="sxs-lookup"><span data-stu-id="b7d78-140">**CanRotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-get_canrotate) | <span data-ttu-id="b7d78-141">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7d78-141">Property</span></span>    | <span data-ttu-id="b7d78-142">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-142">None</span></span>  |
| [<span data-ttu-id="b7d78-143">**Activer**</span><span class="sxs-lookup"><span data-stu-id="b7d78-143">**Move**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-move)           | <span data-ttu-id="b7d78-144">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7d78-144">Method</span></span>      | <span data-ttu-id="b7d78-145">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-145">None</span></span>  |
| [<span data-ttu-id="b7d78-146">**Redimensionner**</span><span class="sxs-lookup"><span data-stu-id="b7d78-146">**Resize**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-resize)       | <span data-ttu-id="b7d78-147">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7d78-147">Method</span></span>      | <span data-ttu-id="b7d78-148">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-148">None</span></span>  |
| [<span data-ttu-id="b7d78-149">**Faire pivoter**</span><span class="sxs-lookup"><span data-stu-id="b7d78-149">**Rotate**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider-rotate)       | <span data-ttu-id="b7d78-150">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7d78-150">Method</span></span>      | <span data-ttu-id="b7d78-151">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-151">None</span></span>  |



 

<span data-ttu-id="b7d78-152">Les propriétés et méthodes supplémentaires suivantes sont requises pour implémenter l’interface [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) .</span><span class="sxs-lookup"><span data-stu-id="b7d78-152">The following additional properties and methods are required for implementing the [**ITransformProvider2**](/windows/desktop/api/UIAutomationCore/nn-uiautomationcore-itransformprovider) interface.</span></span>



| <span data-ttu-id="b7d78-153">Membres nécessaires</span><span class="sxs-lookup"><span data-stu-id="b7d78-153">Required members</span></span>                                              | <span data-ttu-id="b7d78-154">Type de membre</span><span class="sxs-lookup"><span data-stu-id="b7d78-154">Member type</span></span> | <span data-ttu-id="b7d78-155">Notes</span><span class="sxs-lookup"><span data-stu-id="b7d78-155">Notes</span></span> |
|---------------------------------------------------------------|-------------|-------|
| [<span data-ttu-id="b7d78-156">**CanZoom**</span><span class="sxs-lookup"><span data-stu-id="b7d78-156">**CanZoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-get_canzoom)     | <span data-ttu-id="b7d78-157">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7d78-157">Property</span></span>    | <span data-ttu-id="b7d78-158">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-158">None</span></span>  |
| [<span data-ttu-id="b7d78-159">**Zoom**</span><span class="sxs-lookup"><span data-stu-id="b7d78-159">**Zoom**</span></span>](/windows/desktop/api/uiautomationcore/nf-uiautomationcore-itransformprovider2-zoom)           | <span data-ttu-id="b7d78-160">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7d78-160">Method</span></span>      | <span data-ttu-id="b7d78-161">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-161">None</span></span>  |
| [<span data-ttu-id="b7d78-162">**ZoomByUnit**</span><span class="sxs-lookup"><span data-stu-id="b7d78-162">**ZoomByUnit**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-zoombyunit)   | <span data-ttu-id="b7d78-163">Méthode</span><span class="sxs-lookup"><span data-stu-id="b7d78-163">Method</span></span>      | <span data-ttu-id="b7d78-164">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-164">None</span></span>  |
| [<span data-ttu-id="b7d78-165">**ZoomLevel**</span><span class="sxs-lookup"><span data-stu-id="b7d78-165">**ZoomLevel**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomlevel)     | <span data-ttu-id="b7d78-166">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7d78-166">Property</span></span>    | <span data-ttu-id="b7d78-167">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-167">None</span></span>  |
| [<span data-ttu-id="b7d78-168">**ZoomMaximum**</span><span class="sxs-lookup"><span data-stu-id="b7d78-168">**ZoomMaximum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoommaximum) | <span data-ttu-id="b7d78-169">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7d78-169">Property</span></span>    | <span data-ttu-id="b7d78-170">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-170">None</span></span>  |
| [<span data-ttu-id="b7d78-171">**ZoomMinimum**</span><span class="sxs-lookup"><span data-stu-id="b7d78-171">**ZoomMinimum**</span></span>](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itransformprovider2-get_zoomminimum) | <span data-ttu-id="b7d78-172">Propriété</span><span class="sxs-lookup"><span data-stu-id="b7d78-172">Property</span></span>    | <span data-ttu-id="b7d78-173">Aucun</span><span class="sxs-lookup"><span data-stu-id="b7d78-173">None</span></span>  |



 

<span data-ttu-id="b7d78-174">Ce modèle de contrôle n’est associé aucun événement.</span><span class="sxs-lookup"><span data-stu-id="b7d78-174">This control pattern has no associated events.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7d78-175">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b7d78-175">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7d78-176">Types de contrôle et leurs modèles de contrôle pris en charge</span><span class="sxs-lookup"><span data-stu-id="b7d78-176">Control Types and Their Supported Control Patterns</span></span>](uiauto-controlpatternmapping.md)
</dt> <dt>

[<span data-ttu-id="b7d78-177">Vue d'ensemble des modèles de contrôle UI Automation</span><span class="sxs-lookup"><span data-stu-id="b7d78-177">UI Automation Control Patterns Overview</span></span>](uiauto-controlpatternsoverview.md)
</dt> <dt>

[<span data-ttu-id="b7d78-178">Vue d’ensemble de l’arborescence UI Automation</span><span class="sxs-lookup"><span data-stu-id="b7d78-178">UI Automation Tree Overview</span></span>](uiauto-treeoverview.md)
</dt> </dl>

 

 