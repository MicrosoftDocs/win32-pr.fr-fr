---
title: Effet de luminosité
description: Utilisez l’effet luminosité pour contrôler la luminosité de l’image.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- effet de luminosité
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88dd9797aa125e7099ba4a706bac730a30715f6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104558921"
---
# <a name="brightness-effect"></a><span data-ttu-id="ca39b-104">Effet de luminosité</span><span class="sxs-lookup"><span data-stu-id="ca39b-104">Brightness effect</span></span>

<span data-ttu-id="ca39b-105">Utilisez l’effet luminosité pour contrôler la luminosité de l’image.</span><span class="sxs-lookup"><span data-stu-id="ca39b-105">Use the brightness effect to control the brightness of the image.</span></span>

<span data-ttu-id="ca39b-106">Le CLSID de cet effet est CLSID \_ D2D1Brightness.</span><span class="sxs-lookup"><span data-stu-id="ca39b-106">The CLSID for this effect is CLSID\_D2D1Brightness.</span></span>

-   [<span data-ttu-id="ca39b-107">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ca39b-107">Example image</span></span>](#example-image)
-   [<span data-ttu-id="ca39b-108">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ca39b-108">Effect properties</span></span>](#effect-properties)
-   [<span data-ttu-id="ca39b-109">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="ca39b-109">Output bitmap</span></span>](#output-bitmap)
-   [<span data-ttu-id="ca39b-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca39b-110">Requirements</span></span>](#requirements)
-   [<span data-ttu-id="ca39b-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca39b-111">Related topics</span></span>](#related-topics)

## <a name="example-image"></a><span data-ttu-id="ca39b-112">Exemple d’image</span><span class="sxs-lookup"><span data-stu-id="ca39b-112">Example image</span></span>



| <span data-ttu-id="ca39b-113">Avant</span><span class="sxs-lookup"><span data-stu-id="ca39b-113">Before</span></span>                                                      |
|-------------------------------------------------------------|
| ![image avant l’effet.](images/default-before.jpg)  |
| <span data-ttu-id="ca39b-115">After</span><span class="sxs-lookup"><span data-stu-id="ca39b-115">After</span></span>                                                       |
| ![image après la transformation.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a><span data-ttu-id="ca39b-117">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="ca39b-117">Effect properties</span></span>



| <span data-ttu-id="ca39b-118">Nom complet de la propriété</span><span class="sxs-lookup"><span data-stu-id="ca39b-118">Property Display Name</span></span>                                                 | <span data-ttu-id="ca39b-119">Type et valeur par défaut</span><span class="sxs-lookup"><span data-stu-id="ca39b-119">Type and default value</span></span>                              | <span data-ttu-id="ca39b-120">Description</span><span class="sxs-lookup"><span data-stu-id="ca39b-120">Description</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca39b-121">WhitePoint</span><span class="sxs-lookup"><span data-stu-id="ca39b-121">WhitePoint</span></span><br/> <span data-ttu-id="ca39b-122">\_ \_ \_ Point blanc du prop \_ d2d1 de la luminosité</span><span class="sxs-lookup"><span data-stu-id="ca39b-122">D2D1\_BRIGHTNESS\_PROP\_WHITE\_POINT</span></span><br/> | <span data-ttu-id="ca39b-123">\_Vecteur d2d1 \_ 2F</span><span class="sxs-lookup"><span data-stu-id="ca39b-123">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="ca39b-124">{1.0 f, 1.0 f}</span><span class="sxs-lookup"><span data-stu-id="ca39b-124">{1.0f, 1.0f}</span></span><br/> | <span data-ttu-id="ca39b-125">Partie supérieure de la courbe de transfert de luminosité.</span><span class="sxs-lookup"><span data-stu-id="ca39b-125">The upper portion of the brightness transfer curve.</span></span> <span data-ttu-id="ca39b-126">Le point blanc ajuste l’apparence des parties plus claires de l’image.</span><span class="sxs-lookup"><span data-stu-id="ca39b-126">The white point adjusts the appearance of the brighter portions of the image.</span></span> <span data-ttu-id="ca39b-127">Cette propriété est pour la valeur x et la valeur y, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="ca39b-127">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="ca39b-128">Chacune des valeurs de cette propriété est comprise entre 0 et 1 inclus.</span><span class="sxs-lookup"><span data-stu-id="ca39b-128">Each of the values of this property are between 0 and 1, inclusive.</span></span> |
| <span data-ttu-id="ca39b-129">BlackPoint</span><span class="sxs-lookup"><span data-stu-id="ca39b-129">BlackPoint</span></span><br/> <span data-ttu-id="ca39b-130">\_ \_ \_ Point noir du prop \_ d2d1 de luminosité</span><span class="sxs-lookup"><span data-stu-id="ca39b-130">D2D1\_BRIGHTNESS\_PROP\_BLACK\_POINT</span></span><br/> | <span data-ttu-id="ca39b-131">\_Vecteur d2d1 \_ 2F</span><span class="sxs-lookup"><span data-stu-id="ca39b-131">D2D1\_VECTOR\_2F</span></span><br/> <span data-ttu-id="ca39b-132">{0.0 f, 0.0 f}</span><span class="sxs-lookup"><span data-stu-id="ca39b-132">{0.0f, 0.0f}</span></span><br/> | <span data-ttu-id="ca39b-133">La partie inférieure de la courbe de transfert de luminosité.</span><span class="sxs-lookup"><span data-stu-id="ca39b-133">The lower portion of the brightness transfer curve.</span></span> <span data-ttu-id="ca39b-134">Le point noir ajuste l’apparence des parties plus sombres de l’image.</span><span class="sxs-lookup"><span data-stu-id="ca39b-134">The black point adjusts the appearance of the darker portions of the image.</span></span> <span data-ttu-id="ca39b-135">Cette propriété est pour la valeur x et la valeur y, dans cet ordre.</span><span class="sxs-lookup"><span data-stu-id="ca39b-135">This property is for both the x value and the y value, in that order.</span></span> <span data-ttu-id="ca39b-136">Chacune des valeurs de cette propriété est comprise entre 0 et 1 inclus.</span><span class="sxs-lookup"><span data-stu-id="ca39b-136">Each of the values of this property are between 0 and 1, inclusive.</span></span>   |



 

<span data-ttu-id="ca39b-137">Cet effet utilise les points noir et blanc spécifiés pour générer une fonction de transfert utilisée pour ajuster l’image bitmap.</span><span class="sxs-lookup"><span data-stu-id="ca39b-137">This effect uses the specified white and black points to generate a transfer function used to adjust the bitmap.</span></span> <span data-ttu-id="ca39b-138">L’équation suivante décrit la fonction de transfert.</span><span class="sxs-lookup"><span data-stu-id="ca39b-138">The next equation describes the transfer function.</span></span> <span data-ttu-id="ca39b-139">Les intensités d’entrée sont définies entre 0 et 1.</span><span class="sxs-lookup"><span data-stu-id="ca39b-139">The input intensities are defined between 0 and 1.</span></span>

![algorithme de luminosité](images/brightness-formula1.png)

<span data-ttu-id="ca39b-141">L’algorithme Effect implémente une équation qui crée la fonction de transfert.</span><span class="sxs-lookup"><span data-stu-id="ca39b-141">The effect algorithm implements an equation that creates the transfer function.</span></span> <span data-ttu-id="ca39b-142">Nous utilisons cette fonction pour ajuster les pixels de l’image.</span><span class="sxs-lookup"><span data-stu-id="ca39b-142">We use this function to adjust the image pixels.</span></span> <span data-ttu-id="ca39b-143">Les valeurs x et y du point noir et du point blanc sont les coordonnées dans deux dimensions qui sont connectées pour former la transformation.</span><span class="sxs-lookup"><span data-stu-id="ca39b-143">The x and y values of the black point and the white point are the coordinates in two dimensions that are connected to form the transform.</span></span> <span data-ttu-id="ca39b-144">Chaque partie de l’équation de sortie finale :</span><span class="sxs-lookup"><span data-stu-id="ca39b-144">Each part of the final output equation:</span></span>

1.  <span data-ttu-id="ca39b-145">Convertit les données d’image de l’espace linéaire en espace non linéaire à l’aide de cette équation :</span><span class="sxs-lookup"><span data-stu-id="ca39b-145">Converts the image data from linear space to non-linear space using this equation:</span></span>![fonction d’assistance 1](images/brightness-formula2.png)

2.  <span data-ttu-id="ca39b-147">Ajuste l’image en fonction de ces valeurs :</span><span class="sxs-lookup"><span data-stu-id="ca39b-147">Adjusts the image according to these values:</span></span>
    -   <span data-ttu-id="ca39b-148">l' *entrée* correspond aux valeurs d’intensité en pixels de l’image d’entrée de 0 à 1.</span><span class="sxs-lookup"><span data-stu-id="ca39b-148">*input* is the input image pixel intensity values from 0 to 1.</span></span>

    -   <span data-ttu-id="ca39b-149">*PT blanc (x, y)* emplacement de la courbe de transformation pour des intensités de pixel plus claires.</span><span class="sxs-lookup"><span data-stu-id="ca39b-149">*White Pt. (x, y)* the location of the transform curve for brighter pixel intensities.</span></span>

    -   <span data-ttu-id="ca39b-150">Le *point noir (x, y)* est l’emplacement de la courbe de transformation pour les intensités de pixel DIMM.</span><span class="sxs-lookup"><span data-stu-id="ca39b-150">*Black Pt. (x, y)* is the location of the transform curve for dimmer pixel intensities.</span></span>

3.  <span data-ttu-id="ca39b-151">Reconvertit les données de l’image en espace linéaire à l’aide de cette équation :</span><span class="sxs-lookup"><span data-stu-id="ca39b-151">Converts the image data back to linear space using this equation:</span></span> ![fonction d’assistance 2](images/brightness-formula3.png)

<span data-ttu-id="ca39b-153">L’équation de sortie finale et les parties de composant sont indiquées ici.</span><span class="sxs-lookup"><span data-stu-id="ca39b-153">The final output equation and the component parts are shown here.</span></span>

![calculs complets pour l’ajustement de la luminosité](images/brightness-formula4.png)

## <a name="output-bitmap"></a><span data-ttu-id="ca39b-155">Bitmap de sortie</span><span class="sxs-lookup"><span data-stu-id="ca39b-155">Output bitmap</span></span>

<span data-ttu-id="ca39b-156">La taille de la bitmap de sortie est la même que la taille de la bitmap d’entrée.</span><span class="sxs-lookup"><span data-stu-id="ca39b-156">The output bitmap size is the same as the input bitmap size.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca39b-157">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ca39b-157">Requirements</span></span>



| <span data-ttu-id="ca39b-158">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ca39b-158">Requirement</span></span> | <span data-ttu-id="ca39b-159">Valeur</span><span class="sxs-lookup"><span data-stu-id="ca39b-159">Value</span></span> |
|--------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ca39b-160">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca39b-160">Minimum supported client</span></span> | <span data-ttu-id="ca39b-161">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ca39b-161">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ca39b-162">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ca39b-162">Minimum supported server</span></span> | <span data-ttu-id="ca39b-163">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="ca39b-163">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="ca39b-164">En-tête</span><span class="sxs-lookup"><span data-stu-id="ca39b-164">Header</span></span>                   | <span data-ttu-id="ca39b-165">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="ca39b-165">d2d1effects.h</span></span>                                                                      |
| <span data-ttu-id="ca39b-166">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ca39b-166">Library</span></span>                  | <span data-ttu-id="ca39b-167">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="ca39b-167">d2d1.lib, dxguid.lib</span></span>                                                               |



 

## <a name="related-topics"></a><span data-ttu-id="ca39b-168">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca39b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca39b-169">**ID2D1Effect**</span><span class="sxs-lookup"><span data-stu-id="ca39b-169">**ID2D1Effect**</span></span>](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

