---
title: Configuration de la fonctionnalité de fusion
description: Les opérations de fusion sont effectuées sur chaque sortie de nuanceur de pixels (valeur RVBA) avant que la valeur de sortie ne soit écrite dans une cible de rendu. Si l’échantillonnage multiple est activé, la fusion est effectuée sur chaque échantillon multiple ; dans le cas contraire, la fusion est effectuée sur chaque pixel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104990920"
---
# <a name="configuring-blending-functionality"></a><span data-ttu-id="c75bc-104">Configuration de la fonctionnalité de fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-104">Configuring Blending Functionality</span></span>

<span data-ttu-id="c75bc-105">Les opérations de fusion sont effectuées sur chaque sortie de nuanceur de pixels (valeur RVBA) avant que la valeur de sortie ne soit écrite dans une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="c75bc-105">Blending operations are performed on every pixel shader output (RGBA value) before the output value is written to a render target.</span></span> <span data-ttu-id="c75bc-106">Si l’échantillonnage multiple est activé, la fusion est effectuée sur chaque échantillon multiple ; dans le cas contraire, la fusion est effectuée sur chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="c75bc-106">If multisampling is enabled, blending is done on each multisample; otherwise, blending is performed on each pixel.</span></span>

-   [<span data-ttu-id="c75bc-107">Créer l’état de fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-107">Create the Blend State</span></span>](#create-the-blend-state)
-   [<span data-ttu-id="c75bc-108">Lier l’état de fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-108">Bind the Blend State</span></span>](#bind-the-blend-state)
-   [<span data-ttu-id="c75bc-109">Rubriques avancées sur la fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-109">Advanced Blending Topics</span></span>](#advanced-blending-topics)
    -   [<span data-ttu-id="c75bc-110">Alpha-à-couverture</span><span class="sxs-lookup"><span data-stu-id="c75bc-110">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
    -   [<span data-ttu-id="c75bc-111">Fusion des sorties de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c75bc-111">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)
-   [<span data-ttu-id="c75bc-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c75bc-112">Related topics</span></span>](#related-topics)

## <a name="create-the-blend-state"></a><span data-ttu-id="c75bc-113">Créer l’état de fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-113">Create the Blend State</span></span>

<span data-ttu-id="c75bc-114">L’État Blend est une collection d’États utilisée pour contrôler la fusion.</span><span class="sxs-lookup"><span data-stu-id="c75bc-114">The blend state is a collection of states used to control blending.</span></span> <span data-ttu-id="c75bc-115">Ces États (définis dans [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) sont utilisés pour créer l’objet d’État Blend en appelant [**ID3D11Device1 :: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span><span class="sxs-lookup"><span data-stu-id="c75bc-115">These states (defined in [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) are used to create the blend state object by calling [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span></span>

<span data-ttu-id="c75bc-116">Par exemple, voici un exemple très simple de création d’état de fusion qui désactive la fusion alpha et n’utilise pas de masquage de pixel par composant.</span><span class="sxs-lookup"><span data-stu-id="c75bc-116">For instance, here is a very simple example of blend-state creation that disables alpha blending and uses no per-component pixel masking.</span></span>


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



<span data-ttu-id="c75bc-117">Cet exemple est similaire à l' [exemple HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c75bc-117">This example is similar to the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="bind-the-blend-state"></a><span data-ttu-id="c75bc-118">Lier l’état de fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-118">Bind the Blend State</span></span>

<span data-ttu-id="c75bc-119">Après avoir créé l’objet d’état de fusion, liez l’objet d’état de fusion à l’étape de fusion de sortie en appelant [**ID3D11DeviceContext :: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="c75bc-119">After you create the blend-state object, bind the blend-state object to the output-merger stage by calling [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span></span>


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



<span data-ttu-id="c75bc-120">Cette API prend trois paramètres : l’objet d’état de fusion, un facteur de mélange à quatre composants et un exemple de masque.</span><span class="sxs-lookup"><span data-stu-id="c75bc-120">This API takes three parameters: the blend-state object, a four-component blend factor, and a sample mask.</span></span> <span data-ttu-id="c75bc-121">Vous pouvez transmettre **null** pour l’objet d’état de fusion pour spécifier l’état de fusion par défaut ou passer un objet d’état de fusion.</span><span class="sxs-lookup"><span data-stu-id="c75bc-121">You can pass in **NULL** for the blend-state object to specify the default blend state or pass in a blend-state object.</span></span> <span data-ttu-id="c75bc-122">Si vous avez créé l’objet d’état de fusion avec [**d3d11 \_ Blend Blend \_ \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) ou [**d3d11 Blend Blend Blend \_ \_ \_ \_ Factor**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), vous pouvez passer un facteur de fusion pour moduler les valeurs du nuanceur de pixels, de la cible de rendu ou des deux.</span><span class="sxs-lookup"><span data-stu-id="c75bc-122">If you created the blend-state object with [**D3D11\_BLEND\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) or [**D3D11\_BLEND\_INV\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), you can pass a blend factor to modulate values for the pixel shader, render target, or both.</span></span> <span data-ttu-id="c75bc-123">Si vous n’avez pas créé l’objet d’état de fusion avec le facteur de fusion **\_ Blend d3d11 \_ \_** ou le **\_ \_ \_ \_ facteur de fusion d3d11 Blend**, vous pouvez toujours passer un facteur de fusion non null, mais la phase de fusion n’utilise pas le facteur de fusion ; le runtime stocke le facteur de fusion et vous pouvez ensuite appeler [**ID3D11DeviceContext :: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) pour récupérer le facteur de fusion.</span><span class="sxs-lookup"><span data-stu-id="c75bc-123">If you didn't create the blend-state object with **D3D11\_BLEND\_BLEND\_FACTOR** or **D3D11\_BLEND\_INV\_BLEND\_FACTOR**, you can still pass a non-NULL blend factor, but the blending stage does not use the blend factor; the runtime stores the blend factor, and you can later call [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) to retrieve the blend factor.</span></span> <span data-ttu-id="c75bc-124">Si vous transmettez la **valeur null**, le runtime utilise ou stocke un facteur de fusion égal à {1, 1, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="c75bc-124">If you pass **NULL**, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.</span></span> <span data-ttu-id="c75bc-125">L’exemple de masque est un masque défini par l’utilisateur qui détermine comment échantillonner la cible de rendu existante avant de la mettre à jour.</span><span class="sxs-lookup"><span data-stu-id="c75bc-125">The sample mask is a user-defined mask that determines how to sample the existing render target before updating it.</span></span> <span data-ttu-id="c75bc-126">Le masque d’échantillonnage par défaut est 0xFFFFFFFF qui désigne l’échantillonnage des points.</span><span class="sxs-lookup"><span data-stu-id="c75bc-126">The default sampling mask is 0xffffffff which designates point sampling.</span></span>

<span data-ttu-id="c75bc-127">Dans la plupart des schémas de mise en mémoire tampon de profondeur, le pixel le plus proche de l’appareil photo est celui qui est dessiné.</span><span class="sxs-lookup"><span data-stu-id="c75bc-127">In most depth buffering schemes, the pixel closest to the camera is the one that gets drawn.</span></span> <span data-ttu-id="c75bc-128">Lors de [la configuration de l’état du stencil de profondeur](d3d10-graphics-programming-guide-depth-stencil.md), le membre **DepthFunc** de la [**\_ \_ \_ Description du stencil de profondeur d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) peut être n’importe quelle fonction de [**\_ comparaison d3d11 \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="c75bc-128">When [setting up the depth stencil state](d3d10-graphics-programming-guide-depth-stencil.md), the **DepthFunc** member of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) can be any [**D3D11\_COMPARISON\_FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span></span> <span data-ttu-id="c75bc-129">Normalement, vous souhaitez que **DepthFunc** soit **d3d11 une \_ comparaison \_ inférieure**, afin que les pixels les plus proches de l’appareil photo remplacent les pixels situés derrière eux.</span><span class="sxs-lookup"><span data-stu-id="c75bc-129">Normally, you would want **DepthFunc** to be **D3D11\_COMPARISON\_LESS**, so that the pixels closest to the camera will overwrite the pixels behind them.</span></span> <span data-ttu-id="c75bc-130">Toutefois, selon les besoins de votre application, toutes les autres fonctions de comparaison peuvent être utilisées pour effectuer le test de profondeur.</span><span class="sxs-lookup"><span data-stu-id="c75bc-130">However, depending on the needs of your application, any of the other comparison functions may be used to do the depth test.</span></span>

## <a name="advanced-blending-topics"></a><span data-ttu-id="c75bc-131">Rubriques avancées sur la fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-131">Advanced Blending Topics</span></span>

-   [<span data-ttu-id="c75bc-132">Alpha-à-couverture</span><span class="sxs-lookup"><span data-stu-id="c75bc-132">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
-   [<span data-ttu-id="c75bc-133">Fusion des sorties de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c75bc-133">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a><span data-ttu-id="c75bc-134">Alpha-à-couverture</span><span class="sxs-lookup"><span data-stu-id="c75bc-134">Alpha-To-Coverage</span></span>

<span data-ttu-id="c75bc-135">L’alpha-to-Coverage est une technique d’échantillonnage multiple qui est très utile dans des situations telles que des feuillages denses où il existe plusieurs polygones qui utilisent la transparence alpha pour définir des bords dans la surface.</span><span class="sxs-lookup"><span data-stu-id="c75bc-135">Alpha-to-coverage is a multisampling technique that is most useful for situations such as dense foliage where there are several overlapping polygons that use alpha transparency to define edges within the surface.</span></span>

<span data-ttu-id="c75bc-136">Vous pouvez utiliser le membre **AlphaToCoverageEnable** de [**d3d11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) ou [**d3d11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) pour déterminer si le Runtime convertit le. un composant (alpha) du registre de sortie [SV \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 du nuanceur de pixels vers un masque de couverture n-STEP (à partir d’un exemple de **renderTarget** n-Sample).</span><span class="sxs-lookup"><span data-stu-id="c75bc-136">You can use the **AlphaToCoverageEnable** member of [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) or [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) to toggle whether the runtime converts the .a component (alpha) of output register [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 from the pixel shader to an n-step coverage mask (given an n-sample **RenderTarget**).</span></span> <span data-ttu-id="c75bc-137">Le Runtime effectue une opération **and** de ce masque avec la couverture d’exemple classique du pixel dans la primitive (en plus de l’exemple de masque) pour déterminer les exemples à mettre à jour dans tous les **renderTarget** actifs.</span><span class="sxs-lookup"><span data-stu-id="c75bc-137">The runtime performs an **AND** operation of this mask with the typical sample coverage for the pixel in the primitive (in addition to the sample mask) to determine which samples to update in all the active **RenderTarget** s.</span></span>

<span data-ttu-id="c75bc-138">Si le nuanceur de pixels génère une [ \_ couverture de SV](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), le runtime désactive alpha-to-coverage.</span><span class="sxs-lookup"><span data-stu-id="c75bc-138">If the pixel shader outputs [SV\_Coverage](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), the runtime disables alpha-to-coverage.</span></span>

> [!Note]  
> <span data-ttu-id="c75bc-139">Dans l’échantillonnage multiple, le Runtime partage une seule couverture pour tous les **renderTarget** s.</span><span class="sxs-lookup"><span data-stu-id="c75bc-139">In multisampling, the runtime shares only one coverage for all **RenderTarget** s.</span></span> <span data-ttu-id="c75bc-140">Le fait que le runtime lit et convertit. a de la sortie [VP \_ cible](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 à la couverture quand **AlphaToCoverageEnable** a la valeur true ne change pas. valeur qui accède au Blender à **renderTarget** 0 (si un **renderTarget** est défini ici).</span><span class="sxs-lookup"><span data-stu-id="c75bc-140">The fact that the runtime reads and converts .a from output [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 to coverage when **AlphaToCoverageEnable** is TRUE does not change the .a value that goes to the blender at **RenderTarget** 0 (if a **RenderTarget** happens to be set there).</span></span> <span data-ttu-id="c75bc-141">En général, si vous activez l’alpha-à-couverture, vous n’affectez pas la manière dont toutes les sorties de couleur des nuanceurs de pixels interagissent avec **renderTarget** dans l' [étape de fusion de sortie](d3d10-graphics-programming-guide-output-merger-stage.md) , à ceci près que le runtime effectue une opération **and** du masque de couverture avec le masque Alpha-à-couverture.</span><span class="sxs-lookup"><span data-stu-id="c75bc-141">In general, if you enable alpha-to-coverage, you don't affect how all color outputs from pixel shaders interact with **RenderTarget** s through the [output-merger stage](d3d10-graphics-programming-guide-output-merger-stage.md) except that the runtime performs an **AND** operation of the coverage mask with the alpha-to-coverage mask.</span></span> <span data-ttu-id="c75bc-142">Alpha-to-cover fonctionne indépendamment si le runtime peut mélanger **renderTarget** ou si vous utilisez la fusion sur **renderTarget**.</span><span class="sxs-lookup"><span data-stu-id="c75bc-142">Alpha-to-coverage works independently to whether the runtime can blend **RenderTarget** or whether you use blending on **RenderTarget**.</span></span>

 

<span data-ttu-id="c75bc-143">Le matériel graphique ne spécifie pas précisément comment il convertit le nuanceur de pixels de la [ \_ cible](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (alpha) en masque de couverture, sauf que la valeur alpha de 0 (ou moins) doit correspondre à aucune couverture et alpha (ou plus) doit correspondre à une couverture complète (avant que le runtime effectue une opération **and** avec la couverture primitive réelle).</span><span class="sxs-lookup"><span data-stu-id="c75bc-143">Graphics hardware doesn't precisely specify exactly how it converts pixel shader [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alpha) to a coverage mask, except that alpha of 0 (or less) must map to no coverage and alpha of 1 (or greater) must map to full coverage (before the runtime performs an **AND** operation with actual primitive coverage).</span></span> <span data-ttu-id="c75bc-144">Comme alpha passe de 0 à 1, la couverture résultante doit généralement augmenter de façon monotone.</span><span class="sxs-lookup"><span data-stu-id="c75bc-144">As alpha goes from 0 to 1, the resulting coverage should generally increase monotonically.</span></span> <span data-ttu-id="c75bc-145">Toutefois, le matériel peut effectuer le tramage de zone pour fournir une meilleure quantification des valeurs alpha au détriment de la résolution spatiale et du bruit.</span><span class="sxs-lookup"><span data-stu-id="c75bc-145">However, hardware might perform area dithering to provide some better quantization of alpha values at the cost of spatial resolution and noise.</span></span> <span data-ttu-id="c75bc-146">Une valeur alpha NaN (pas un nombre) entraîne un masque aucun (zéro) de couverture.</span><span class="sxs-lookup"><span data-stu-id="c75bc-146">An alpha value of NaN (Not a Number) results in a no coverage (zero) mask.</span></span>

<span data-ttu-id="c75bc-147">La couverture alpha-à-couverture est également traditionnellement utilisée pour la transparence de la porte d’écran ou pour la définition d’silhouettes détaillées pour les sprites autrement opaques.</span><span class="sxs-lookup"><span data-stu-id="c75bc-147">Alpha-to-coverage is also traditionally used for screen-door transparency or defining detailed silhouettes for otherwise opaque sprites.</span></span>

### <a name="blending-pixel-shader-outputs"></a><span data-ttu-id="c75bc-148">Fusion des sorties de nuanceur de pixels</span><span class="sxs-lookup"><span data-stu-id="c75bc-148">Blending Pixel Shader Outputs</span></span>

<span data-ttu-id="c75bc-149">Cette fonctionnalité permet à la fusion de sortie d’utiliser les sorties de nuanceur de pixels simultanément en tant que sources d’entrée pour une opération de fusion avec la cible de rendu unique à l’emplacement 0.</span><span class="sxs-lookup"><span data-stu-id="c75bc-149">This feature enables the output merger to use both the pixel shader outputs simultaneously as input sources to a blending operation with the single render target at slot 0.</span></span>

<span data-ttu-id="c75bc-150">Cet exemple prend deux résultats et les combine en une seule passe, en fusionnant un dans la destination avec une multiplication et l’autre avec un Add :</span><span class="sxs-lookup"><span data-stu-id="c75bc-150">This example takes two results and combines them in a single pass, blending one into the destination with a multiply and the other with an add:</span></span>


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



<span data-ttu-id="c75bc-151">Cet exemple configure la sortie du premier nuanceur de pixels comme couleur source et la deuxième sortie en tant que facteur de mélange de composant par couleur.</span><span class="sxs-lookup"><span data-stu-id="c75bc-151">This example configures the first pixel shader output as the source color and the second output as a per-color component blend factor.</span></span>


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



<span data-ttu-id="c75bc-152">Cet exemple montre comment les facteurs de fusion doivent correspondre au Swizzles du nuanceur :</span><span class="sxs-lookup"><span data-stu-id="c75bc-152">This example illustrates how the blend factors must match the shader swizzles:</span></span>


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



<span data-ttu-id="c75bc-153">Ensemble, les facteurs de mélange et le code du nuanceur impliquent que le nuanceur de pixels est requis pour la sortie au moins de o0. r et O1. a.</span><span class="sxs-lookup"><span data-stu-id="c75bc-153">Together, the blend factors and the shader code imply that the pixel shader is required to output at least o0.r and o1.a.</span></span> <span data-ttu-id="c75bc-154">Les composants de sortie supplémentaires peuvent être générés par le nuanceur, mais ils sont ignorés, mais moins de composants produirait des résultats indéfinis.</span><span class="sxs-lookup"><span data-stu-id="c75bc-154">Extra output components can be output by the shader but would be ignored, fewer components would produce undefined results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c75bc-155">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c75bc-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c75bc-156">Sortie-étape de fusion</span><span class="sxs-lookup"><span data-stu-id="c75bc-156">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="c75bc-157">Étapes de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c75bc-157">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 