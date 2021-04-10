---
title: Effet d’ombre
description: Utilisez l’effet d’ombre pour générer une ombre à partir du canal alpha d’une image.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- effet d’ombre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317141"
---
# <a name="shadow-effect"></a><span data-ttu-id="b4a19-104">Effet d’ombre</span><span class="sxs-lookup"><span data-stu-id="b4a19-104">Shadow effect</span></span>

<span data-ttu-id="b4a19-105">Utilisez l’effet d’ombre pour générer une ombre à partir du canal alpha d’une image.</span><span class="sxs-lookup"><span data-stu-id="b4a19-105">Use the shadow effect to generate a shadow from the alpha channel of an image.</span></span> <span data-ttu-id="b4a19-106">L’ombre est plus opaque pour les valeurs alpha supérieures et plus transparente pour les valeurs alpha inférieures.</span><span class="sxs-lookup"><span data-stu-id="b4a19-106">The shadow is more opaque for higher alpha values and more transparent for lower alpha values.</span></span> <span data-ttu-id="b4a19-107">Vous pouvez définir la quantité de flou et la couleur de l’ombre.</span><span class="sxs-lookup"><span data-stu-id="b4a19-107">You can set the amount of blur and the color of the shadow.</span></span>

-   [<span data-ttu-id="b4a19-108">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="b4a19-108">Example image</span></span>](#example-image)
-   [<span data-ttu-id="b4a19-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b4a19-109">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="b4a19-110">Modes d’optimisation</span><span class="sxs-lookup"><span data-stu-id="b4a19-110">Optimization modes</span></span>](#optimization-modes)
-   [<span data-ttu-id="b4a19-111">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="b4a19-111">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="b4a19-112">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4a19-112">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="b4a19-113">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4a19-113">Related topics</span></span>](#related-topics)

<span data-ttu-id="b4a19-114">Le CLSID de cet effet est CLSID \_ D2D1Shadow.</span><span class="sxs-lookup"><span data-stu-id="b4a19-114">The CLSID for this effect is CLSID\_D2D1Shadow.</span></span>

## <a name="example-image"></a><span data-ttu-id="b4a19-115">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="b4a19-115">Example image</span></span>

<span data-ttu-id="b4a19-116">L’exemple ci-dessous montre la sortie de l’effet d’ombre qui est traduite par l’image source composite au niveau de l’emplacement d’origine.</span><span class="sxs-lookup"><span data-stu-id="b4a19-116">The example here shows the output of the shadow effect translated down and right with the source image composited over it in the original location.</span></span> <span data-ttu-id="b4a19-117">L’effet d’ombre génère uniquement l’ombre.</span><span class="sxs-lookup"><span data-stu-id="b4a19-117">The shadow effect only outputs the shadow.</span></span>



| <span data-ttu-id="b4a19-118">Avant</span><span class="sxs-lookup"><span data-stu-id="b4a19-118">Before</span></span>                                                  |
|---------------------------------------------------------|
| ![image avant l’effet.](images/8-crop.png)      |
| <span data-ttu-id="b4a19-120">After</span><span class="sxs-lookup"><span data-stu-id="b4a19-120">After</span></span>                                                   |
| ![image après la transformation.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="b4a19-122">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b4a19-122">Effect properties</span></span>



| <span data-ttu-id="b4a19-123">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="b4a19-123">Display name and index enumeration</span></span>                                                        | <span data-ttu-id="b4a19-124">Description</span><span class="sxs-lookup"><span data-stu-id="b4a19-124">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a19-125">BlurStandardDeviation</span><span class="sxs-lookup"><span data-stu-id="b4a19-125">BlurStandardDeviation</span></span><br/> <span data-ttu-id="b4a19-126">\_ \_ \_ Écart type de flou \_ \_ de l’ombre d2d1</span><span class="sxs-lookup"><span data-stu-id="b4a19-126">D2D1\_SHADOW\_PROP\_BLUR\_STANDARD\_DEVIATION</span></span><br/> | <span data-ttu-id="b4a19-127">Quantité de flou à appliquer au canal alpha de l’image.</span><span class="sxs-lookup"><span data-stu-id="b4a19-127">The amount of blur to be applied to the alpha channel of the image.</span></span> <span data-ttu-id="b4a19-128">Vous pouvez calculer le rayon de flou du noyau en multipliant l’écart type par 3.</span><span class="sxs-lookup"><span data-stu-id="b4a19-128">You can compute the blur radius of the kernel by multiplying the standard deviation by 3.</span></span> <span data-ttu-id="b4a19-129">Les unités de l’écart type et du rayon de flou sont des DIP.</span><span class="sxs-lookup"><span data-stu-id="b4a19-129">The units of both the standard deviation and blur radius are DIPs.</span></span><br/> <span data-ttu-id="b4a19-130">Cette propriété est la même que la propriété d’écart type [flou gaussien](gaussian-blur.md) .</span><span class="sxs-lookup"><span data-stu-id="b4a19-130">This property is the same as the [Gaussian Blur](gaussian-blur.md) standard deviation property.</span></span> <br/> <span data-ttu-id="b4a19-131">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="b4a19-131">The type is FLOAT.</span></span><br/> <span data-ttu-id="b4a19-132">La valeur par défaut est 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="b4a19-132">The default value is 3.0f.</span></span><br/> |
| <span data-ttu-id="b4a19-133">Couleur</span><span class="sxs-lookup"><span data-stu-id="b4a19-133">Color</span></span><br/> <span data-ttu-id="b4a19-134">Couleur de l' \_ ombre d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4a19-134">D2D1\_SHADOW\_PROP\_COLOR</span></span><br/>                                     | <span data-ttu-id="b4a19-135">Couleur de l'ombre portée.</span><span class="sxs-lookup"><span data-stu-id="b4a19-135">The color of the drop shadow.</span></span> <span data-ttu-id="b4a19-136">Cette propriété est un \_ vecteur d2d1 \_ 4F défini en tant que : (R, G, B, a).</span><span class="sxs-lookup"><span data-stu-id="b4a19-136">This property is a D2D1\_VECTOR\_4F defined as: (R, G, B, A).</span></span> <span data-ttu-id="b4a19-137">Vous devez spécifier cette couleur dans l’alpha simple.</span><span class="sxs-lookup"><span data-stu-id="b4a19-137">You must specify this color in straight alpha.</span></span><br/> <span data-ttu-id="b4a19-138">Le type est D2D1 \_ Vector \_ 4F.</span><span class="sxs-lookup"><span data-stu-id="b4a19-138">The type is D2D1\_VECTOR\_4F.</span></span><br/> <span data-ttu-id="b4a19-139">La valeur par défaut est {0.0 f, 0.0 f, 0.0 f, 1.0 f}.</span><span class="sxs-lookup"><span data-stu-id="b4a19-139">The default value is {0.0f, 0.0f, 0.0f, 1.0f}.</span></span><br/>                                                                                                                                                                     |
| <span data-ttu-id="b4a19-140">Optimization</span><span class="sxs-lookup"><span data-stu-id="b4a19-140">Optimization</span></span><br/> <span data-ttu-id="b4a19-141">Optimisation de la D2D1 des \_ clichés instantanés \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4a19-141">D2D1\_SHADOW\_PROP\_OPTIMIZATION</span></span><br/>                       | <span data-ttu-id="b4a19-142">Niveau d’optimisation des performances.</span><span class="sxs-lookup"><span data-stu-id="b4a19-142">The level of performance optimization.</span></span><br/> <span data-ttu-id="b4a19-143">Le type est D2D1 \_ Shadow \_ Optimization.</span><span class="sxs-lookup"><span data-stu-id="b4a19-143">The type is D2D1\_SHADOW\_OPTIMIZATION.</span></span><br/> <span data-ttu-id="b4a19-144">La valeur par défaut est D2D1 l’optimisation de l' \_ ombre Shadow \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b4a19-144">The default value is D2D1\_SHADOW\_OPTIMIZATION\_BALANCED.</span></span><br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a><span data-ttu-id="b4a19-145">Modes d’optimisation</span><span class="sxs-lookup"><span data-stu-id="b4a19-145">Optimization modes</span></span>



| <span data-ttu-id="b4a19-146">Nom</span><span class="sxs-lookup"><span data-stu-id="b4a19-146">Name</span></span>                                          | <span data-ttu-id="b4a19-147">Description</span><span class="sxs-lookup"><span data-stu-id="b4a19-147">Description</span></span>                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a19-148">Vitesse d’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4a19-148">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_SPEED</span></span>    | <span data-ttu-id="b4a19-149">Applique des optimisations internes telles que la pré-mise à l’échelle à des rayons relativement petits.</span><span class="sxs-lookup"><span data-stu-id="b4a19-149">Applies internal optimizations such as pre-scaling at relatively small radii.</span></span> <span data-ttu-id="b4a19-150">Utilise le filtrage linéaire.</span><span class="sxs-lookup"><span data-stu-id="b4a19-150">Uses linear filtering.</span></span>                                  |
| <span data-ttu-id="b4a19-151">D2D1 \_ DIRECTIONALBLUR \_ Optimization \_ Balanced</span><span class="sxs-lookup"><span data-stu-id="b4a19-151">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_BALANCED</span></span> | <span data-ttu-id="b4a19-152">Utilise les mêmes seuils d’optimisation que le mode vitesse, mais utilise le filtrage trilinéaire.</span><span class="sxs-lookup"><span data-stu-id="b4a19-152">Uses the same optimization thresholds as Speed mode, but uses trilinear filtering.</span></span>                                                    |
| <span data-ttu-id="b4a19-153">Qualité de l’optimisation de D2D1 \_ DIRECTIONALBLUR \_ \_</span><span class="sxs-lookup"><span data-stu-id="b4a19-153">D2D1\_DIRECTIONALBLUR\_OPTIMIZATION\_QUALITY</span></span>  | <span data-ttu-id="b4a19-154">Utilise uniquement des optimisations internes avec de grands rayons de flou, où les approximations sont moins susceptibles d’être visibles.</span><span class="sxs-lookup"><span data-stu-id="b4a19-154">Only uses internal optimizations with large blur radii, where approximations are less likely to be visible.</span></span> <span data-ttu-id="b4a19-155">Utilise le filtrage trilinéaire.</span><span class="sxs-lookup"><span data-stu-id="b4a19-155">Uses trilinear filtering.</span></span> |



 

## <a name="output-bitmap"></a><span data-ttu-id="b4a19-156">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="b4a19-156">Output bitmap</span></span>

<span data-ttu-id="b4a19-157">La taille de la bitmap de sortie est la taille de la sortie de flou.</span><span class="sxs-lookup"><span data-stu-id="b4a19-157">The size of the output bitmap is the size of the blur output.</span></span> <span data-ttu-id="b4a19-158">L’importance de la croissance de la bitmap de sortie par rapport à la bitmap d’origine peut être calculée à l’aide de l’équation suivante :</span><span class="sxs-lookup"><span data-stu-id="b4a19-158">The amount the output bitmap growth relative to the original bitmap can be calculated using the following equation:</span></span>

<span data-ttu-id="b4a19-159">Croissance des bitmaps en sortie (X et Y) = BlurStandardDeviation (DIP (Device-Independent Pixel)) \* 6 \* (dpi utilisateur)/96</span><span class="sxs-lookup"><span data-stu-id="b4a19-159">Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs))\*6\*(User DPI)/96</span></span>

<span data-ttu-id="b4a19-160">La sortie augmente uniformément dans tout le sens, par exemple si la taille augmente de 10 pixels dans chaque direction, l’angle supérieur gauche de la bitmap se trouve à (-5,-5) et le coin inférieur droit est (105, 105) comme indiqué dans le diagramme ici.</span><span class="sxs-lookup"><span data-stu-id="b4a19-160">The output increases equally in all direction, so for example if the size increases by 10 pixels in each direction, the upper left corner of the bitmap is located at (-5, -5) and the lower right will be at (105, 105) as shown in the diagram here.</span></span>

![diagramme de croissance de la taille de sortie de l’effet d’ombre.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a><span data-ttu-id="b4a19-162">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b4a19-162">Requirements</span></span>



| <span data-ttu-id="b4a19-163">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b4a19-163">Requirement</span></span> | <span data-ttu-id="b4a19-164">Valeur</span><span class="sxs-lookup"><span data-stu-id="b4a19-164">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4a19-165">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4a19-165">Minimum supported client</span></span> | <span data-ttu-id="b4a19-166">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b4a19-166">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b4a19-167">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b4a19-167">Minimum supported server</span></span> | <span data-ttu-id="b4a19-168">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b4a19-168">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b4a19-169">En-tête</span><span class="sxs-lookup"><span data-stu-id="b4a19-169">Header</span></span>                   | <span data-ttu-id="b4a19-170">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b4a19-170">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="b4a19-171">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b4a19-171">Library</span></span>                  | <span data-ttu-id="b4a19-172">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b4a19-172">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="b4a19-173">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b4a19-173">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b4a19-174">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="b4a19-174">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

