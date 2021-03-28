---
title: Prise en main avec l’étape de rastérisation
description: Cette section décrit la définition de la fenêtre d’affichage, du rectangle de ciseaux, de l’état du rastériseur et de l’échantillonnage multiple.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- échantillonnage multiple, état de rastériseur (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315215"
---
# <a name="getting-started-with-the-rasterizer-stage"></a><span data-ttu-id="466a3-104">Prise en main avec l’étape de rastérisation</span><span class="sxs-lookup"><span data-stu-id="466a3-104">Getting Started with the Rasterizer Stage</span></span>

<span data-ttu-id="466a3-105">Cette section décrit la définition de la fenêtre d’affichage, du rectangle de ciseaux, de l’état du rastériseur et de l’échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="466a3-105">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span>

## <a name="set-the-viewport"></a><span data-ttu-id="466a3-106">Définir la fenêtre d’affichage</span><span class="sxs-lookup"><span data-stu-id="466a3-106">Set the Viewport</span></span>

<span data-ttu-id="466a3-107">Une fenêtre d’affichage mappe les positions de vertex (dans l’espace de l’élément) aux positions des cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="466a3-107">A viewport maps vertex positions (in clip space) into render target positions.</span></span> <span data-ttu-id="466a3-108">Cette étape met à l’échelle les positions 3D dans l’espace 2D.</span><span class="sxs-lookup"><span data-stu-id="466a3-108">This step scales the 3D positions into 2D space.</span></span> <span data-ttu-id="466a3-109">Une cible de rendu est orientée avec les axes Y pointant vers le dessous ; Cela nécessite que les coordonnées Y soient retournées lors de l’échelle de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="466a3-109">A render target is oriented with the Y axes pointing down; this requires that the Y coordinates get flipped during the viewport scale.</span></span> <span data-ttu-id="466a3-110">En outre, les étendues x et y (plage des valeurs x et y) sont mises à l’échelle pour s’ajuster à la taille de la fenêtre d’affichage en fonction des formules suivantes :</span><span class="sxs-lookup"><span data-stu-id="466a3-110">In addition, the x and y extents (range of the x and y values) are scaled to fit the viewport size according to the following formulas:</span></span>


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



<span data-ttu-id="466a3-111">Le didacticiel 1 crée une fenêtre d’affichage 640 × 480 à l’aide de [**d3d11 \_ Viewport**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) et en appelant [**ID3D11DeviceContext :: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span><span class="sxs-lookup"><span data-stu-id="466a3-111">Tutorial 1 creates a 640 × 480 viewport using [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) and by calling [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span></span>


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



<span data-ttu-id="466a3-112">La description de la fenêtre d’affichage spécifie la taille de la fenêtre d’affichage, la plage de la profondeur de la carte (à l’aide de *mindepth* et *maxdepth*) et le placement de l’angle supérieur gauche de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="466a3-112">The viewport description specifies the size of the viewport, the range to map depth to (using *MinDepth* and *MaxDepth*), and the placement of the top left of the viewport.</span></span> <span data-ttu-id="466a3-113">*Mindepth* doit être inférieur ou égal à *maxdepth*; la plage pour *mindepth* et *maxdepth* est comprise entre 0,0 et 1,0 inclus.</span><span class="sxs-lookup"><span data-stu-id="466a3-113">*MinDepth* must be less than or equal to *MaxDepth*; the range for both *MinDepth* and *MaxDepth* is between 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="466a3-114">Il est courant que la fenêtre d’affichage soit mappée à une cible de rendu, mais ce n’est pas nécessaire. en outre, la fenêtre d’affichage n’a pas besoin d’avoir la même taille ou position que la cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="466a3-114">It is common for the viewport to map to a render target but it is not necessary; additionally, the viewport does not have to have the same size or position as the render target.</span></span>

<span data-ttu-id="466a3-115">Vous pouvez créer un tableau de Viewports, mais un seul peut être appliqué à une sortie primitive à partir du nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="466a3-115">You can create an array of viewports, but only one can be applied to a primitive output from the geometry shader.</span></span> <span data-ttu-id="466a3-116">Une seule fenêtre d’affichage peut être activée à la fois.</span><span class="sxs-lookup"><span data-stu-id="466a3-116">Only one viewport can be set active at a time.</span></span> <span data-ttu-id="466a3-117">Le pipeline utilise une fenêtre d’affichage par défaut (et un rectangle à ciseaux, présenté dans la section suivante) pendant la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="466a3-117">The pipeline uses a default viewport (and scissor rectangle, discussed in the next section) during rasterization.</span></span> <span data-ttu-id="466a3-118">La valeur par défaut est toujours le premier Viewport (ou rectangle à ciseaux) dans le tableau.</span><span class="sxs-lookup"><span data-stu-id="466a3-118">The default is always the first viewport (or scissor rectangle) in the array.</span></span> <span data-ttu-id="466a3-119">Pour effectuer une sélection par primitive de la fenêtre d’affichage dans le nuanceur Geometry, spécifiez la sémantique ViewportArrayIndex sur le composant de sortie GS approprié dans la déclaration de signature de sortie GS.</span><span class="sxs-lookup"><span data-stu-id="466a3-119">To perform a per-primitive selection of the viewport in the geometry shader, specify the ViewportArrayIndex semantic on the appropriate GS output component in the GS output signature declaration.</span></span>

<span data-ttu-id="466a3-120">Le nombre maximal d’Viewports (et de rectangles ciseaux) qui peuvent être liés à l’étape de rastérisation à un moment donné est 16 (spécifié par **d3d11 \_ VIEWPORT \_ et \_ SCISSORRECT \_ Object \_ Count \_ per \_ pipeline**).</span><span class="sxs-lookup"><span data-stu-id="466a3-120">The maximum number of viewports (and scissor rectangles) that can be bound to the rasterizer stage at any one time is 16 (specified by **D3D11\_VIEWPORT\_AND\_SCISSORRECT\_OBJECT\_COUNT\_PER\_PIPELINE**).</span></span>

## <a name="set-the-scissor-rectangle"></a><span data-ttu-id="466a3-121">Définir le rectangle de la ciseaux</span><span class="sxs-lookup"><span data-stu-id="466a3-121">Set the Scissor Rectangle</span></span>

<span data-ttu-id="466a3-122">Un rectangle à ciseaux vous donne une autre possibilité de réduire le nombre de pixels qui seront envoyés à l’étape de fusion de sortie.</span><span class="sxs-lookup"><span data-stu-id="466a3-122">A scissor rectangle gives you another opportunity to reduce the number of pixels that will be sent to the output merger stage.</span></span> <span data-ttu-id="466a3-123">Les pixels en dehors du rectangle de la ciseaux sont ignorés.</span><span class="sxs-lookup"><span data-stu-id="466a3-123">Pixels outside of the scissor rectangle are discarded.</span></span> <span data-ttu-id="466a3-124">La taille du rectangle de la ciseaux est spécifiée dans des entiers.</span><span class="sxs-lookup"><span data-stu-id="466a3-124">The size of the scissor rectangle is specified in integers.</span></span> <span data-ttu-id="466a3-125">Un seul rectangle symétrique (basé sur *ViewportArrayIndex* dans la [sémantique de valeur système](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) peut être appliqué à un triangle au cours de la pixellisation.</span><span class="sxs-lookup"><span data-stu-id="466a3-125">Only one scissor rectangle (based on *ViewportArrayIndex* in [system value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) can be applied to a triangle during rasterization.</span></span>

<span data-ttu-id="466a3-126">Pour activer le rectangle de la ciseaux, utilisez le membre *ScissorEnable* (dans [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="466a3-126">To enable the scissor rectangle, use the *ScissorEnable* member (in [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span> <span data-ttu-id="466a3-127">Le rectangle de la ciseaux par défaut est un rectangle vide. autrement dit, toutes les valeurs Rect sont 0.</span><span class="sxs-lookup"><span data-stu-id="466a3-127">The default scissor rectangle is an empty rectangle; that is, all rect values are 0.</span></span> <span data-ttu-id="466a3-128">En d’autres termes, si vous ne configurez pas le rectangle de la ciseaux et que la ciseaux est activée, vous n’allez pas envoyer de pixels à l’étape de fusion de sortie.</span><span class="sxs-lookup"><span data-stu-id="466a3-128">In other words, if you do not set up the scissor rectangle and scissor is enabled, you will not send any pixels to the output-merger stage.</span></span> <span data-ttu-id="466a3-129">Le programme d’installation le plus courant consiste à initialiser le rectangle à ciseaux à la taille de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="466a3-129">The most common setup is to initialize the scissor rectangle to the size of the viewport.</span></span>

<span data-ttu-id="466a3-130">Pour définir un tableau de rectangles de ciseaux sur l’appareil, appelez [**ID3D11DeviceContext :: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) avec [**d3d11 \_ Rect**](d3d11-rect.md).</span><span class="sxs-lookup"><span data-stu-id="466a3-130">To set an array of scissor rectangles to the device, call [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) with [**D3D11\_RECT**](d3d11-rect.md).</span></span>


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



<span data-ttu-id="466a3-131">Cette méthode prend deux paramètres : (1) le nombre de rectangles dans le tableau et (2) un tableau de rectangles.</span><span class="sxs-lookup"><span data-stu-id="466a3-131">This method takes two parameters: (1) the number of rectangles in the array and (2) an array of rectangles.</span></span>

<span data-ttu-id="466a3-132">Le pipeline utilise un index de rectangles de ciseaux par défaut lors de la pixellisation (la valeur par défaut est un rectangle de taille zéro avec le découpage désactivé).</span><span class="sxs-lookup"><span data-stu-id="466a3-132">The pipeline uses a default scissor rectangle index during rasterization (the default is a zero-size rectangle with clipping disabled).</span></span> <span data-ttu-id="466a3-133">Pour ce faire, spécifiez la \_ sémantique SV ViewportArrayIndex sur un composant de sortie GS dans la déclaration de signature de sortie GS.</span><span class="sxs-lookup"><span data-stu-id="466a3-133">To override this, specify the SV\_ViewportArrayIndex semantic to a GS output component in the GS output signature declaration.</span></span> <span data-ttu-id="466a3-134">Ainsi, l’étape GS marque ce composant GS output comme un composant généré par le système avec cette sémantique.</span><span class="sxs-lookup"><span data-stu-id="466a3-134">This will cause the GS stage to mark this GS output component as a system-generated component with this semantic.</span></span> <span data-ttu-id="466a3-135">L’étape de rastérisation reconnaît cette sémantique et utilise le paramètre auquel elle est attachée en tant qu’index de rectangles de ciseaux pour accéder au tableau de rectangles de ciseaux.</span><span class="sxs-lookup"><span data-stu-id="466a3-135">The rasterizer stage recognizes this semantic and will use the parameter it is attached to as the scissor rectangle index to access the array of scissor rectangles.</span></span> <span data-ttu-id="466a3-136">N’oubliez pas d’indiquer à l’étape du rastériseur d’utiliser le rectangle de la ciseaux que vous définissez en activant la valeur *ScissorEnable* dans la description du rastériseur avant de créer l’objet rastériseur.</span><span class="sxs-lookup"><span data-stu-id="466a3-136">Don't forget to tell the rasterizer stage to use the scissor rectangle that you define by enabling the *ScissorEnable* value in the rasterizer description before creating the rasterizer object.</span></span>

## <a name="set-rasterizer-state"></a><span data-ttu-id="466a3-137">Définir l’état du rastériseur</span><span class="sxs-lookup"><span data-stu-id="466a3-137">Set Rasterizer State</span></span>

<span data-ttu-id="466a3-138">À partir de Direct3D 10, l’état de rastériseur est encapsulé dans un objet d’État rastériseur.</span><span class="sxs-lookup"><span data-stu-id="466a3-138">Beginning with Direct3D 10, rasterizer state is encapsulated in a rasterizer state object.</span></span> <span data-ttu-id="466a3-139">Vous pouvez créer jusqu’à 4096 objets d’État rastériseur qui peuvent ensuite être définis sur l’appareil en passant un handle à l’objet d’État.</span><span class="sxs-lookup"><span data-stu-id="466a3-139">You may create up to 4096 rasterizer state objects which can then be set to the device by passing a handle to the state object.</span></span>

<span data-ttu-id="466a3-140">Utilisez [**ID3D11Device1 :: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) pour créer un objet d’état de rastériseur à partir d’une description de rastériseur (consultez [**d3d11 \_ rastériseur \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="466a3-140">Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) to create a rasterizer state object from a rasterizer description (see [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span>


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



<span data-ttu-id="466a3-141">Cet exemple de jeu d’état effectue peut-être l’installation du rastériseur le plus basique :</span><span class="sxs-lookup"><span data-stu-id="466a3-141">This example set of state accomplishes perhaps the most basic rasterizer setup:</span></span>

-   <span data-ttu-id="466a3-142">Mode de remplissage plein</span><span class="sxs-lookup"><span data-stu-id="466a3-142">Solid fill mode</span></span>
-   <span data-ttu-id="466a3-143">Élimination ou suppression des faces arrière ; supposer le sens inverse des aiguilles d’une montre pour les primitives</span><span class="sxs-lookup"><span data-stu-id="466a3-143">Cull out or remove back faces; assume counter-clockwise winding order for primitives</span></span>
-   <span data-ttu-id="466a3-144">Désactiver le décalage de profondeur, mais activer la mise en mémoire tampon de profondeur et activer le rectangle de la ciseaux</span><span class="sxs-lookup"><span data-stu-id="466a3-144">Turn off depth bias but enable depth buffering and enable the scissor rectangle</span></span>
-   <span data-ttu-id="466a3-145">Désactiver l’échantillonnage multiple et l’anticrénelage de ligne</span><span class="sxs-lookup"><span data-stu-id="466a3-145">Turn off multisampling and line anti-aliasing</span></span>

<span data-ttu-id="466a3-146">En outre, les opérations de rastérisation de base incluent toujours les éléments suivants : découpage (vers la vue frustum), Division de perspective et échelle de la fenêtre d’affichage.</span><span class="sxs-lookup"><span data-stu-id="466a3-146">In addition, basic rasterizer operations, always include the following: clipping (to the view frustum), perspective divide, and the viewport scale.</span></span> <span data-ttu-id="466a3-147">Après avoir créé l’objet d’état de rastériseur, définissez-le sur l’appareil comme suit :</span><span class="sxs-lookup"><span data-stu-id="466a3-147">After successfully creating the rasterizer state object, set it to the device like this:</span></span>


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a><span data-ttu-id="466a3-148">Échantillonnage multiple</span><span class="sxs-lookup"><span data-stu-id="466a3-148">Multisampling</span></span>

<span data-ttu-id="466a3-149">L’échantillonnage multiple échantillonne une partie ou la totalité des composants d’une image à une résolution supérieure (suivie d’un sous-échantillonnage à la résolution d’origine) pour réduire la forme d’alias la plus visible provoquée par le dessin des bords de polygones.</span><span class="sxs-lookup"><span data-stu-id="466a3-149">Multisampling samples some or all of the components of an image at a higher resolution (followed by downsampling to the original resolution) to reduce the most visible form of aliasing caused by drawing polygon edges.</span></span> <span data-ttu-id="466a3-150">Même si l’échantillonnage multiple nécessite des exemples de sous-pixels, les GPU modernes implémentent l’échantillonnage multiple afin qu’un nuanceur de pixels s’exécute une fois par pixel.</span><span class="sxs-lookup"><span data-stu-id="466a3-150">Even though multisampling requires sub-pixel samples, modern GPU's implement multisampling so that a pixel shader runs once per pixel.</span></span> <span data-ttu-id="466a3-151">Cela fournit un compromis acceptable entre les performances (surtout dans une application liée au GPU) et l’anticrénelage de l’image finale.</span><span class="sxs-lookup"><span data-stu-id="466a3-151">This provides an acceptable tradeoff between performance (especially in a GPU bound application) and anti-aliasing the final image.</span></span>

<span data-ttu-id="466a3-152">Pour utiliser l’échantillonnage multiple, définissez le champ activer dans la [**Description de pixellisation**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), créez une cible de rendu à échantillonnage multiple et lisez la cible de rendu avec un nuanceur pour résoudre les exemples en une couleur de pixel unique ou appelez [**ID3D11DeviceContext :: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) pour résoudre les exemples à l’aide de la carte vidéo.</span><span class="sxs-lookup"><span data-stu-id="466a3-152">To use multisampling, set the enable field in the [**rasterization description**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), create a multisampled render target, and either read the render target with a shader to resolve the samples into a single pixel color or call [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) to resolve the samples using the video card.</span></span> <span data-ttu-id="466a3-153">Le scénario le plus courant consiste à dessiner sur une ou plusieurs cibles de rendu à échantillonnage unique.</span><span class="sxs-lookup"><span data-stu-id="466a3-153">The most common scenario is to draw to one or more multisampled render targets.</span></span>

<span data-ttu-id="466a3-154">L’échantillonnage multiple est indépendant du fait qu’un exemple de masque est utilisé, qu’il soit activé ou non, ou que les opérations [du](d3d10-graphics-programming-guide-blend-state.md) stencil (qui sont toujours effectuées par exemple).</span><span class="sxs-lookup"><span data-stu-id="466a3-154">Multisampling is independent of whether or not a sample mask is used, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) is enabled, or stencil operations (which are always performed per-sample).</span></span>

<span data-ttu-id="466a3-155">Le test de profondeur est affecté par l’échantillonnage multiple :</span><span class="sxs-lookup"><span data-stu-id="466a3-155">Depth testing is affected by multisampling:</span></span>

-   <span data-ttu-id="466a3-156">Lorsque l’échantillonnage multiple est activé, la profondeur est interpolée par échantillon et le test de profondeur/stencil est effectué par échantillon. la couleur de sortie du nuanceur de pixels est dupliquée pour tous les exemples de passage.</span><span class="sxs-lookup"><span data-stu-id="466a3-156">When multisampling is enabled, depth is interpolated per sample and the depth/stencil test is done per sample; the pixel shader output color is duplicated for all passing samples.</span></span> <span data-ttu-id="466a3-157">Si le nuanceur de pixels génère une profondeur, la valeur de profondeur est dupliquée pour tous les échantillons (même si ce scénario perd l’avantage de l’échantillonnage multiple).</span><span class="sxs-lookup"><span data-stu-id="466a3-157">If the pixel shader outputs depth, the depth value is duplicated for all samples (although this scenario loses the benefit of multisampling).</span></span>
-   <span data-ttu-id="466a3-158">Lorsque l’échantillonnage multiple est désactivé, le test de profondeur/gabarit est toujours effectué par échantillon, mais la profondeur n’est pas interpolée par échantillon.</span><span class="sxs-lookup"><span data-stu-id="466a3-158">When multisampling is disabled, depth/stencil testing is still done per-sample, but depth is not interpolated per-sample.</span></span>

<span data-ttu-id="466a3-159">Il n’existe aucune restriction pour mélanger un rendu à échantillonnage et non multiéchantillonnés dans une cible de rendu unique.</span><span class="sxs-lookup"><span data-stu-id="466a3-159">There are no restrictions for mixing multisampled and non-multisampled rendering within a single render target.</span></span> <span data-ttu-id="466a3-160">Si vous activez l’échantillonnage multiple et que vous dessinez sur une cible de rendu non multiéchantillonnée, vous obtenez le même résultat que si l’échantillonnage multiple n’était pas activé. l’échantillonnage s’effectue avec un seul échantillon par pixel.</span><span class="sxs-lookup"><span data-stu-id="466a3-160">If you enable multisampling and draw to a non-multisampled render target, you produce the same result as if multisampling were not enabled; sampling is done with a single sample per-pixel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="466a3-161">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="466a3-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="466a3-162">Étape du rastériseur</span><span class="sxs-lookup"><span data-stu-id="466a3-162">Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 