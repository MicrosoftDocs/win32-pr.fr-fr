---
title: Effet de transformation de perspective 3D
description: Utilisez l’effet transformation de perspective 3D pour faire pivoter l’image en 3 dimensions comme si elle était affichée à partir d’une distance.
ms.assetid: 0E1A940E-2DCA-4772-BB68-7E5EF5CEF833
keywords:
- effet transformation de perspective 3D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ed2b1c5131319dd711d2c7802a0bfabceaaa32e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844426"
---
# <a name="3d-perspective-transform-effect"></a><span data-ttu-id="ff6f4-104">Effet de transformation de perspective 3D</span><span class="sxs-lookup"><span data-stu-id="ff6f4-104">3D perspective transform effect</span></span>

<span data-ttu-id="ff6f4-105">Utilisez l’effet transformation de perspective 3D pour faire pivoter l’image en 3 dimensions comme si elle était affichée à partir d’une distance.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-105">Use the 3D perspective transform effect to rotate the image in 3 dimensions as if viewed from a distance.</span></span>

<span data-ttu-id="ff6f4-106">La transformation de perspective 3D est plus pratique que l’effet de transformation 3D, mais expose uniquement un sous-ensemble de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-106">The 3D perspective transform is more convenient than the 3D transform effect, but only exposes a subset of the functionality.</span></span> <span data-ttu-id="ff6f4-107">Vous pouvez calculer une matrice de transformation 3D complète et appliquer une matrice de transformation plus arbitraire à une image à l’aide de l’effet [transformation 3D](3d-transform.md) .</span><span class="sxs-lookup"><span data-stu-id="ff6f4-107">You can compute a full 3D transformation matrix and apply a more arbitrary transform matrix to an image using the [3D transform](3d-transform.md) effect.</span></span>

<span data-ttu-id="ff6f4-108">Le CLSID de cet effet est CLSID \_ D2D13DPerspectiveTransform.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-108">The CLSID for this effect is CLSID\_D2D13DPerspectiveTransform.</span></span>

-   [<span data-ttu-id="ff6f4-109">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ff6f4-109">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ff6f4-110">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ff6f4-110">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ff6f4-111">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="ff6f4-111">Interpolation modes</span></span>](#interpolation-modes)
-   [<span data-ttu-id="ff6f4-112">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="ff6f4-112">Border modes</span></span>](#border-modes)
-   [<span data-ttu-id="ff6f4-113">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="ff6f4-113">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="ff6f4-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff6f4-114">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ff6f4-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff6f4-115">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ff6f4-116">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ff6f4-116">Example image</span></span>



| <span data-ttu-id="ff6f4-117">Avant</span><span class="sxs-lookup"><span data-stu-id="ff6f4-117">Before</span></span>                                                               |
|----------------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)           |
| <span data-ttu-id="ff6f4-119">After</span><span class="sxs-lookup"><span data-stu-id="ff6f4-119">After</span></span>                                                                |
| ![image après l’effet.](images/23-3dperspectivetransform.png) |



 


```C++
ComPtr<ID2D1Effect> perspectiveTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D13DPerspectiveTransform, &perspectiveTransformEffect);

perspectiveTransformEffect->SetInput(0, bitmap);

perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_PERSPECTIVE_ORIGIN, D2D1::Vector3F(0.0f, 192.0f, 0.0f));
perspectiveTransformEffect->SetValue(D2D1_3DPERSPECTIVETRANSFORM_PROP_ROTATION, D2D1::Vector3F(0.0f, 30.0f, 0.0f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(perspectiveTransformEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="ff6f4-121">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ff6f4-121">Effect properties</span></span>



| <span data-ttu-id="ff6f4-122">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="ff6f4-122">Display name and index enumeration</span></span>                                                              | <span data-ttu-id="ff6f4-123">Description</span><span class="sxs-lookup"><span data-stu-id="ff6f4-123">Description</span></span>                                                                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6f4-124">InterpolationMode</span><span class="sxs-lookup"><span data-stu-id="ff6f4-124">InterpolationMode</span></span><br/> <span data-ttu-id="ff6f4-125">\_Mode d’interpolation d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-125">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_INTERPOLATION\_MODE</span></span><br/> | <span data-ttu-id="ff6f4-126">Mode d’interpolation utilisé par l’effet sur l’image.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-126">The interpolation mode the effect uses on the image.</span></span> <span data-ttu-id="ff6f4-127">Il existe 5 modes de mise à l’échelle qui vont de la qualité et de la vitesse.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-127">There are 5 scale modes that range in quality and speed.</span></span><br/> <span data-ttu-id="ff6f4-128">Le type est D2D1 \_ 3DPERSPECTIVETRANSFORM \_ interpolation \_ mode.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-128">Type is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE.</span></span><br/> <span data-ttu-id="ff6f4-129">La valeur par défaut est D2D1 \_ 3DPERSPECTIVETRANSFORM \_ interpolation \_ mode \_ Linear.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-129">Default value is D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span><br/>              |
| <span data-ttu-id="ff6f4-130">BorderMode</span><span class="sxs-lookup"><span data-stu-id="ff6f4-130">BorderMode</span></span><br/> <span data-ttu-id="ff6f4-131">\_Mode de bordure d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-131">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_BORDER\_MODE</span></span><br/>               | <span data-ttu-id="ff6f4-132">Le mode utilisé pour calculer la bordure de l’image, soft ou Hard.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-132">The mode used to calculate the border of the image, soft or hard.</span></span> <span data-ttu-id="ff6f4-133">Pour plus d’informations, consultez [modes de bordure](https://www.bing.com/search?q=Border+modes) .</span><span class="sxs-lookup"><span data-stu-id="ff6f4-133">See [Border modes](https://www.bing.com/search?q=Border+modes) for more info.</span></span><br/> <span data-ttu-id="ff6f4-134">Le type est D2D1 \_ Border \_ mode.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-134">Type is D2D1\_BORDER\_MODE.</span></span><br/> <span data-ttu-id="ff6f4-135">La valeur par défaut est D2D1 \_ mode de bordure \_ \_ souple.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-135">Default value is D2D1\_BORDER\_MODE\_SOFT.</span></span><br/>                                                              |
| <span data-ttu-id="ff6f4-136">Profondeur</span><span class="sxs-lookup"><span data-stu-id="ff6f4-136">Depth</span></span><br/> <span data-ttu-id="ff6f4-137">\_Profondeur d2d1 3DPERSPECTIVETRANSFORM \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-137">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_DEPTH</span></span><br/>                           | <span data-ttu-id="ff6f4-138">Distance entre le *PerspectiveOrigin* et le plan de projection.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-138">The distance from the *PerspectiveOrigin* to the projection plane.</span></span> <span data-ttu-id="ff6f4-139">La valeur spécifiée dans DIP et doit être supérieure à 0.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-139">The value specified in DIPs and must be greater than 0.</span></span><br/> <span data-ttu-id="ff6f4-140">Le type est FLOAT.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-140">Type is FLOAT.</span></span><br/> <span data-ttu-id="ff6f4-141">La valeur par défaut est 1000.0 f.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-141">Default value is 1000.0f.</span></span><br/>                                                                                               |
| <span data-ttu-id="ff6f4-142">PerspectiveOrigin</span><span class="sxs-lookup"><span data-stu-id="ff6f4-142">PerspectiveOrigin</span></span><br/> <span data-ttu-id="ff6f4-143">Origine de la \_ perspective d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-143">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_PERSPECTIVE\_ORIGIN</span></span><br/> | <span data-ttu-id="ff6f4-144">L’emplacement X et Y de la visionneuse dans la scène 3D.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-144">The X and Y location of the viewer in the 3D scene.</span></span> <span data-ttu-id="ff6f4-145">Cette propriété est un \_ vecteur d2d1 \_ 2F défini en tant que : (point X, point Y).</span><span class="sxs-lookup"><span data-stu-id="ff6f4-145">This property is a D2D1\_VECTOR\_2F defined as: (point X, point Y).</span></span> <span data-ttu-id="ff6f4-146">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-146">The units are in DIPs.</span></span><br/> <span data-ttu-id="ff6f4-147">Vous définissez la valeur Z avec la propriété *Depth* .</span><span class="sxs-lookup"><span data-stu-id="ff6f4-147">You set the Z value with the *Depth* property.</span></span><br/> <span data-ttu-id="ff6f4-148">Le type est D2D1 \_ Vector \_ 2F.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-148">Type is D2D1\_VECTOR\_2F.</span></span><br/> <span data-ttu-id="ff6f4-149">La valeur par défaut est {0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-149">Default value is {0.0f, 0.0f}.</span></span><br/> |
| <span data-ttu-id="ff6f4-150">LocalOffset</span><span class="sxs-lookup"><span data-stu-id="ff6f4-150">LocalOffset</span></span><br/> <span data-ttu-id="ff6f4-151">Décalage local de D2D1 \_ 3DPERSPECTIVETRANSFORM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-151">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_LOCAL\_OFFSET</span></span><br/>             | <span data-ttu-id="ff6f4-152">Translation que l’effet effectue avant de faire pivoter le plan de projection.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-152">A translation the effect performs before it rotates the projection plane.</span></span> <span data-ttu-id="ff6f4-153">Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="ff6f4-153">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="ff6f4-154">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-154">The units are in DIPs.</span></span><br/> <span data-ttu-id="ff6f4-155">Le type est D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-155">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="ff6f4-156">La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-156">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                        |
| <span data-ttu-id="ff6f4-157">GlobalOffset</span><span class="sxs-lookup"><span data-stu-id="ff6f4-157">GlobalOffset</span></span><br/> <span data-ttu-id="ff6f4-158">\_ \_ \_ Décalage global d2d1 3DPERSPECTIVETRANSFORM \_ prop</span><span class="sxs-lookup"><span data-stu-id="ff6f4-158">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_GLOBAL\_OFFSET</span></span><br/>           | <span data-ttu-id="ff6f4-159">Translation que l’effet effectue après avoir fait pivoter le plan de projection.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-159">A translation the effect performs after it rotates the projection plane.</span></span> <span data-ttu-id="ff6f4-160">Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="ff6f4-160">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="ff6f4-161">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-161">The units are in DIPs.</span></span><br/> <span data-ttu-id="ff6f4-162">Le type est D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-162">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="ff6f4-163">La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-163">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                         |
| <span data-ttu-id="ff6f4-164">RotationOrigin</span><span class="sxs-lookup"><span data-stu-id="ff6f4-164">RotationOrigin</span></span><br/> <span data-ttu-id="ff6f4-165">\_Origine de rotation d2d1 3DPERSPECTIVETRANSFORM \_ prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-165">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION\_ORIGIN</span></span><br/>       | <span data-ttu-id="ff6f4-166">Point central de la rotation effectuée par l’effet.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-166">The center point of the rotation the effect performs.</span></span> <span data-ttu-id="ff6f4-167">Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="ff6f4-167">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="ff6f4-168">Les unités sont en DIP.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-168">The units are in DIPs.</span></span><br/> <span data-ttu-id="ff6f4-169">Le type est D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-169">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="ff6f4-170">La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-170">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                            |
| <span data-ttu-id="ff6f4-171">Rotation</span><span class="sxs-lookup"><span data-stu-id="ff6f4-171">Rotation</span></span><br/> <span data-ttu-id="ff6f4-172">\_Rotation d2d1 3DPERSPECTIVETRANSFORM \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-172">D2D1\_3DPERSPECTIVETRANSFORM\_PROP\_ROTATION</span></span><br/>                     | <span data-ttu-id="ff6f4-173">Angles de rotation pour chaque axe.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-173">The angles of rotation for each axis.</span></span> <span data-ttu-id="ff6f4-174">Cette propriété est un \_ vecteur d2d1 \_ 3F défini en tant que : (X, Y, Z).</span><span class="sxs-lookup"><span data-stu-id="ff6f4-174">This property is a D2D1\_VECTOR\_3F defined as: (X, Y, Z).</span></span> <span data-ttu-id="ff6f4-175">Les unités sont en degrés.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-175">The units are in degrees.</span></span><br/> <span data-ttu-id="ff6f4-176">Le type est D2D1 \_ Vector \_ 3F.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-176">Type is D2D1\_VECTOR\_3F.</span></span><br/> <span data-ttu-id="ff6f4-177">La valeur par défaut est {0.0 f, 0.0 f, 0.0 f}.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-177">Default value is {0.0f, 0.0f, 0.0f}.</span></span><br/>                                                                         |



 

## <a name="interpolation-modes"></a><span data-ttu-id="ff6f4-178">Modes d’interpolation</span><span class="sxs-lookup"><span data-stu-id="ff6f4-178">Interpolation modes</span></span>



| <span data-ttu-id="ff6f4-179">Énumération</span><span class="sxs-lookup"><span data-stu-id="ff6f4-179">Enumeration</span></span>                                                              | <span data-ttu-id="ff6f4-180">Description</span><span class="sxs-lookup"><span data-stu-id="ff6f4-180">Description</span></span>                                                                                                                                                |
|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6f4-181">\_Mode d’interpolation d2d1 3DPERSPECTIVETRANSFORM \_ \_ \_ le plus proche \_ voisin</span><span class="sxs-lookup"><span data-stu-id="ff6f4-181">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_NEAREST\_NEIGHBOR</span></span>     | <span data-ttu-id="ff6f4-182">Échantillonne le point unique le plus proche et l’utilise.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-182">Samples the nearest single point and uses that.</span></span> <span data-ttu-id="ff6f4-183">Ce mode utilise moins de temps de traitement, mais génère l’image de qualité la plus faible.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-183">This mode uses less processing time, but outputs the lowest quality image.</span></span>                                 |
| <span data-ttu-id="ff6f4-184">D2D1 \_ \_ mode d’interpolation \_ 3DPERSPECTIVETRANSFORM \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="ff6f4-184">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR</span></span>                | <span data-ttu-id="ff6f4-185">Utilise un échantillon à quatre points et une interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-185">Uses a four point sample and linear interpolation.</span></span> <span data-ttu-id="ff6f4-186">Ce mode utilise plus de temps de traitement que le mode voisin le plus proche, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-186">This mode uses more processing time than the nearest neighbor mode, but outputs a higher quality image.</span></span> |
| <span data-ttu-id="ff6f4-187">D2D1 \_ 3DPERSPECTIVETRANSFORM \_ mode d' \_ interpolation \_ cubique</span><span class="sxs-lookup"><span data-stu-id="ff6f4-187">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_CUBIC</span></span>                 | <span data-ttu-id="ff6f4-188">Utilise un exemple de noyau cubique 16 pour l’interpolation.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-188">Uses a 16 sample cubic kernel for interpolation.</span></span> <span data-ttu-id="ff6f4-189">Ce mode utilise le plus de temps de traitement, mais génère une image de qualité supérieure.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-189">This mode uses the most processing time, but outputs a higher quality image.</span></span>                              |
| <span data-ttu-id="ff6f4-190">\_Mode d’interpolation d2d1 3DPERSPECTIVETRANSFORM multi- \_ \_ \_ \_ exemple \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="ff6f4-190">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_MULTI\_SAMPLE\_LINEAR</span></span> | <span data-ttu-id="ff6f4-191">Utilise 4 échantillons linéaires au sein d’un même pixel pour une bonne anticrénelage.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-191">Uses 4 linear samples within a single pixel for good edge anti-aliasing.</span></span> <span data-ttu-id="ff6f4-192">Ce mode est adapté à la réduction de la taille des images avec quelques pixels.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-192">This mode is good for scaling down by small amounts on images with few pixels.</span></span>    |
| <span data-ttu-id="ff6f4-193">D2D1 \_ \_ mode d’interpolation \_ 3DPERSPECTIVETRANSFORM \_ anisotrope</span><span class="sxs-lookup"><span data-stu-id="ff6f4-193">D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_ANISOTROPIC</span></span>           | <span data-ttu-id="ff6f4-194">Utilise le filtrage anisotrope pour échantillonner un modèle en fonction de la forme transformée de l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-194">Uses anisotropic filtering to sample a pattern according to the transformed shape of the bitmap.</span></span>                                                           |



 

> [!Note]  
> <span data-ttu-id="ff6f4-195">Si vous ne sélectionnez pas de mode, l’effet par défaut est D2D1 \_ 3DPERSPECTIVETRANSFORM \_ interpolation \_ mode \_ Linear.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-195">If you don't select a mode, the effect defaults to D2D1\_3DPERSPECTIVETRANSFORM\_INTERPOLATION\_MODE\_LINEAR.</span></span>

 

> [!Note]  
> <span data-ttu-id="ff6f4-196">Le mode anisotrope génère des mipmaps lors de la mise à l’échelle. Toutefois, si vous affectez à la propriété **Cached** la valeur true sur les effets entrés dans cet effet, le des mipmaps ne sera pas généré à chaque fois pour des images suffisamment petites.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-196">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to this effect, the mipmaps won't be generated every time for sufficiently small images.</span></span>

 

## <a name="border-modes"></a><span data-ttu-id="ff6f4-197">Modes de bordure</span><span class="sxs-lookup"><span data-stu-id="ff6f4-197">Border modes</span></span>



| <span data-ttu-id="ff6f4-198">Nom</span><span class="sxs-lookup"><span data-stu-id="ff6f4-198">Name</span></span>                     | <span data-ttu-id="ff6f4-199">Description</span><span class="sxs-lookup"><span data-stu-id="ff6f4-199">Description</span></span>                                                                                                      |
|--------------------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6f4-200">\_Mode de bordure d2d1 \_ \_</span><span class="sxs-lookup"><span data-stu-id="ff6f4-200">D2D1\_BORDER\_MODE\_SOFT</span></span> | <span data-ttu-id="ff6f4-201">L’effet remplit l’image avec des pixels noirs transparents au fur et à mesure de l’interpolation, ce qui génère une bordure douce.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-201">The effect pads the image with transparent black pixels as it interpolates, resulting in a soft edge.</span></span><br/> |
| <span data-ttu-id="ff6f4-202">D2D1 \_ mode de bordure \_ \_ difficile</span><span class="sxs-lookup"><span data-stu-id="ff6f4-202">D2D1\_BORDER\_MODE\_HARD</span></span> | <span data-ttu-id="ff6f4-203">L’effet attache la sortie à la taille de l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-203">The effect clamps the output to the size of the input image.</span></span> <br/>                                         |



 

## <a name="output-bitmap"></a><span data-ttu-id="ff6f4-204">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="ff6f4-204">Output bitmap</span></span>

<span data-ttu-id="ff6f4-205">La taille de l’image bitmap de sortie dépend de la matrice de transformation appliquée à l’image.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-205">The size of the output bitmap depends on the transform matrix that is applied to the image.</span></span>

<span data-ttu-id="ff6f4-206">L’effet exécute l’opération de transformation, puis applique un cadre englobant autour du résultat.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-206">The effect performs the transform operation and then applies a bounding box around the result.</span></span> <span data-ttu-id="ff6f4-207">La bitmap de sortie correspond à la taille du cadre englobant.</span><span class="sxs-lookup"><span data-stu-id="ff6f4-207">The output bitmap is the size of the bounding box.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff6f4-208">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ff6f4-208">Requirements</span></span>



| <span data-ttu-id="ff6f4-209">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ff6f4-209">Requirement</span></span> | <span data-ttu-id="ff6f4-210">Valeur</span><span class="sxs-lookup"><span data-stu-id="ff6f4-210">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ff6f4-211">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff6f4-211">Minimum supported client</span></span> | <span data-ttu-id="ff6f4-212">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ff6f4-212">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ff6f4-213">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ff6f4-213">Minimum supported server</span></span> | <span data-ttu-id="ff6f4-214">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ff6f4-214">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ff6f4-215">En-tête</span><span class="sxs-lookup"><span data-stu-id="ff6f4-215">Header</span></span>                   | <span data-ttu-id="ff6f4-216">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ff6f4-216">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ff6f4-217">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ff6f4-217">Library</span></span>                  | <span data-ttu-id="ff6f4-218">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ff6f4-218">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ff6f4-219">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ff6f4-219">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff6f4-220">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ff6f4-220">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

