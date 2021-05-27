---
title: Vue d’ensemble des couches
description: Décrit les principes de base des couches Direct2D.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, couches
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ac68ba25d1e8f35c5a41daec4d7a5295235a5d98
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549184"
---
# <a name="layers-overview"></a><span data-ttu-id="eda34-104">Vue d’ensemble des couches</span><span class="sxs-lookup"><span data-stu-id="eda34-104">Layers Overview</span></span>

<span data-ttu-id="eda34-105">Cette vue d’ensemble décrit les principes fondamentaux de l’utilisation des couches Direct2D.</span><span class="sxs-lookup"><span data-stu-id="eda34-105">This overview describes the basics of using Direct2D layers.</span></span> <span data-ttu-id="eda34-106">Elle contient les sections suivantes.</span><span class="sxs-lookup"><span data-stu-id="eda34-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="eda34-107">Que sont les couches ?</span><span class="sxs-lookup"><span data-stu-id="eda34-107">What Are Layers?</span></span>](#what-are-layers)
-   [<span data-ttu-id="eda34-108">Couches dans Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="eda34-108">Layers in Windows 8 and later</span></span>](#layers-in-windows-8-and-later)
    -   [<span data-ttu-id="eda34-109">ID2D1DeviceContext et PushLayer</span><span class="sxs-lookup"><span data-stu-id="eda34-109">ID2D1DeviceContext and PushLayer</span></span>](#id2d1devicecontext-and-pushlayer)
    -   [<span data-ttu-id="eda34-110">Couche \_ d2d1 \_ PARAMETERS1 et d2d1 \_ couche \_ options1</span><span class="sxs-lookup"><span data-stu-id="eda34-110">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>](/windows)
    -   [<span data-ttu-id="eda34-111">Modes de fusion</span><span class="sxs-lookup"><span data-stu-id="eda34-111">Blend Modes</span></span>](#blend-modes)
    -   [<span data-ttu-id="eda34-112">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="eda34-112">Interoperation</span></span>](#interoperation)
-   [<span data-ttu-id="eda34-113">Créer des couches</span><span class="sxs-lookup"><span data-stu-id="eda34-113">Creating Layers</span></span>](#creating-layers)
-   [<span data-ttu-id="eda34-114">Limites du contenu</span><span class="sxs-lookup"><span data-stu-id="eda34-114">Content Bounds</span></span>](#content-bounds)
-   [<span data-ttu-id="eda34-115">Masques géométriques</span><span class="sxs-lookup"><span data-stu-id="eda34-115">Geometric Masks</span></span>](#geometric-masks)
-   [<span data-ttu-id="eda34-116">Masques d’opacité</span><span class="sxs-lookup"><span data-stu-id="eda34-116">Opacity Masks</span></span>](#opacity-masks)
-   [<span data-ttu-id="eda34-117">Alternatives aux couches</span><span class="sxs-lookup"><span data-stu-id="eda34-117">Alternatives to Layers</span></span>](#alternatives-to-layers)
-   [<span data-ttu-id="eda34-118">Découpage d’une forme arbitraire</span><span class="sxs-lookup"><span data-stu-id="eda34-118">Clipping an arbitrary shape</span></span>](#clipping-an-arbitrary-shape)
    -   [<span data-ttu-id="eda34-119">Clips alignés sur l’axe</span><span class="sxs-lookup"><span data-stu-id="eda34-119">Axis aligned clips</span></span>](#axis-aligned-clips)
-   [<span data-ttu-id="eda34-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eda34-120">Related topics</span></span>](#related-topics)

## <a name="what-are-layers"></a><span data-ttu-id="eda34-121">Que sont les couches ?</span><span class="sxs-lookup"><span data-stu-id="eda34-121">What Are Layers?</span></span>

<span data-ttu-id="eda34-122">Les couches, représentées par les objets [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , permettent à une application de manipuler un groupe d’opérations de dessin.</span><span class="sxs-lookup"><span data-stu-id="eda34-122">Layers, represented by [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) objects, enable an application to manipulate a group of drawing operations.</span></span> <span data-ttu-id="eda34-123">Vous utilisez une couche en la « poussant » sur une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="eda34-123">You use a layer by "pushing" it onto a render target.</span></span> <span data-ttu-id="eda34-124">Les opérations de dessin ultérieures effectuées par la cible de rendu sont dirigées vers la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-124">Subsequent drawing operations by the render target are directed to the layer.</span></span> <span data-ttu-id="eda34-125">Une fois que vous avez terminé avec la couche, vous « pop » la couche à partir de la cible de rendu, qui répartit le contenu de la couche sur la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="eda34-125">After you're finished with the layer, you "pop" the layer from the render target, which composites the layer's content back to the render target.</span></span>

<span data-ttu-id="eda34-126">Comme les pinceaux, les couches sont des ressources dépendantes du périphérique créées par des cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="eda34-126">Like brushes, layers are device-dependent resources created by render targets.</span></span> <span data-ttu-id="eda34-127">Les couches peuvent être utilisées sur n’importe quelle cible de rendu dans le même domaine de ressource qui contient la cible de rendu qui l’a créée.</span><span class="sxs-lookup"><span data-stu-id="eda34-127">Layers can be used on any render target in the same resource domain that contains the render target that created it.</span></span> <span data-ttu-id="eda34-128">Toutefois, une ressource de couche ne peut être utilisée que par une cible de rendu à la fois.</span><span class="sxs-lookup"><span data-stu-id="eda34-128">However, a layer resource can only be used by one render target at a time.</span></span> <span data-ttu-id="eda34-129">Pour plus d’informations sur les ressources, consultez [vue d’ensemble des ressources](resources-and-resource-domains.md).</span><span class="sxs-lookup"><span data-stu-id="eda34-129">For more information about resources, see the [Resources Overview](resources-and-resource-domains.md).</span></span>

<span data-ttu-id="eda34-130">Bien que les couches offrent une technique de rendu puissante pour produire des effets intéressants, un nombre excessif de couches dans une application peut nuire à ses performances, en raison des différents coûts associés à la gestion des couches et des ressources de couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-130">Although layers offer a powerful rendering technique for producing interesting effects, excessive number of layers in an application can adversely affect its performance, because of the various costs associated with managing layers and layer resources.</span></span> <span data-ttu-id="eda34-131">Par exemple, il y a un coût de remplissage ou d’effacement de la couche, puis de la fusionner de nouveau, en particulier sur du matériel de haut de gamme.</span><span class="sxs-lookup"><span data-stu-id="eda34-131">For example, there is the cost of filling or clearing the layer and then blending it back, especially on higher-end hardware.</span></span> <span data-ttu-id="eda34-132">Ensuite, il y a le coût de la gestion des ressources de couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-132">Then, there is the cost of managing the layer resources.</span></span> <span data-ttu-id="eda34-133">Si vous les réallouez fréquemment, les blocages résultants sur le GPU sont le problème le plus significatif.</span><span class="sxs-lookup"><span data-stu-id="eda34-133">If you reallocate these frequently, the resulting stalls against the GPU will be the most significant problem.</span></span> <span data-ttu-id="eda34-134">Lorsque vous concevez votre application, essayez d’optimiser la réutilisation des ressources de couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-134">When you design your application, try to maximize reusing layer resources.</span></span>

## <a name="layers-in-windows-8-and-later"></a><span data-ttu-id="eda34-135">Couches dans Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="eda34-135">Layers in Windows 8 and later</span></span>

<span data-ttu-id="eda34-136">Windows 8 a introduit de nouvelles API liées à la couche qui simplifient, améliorent les performances de et ajoutent des fonctionnalités aux couches.</span><span class="sxs-lookup"><span data-stu-id="eda34-136">Windows 8 introduced new layer related APIs that simplify, improve the performance of, and add features to layers.</span></span>

### <a name="id2d1devicecontext-and-pushlayer"></a><span data-ttu-id="eda34-137">ID2D1DeviceContext et PushLayer</span><span class="sxs-lookup"><span data-stu-id="eda34-137">ID2D1DeviceContext and PushLayer</span></span>

<span data-ttu-id="eda34-138">L’interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) est dérivée de l’interface [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) et est la clé de l’affichage du contenu Direct2D dans Windows 8. pour plus d’informations sur cette interface, consultez [contextes de périphériques et](devices-and-device-contexts.md)de périphériques.</span><span class="sxs-lookup"><span data-stu-id="eda34-138">The [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface is derived from the [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) interface and is key to displaying Direct2D content in Windows 8, for more information about this interface see [Devices and Device Contexts](devices-and-device-contexts.md).</span></span> <span data-ttu-id="eda34-139">Avec l’interface de contexte de périphérique, vous pouvez ignorer l’appel de la méthode [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , puis passer la valeur null à la méthode [**ID2D1DeviceContext ::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="eda34-139">With the device context interface, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**ID2D1DeviceContext::PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span> <span data-ttu-id="eda34-140">Direct2D gère automatiquement la ressource de couche et peut partager des ressources entre les couches et les graphiques d’effet.</span><span class="sxs-lookup"><span data-stu-id="eda34-140">Direct2D automatically manages the layer resource and can share resources between layers and effect graphs.</span></span>

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a><span data-ttu-id="eda34-141">Couche \_ d2d1 \_ PARAMETERS1 et d2d1 \_ couche \_ options1</span><span class="sxs-lookup"><span data-stu-id="eda34-141">D2D1\_LAYER\_PARAMETERS1 and D2D1\_LAYER\_OPTIONS1</span></span>

<span data-ttu-id="eda34-142">La [**structure \_ \_ PARAMETERS1 de la couche d2d1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) est la même que celle des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), sauf que le membre final de la structure est maintenant une énumération options1 de la [**\_ couche \_ d2d1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) .</span><span class="sxs-lookup"><span data-stu-id="eda34-142">The [**D2D1\_LAYER\_PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) structure is the same as [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), except the final member of the structure is now a [**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) enumeration.</span></span>

<span data-ttu-id="eda34-143">[**D2d1 \_ La couche \_ options1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) n’a pas d’option ClearType et a deux options différentes que vous pouvez utiliser pour améliorer les performances :</span><span class="sxs-lookup"><span data-stu-id="eda34-143">[**D2D1\_LAYER\_OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) has no ClearType option and has two different options that you can use to improve performance:</span></span>

-   <span data-ttu-id="eda34-144">[**D2d1 \_ \_Initialisation de la couche options1 \_ \_ à partir de l' \_ arrière-plan**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D effectue le rendu des primitives sur la couche sans l’effacer avec le noir transparent.</span><span class="sxs-lookup"><span data-stu-id="eda34-144">[**D2D1\_LAYER\_OPTIONS1\_INITIALIZE\_FROM\_BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D renders primitives to the layer without clearing it with transparent black.</span></span> <span data-ttu-id="eda34-145">Il ne s’agit pas de la valeur par défaut, mais dans la plupart des cas, il en résulte une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="eda34-145">This is not the default, but in most cases results in better performance.</span></span>

-   <span data-ttu-id="eda34-146">[**D2d1 \_ Options1 de la couche \_ \_ Ignorer \_ alpha**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): si la surface sous-jacente est définie sur [**d2d1 \_ \_ mode Alpha \_ ignorée**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), cette option permet à Direct2D d’éviter de modifier le canal alpha de la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-146">[**D2D1\_LAYER\_OPTIONS1\_IGNORE\_ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): if the underlying surface is set to [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), this option lets Direct2D avoid modifying the alpha channel of the layer.</span></span> <span data-ttu-id="eda34-147">Ne l’utilisez pas dans d’autres cas.</span><span class="sxs-lookup"><span data-stu-id="eda34-147">Do not use this in other cases.</span></span>

### <a name="blend-modes"></a><span data-ttu-id="eda34-148">Modes de fusion</span><span class="sxs-lookup"><span data-stu-id="eda34-148">Blend Modes</span></span>

<span data-ttu-id="eda34-149">À compter de Windows 8, le contexte de périphérique a un [**mode de fusion primitif**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) qui détermine la façon dont chaque primitive est fusionnée avec la surface cible.</span><span class="sxs-lookup"><span data-stu-id="eda34-149">Starting in Windows 8, the device context has a [**primitive blend mode**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) that determines how each primitive is blended with the target surface.</span></span> <span data-ttu-id="eda34-150">Ce mode s’applique également aux couches lorsque vous appelez la méthode [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="eda34-150">This mode also applies to layers when you call the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method.</span></span>

<span data-ttu-id="eda34-151">Par exemple, si vous utilisez une couche pour découper des primitives avec transparence, définissez le mode de [**\_ \_ \_ copie de fusion primitif d2d1**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) sur le contexte de périphérique pour obtenir des résultats corrects.</span><span class="sxs-lookup"><span data-stu-id="eda34-151">For example, if you are using a layer to clip primitives with transparency set the [**D2D1\_PRIMITIVE\_BLEND\_COPY**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) mode on the device context for proper results.</span></span> <span data-ttu-id="eda34-152">Le mode de copie fait en sorte que le contexte de l’appareil effectue l’interpolation linéaire sur les 4 canaux de couleur, y compris le canal alpha, de chaque pixel avec le contenu de la surface cible en fonction du masque géométrique de la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-152">The copy mode makes the device context linear interpolate all 4 color channels, including the alpha channel, of each pixel with the contents of the target surface according to the geometric mask of the layer.</span></span>

### <a name="interoperation"></a><span data-ttu-id="eda34-153">Interopérabilité</span><span class="sxs-lookup"><span data-stu-id="eda34-153">Interoperation</span></span>

<span data-ttu-id="eda34-154">À partir de Windows 8, Direct2D prend en charge l’interopérabilité avec Direct3D et GDI lorsqu’une couche ou un clip est poussé.</span><span class="sxs-lookup"><span data-stu-id="eda34-154">Starting in Windows 8, Direct2D supports interoperation with Direct3D and GDI while a layer or clip is pushed.</span></span> <span data-ttu-id="eda34-155">Vous appelez [**ID2D1GdiInteropRenderTarget :: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) alors qu’une couche est Poussée pour interagir avec GDI.</span><span class="sxs-lookup"><span data-stu-id="eda34-155">You call [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) while a layer is pushed to interoperate with GDI.</span></span> <span data-ttu-id="eda34-156">Vous appelez [**ID2D1DeviceContext :: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) , puis le rendu sur la surface sous-jacente pour interagir avec Direct3D.</span><span class="sxs-lookup"><span data-stu-id="eda34-156">You call [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) and then render to the underlying surface to interoperate with Direct3D.</span></span> <span data-ttu-id="eda34-157">Il est de votre responsabilité d’effectuer un rendu à l’intérieur de la couche ou du clip avec Direct3D ou GDI.</span><span class="sxs-lookup"><span data-stu-id="eda34-157">It is your responsibility to render inside the layer or clip with Direct3D or GDI.</span></span> <span data-ttu-id="eda34-158">Si vous essayez d’effectuer un rendu à l’extérieur de la couche ou de découper, les résultats ne sont pas définis.</span><span class="sxs-lookup"><span data-stu-id="eda34-158">If you try to render outside the layer or clip the results are undefined.</span></span>

## <a name="creating-layers"></a><span data-ttu-id="eda34-159">Créer des couches</span><span class="sxs-lookup"><span data-stu-id="eda34-159">Creating Layers</span></span>

<span data-ttu-id="eda34-160">L’utilisation de couches nécessite une bonne connaissance des méthodes [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , ainsi que de la structure des paramètres de la [**\_ \_ couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) , qui contient un ensemble de données paramétriques qui définissent la façon dont la couche peut être utilisée.</span><span class="sxs-lookup"><span data-stu-id="eda34-160">Working with layers requires familiarity with the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) methods, and the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure, which contains a set of parametric data that defines how the layer can be used.</span></span> <span data-ttu-id="eda34-161">La liste suivante décrit les méthodes et la structure.</span><span class="sxs-lookup"><span data-stu-id="eda34-161">The following list describes the methods and structure.</span></span>

-   <span data-ttu-id="eda34-162">Appelez la méthode [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) pour créer une ressource de couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-162">Call the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method to create a layer resource.</span></span>
    > [!Note]  
    > <span data-ttu-id="eda34-163">À partir de Windows 8, vous pouvez ignorer l’appel de la méthode [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) , puis passer NULL à la méthode [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) sur l’interface [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) .</span><span class="sxs-lookup"><span data-stu-id="eda34-163">Starting in Windows 8, you can skip calling the [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) method and then pass NULL to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) method on the [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) interface.</span></span> <span data-ttu-id="eda34-164">C’est plus simple et permet à Direct2D de gérer automatiquement la ressource de couche et de partager les ressources entre les couches et les graphiques d’effet.</span><span class="sxs-lookup"><span data-stu-id="eda34-164">This is simpler and allows Direct2D to automatically manage the layer resource and share resources between layers and effect graphs.</span></span>

     

-   <span data-ttu-id="eda34-165">Une fois que la cible de rendu a commencé le dessin (une fois que sa méthode [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) a été appelée), vous pouvez utiliser la méthode [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) .</span><span class="sxs-lookup"><span data-stu-id="eda34-165">After render target has begun drawing (after its [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) method has been called), you can use the [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method.</span></span> <span data-ttu-id="eda34-166">La méthode **PushLayer** ajoute la couche spécifiée à la cible de rendu, afin que la cible reçoive toutes les opérations de dessin suivantes jusqu’à ce que [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) soit appelé.</span><span class="sxs-lookup"><span data-stu-id="eda34-166">The **PushLayer** method adds the specified layer to the render target, so that the target receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <span data-ttu-id="eda34-167">Cette méthode prend un objet [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) retourné en appelant [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) et un *layerParameters* dans la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="eda34-167">This method takes an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) object returned by calling [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) and an *layerParameters* in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure.</span></span> <span data-ttu-id="eda34-168">Le tableau suivant décrit les champs de la structure.</span><span class="sxs-lookup"><span data-stu-id="eda34-168">The following table describes the fields of the structure.</span></span> 

    | <span data-ttu-id="eda34-169">Champ</span><span class="sxs-lookup"><span data-stu-id="eda34-169">Field</span></span>                 | <span data-ttu-id="eda34-170">Description</span><span class="sxs-lookup"><span data-stu-id="eda34-170">Description</span></span>|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="eda34-171">**contentBounds**</span><span class="sxs-lookup"><span data-stu-id="eda34-171">**contentBounds**</span></span>     | <span data-ttu-id="eda34-172">Limites de contenu de la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-172">The content bounds of the layer.</span></span> <span data-ttu-id="eda34-173">Le contenu en dehors de ces limites est garanti qu’il n’est pas rendu.</span><span class="sxs-lookup"><span data-stu-id="eda34-173">Content outside these bounds is guaranteed not to render.</span></span> <span data-ttu-id="eda34-174">La valeur par défaut de ce paramètre est [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span><span class="sxs-lookup"><span data-stu-id="eda34-174">This parameter defaults to [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect).</span></span> <span data-ttu-id="eda34-175">Lorsque la valeur par défaut est utilisée, les limites de contenu sont effectivement prises pour être les limites de la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="eda34-175">When the default value is used, the content bounds are effectively taken to be the bounds of the render target.</span></span> |
    | <span data-ttu-id="eda34-176">**geometricMask**</span><span class="sxs-lookup"><span data-stu-id="eda34-176">**geometricMask**</span></span>     | <span data-ttu-id="eda34-177">Facultatif Zone, définie par un [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), à laquelle la couche doit être découpée.</span><span class="sxs-lookup"><span data-stu-id="eda34-177">(Optional) The area, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), to which the layer should be clipped.</span></span> <span data-ttu-id="eda34-178">A la valeur **null** si la couche ne doit pas être découpée en géométrie.</span><span class="sxs-lookup"><span data-stu-id="eda34-178">Set to **NULL** if the layer shouldn't be clipped to a geometry.</span></span> |
    | <span data-ttu-id="eda34-179">**maskAntialiasMode**</span><span class="sxs-lookup"><span data-stu-id="eda34-179">**maskAntialiasMode**</span></span> | <span data-ttu-id="eda34-180">Valeur qui spécifie le mode d’anticrénelage pour le masque géométrique spécifié par le champ **geometricMask** .</span><span class="sxs-lookup"><span data-stu-id="eda34-180">A value that specifies the antialiasing mode for the geometric mask specified by the **geometricMask** field.</span></span> |
    | <span data-ttu-id="eda34-181">**maskTransform**</span><span class="sxs-lookup"><span data-stu-id="eda34-181">**maskTransform**</span></span>     | <span data-ttu-id="eda34-182">Valeur qui spécifie la transformation appliquée au masque géométrique lors de la composition de la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-182">A value that specifies the transform that is applied to the geometric mask when composing the layer.</span></span> <span data-ttu-id="eda34-183">Cela est relatif à la transformation universelle.</span><span class="sxs-lookup"><span data-stu-id="eda34-183">This is relative to the world transform.</span></span>  |
    | <span data-ttu-id="eda34-184">**'**</span><span class="sxs-lookup"><span data-stu-id="eda34-184">**opacity**</span></span>           | <span data-ttu-id="eda34-185">Valeur d’opacité de la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-185">The opacity value of the layer.</span></span> <span data-ttu-id="eda34-186">L’opacité de chaque ressource de la couche est multipliée par cette valeur lors de la composition vers la cible.</span><span class="sxs-lookup"><span data-stu-id="eda34-186">The opacity of each resource in the layer is multiplied with this value when compositing to the target.</span></span>  |
    | <span data-ttu-id="eda34-187">**opacityBrush**</span><span class="sxs-lookup"><span data-stu-id="eda34-187">**opacityBrush**</span></span>      | <span data-ttu-id="eda34-188">Facultatif Pinceau utilisé pour modifier l’opacité de la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-188">(Optional) A brush that is used to modify the opacity of the layer.</span></span> <span data-ttu-id="eda34-189">Le pinceau est mappé à la couche et le canal alpha de chaque pixel de pinceau mappé est multiplié par rapport au pixel de couche correspondant.</span><span class="sxs-lookup"><span data-stu-id="eda34-189">The brush is mapped to the layer, and the alpha channel of each mapped brush pixel is multiplied against the corresponding layer pixel.</span></span> <span data-ttu-id="eda34-190">Affectez la valeur **null** si la couche ne doit pas avoir de masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="eda34-190">Set to **NULL** if the layer shouldn't have an opacity mask.</span></span>   |
    | <span data-ttu-id="eda34-191">**layerOptions**</span><span class="sxs-lookup"><span data-stu-id="eda34-191">**layerOptions**</span></span>      | <span data-ttu-id="eda34-192">Valeur qui spécifie si la couche envisage de restituer du texte avec l’anticrénelage ClearType.</span><span class="sxs-lookup"><span data-stu-id="eda34-192">A value that specifies whether the layer intends to render text with ClearType antialiasing.</span></span> <span data-ttu-id="eda34-193">Par défaut, ce paramètre a la valeur OFF.</span><span class="sxs-lookup"><span data-stu-id="eda34-193">This parameter defaults to off.</span></span> <span data-ttu-id="eda34-194">Son activation permet à ClearType de fonctionner correctement, mais cela entraîne une vitesse de rendu légèrement plus lente.</span><span class="sxs-lookup"><span data-stu-id="eda34-194">Turning it on enables ClearType to work correctly, but it results in slightly slower rendering speed.</span></span>    |

    

     

    > [!Note]  
    > <span data-ttu-id="eda34-195">À partir de Windows 8, vous ne pouvez pas effectuer de rendu avec ClearType dans une couche, donc le paramètre **layerOptions** doit toujours être défini sur [**options de \_ couche d2d1 \_ \_ aucune**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span><span class="sxs-lookup"><span data-stu-id="eda34-195">Starting in Windows 8, you cannot render with ClearType in a layer, so the **layerOptions** parameter should always be set to [**D2D1\_LAYER\_OPTIONS\_NONE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)</span></span>

     

    <span data-ttu-id="eda34-196">Pour plus de commodité, Direct2D fournit la méthode [**d2d1 :: LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) pour vous aider à créer des structures de [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) .</span><span class="sxs-lookup"><span data-stu-id="eda34-196">For convenience, Direct2D provides the [**D2D1::LayerParameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) method to help you create [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structures.</span></span>

-   <span data-ttu-id="eda34-197">Pour compositiser le contenu de la couche dans la cible de rendu, appelez la méthode [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) .</span><span class="sxs-lookup"><span data-stu-id="eda34-197">To composite the contents of the layer into the render target, call the [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) method.</span></span> <span data-ttu-id="eda34-198">Vous devez appeler la méthode **PopLayer** avant d’appeler la méthode [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) .</span><span class="sxs-lookup"><span data-stu-id="eda34-198">You must call the **PopLayer** method before you call the [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) method.</span></span>

<span data-ttu-id="eda34-199">L’exemple suivant montre comment utiliser [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span><span class="sxs-lookup"><span data-stu-id="eda34-199">The following example shows how to use [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)), [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)), and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer).</span></span> <span data-ttu-id="eda34-200">Tous les champs de la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) sont définis sur leurs valeurs par défaut, à l’exception de **opacityBrush**, qui est défini sur un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span><span class="sxs-lookup"><span data-stu-id="eda34-200">All fields in the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure are set to their defaults, except **opacityBrush**, which is set to an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span>


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



<span data-ttu-id="eda34-201">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="eda34-201">Code has been omitted from this example.</span></span>

<span data-ttu-id="eda34-202">Notez que lorsque vous appelez [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) et [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), vérifiez que chaque **PushLayer** a un appel **PopLayer** correspondant.</span><span class="sxs-lookup"><span data-stu-id="eda34-202">Note that when you call [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) and [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer), ensure that each **PushLayer** has a matching **PopLayer** call.</span></span> <span data-ttu-id="eda34-203">S’il y a plus d’appels **PopLayer** que d’appels **PushLayer** , la cible de rendu est placée dans un état d’erreur.</span><span class="sxs-lookup"><span data-stu-id="eda34-203">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="eda34-204">Si [**flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) est appelé avant que toutes les couches en suspens soient dépilées, la cible de rendu est placée dans un état d’erreur et retourne une erreur.</span><span class="sxs-lookup"><span data-stu-id="eda34-204">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state and returns an error.</span></span> <span data-ttu-id="eda34-205">Pour effacer l’état d’erreur, utilisez [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span><span class="sxs-lookup"><span data-stu-id="eda34-205">To clear the error state, use [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

## <a name="content-bounds"></a><span data-ttu-id="eda34-206">Limites du contenu</span><span class="sxs-lookup"><span data-stu-id="eda34-206">Content Bounds</span></span>

<span data-ttu-id="eda34-207">**ContentBounds** définit la limite de ce qui doit être dessiné sur la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-207">The **contentBounds** sets the limit of what is to be drawn to the layer.</span></span> <span data-ttu-id="eda34-208">Seuls les éléments des limites de contenu sont composites à la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="eda34-208">Only those things within the content bounds are composited back to the render target.</span></span>

<span data-ttu-id="eda34-209">L’exemple suivant montre comment spécifier **contentBounds** afin que l’image d’origine soit découpée en limites de contenu avec l’angle supérieur gauche à (10, 108) et le coin inférieur droit à (121, 177).</span><span class="sxs-lookup"><span data-stu-id="eda34-209">The example that follows shows how to specify **contentBounds** so that the original image is clipped to the content bounds with the upper-left corner at (10, 108) and the lower-right corner at (121, 177).</span></span> <span data-ttu-id="eda34-210">L’illustration suivante montre l’image d’origine et le résultat du découpage de l’image vers les limites du contenu.</span><span class="sxs-lookup"><span data-stu-id="eda34-210">The following illustration shows the original image and the result of clipping the image to the content bounds.</span></span>

![illustration de limites de contenu sur une image d’origine et l’image découpée résultante](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="eda34-212">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="eda34-212">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="eda34-213">L’image découpée résultante est également affectée si vous spécifiez un **geometricMask**.</span><span class="sxs-lookup"><span data-stu-id="eda34-213">The resulting clipped image is further affected if you specify a **geometricMask**.</span></span> <span data-ttu-id="eda34-214">Pour plus d’informations, consultez la section [masques géométriques](#geometric-masks) .</span><span class="sxs-lookup"><span data-stu-id="eda34-214">See the [Geometric Masks](#geometric-masks) section for more information.</span></span>

 

## <a name="geometric-masks"></a><span data-ttu-id="eda34-215">Masques géométriques</span><span class="sxs-lookup"><span data-stu-id="eda34-215">Geometric Masks</span></span>

<span data-ttu-id="eda34-216">Un masque géométrique est un élément ou un découpage, défini par un objet [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , qui masque une couche lorsqu’elle est dessinée par une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="eda34-216">A geometric mask is a clip or a cutout, defined by an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) object, that masks a layer when it is drawn by a render target.</span></span> <span data-ttu-id="eda34-217">Vous pouvez utiliser le champ **geometricMask** de la structure des [**\_ \_ paramètres de couche d2d1**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) pour masquer les résultats dans une géométrie.</span><span class="sxs-lookup"><span data-stu-id="eda34-217">You can use the **geometricMask** field of the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to mask the results to a geometry.</span></span> <span data-ttu-id="eda34-218">Par exemple, si vous souhaitez afficher une image masquée par une lettre de bloc « A », vous pouvez d’abord créer une géométrie représentant la lettre « A » et utiliser cette géométrie comme masque géométrique pour une couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-218">For example, if you want to display an image masked by a block letter "A", you can first create a geometry representing the block letter "A" and use that geometry as a geometric mask for a layer.</span></span> <span data-ttu-id="eda34-219">Ensuite, après avoir effectué un push de la couche, vous pouvez dessiner l’image.</span><span class="sxs-lookup"><span data-stu-id="eda34-219">Then, after pushing the layer, you can draw the image.</span></span> <span data-ttu-id="eda34-220">Le fait de détourer la couche entraîne le découpage de l’image en forme de lettre « A ».</span><span class="sxs-lookup"><span data-stu-id="eda34-220">Popping the layer results in the image being clipped to the block letter "A" shape.</span></span>

<span data-ttu-id="eda34-221">L’exemple suivant montre comment créer un [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) contenant une forme de montagne, puis passer la géométrie du tracé à [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span><span class="sxs-lookup"><span data-stu-id="eda34-221">The example that follows shows how to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) containing a shape of a mountain and then pass the path geometry to the [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)).</span></span> <span data-ttu-id="eda34-222">Il dessine ensuite une bitmap et des carrés.</span><span class="sxs-lookup"><span data-stu-id="eda34-222">It then draws a bitmap and squares.</span></span> <span data-ttu-id="eda34-223">S’il n’existe qu’une image bitmap à afficher dans la couche, utilisez [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau bitmap avec pincement pour plus d’efficacité.</span><span class="sxs-lookup"><span data-stu-id="eda34-223">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="eda34-224">L’illustration suivante montre la sortie de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="eda34-224">The following illustration shows the output from the example.</span></span>

![illustration d’une image d’une feuille et de l’image résultante après l’application d’un masque géométrique d’une montagne](images/layers-bitmapmask.png)

<span data-ttu-id="eda34-226">Le premier exemple définit la géométrie à utiliser comme masque.</span><span class="sxs-lookup"><span data-stu-id="eda34-226">The first example defines the geometry to be used as a mask.</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



<span data-ttu-id="eda34-227">L’exemple suivant utilise la géométrie comme masque pour la couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-227">The next example uses the geometry as a mask for the layer.</span></span>


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



<span data-ttu-id="eda34-228">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="eda34-228">Code has been omitted from this example.</span></span>

> [!Note]
>
> <span data-ttu-id="eda34-229">En général, si vous spécifiez un **geometricMask**, vous pouvez utiliser la valeur par défaut, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), pour **contentBounds**.</span><span class="sxs-lookup"><span data-stu-id="eda34-229">In general, if you specify a **geometricMask**, you can use the default value, [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect), for the **contentBounds**.</span></span>
>
> <span data-ttu-id="eda34-230">Si **contentBounds** a la valeur null et que **GEOMETRICMASK** est non null, les limites de contenu sont en fait les limites du masque géométrique après l’application de la transformation de masque.</span><span class="sxs-lookup"><span data-stu-id="eda34-230">If **contentBounds** is NULL, and **geometricMask** is non-NULL, then the content bounds are effectively the bounds of the geometric mask after the mask transform is applied.</span></span>
>
> <span data-ttu-id="eda34-231">Si **contentBounds** n’a pas la valeur null et que **geometricMask** n’a pas la valeur null, le masque géométrique transformé est correctement rogné par rapport aux limites de contenu et les limites de contenu sont supposées être infinies.</span><span class="sxs-lookup"><span data-stu-id="eda34-231">If **contentBounds** is non-NULL, and **geometricMask** is non-NULL, then the transformed geometric mask is effectively clipped against content bounds and the content bounds are assumed to be infinite.</span></span>

 

## <a name="opacity-masks"></a><span data-ttu-id="eda34-232">Masques d’opacité</span><span class="sxs-lookup"><span data-stu-id="eda34-232">Opacity Masks</span></span>

<span data-ttu-id="eda34-233">Un masque d’opacité est un masque, décrit par un pinceau ou un bitmap, qui est appliqué à un autre objet pour rendre cet objet partiellement ou complètement transparent.</span><span class="sxs-lookup"><span data-stu-id="eda34-233">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="eda34-234">Il permet d’utiliser le canal alpha d’un pinceau à utiliser comme masque de contenu.</span><span class="sxs-lookup"><span data-stu-id="eda34-234">It allows the use of the alpha channel of a brush to be used as a content mask.</span></span> <span data-ttu-id="eda34-235">Par exemple, vous pouvez définir un pinceau de dégradé radial qui varie d’opaque à transparent pour créer un effet d’vignette.</span><span class="sxs-lookup"><span data-stu-id="eda34-235">For example, you can define a radial gradient brush that varies from opaque to transparent to create a vignette effect.</span></span>

<span data-ttu-id="eda34-236">L’exemple qui suit utilise un [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) comme masque d’opacité.</span><span class="sxs-lookup"><span data-stu-id="eda34-236">The example that follows uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m\_pRadialGradientBrush*) as an opacity mask.</span></span> <span data-ttu-id="eda34-237">Il dessine ensuite une bitmap et des carrés.</span><span class="sxs-lookup"><span data-stu-id="eda34-237">It then draws a bitmap and squares.</span></span> <span data-ttu-id="eda34-238">S’il n’existe qu’une image bitmap à afficher dans la couche, utilisez [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau bitmap avec pincement pour plus d’efficacité.</span><span class="sxs-lookup"><span data-stu-id="eda34-238">If there is only a bitmap in the layer to render, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush for efficiency.</span></span> <span data-ttu-id="eda34-239">L’illustration suivante montre la sortie de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="eda34-239">The following illustration shows the output from this example.</span></span>

![illustration d’une image d’arbres et de l’image résultante après l’application d’un masque d’opacité](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



<span data-ttu-id="eda34-241">Le code a été omis de cet exemple.</span><span class="sxs-lookup"><span data-stu-id="eda34-241">Code has been omitted from this example.</span></span>

> [!Note]  
> <span data-ttu-id="eda34-242">Cet exemple utilise une couche pour appliquer un masque d’opacité à un objet unique pour que l’exemple reste aussi simple que possible.</span><span class="sxs-lookup"><span data-stu-id="eda34-242">This example uses a layer to apply an opacity mask to a single object to keep the example as simple as possible.</span></span> <span data-ttu-id="eda34-243">Lors de l’application d’un masque d’opacité à un objet unique, il est plus efficace d’utiliser les méthodes [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) ou [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) , plutôt qu’une couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-243">When applying an opacity mask to a single object, its more efficient to use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) or [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) methods, rather than a layer.</span></span>

 

<span data-ttu-id="eda34-244">Pour obtenir des instructions sur l’application d’un masque d’opacité sans utiliser de couche, consultez [vue d’ensemble des masques d’opacité](opacity-masks-overview.md).</span><span class="sxs-lookup"><span data-stu-id="eda34-244">For instructions on how to apply an opacity mask without using a layer, see the [Opacity Masks Overview](opacity-masks-overview.md).</span></span>

## <a name="alternatives-to-layers"></a><span data-ttu-id="eda34-245">Alternatives aux couches</span><span class="sxs-lookup"><span data-stu-id="eda34-245">Alternatives to Layers</span></span>

<span data-ttu-id="eda34-246">Comme mentionné précédemment, un nombre excessif de couches peut nuire aux performances de votre application.</span><span class="sxs-lookup"><span data-stu-id="eda34-246">As mentioned earlier, excessive number of layers can adversely affect the performance of your application.</span></span> <span data-ttu-id="eda34-247">Pour améliorer les performances, évitez d’utiliser les couches dans la mesure du possible ; Utilisez plutôt leurs alternatives.</span><span class="sxs-lookup"><span data-stu-id="eda34-247">To improve performance, avoid using layers whenever possible; instead use their alternatives.</span></span> <span data-ttu-id="eda34-248">L’exemple de code suivant montre comment utiliser [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) et [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) pour découper une région, comme alternative à l’utilisation d’une couche avec des limites de contenu.</span><span class="sxs-lookup"><span data-stu-id="eda34-248">The following code example shows how to use [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) and [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) to clip a region, as an alternative to using a layer with content bounds.</span></span>


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



<span data-ttu-id="eda34-249">De même, utilisez [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau bitmap avec pincement, comme alternative à l’utilisation d’une couche avec un masque d’opacité lorsqu’il n’existe qu’un seul contenu à afficher dans la couche, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="eda34-249">Similarly, use [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) with a clamped bitmap brush as an alternative to using a layer with an opacity mask when there is only one content in the layer to render, as shown in the following example.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



<span data-ttu-id="eda34-250">En guise d’alternative à l’utilisation d’une couche avec un masque géométrique, envisagez d’utiliser un masque bitmap pour découper une région, comme illustré dans l’exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="eda34-250">As an alternative to using a layer with a geometric mask, consider using a bitmap mask to clip a region, as shown in the following example.</span></span>


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



<span data-ttu-id="eda34-251">Enfin, si vous souhaitez appliquer l’opacité à une seule primitive, vous devez multiplier l’opacité dans la couleur du pinceau, puis restituer la primitive.</span><span class="sxs-lookup"><span data-stu-id="eda34-251">Lastly, if you want to apply opacity to a single primitive, you should multiply the opacity into the into the brush color and then render the primitive.</span></span> <span data-ttu-id="eda34-252">Vous n’avez pas besoin d’une image bitmap de masque d’opacité ou de couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-252">You do not need a layer or an opacity mask bitmap.</span></span>


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a><span data-ttu-id="eda34-253">Découpage d’une forme arbitraire</span><span class="sxs-lookup"><span data-stu-id="eda34-253">Clipping an arbitrary shape</span></span>

<span data-ttu-id="eda34-254">La figure ci-dessous illustre le résultat de l’application d’un clip à une image.</span><span class="sxs-lookup"><span data-stu-id="eda34-254">The figure here shows the result of applying a clip to an image.</span></span>

![image qui montre un exemple d’image avant et après un clip.](images/clip.png)

<span data-ttu-id="eda34-256">Vous pouvez obtenir ce résultat en utilisant des couches avec un masque Geometry ou la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) avec un pinceau d’opacité.</span><span class="sxs-lookup"><span data-stu-id="eda34-256">You can get this result by using layers with a geometry mask or the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method with an opacity brush.</span></span>

<span data-ttu-id="eda34-257">Voici un exemple qui utilise une couche :</span><span class="sxs-lookup"><span data-stu-id="eda34-257">Here's an example that uses a layer:</span></span>


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



<span data-ttu-id="eda34-258">Voici un exemple qui utilise la méthode [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) :</span><span class="sxs-lookup"><span data-stu-id="eda34-258">Here's an example that uses the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method:</span></span>


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



<span data-ttu-id="eda34-259">Dans cet exemple de code, lorsque vous appelez la méthode PushLayer, vous ne transmettez pas de couche créée par une application.</span><span class="sxs-lookup"><span data-stu-id="eda34-259">In this code example, when you call the PushLayer method, you don't pass in an app created layer.</span></span> <span data-ttu-id="eda34-260">Direct2D crée une couche pour vous.</span><span class="sxs-lookup"><span data-stu-id="eda34-260">Direct2D creates a layer for you.</span></span> <span data-ttu-id="eda34-261">Direct2D est en mesure de gérer l’allocation et la destruction de cette ressource sans aucune implication de l’application.</span><span class="sxs-lookup"><span data-stu-id="eda34-261">Direct2D is able to manage the allocation and destruction of this resource without any involvement from the app.</span></span> <span data-ttu-id="eda34-262">Cela permet à Direct2D de réutiliser des couches en interne et d’appliquer des optimisations de gestion des ressources.</span><span class="sxs-lookup"><span data-stu-id="eda34-262">This allows Direct2D to reuse layers internally and apply resource management optimizations.</span></span>

> [!Note]  
> <span data-ttu-id="eda34-263">Dans Windows 8, de nombreuses optimisations ont été apportées à l’utilisation des couches et nous vous recommandons d’essayer d’utiliser les API de couche au lieu de [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) chaque fois que cela est possible.</span><span class="sxs-lookup"><span data-stu-id="eda34-263">In Windows 8 many optimizations have been made to the usage of layers and we recommend you try using layer APIs instead of [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) whenever possible.</span></span>

 

### <a name="axis-aligned-clips"></a><span data-ttu-id="eda34-264">Clips alignés sur l’axe</span><span class="sxs-lookup"><span data-stu-id="eda34-264">Axis aligned clips</span></span>

<span data-ttu-id="eda34-265">Si la région à découper est alignée sur l’axe de la surface de dessin, plutôt que arbitraire.</span><span class="sxs-lookup"><span data-stu-id="eda34-265">If the region to be clipped is aligned to the axis of the drawing surface, instead of arbitrary.</span></span> <span data-ttu-id="eda34-266">Ce cas est adapté à l’utilisation d’un rectangle de découpage au lieu d’une couche.</span><span class="sxs-lookup"><span data-stu-id="eda34-266">This case is suited for using a clip rectangle instead of a layer.</span></span> <span data-ttu-id="eda34-267">Le gain de performance est plus pour la géométrie avec alias que la géométrie avec anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="eda34-267">The performance gain is more for aliased geometry than antialiased geometry.</span></span> <span data-ttu-id="eda34-268">Pour plus d’informations sur les clips alignés sur l’axe, consultez la rubrique [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .</span><span class="sxs-lookup"><span data-stu-id="eda34-268">For more info on axis aligned clips, see the [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) topic.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eda34-269">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="eda34-269">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eda34-270">Référence Direct2D</span><span class="sxs-lookup"><span data-stu-id="eda34-270">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 