---
title: Configuration de la fonctionnalité Depth-Stencil
description: Cette section décrit les étapes de configuration de la mémoire tampon du stencil de profondeur et l’état du gabarit de profondeur pour l’étape de fusion de sortie.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728741"
---
# <a name="configuring-depth-stencil-functionality"></a><span data-ttu-id="40754-103">Configuration de la fonctionnalité Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="40754-103">Configuring Depth-Stencil Functionality</span></span>

<span data-ttu-id="40754-104">Cette section décrit les étapes de configuration de la mémoire tampon du stencil de profondeur et l’état du gabarit de profondeur pour l’étape de fusion de sortie.</span><span class="sxs-lookup"><span data-stu-id="40754-104">This section covers the steps for setting up the depth-stencil buffer, and depth-stencil state for the output-merger stage.</span></span>

-   [<span data-ttu-id="40754-105">Créer une ressource Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="40754-105">Create a Depth-Stencil Resource</span></span>](#create-a-depth-stencil-resource)
-   [<span data-ttu-id="40754-106">Créer un état de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="40754-106">Create Depth-Stencil State</span></span>](#create-depth-stencil-state)
-   [<span data-ttu-id="40754-107">Lier Depth-Stencil données à l’étape OM</span><span class="sxs-lookup"><span data-stu-id="40754-107">Bind Depth-Stencil Data to the OM Stage</span></span>](#bind-depth-stencil-data-to-the-om-stage)

<span data-ttu-id="40754-108">Une fois que vous savez comment utiliser la mémoire tampon du stencil de profondeur et l’état du gabarit de profondeur correspondant, reportez-vous à [techniques de stencil avancées](#advanced-stencil-techniques).</span><span class="sxs-lookup"><span data-stu-id="40754-108">Once you know how to use the depth-stencil buffer and the corresponding depth-stencil state, refer to [advanced-stencil techniques](#advanced-stencil-techniques).</span></span>

## <a name="create-a-depth-stencil-resource"></a><span data-ttu-id="40754-109">Créer une ressource Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="40754-109">Create a Depth-Stencil Resource</span></span>

<span data-ttu-id="40754-110">Créez la mémoire tampon du stencil de profondeur à l’aide d’une ressource de texture.</span><span class="sxs-lookup"><span data-stu-id="40754-110">Create the depth-stencil buffer using a texture resource.</span></span>


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a><span data-ttu-id="40754-111">Créer un état de Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="40754-111">Create Depth-Stencil State</span></span>

<span data-ttu-id="40754-112">L’état de gabarit de profondeur indique à l’étape de fusion de sortie comment effectuer le [test de stencil de profondeur](d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="40754-112">The depth-stencil state tells the output-merger stage how to perform the [depth-stencil test](d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="40754-113">Le test de stencil de profondeur détermine si un pixel donné doit être dessiné ou non.</span><span class="sxs-lookup"><span data-stu-id="40754-113">The depth-stencil test determines whether or not a given pixel should be drawn.</span></span>


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



<span data-ttu-id="40754-114">DepthEnable et StencilEnable activent (et désactivent) le test de profondeur et de stencil.</span><span class="sxs-lookup"><span data-stu-id="40754-114">DepthEnable and StencilEnable enable (and disable) depth and stencil testing.</span></span> <span data-ttu-id="40754-115">Affectez à DepthEnable la **valeur false** pour désactiver le test de profondeur et empêcher l’écriture dans le tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="40754-115">Set DepthEnable to **FALSE** to disable depth testing and prevent writing to the depth buffer.</span></span> <span data-ttu-id="40754-116">Définissez StencilEnable sur **false** pour désactiver le test stencil et empêcher l’écriture dans la mémoire tampon du stencil (lorsque DepthEnable a la **valeur false** et que StencilEnable a la **valeur true**, le test de profondeur passe toujours dans l’opération de stencil).</span><span class="sxs-lookup"><span data-stu-id="40754-116">Set StencilEnable to **FALSE** to disable stencil testing and prevent writing to the stencil buffer (when DepthEnable is **FALSE** and StencilEnable is **TRUE**, the depth test always passes in the stencil operation).</span></span>

<span data-ttu-id="40754-117">DepthEnable affecte uniquement l’étape de fusion de sortie. il n’affecte pas le découpage, le décalage de profondeur ou le verrouillage des valeurs avant que les données ne soient entrées dans un nuanceur de pixels.</span><span class="sxs-lookup"><span data-stu-id="40754-117">DepthEnable only affects the output-merger stage - it does not affect clipping, depth bias, or clamping of values before the data is input to a pixel shader.</span></span>

## <a name="bind-depth-stencil-data-to-the-om-stage"></a><span data-ttu-id="40754-118">Lier Depth-Stencil données à l’étape OM</span><span class="sxs-lookup"><span data-stu-id="40754-118">Bind Depth-Stencil Data to the OM Stage</span></span>

<span data-ttu-id="40754-119">Liez l’état de gabarit de profondeur.</span><span class="sxs-lookup"><span data-stu-id="40754-119">Bind the depth-stencil state.</span></span>


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



<span data-ttu-id="40754-120">Liez la ressource de stencil de profondeur à l’aide d’une vue.</span><span class="sxs-lookup"><span data-stu-id="40754-120">Bind the depth-stencil resource using a view.</span></span>


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



<span data-ttu-id="40754-121">Un tableau de vues de cible de rendu peut être passé dans [**ID3D11DeviceContext :: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), mais toutes ces vues de cible de rendu correspondent à une vue de stencil de profondeur unique.</span><span class="sxs-lookup"><span data-stu-id="40754-121">An array of render-target views may be passed into [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), however all of those render-target views will correspond to a single depth stencil view.</span></span> <span data-ttu-id="40754-122">Le tableau de la cible de rendu dans Direct3D 11 est une fonctionnalité qui permet à une application d’effectuer un rendu sur plusieurs cibles de rendu simultanément au niveau de la primitive.</span><span class="sxs-lookup"><span data-stu-id="40754-122">The render target array in Direct3D 11 is a feature that enables an application to render onto multiple render targets simultaneously at the primitive level.</span></span> <span data-ttu-id="40754-123">Les tableaux cibles de rendu offrent des performances accrues par rapport à la définition individuelle des cibles de rendu avec plusieurs appels à **ID3D11DeviceContext :: OMSetRenderTargets** (essentiellement la méthode utilisée dans Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="40754-123">Render target arrays offer increased performance over individually setting render targets with multiple calls to **ID3D11DeviceContext::OMSetRenderTargets** (essentially the method employed in Direct3D 9).</span></span>

<span data-ttu-id="40754-124">Les cibles de rendu doivent toutes être du même type de ressource.</span><span class="sxs-lookup"><span data-stu-id="40754-124">Render targets must all be the same type of resource.</span></span> <span data-ttu-id="40754-125">Si l’anticrénelage est utilisé, toutes les cibles de rendu liées et les tampons de profondeur doivent avoir le même nombre d’échantillons.</span><span class="sxs-lookup"><span data-stu-id="40754-125">If multisample antialiasing is used, all bound render targets and depth buffers must have the same sample counts.</span></span>

<span data-ttu-id="40754-126">Quand une mémoire tampon est utilisée comme cible de rendu, le test du stencil de profondeur et les cibles de rendu multiples ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="40754-126">When a buffer is used as a render target, depth-stencil testing and multiple render targets are not supported.</span></span>

-   <span data-ttu-id="40754-127">Jusqu’à 8 cibles de rendu peuvent être liées simultanément.</span><span class="sxs-lookup"><span data-stu-id="40754-127">As many as 8 render targets can be bound simultaneously.</span></span>
-   <span data-ttu-id="40754-128">Toutes les cibles de rendu doivent avoir la même taille dans toutes les dimensions (largeur et hauteur, et profondeur pour la taille 3D ou de tableau pour les \* types tableau).</span><span class="sxs-lookup"><span data-stu-id="40754-128">All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for \*Array types).</span></span>
-   <span data-ttu-id="40754-129">Chaque cible de rendu peut avoir un format de données différent.</span><span class="sxs-lookup"><span data-stu-id="40754-129">Each render target may have a different data format.</span></span>
-   <span data-ttu-id="40754-130">Les masques d’écriture contrôlent les données qui sont écrites dans une cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-130">Write masks control what data gets written to a render target.</span></span> <span data-ttu-id="40754-131">L’écriture de sortie masque le contrôle sur une cible par rendu, au niveau de chaque composant, quelles données sont écrites dans la ou les cibles de rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-131">The output write masks control on a per-render target, per-component level what data gets written to the render target(s).</span></span>

## <a name="advanced-stencil-techniques"></a><span data-ttu-id="40754-132">Techniques avancées de stencil</span><span class="sxs-lookup"><span data-stu-id="40754-132">Advanced Stencil Techniques</span></span>

<span data-ttu-id="40754-133">La partie stencil de la mémoire tampon du stencil de profondeur peut être utilisée pour créer des effets de rendu tels que la composition, le décalque et le mode plan.</span><span class="sxs-lookup"><span data-stu-id="40754-133">The stencil portion of the depth-stencil buffer can be used for creating rendering effects such as compositing, decaling, and outlining.</span></span>

-   [<span data-ttu-id="40754-134">Composition</span><span class="sxs-lookup"><span data-stu-id="40754-134">Compositing</span></span>](#compositing)
-   [<span data-ttu-id="40754-135">Décalque</span><span class="sxs-lookup"><span data-stu-id="40754-135">Decaling</span></span>](#decaling)
-   [<span data-ttu-id="40754-136">Plans et silhouettes</span><span class="sxs-lookup"><span data-stu-id="40754-136">Outlines and Silhouettes</span></span>](#outlines-and-silhouettes)
-   [<span data-ttu-id="40754-137">Stencil recto-verso</span><span class="sxs-lookup"><span data-stu-id="40754-137">Two-Sided Stencil</span></span>](#two-sided-stencil)
-   [<span data-ttu-id="40754-138">Lecture de la mémoire tampon de Depth-Stencil sous forme de texture</span><span class="sxs-lookup"><span data-stu-id="40754-138">Reading the Depth-Stencil Buffer as a Texture</span></span>](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a><span data-ttu-id="40754-139">Composition</span><span class="sxs-lookup"><span data-stu-id="40754-139">Compositing</span></span>

<span data-ttu-id="40754-140">Votre application peut utiliser la mémoire tampon de stencil pour les images 2D ou 3D composite sur une scène 3D.</span><span class="sxs-lookup"><span data-stu-id="40754-140">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="40754-141">Un masque dans le tampon de stencil est utilisé pour occultait une zone de la surface cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-141">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="40754-142">Des informations 2D stockées, telles que du texte ou des bitmaps, peuvent ensuite être écrites dans la zone bloqués.</span><span class="sxs-lookup"><span data-stu-id="40754-142">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="40754-143">Votre application peut également restituer des primitives 3D supplémentaires dans la région masquée du stencil de la surface cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-143">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="40754-144">Il peut même rendre une scène entière.</span><span class="sxs-lookup"><span data-stu-id="40754-144">It can even render an entire scene.</span></span>

<span data-ttu-id="40754-145">Les jeux composent souvent plusieurs scènes 3D ensemble.</span><span class="sxs-lookup"><span data-stu-id="40754-145">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="40754-146">Par exemple, la conduite des jeux affiche généralement un miroir en mode arrière.</span><span class="sxs-lookup"><span data-stu-id="40754-146">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="40754-147">Le miroir contient la vue de la scène 3D derrière le pilote.</span><span class="sxs-lookup"><span data-stu-id="40754-147">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="40754-148">Il s’agit essentiellement d’une deuxième scène 3D composite avec la vue d’avance du pilote.</span><span class="sxs-lookup"><span data-stu-id="40754-148">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

### <a name="decaling"></a><span data-ttu-id="40754-149">Décalque</span><span class="sxs-lookup"><span data-stu-id="40754-149">Decaling</span></span>

<span data-ttu-id="40754-150">Les applications Direct3D utilisent le décalqueing pour contrôler les pixels d’une image primitive particulière qui sont dessinés sur la surface cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-150">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="40754-151">Les applications appliquent des dépassements aux images de primitives pour permettre l’affichage correct de polygones polygones.</span><span class="sxs-lookup"><span data-stu-id="40754-151">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="40754-152">Par exemple, lorsque vous appliquez des marques de pneu et des lignes jaunes à une chaussée, les marquages doivent apparaître directement en haut de la route.</span><span class="sxs-lookup"><span data-stu-id="40754-152">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="40754-153">Toutefois, les valeurs z des marquages et de la route sont les mêmes.</span><span class="sxs-lookup"><span data-stu-id="40754-153">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="40754-154">Par conséquent, il se peut que la mémoire tampon de profondeur ne produise pas une séparation nette entre les deux.</span><span class="sxs-lookup"><span data-stu-id="40754-154">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="40754-155">Certains pixels de la primitive arrière peuvent être rendus au-dessus de la primitive avant et vice versa.</span><span class="sxs-lookup"><span data-stu-id="40754-155">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="40754-156">L’image résultante semble en scintillement du cadre au frame.</span><span class="sxs-lookup"><span data-stu-id="40754-156">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="40754-157">Cet effet est appelé z-combat ou flimmering.</span><span class="sxs-lookup"><span data-stu-id="40754-157">This effect is called z-fighting or flimmering.</span></span>

<span data-ttu-id="40754-158">Pour résoudre ce problème, utilisez un gabarit pour masquer la section de la primitive de retour où le décalcomanie s’affichera.</span><span class="sxs-lookup"><span data-stu-id="40754-158">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="40754-159">Désactivez la mise en mémoire tampon z et affichez l’image de la primitive avant dans la zone masquée de la surface de rendu-cible.</span><span class="sxs-lookup"><span data-stu-id="40754-159">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="40754-160">Plusieurs fusions de texture peuvent être utilisées pour résoudre ce problème.</span><span class="sxs-lookup"><span data-stu-id="40754-160">Multiple texture blending can be used to solve this problem.</span></span>

### <a name="outlines-and-silhouettes"></a><span data-ttu-id="40754-161">Plans et silhouettes</span><span class="sxs-lookup"><span data-stu-id="40754-161">Outlines and Silhouettes</span></span>

<span data-ttu-id="40754-162">Vous pouvez utiliser la mémoire tampon de stencil pour obtenir des effets plus abstraits, tels que le mode plan et silhouetting.</span><span class="sxs-lookup"><span data-stu-id="40754-162">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="40754-163">Si votre application effectue deux passes de rendu, une pour générer le masque de stencil et la seconde pour appliquer le masque de stencil à l’image, mais avec les primitives légèrement plus petites sur la deuxième passe, l’image résultante contient uniquement le contour de la primitive.</span><span class="sxs-lookup"><span data-stu-id="40754-163">If your application does two render passes - one to generate the stencil mask and second to apply the stencil mask to the image, but with the primitives slightly smaller on the second pass - the resulting image will contain only the primitive's outline.</span></span> <span data-ttu-id="40754-164">L’application peut ensuite remplir la zone masquée du gabarit de l’image avec une couleur unie, ce qui donne à la primitive un aspect en relief.</span><span class="sxs-lookup"><span data-stu-id="40754-164">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="40754-165">Si la taille et la forme du masque du gabarit sont identiques à celles de la primitive que vous affichez, l’image résultante contient un trou où la primitive doit être.</span><span class="sxs-lookup"><span data-stu-id="40754-165">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="40754-166">Votre application peut alors remplir le trou avec du noir pour produire une silhouette de la primitive.</span><span class="sxs-lookup"><span data-stu-id="40754-166">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

### <a name="two-sided-stencil"></a><span data-ttu-id="40754-167">Two-Sided le stencil</span><span class="sxs-lookup"><span data-stu-id="40754-167">Two-Sided Stencil</span></span>

<span data-ttu-id="40754-168">Les volumes de clichés instantanés permettent de dessiner des ombres avec la mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="40754-168">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="40754-169">L’application calcule les volumes de clichés instantanés convertis par la géométrie de la Boucher, en calculant les bords silhouettes et en les séparant de la lumière dans un ensemble de volumes 3D.</span><span class="sxs-lookup"><span data-stu-id="40754-169">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="40754-170">Ces volumes sont ensuite restitués deux fois dans la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="40754-170">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="40754-171">Le premier rendu dessine des polygones vers l’avant et incrémente les valeurs de mémoire tampon de stencil.</span><span class="sxs-lookup"><span data-stu-id="40754-171">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="40754-172">Le deuxième rendu dessine les polygones de l’arrière-plan du volume de cliché instantané et décrémente les valeurs de la mémoire tampon du stencil.</span><span class="sxs-lookup"><span data-stu-id="40754-172">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="40754-173">Normalement, toutes les valeurs incrémentées et décrémentées s’annulent les unes des autres. Toutefois, la scène était déjà rendue avec une géométrie normale provoquant l’échec du test de la mémoire tampon z pour certains pixels, car le volume de cliché instantané est rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-173">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="40754-174">Les valeurs laissées dans la mémoire tampon du stencil correspondent aux pixels qui se trouvent dans l’ombre.</span><span class="sxs-lookup"><span data-stu-id="40754-174">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="40754-175">Ces contenus de tampons de stencil restants sont utilisés comme masque, afin de mélanger en 3D un grand nombre de cœurs noirs englobant tous dans la scène.</span><span class="sxs-lookup"><span data-stu-id="40754-175">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="40754-176">Avec la mémoire tampon de stencil jouant le rôle de masque, le résultat est d’assombrir les pixels qui se trouvent dans les ombres.</span><span class="sxs-lookup"><span data-stu-id="40754-176">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="40754-177">Cela signifie que la géométrie de l’ombre est dessinée deux fois par source de lumière, ce qui entraîne une pression sur le débit du vertex du GPU.</span><span class="sxs-lookup"><span data-stu-id="40754-177">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="40754-178">La fonctionnalité de stencil à deux côtés a été conçue pour atténuer cette situation.</span><span class="sxs-lookup"><span data-stu-id="40754-178">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="40754-179">Dans cette approche, il existe deux ensembles de l’état du gabarit (nommés ci-dessous), un jeu pour les triangles frontaux et l’autre pour les triangles de face arrière.</span><span class="sxs-lookup"><span data-stu-id="40754-179">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="40754-180">De cette façon, une seule passe est dessinée par volume de cliché instantané, par lumière.</span><span class="sxs-lookup"><span data-stu-id="40754-180">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="40754-181">Vous trouverez un exemple d’implémentation de stencil à deux côtés dans l' [exemple ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="40754-181">An example of two-sided stencil implementation can be found in the [ShadowVolume10 Sample](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span></span>

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a><span data-ttu-id="40754-182">Lecture de la mémoire tampon de Depth-Stencil sous forme de texture</span><span class="sxs-lookup"><span data-stu-id="40754-182">Reading the Depth-Stencil Buffer as a Texture</span></span>

<span data-ttu-id="40754-183">Une mémoire tampon de stencil de profondeur inactive peut être lue par un nuanceur comme une texture.</span><span class="sxs-lookup"><span data-stu-id="40754-183">An inactive depth-stencil buffer can be read by a shader as a texture.</span></span> <span data-ttu-id="40754-184">Une application qui lit une mémoire tampon de stencil de profondeur comme une texture est rendue en deux passes, la première passe écrit dans la mémoire tampon de stencil de profondeur et la deuxième passe lit à partir de la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="40754-184">An application that reads a depth-stencil buffer as a texture renders in two passes, the first pass writes to the depth-stencil buffer and the second pass reads from the buffer.</span></span> <span data-ttu-id="40754-185">Cela permet à un nuanceur de comparer les valeurs de la profondeur ou du gabarit précédemment écrites dans la mémoire tampon par rapport à la valeur du Notez pixel qui est affiché.</span><span class="sxs-lookup"><span data-stu-id="40754-185">This allows a shader to compare depth or stencil values previously written to the buffer against the value for the pixel currrently being rendered.</span></span> <span data-ttu-id="40754-186">Le résultat de la comparaison peut être utilisé pour créer des effets tels que le mappage de clichés instantanés ou les particules souples dans un système de particules.</span><span class="sxs-lookup"><span data-stu-id="40754-186">The result of the comparison can be used to create effects such as shadow mapping or soft particles in a particle system.</span></span>

<span data-ttu-id="40754-187">Pour créer une mémoire tampon de stencil de profondeur qui peut être utilisée à la fois comme ressource de stencil de profondeur et comme ressource de nuanceur, quelques modifications doivent être apportées à l’exemple de code dans la section [créer une ressource de Depth-Stencil](#create-a-depth-stencil-resource) .</span><span class="sxs-lookup"><span data-stu-id="40754-187">To create a depth-stencil buffer that can be used as both a depth-stencil resource and a shader resource a few changes need to be made to sample code in the [Create a Depth-Stencil Resource](#create-a-depth-stencil-resource) section.</span></span>

-   <span data-ttu-id="40754-188">La ressource de stencil de profondeur doit avoir un format non typé tel que DXGI \_ format \_ R32 type non \_ .</span><span class="sxs-lookup"><span data-stu-id="40754-188">The depth-stencil resource must have a typeless format such as DXGI\_FORMAT\_R32\_TYPELESS.</span></span>
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   <span data-ttu-id="40754-189">La ressource de stencil de profondeur doit utiliser à la fois le \_ stencil de profondeur de liaison D3D10 et les \_ \_ indicateurs de liaison de ressource de \_ nuanceur de liaison D3D10 \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="40754-189">The depth-stencil resource must use both the D3D10\_BIND\_DEPTH\_STENCIL and D3D10\_BIND\_SHADER\_RESOURCE bind flags.</span></span>
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

<span data-ttu-id="40754-190">En outre, une vue de ressource de nuanceur doit être créée pour la mémoire tampon de profondeur à l’aide d’une structure de [**\_ vue de \_ ressource \_ \_ d3d11 Shader**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) et de [**ID3D11Device :: CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="40754-190">In addition a shader resource view needs to be created for the depth buffer using a [**D3D11\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) structure and [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span></span> <span data-ttu-id="40754-191">La vue de ressource de nuanceur utilise un format typé tel que **dxgi \_ format \_ R32 \_ float** , qui est l’équivalent au format de type non spécifié lors de la création de la ressource de stencil de profondeur.</span><span class="sxs-lookup"><span data-stu-id="40754-191">The shader resource view will use a typed format such as **DXGI\_FORMAT\_R32\_FLOAT** that is the equivalent to the typeless format specified when the depth-stencil resource was created.</span></span>

<span data-ttu-id="40754-192">Dans la première passe de rendu, le tampon de profondeur est lié comme décrit dans la section [lier les données Depth-Stencil à la phase OM](#bind-depth-stencil-data-to-the-om-stage) .</span><span class="sxs-lookup"><span data-stu-id="40754-192">In the first render pass the depth buffer is bound as described in the [Bind Depth-Stencil Data to the OM Stage](#bind-depth-stencil-data-to-the-om-stage) section.</span></span> <span data-ttu-id="40754-193">Notez que le format est passé à la [**\_ vue du stencil de profondeur d3d11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc). Le format utilise un format typé tel que **dxgi \_ format \_ d32 \_ float**.</span><span class="sxs-lookup"><span data-stu-id="40754-193">Note that the format passed to [**D3D11\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc).Format will use a typed format such as **DXGI\_FORMAT\_D32\_FLOAT**.</span></span> <span data-ttu-id="40754-194">Après la première passe de rendu, la mémoire tampon de profondeur contient les valeurs de profondeur pour la scène.</span><span class="sxs-lookup"><span data-stu-id="40754-194">After the first render pass the depth buffer will contain the depth values for the scene.</span></span>

<span data-ttu-id="40754-195">Dans la deuxième étape de rendu, la fonction [**ID3D11DeviceContext :: OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) est utilisée pour définir la vue de stencil de profondeur sur **null** ou une ressource de stencil de profondeur différente, et la vue de ressource de nuanceur est transmise au nuanceur à l’aide de [**ID3D11EffectShaderResourceVariable :: SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span><span class="sxs-lookup"><span data-stu-id="40754-195">In the second render pass the [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) function is used to set the depth-stencil view to **NULL** or a different depth-stencil resource and the shader resource view is passed to the shader using [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span></span> <span data-ttu-id="40754-196">Cela permet au nuanceur de rechercher les valeurs de profondeur calculées dans la première passe de rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-196">This allows the shader to look up the depth values calculated in the first rendering pass.</span></span> <span data-ttu-id="40754-197">Notez qu’une transformation devra être appliquée pour récupérer les valeurs de profondeur si le point de vue de la première passe de rendu est différent de la deuxième passe de rendu.</span><span class="sxs-lookup"><span data-stu-id="40754-197">Note that a transformation will need to be applied to retrieve depth values if the point of view of the first render pass is different from the second render pass.</span></span> <span data-ttu-id="40754-198">Par exemple, si une technique de mappage des clichés instantanés est utilisée, la première passe de rendu sera du point de vue d’une source de lumière, tandis que la deuxième passe de rendu va du point de vue de la visionneuse.</span><span class="sxs-lookup"><span data-stu-id="40754-198">For example, if a shadow mapping technique is being used the first render pass will be from the perspective of a light source while the second render pass will from the viewer's perspective.</span></span>

## <a name="related-topics"></a><span data-ttu-id="40754-199">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="40754-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40754-200">Sortie-étape de fusion</span><span class="sxs-lookup"><span data-stu-id="40754-200">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="40754-201">Étapes de pipeline (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="40754-201">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 