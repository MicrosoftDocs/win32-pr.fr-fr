---
title: Effet de gestion des couleurs
description: Utilisez l’effet gestion des couleurs pour transformer une image d’un profil de couleurs ICC (International Color Consortium) en un autre. L’effet transforme l’image en fonction de la spécification ICC.
ms.assetid: 7351C4B4-F289-4236-BB42-1B3BD8753248
keywords:
- effet de gestion des couleurs
ms.topic: article
ms.date: 02/05/2019
ms.openlocfilehash: 5f3783132e0e2af511a99fd8c44d5f899e577a3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384499"
---
# <a name="color-management-effect"></a><span data-ttu-id="b2c27-105">Effet de gestion des couleurs</span><span class="sxs-lookup"><span data-stu-id="b2c27-105">Color management effect</span></span>

<span data-ttu-id="b2c27-106">Utilisez l’effet gestion des couleurs pour transformer une image d’un profil de couleurs ICC (International Color Consortium) en un autre.</span><span class="sxs-lookup"><span data-stu-id="b2c27-106">Use the color management effect to transform an image from one ICC (International Color Consortium) color profile to another.</span></span> <span data-ttu-id="b2c27-107">L’effet transforme l’image en fonction de la [spécification ICC](https://www.color.org).</span><span class="sxs-lookup"><span data-stu-id="b2c27-107">The effect transforms the image according to the [ICC specification](https://www.color.org).</span></span>

<span data-ttu-id="b2c27-108">Le CLSID de cet effet est CLSID \_ D2D1ColorManagement.</span><span class="sxs-lookup"><span data-stu-id="b2c27-108">The CLSID for this effect is CLSID\_D2D1ColorManagement.</span></span>

- [<span data-ttu-id="b2c27-109">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b2c27-109">Effect properties</span></span>](#effect-properties)
- [<span data-ttu-id="b2c27-110">Modes d’intention de rendu</span><span class="sxs-lookup"><span data-stu-id="b2c27-110">Rendering intent modes</span></span>](#rendering-intent-modes)
- [<span data-ttu-id="b2c27-111">Images d’entrée en mode Alpha</span><span class="sxs-lookup"><span data-stu-id="b2c27-111">Input image alpha modes</span></span>](#input-image-alpha-modes)
- [<span data-ttu-id="b2c27-112">Conformité avec la spécification ICC</span><span class="sxs-lookup"><span data-stu-id="b2c27-112">Compliance with ICC specification</span></span>](#compliance-with-icc-specification)
- [<span data-ttu-id="b2c27-113">Comportement du canal alpha</span><span class="sxs-lookup"><span data-stu-id="b2c27-113">Alpha channel behavior</span></span>](#alpha-channel-behavior)
- [<span data-ttu-id="b2c27-114">Modes de qualité</span><span class="sxs-lookup"><span data-stu-id="b2c27-114">Quality modes</span></span>](#quality-modes)
- [<span data-ttu-id="b2c27-115">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b2c27-115">Sample code</span></span>](#sample-code)
- [<span data-ttu-id="b2c27-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2c27-116">Requirements</span></span>](#requirements)
- [<span data-ttu-id="b2c27-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2c27-117">Related topics</span></span>](#related-topics)

## <a name="effect-properties"></a><span data-ttu-id="b2c27-118">Propriétés d’effet</span><span class="sxs-lookup"><span data-stu-id="b2c27-118">Effect properties</span></span>

| <span data-ttu-id="b2c27-119">Nom complet et énumération d’index</span><span class="sxs-lookup"><span data-stu-id="b2c27-119">Display name and index enumeration</span></span> | <span data-ttu-id="b2c27-120">Description</span><span class="sxs-lookup"><span data-stu-id="b2c27-120">Description</span></span> |
|-|-|
| <span data-ttu-id="b2c27-121">SourceContext</span><span class="sxs-lookup"><span data-stu-id="b2c27-121">SourceContext</span></span><br/> <span data-ttu-id="b2c27-122">\_Contexte de \_ \_ couleur source \_ d2d1 COLORMANAGEMENT prop \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-122">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="b2c27-123">Informations sur l’espace colorimétrique source.</span><span class="sxs-lookup"><span data-stu-id="b2c27-123">The source color space information.</span></span> <span data-ttu-id="b2c27-124">Le type est [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="b2c27-124">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="b2c27-125">La valeur par défaut est NULL.</span><span class="sxs-lookup"><span data-stu-id="b2c27-125">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="b2c27-126">SourceIntent</span><span class="sxs-lookup"><span data-stu-id="b2c27-126">SourceIntent</span></span><br/> <span data-ttu-id="b2c27-127">\_Intention de \_ \_ rendu source \_ d2d1 COLORMANAGEMENT prop \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-127">D2D1\_COLORMANAGEMENT\_PROP\_SOURCE\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="b2c27-128">L’intention de rendu ICC à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b2c27-128">Which ICC rendering intent to use.</span></span> <span data-ttu-id="b2c27-129">Le type est D2D1 \_ COLORMANAGEMENT \_ rendu \_ intentionnel.</span><span class="sxs-lookup"><span data-stu-id="b2c27-129">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="b2c27-130">La valeur par défaut est D2D1 \_ COLORMANAGEMENT de \_ rendu \_ Intent \_ .</span><span class="sxs-lookup"><span data-stu-id="b2c27-130">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="b2c27-131">DestinationContext</span><span class="sxs-lookup"><span data-stu-id="b2c27-131">DestinationContext</span></span><br/> <span data-ttu-id="b2c27-132">Contexte de la \_ couleur de destination d2d1 COLORMANAGEMENT \_ prop \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-132">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_COLOR\_CONTEXT</span></span><br/> | <span data-ttu-id="b2c27-133">Informations sur l’espace colorimétrique de destination.</span><span class="sxs-lookup"><span data-stu-id="b2c27-133">The destination color space information.</span></span> <span data-ttu-id="b2c27-134">Le type est [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span><span class="sxs-lookup"><span data-stu-id="b2c27-134">The type is [**ID2D1ColorContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1colorcontext).</span></span><br/> <span data-ttu-id="b2c27-135">La valeur par défaut est NULL.</span><span class="sxs-lookup"><span data-stu-id="b2c27-135">The default value is NULL.</span></span><br/> |
| <span data-ttu-id="b2c27-136">DestinationIntent</span><span class="sxs-lookup"><span data-stu-id="b2c27-136">DestinationIntent</span></span><br/> <span data-ttu-id="b2c27-137">\_Intention de \_ \_ rendu de destination d2d1 COLORMANAGEMENT prop \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-137">D2D1\_COLORMANAGEMENT\_PROP\_DESTINATION\_RENDERING\_INTENT</span></span><br/> | <span data-ttu-id="b2c27-138">L’intention de rendu ICC à utiliser.</span><span class="sxs-lookup"><span data-stu-id="b2c27-138">Which ICC rendering intent to use.</span></span> <span data-ttu-id="b2c27-139">Le type est D2D1 \_ COLORMANAGEMENT \_ rendu \_ intentionnel.</span><span class="sxs-lookup"><span data-stu-id="b2c27-139">The type is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT.</span></span><br/> <span data-ttu-id="b2c27-140">La valeur par défaut est D2D1 \_ COLORMANAGEMENT de \_ rendu \_ Intent \_ .</span><span class="sxs-lookup"><span data-stu-id="b2c27-140">The default value is D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL.</span></span><br/> |
| <span data-ttu-id="b2c27-141">AlphaMode</span><span class="sxs-lookup"><span data-stu-id="b2c27-141">AlphaMode</span></span><br/> <span data-ttu-id="b2c27-142">\_ \_ \_ Mode Alpha d2d1 COLORMANAGEMENT \_ prop</span><span class="sxs-lookup"><span data-stu-id="b2c27-142">D2D1\_COLORMANAGEMENT\_PROP\_ALPHA\_MODE</span></span><br/> | <span data-ttu-id="b2c27-143">Comment interpréter les données alpha contenues dans l’image d’entrée.</span><span class="sxs-lookup"><span data-stu-id="b2c27-143">How to interpret alpha data that is contained in the input image.</span></span> <span data-ttu-id="b2c27-144">Le type est D2D1 \_ COLORMANAGEMENT \_ alpha \_ mode.</span><span class="sxs-lookup"><span data-stu-id="b2c27-144">The type is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE.</span></span><br/> <span data-ttu-id="b2c27-145">La valeur par défaut est \_ d2d1 \_ COLORMANAGEMENT \_ en mode Alpha \_ prémultiplié.</span><span class="sxs-lookup"><span data-stu-id="b2c27-145">The default value is D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED.</span></span><br/> |
| <span data-ttu-id="b2c27-146">Qualité</span><span class="sxs-lookup"><span data-stu-id="b2c27-146">Quality</span></span><br/> <span data-ttu-id="b2c27-147">\_Qualité d2d1 COLORMANAGEMENT \_ prop \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-147">D2D1\_COLORMANAGEMENT\_PROP\_QUALITY</span></span><br/> | <span data-ttu-id="b2c27-148">Niveau de qualité de la transformation.</span><span class="sxs-lookup"><span data-stu-id="b2c27-148">The quality level of the transform.</span></span> <span data-ttu-id="b2c27-149">Le type est D2D1 \_ COLORMANAGEMENT \_ Quality.</span><span class="sxs-lookup"><span data-stu-id="b2c27-149">The type is D2D1\_COLORMANAGEMENT\_QUALITY.</span></span><br/> <span data-ttu-id="b2c27-150">La valeur par défaut est D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal.</span><span class="sxs-lookup"><span data-stu-id="b2c27-150">The default value is D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL.</span></span><br/> |

## <a name="rendering-intent-modes"></a><span data-ttu-id="b2c27-151">Modes d’intention de rendu</span><span class="sxs-lookup"><span data-stu-id="b2c27-151">Rendering intent modes</span></span>

| <span data-ttu-id="b2c27-152">Énumération</span><span class="sxs-lookup"><span data-stu-id="b2c27-152">Enumeration</span></span> | <span data-ttu-id="b2c27-153">Description</span><span class="sxs-lookup"><span data-stu-id="b2c27-153">Description</span></span> |
|-|-|
| <span data-ttu-id="b2c27-154">Perception de l’intention de rendu D2D1 \_ COLORMANAGEMENT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-154">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_PERCEPTUAL</span></span> | <span data-ttu-id="b2c27-155">L’effet compresse ou développe la gamme complète des couleurs de l’image pour remplir la gamme des couleurs de l’appareil, afin que la balance grise soit préservée mais que la précision colorimétrique ne puisse pas être préservée.</span><span class="sxs-lookup"><span data-stu-id="b2c27-155">The effect compresses or expands the full color gamut of the image to fill the color gamut of the device, so that gray balance is preserved but colorimetric accuracy may not be preserved.</span></span> |
| <span data-ttu-id="b2c27-156">\_ \_ \_ \_ \_ Colorimétrie relative à l’intention de rendu d2d1 COLORMANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="b2c27-156">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_RELATIVE\_COLORIMETRIC</span></span> | <span data-ttu-id="b2c27-157">L’effet préserve la chrominance des couleurs de l’image au détriment de la teinte et de la luminosité.</span><span class="sxs-lookup"><span data-stu-id="b2c27-157">The effect preserves the chroma of colors in the image at the possible expense of hue and lightness.</span></span> |
| <span data-ttu-id="b2c27-158">SATURATION de l’intention de rendu D2D1 \_ COLORMANAGEMENT \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-158">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_SATURATION</span></span> | <span data-ttu-id="b2c27-159">L’effet ajuste les couleurs qui se trouvent en dehors de la plage de couleurs que le périphérique de sortie affiche sur la couleur la plus proche disponible.</span><span class="sxs-lookup"><span data-stu-id="b2c27-159">The effect adjusts colors that fall outside the range of colors the output device renders to the closest color available.</span></span> <span data-ttu-id="b2c27-160">Elle ne conserve pas le point blanc.</span><span class="sxs-lookup"><span data-stu-id="b2c27-160">It does not preserve the white point.</span></span> |
| <span data-ttu-id="b2c27-161">\_ \_ \_ \_ COLORIMÉTRIE absolue de rendu d2d1 \_ COLORMANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="b2c27-161">D2D1\_COLORMANAGEMENT\_RENDERING\_INTENT\_ABSOLUTE\_COLORIMETRIC</span></span> | <span data-ttu-id="b2c27-162">L’effet ajuste toutes les couleurs qui se trouvent en dehors de la plage que le périphérique de sortie peut afficher sur la couleur la plus proche qui peut être rendue.</span><span class="sxs-lookup"><span data-stu-id="b2c27-162">The effect adjusts any colors that fall outside the range that the output device can render to the closest color that can be rendered.</span></span> <span data-ttu-id="b2c27-163">L’effet ne change pas les autres couleurs et conserve le point blanc.</span><span class="sxs-lookup"><span data-stu-id="b2c27-163">The effect does not change the other colors and preserves the white point.</span></span> |

## <a name="input-image-alpha-modes"></a><span data-ttu-id="b2c27-164">Images d’entrée en mode Alpha</span><span class="sxs-lookup"><span data-stu-id="b2c27-164">Input image alpha modes</span></span>

| <span data-ttu-id="b2c27-165">Énumération</span><span class="sxs-lookup"><span data-stu-id="b2c27-165">Enumeration</span></span> | <span data-ttu-id="b2c27-166">Description</span><span class="sxs-lookup"><span data-stu-id="b2c27-166">Description</span></span> |
|-|-|
| <span data-ttu-id="b2c27-167">D2D1 \_ COLORMANAGEMENT \_ \_ en mode Alpha \_ prémultiplié</span><span class="sxs-lookup"><span data-stu-id="b2c27-167">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_PREMULTIPLIED</span></span> | <span data-ttu-id="b2c27-168">L’effet suppose que le mode Alpha est prémultiplié.</span><span class="sxs-lookup"><span data-stu-id="b2c27-168">The effect assumes the alpha mode is premultiplied.</span></span> |
| <span data-ttu-id="b2c27-169">\_Mode d2d1 \_ COLORMANAGEMENT \_ alpha \_ simple</span><span class="sxs-lookup"><span data-stu-id="b2c27-169">D2D1\_COLORMANAGEMENT\_ALPHA\_MODE\_STRAIGHT</span></span> | <span data-ttu-id="b2c27-170">L’effet suppose que le mode Alpha est droit.</span><span class="sxs-lookup"><span data-stu-id="b2c27-170">The effect assumes the alpha mode is straight.</span></span> |

## <a name="d2d1_gamma1_g2084-behavior-changes"></a><span data-ttu-id="b2c27-171">D2D1_GAMMA1_G2084 les changements de comportement</span><span class="sxs-lookup"><span data-stu-id="b2c27-171">D2D1_GAMMA1_G2084 behavior changes</span></span>
    
<span data-ttu-id="b2c27-172">Si votre application utilise l’espace de [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) , ou l’une des valeurs d’énumération [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) qui utilisent l’espace de couleurs SMPTE St. 084 (perception du quantificateur), l’application envisage d’utiliser les données HDR.</span><span class="sxs-lookup"><span data-stu-id="b2c27-172">If your application uses the [D2D1_GAMMA1_G2084](/windows/desktop/api/d2d1_3/ne-d2d1_3-d2d1_gamma1) space, or one of the [DXGI_COLOR_SPACE_TYPE](/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type) enumeration values that use the SMPTE ST.2084 (Perceptual Quantizer) color space, then the application intends to work with HDR data.</span></span>

<span data-ttu-id="b2c27-173">Les API [**ID2D1DeviceContext5 :: CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) et [**ID2D1DeviceContext5 :: CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) ne sont pas en compte pour cela ; au lieu de cela, le contenu HDR est mis à l’échelle pour s’ajuster à la plage 0-1 au cours de l’opération G2084 Degamma.</span><span class="sxs-lookup"><span data-stu-id="b2c27-173">The [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile__id2d1colorcontext1)) and [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace) APIs don't account for that; rather, the HDR content is scaled to fit in the 0-1 range during the G2084 DeGamma operation.</span></span>

<span data-ttu-id="b2c27-174">Dans la pratique, le contenu encodé dans cet espace gamma utilise un WhiteLevel de référence de 10 000 nits, qui serait normalement représenté dans CCCS en tant que 10 000/80 = 125,0.</span><span class="sxs-lookup"><span data-stu-id="b2c27-174">In practice, content that is encoded in this gamma space uses a reference WhiteLevel of 10,000 Nits, which would normally be represented in CCCS as 10,000 / 80 = 125.0.</span></span> <span data-ttu-id="b2c27-175">Ainsi, pour mieux faciliter votre application, il est plus simple pour cette conversion gamma de faire évoluer également la luminance d’un facteur de 125.</span><span class="sxs-lookup"><span data-stu-id="b2c27-175">So, to better facilitate your app, it's simplest for this gamma conversion to also scale the luminance by a factor of 125.</span></span> <span data-ttu-id="b2c27-176">À partir de Windows 10, version 1809 (10,0 ; Build 17763), le comportement de l’effet de gestion des couleurs est tel qu’il applique cette mise à l’échelle.</span><span class="sxs-lookup"><span data-stu-id="b2c27-176">As of Windows 10, version 1809 (10.0; Build 17763), the behavior of the color management effect is such that it applies this scaling.</span></span> <span data-ttu-id="b2c27-177">Cela signifie que vous, en tant que développeur, n’avez pas besoin d’appliquer un deuxième [effet de réglage de niveau blanc](white-level-adjustment-effect.md) dans le pipeline.</span><span class="sxs-lookup"><span data-stu-id="b2c27-177">That means that you, as the developer, don't have to apply a second [White level adjustment effect](white-level-adjustment-effect.md) into the pipeline.</span></span>

## <a name="compliance-with-icc-specification"></a><span data-ttu-id="b2c27-178">Conformité avec la spécification ICC</span><span class="sxs-lookup"><span data-stu-id="b2c27-178">Compliance with ICC specification</span></span>

<span data-ttu-id="b2c27-179">L’effet de gestion des couleurs est conforme à la spécification ICC v 4.3, avec les limitations suivantes :</span><span class="sxs-lookup"><span data-stu-id="b2c27-179">The color management effect is compliant with the ICC v4.3 specification, with these limitations:</span></span>

- <span data-ttu-id="b2c27-180">L’effet prend en charge les espaces colorimétriques 1, 3 et 4 canaux.</span><span class="sxs-lookup"><span data-stu-id="b2c27-180">The effect supports 1, 3, and 4 channel color spaces.</span></span>
- <span data-ttu-id="b2c27-181">L’effet ne prend pas en charge les profils de couleurs ColorSpace ou nommés.</span><span class="sxs-lookup"><span data-stu-id="b2c27-181">The effect doesn't support ColorSpace or Named Color profiles.</span></span>

## <a name="alpha-channel-behavior"></a><span data-ttu-id="b2c27-182">Comportement du canal alpha</span><span class="sxs-lookup"><span data-stu-id="b2c27-182">Alpha channel behavior</span></span>

<span data-ttu-id="b2c27-183">En général, l’effet définit alpha sur 1 (opaque) s’il n’y a aucune donnée alpha dans l’image source et les données alpha sont ignorées si l’image de destination ne contient aucune place.</span><span class="sxs-lookup"><span data-stu-id="b2c27-183">In general, the effect sets alpha to 1 (opaque) if there is no alpha data in the source image and the alpha data is discarded if there is no room in the destination image.</span></span> <span data-ttu-id="b2c27-184">Le tableau ci-dessous décrit le comportement alpha.</span><span class="sxs-lookup"><span data-stu-id="b2c27-184">The table here describes the alpha behavior.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b2c27-185">Colorspace source, format de pixel</span><span class="sxs-lookup"><span data-stu-id="b2c27-185">Source colorspace, pixel format</span></span></th>
<th><span data-ttu-id="b2c27-186">Colorspace de destination, format de pixel</span><span class="sxs-lookup"><span data-stu-id="b2c27-186">Destination colorspace, pixel format</span></span></th>
<th><span data-ttu-id="b2c27-187">Comportement alpha</span><span class="sxs-lookup"><span data-stu-id="b2c27-187">Alpha behavior</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="b2c27-188">1 canal, format de pixel R $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2c27-188">1 channel, R pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2c27-189">1 canal, format de pixel R</span><span class="sxs-lookup"><span data-stu-id="b2c27-189">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="b2c27-190">(Aucune donnée alpha)</span><span class="sxs-lookup"><span data-stu-id="b2c27-190">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-191">1 canal, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-191">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-192">Les données alpha sont définies sur 1 (opaque)</span><span class="sxs-lookup"><span data-stu-id="b2c27-192">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b2c27-193">3 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-193">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-194">Les données alpha sont définies sur 1 (opaque)</span><span class="sxs-lookup"><span data-stu-id="b2c27-194">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-195">4 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-195">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-196">(Aucune donnée alpha)</span><span class="sxs-lookup"><span data-stu-id="b2c27-196">(No alpha data)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="b2c27-197">1 canal, format de pixel RVBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2c27-197">1 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2c27-198">1 canal, format de pixel R</span><span class="sxs-lookup"><span data-stu-id="b2c27-198">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="b2c27-199">Les données alpha sont ignorées</span><span class="sxs-lookup"><span data-stu-id="b2c27-199">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-200">1 canal, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-200">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-201">Les données alpha sont transmises</span><span class="sxs-lookup"><span data-stu-id="b2c27-201">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b2c27-202">3 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-202">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-203">Les données alpha sont transmises</span><span class="sxs-lookup"><span data-stu-id="b2c27-203">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-204">4 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-204">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-205">Les données alpha sont ignorées</span><span class="sxs-lookup"><span data-stu-id="b2c27-205">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="b2c27-206">3 canaux, format de pixel RVBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2c27-206">3 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2c27-207">1 canal, format de pixel R</span><span class="sxs-lookup"><span data-stu-id="b2c27-207">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="b2c27-208">Les données alpha sont ignorées</span><span class="sxs-lookup"><span data-stu-id="b2c27-208">Alpha data is discarded</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-209">1 canal, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-209">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-210">Les données alpha sont transmises</span><span class="sxs-lookup"><span data-stu-id="b2c27-210">Alpha data is passed through</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b2c27-211">3 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-211">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-212">Les données alpha sont transmises</span><span class="sxs-lookup"><span data-stu-id="b2c27-212">Alpha data is passed through</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-213">4 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-213">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-214">Les données alpha sont ignorées</span><span class="sxs-lookup"><span data-stu-id="b2c27-214">Alpha data is discarded</span></span></td>

</tr>
<tr class="odd">
<td rowspan="4"><span data-ttu-id="b2c27-215">4 canaux, format de pixel RVBA $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="b2c27-215">4 channel, RGBA pixel format ${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="b2c27-216">1 canal, format de pixel R</span><span class="sxs-lookup"><span data-stu-id="b2c27-216">1 channel, R pixel format</span></span></td>
<td><span data-ttu-id="b2c27-217">(Aucune donnée alpha)</span><span class="sxs-lookup"><span data-stu-id="b2c27-217">(No alpha data)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-218">1 canal, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-218">1 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-219">Les données alpha sont définies sur 1 (opaque)</span><span class="sxs-lookup"><span data-stu-id="b2c27-219">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="b2c27-220">3 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-220">3 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-221">Les données alpha sont définies sur 1 (opaque)</span><span class="sxs-lookup"><span data-stu-id="b2c27-221">Alpha data is set to 1 (opaque)</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="b2c27-222">4 canaux, format de pixel RVBA</span><span class="sxs-lookup"><span data-stu-id="b2c27-222">4 channel, RGBA pixel format</span></span></td>
<td><span data-ttu-id="b2c27-223">(Aucune donnée alpha)</span><span class="sxs-lookup"><span data-stu-id="b2c27-223">(No alpha data)</span></span></td>

</tr>
</tbody>
</table>

## <a name="quality-modes"></a><span data-ttu-id="b2c27-224">Modes de qualité</span><span class="sxs-lookup"><span data-stu-id="b2c27-224">Quality modes</span></span>

| <span data-ttu-id="b2c27-225">Mode</span><span class="sxs-lookup"><span data-stu-id="b2c27-225">Mode</span></span> | <span data-ttu-id="b2c27-226">Description</span><span class="sxs-lookup"><span data-stu-id="b2c27-226">Description</span></span> |
|-|-|
| <span data-ttu-id="b2c27-227">\_Preuve de \_ qualité d2d1 COLORMANAGEMENT \_</span><span class="sxs-lookup"><span data-stu-id="b2c27-227">D2D1\_COLORMANAGEMENT\_QUALITY\_PROOF</span></span> | <span data-ttu-id="b2c27-228">Mode de qualité le plus bas.</span><span class="sxs-lookup"><span data-stu-id="b2c27-228">The lowest quality mode.</span></span> <span data-ttu-id="b2c27-229">Ce mode nécessite le niveau de fonctionnalité 9 \_ 1 ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="b2c27-229">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="b2c27-230">D2D1 \_ COLORMANAGEMENT \_ Quality \_ normal</span><span class="sxs-lookup"><span data-stu-id="b2c27-230">D2D1\_COLORMANAGEMENT\_QUALITY\_NORMAL</span></span> | <span data-ttu-id="b2c27-231">Mode de qualité normal.</span><span class="sxs-lookup"><span data-stu-id="b2c27-231">Normal quality mode.</span></span> <span data-ttu-id="b2c27-232">Ce mode nécessite le niveau de fonctionnalité 9 \_ 1 ou supérieur.</span><span class="sxs-lookup"><span data-stu-id="b2c27-232">This mode requires feature level 9\_1 or above.</span></span> |
| <span data-ttu-id="b2c27-233">\_ \_ Meilleure qualité d2d1 \_ COLORMANAGEMENT</span><span class="sxs-lookup"><span data-stu-id="b2c27-233">D2D1\_COLORMANAGEMENT\_QUALITY\_BEST</span></span> | <span data-ttu-id="b2c27-234">Mode de qualité optimal.</span><span class="sxs-lookup"><span data-stu-id="b2c27-234">The best quality mode.</span></span> <span data-ttu-id="b2c27-235">Ce mode requiert le niveau de fonctionnalité 10 \_ 0 ou supérieur, ainsi que les mémoires tampons de précision à virgule flottante.</span><span class="sxs-lookup"><span data-stu-id="b2c27-235">This mode requires feature level 10\_0 or above, as well as floating point precision buffers.</span></span> <span data-ttu-id="b2c27-236">Ce mode prend en charge la précision à virgule flottante, ainsi que la plage étendue, comme défini dans la spécification ICC v 4.3.</span><span class="sxs-lookup"><span data-stu-id="b2c27-236">This mode supports floating point precision as well as extended range as defined in the ICC v4.3 specification.</span></span> |

<span data-ttu-id="b2c27-237">L’effet de gestion des couleurs échoue lors du dessin si l’application demande un mode de qualité qui n’est pas pris en charge par le matériel.</span><span class="sxs-lookup"><span data-stu-id="b2c27-237">The color management effect fails when drawing if the application requests a quality mode that is not supported by the hardware.</span></span> <span data-ttu-id="b2c27-238">Vous pouvez déterminer le niveau de fonctionnalité quand vous appelez [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span><span class="sxs-lookup"><span data-stu-id="b2c27-238">You can determine the feature level when you call [**D3D11CreateDevice**](/windows/desktop/api/d3d11/nf-d3d11-d3d11createdevice).</span></span> <span data-ttu-id="b2c27-239">Vous pouvez vérifier la prise en charge de la mémoire tampon à virgule flottante en appelant [**ID2D1EffectContext :: IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) avec la valeur d2d1 de précision de la [**\_ mémoire tampon \_ \_ 32BPC \_ float**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span><span class="sxs-lookup"><span data-stu-id="b2c27-239">You can check for floating point buffer support by calling [**ID2D1EffectContext::IsBufferPrecisionSupported**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-isbufferprecisionsupported) with the value [**D2D1\_BUFFER\_PRECISION\_32BPC\_FLOAT**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_buffer_precision).</span></span>

## <a name="sample-code"></a><span data-ttu-id="b2c27-240">Exemple de code</span><span class="sxs-lookup"><span data-stu-id="b2c27-240">Sample code</span></span>

<span data-ttu-id="b2c27-241">Pour obtenir un exemple de cet effet, téléchargez l' [exemple ajustement des photos des effets Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)et consultez la leçon 4 de l’exemple.</span><span class="sxs-lookup"><span data-stu-id="b2c27-241">For an example of this effect, download the [Direct2D effects photo adjustment sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment), and see Lesson 4 of the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c27-242">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2c27-242">Requirements</span></span>

| <span data-ttu-id="b2c27-243">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2c27-243">Requirement</span></span> | <span data-ttu-id="b2c27-244">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2c27-244">Value</span></span> |
|-|-|
| <span data-ttu-id="b2c27-245">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2c27-245">Minimum supported client</span></span> | <span data-ttu-id="b2c27-246">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b2c27-246">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b2c27-247">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2c27-247">Minimum supported server</span></span> | <span data-ttu-id="b2c27-248">Windows 8 et mise à jour de plate-forme pour les applications de bureau Windows 7 \[ \| applications du Windows Store\]</span><span class="sxs-lookup"><span data-stu-id="b2c27-248">Windows 8 and Platform Update for Windows 7 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="b2c27-249">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2c27-249">Header</span></span> | <span data-ttu-id="b2c27-250">d2d1effects. h</span><span class="sxs-lookup"><span data-stu-id="b2c27-250">d2d1effects.h</span></span> |
| <span data-ttu-id="b2c27-251">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="b2c27-251">Library</span></span> | <span data-ttu-id="b2c27-252">d2d1. lib, dxguid. lib</span><span class="sxs-lookup"><span data-stu-id="b2c27-252">d2d1.lib, dxguid.lib</span></span> |

## <a name="related-topics"></a><span data-ttu-id="b2c27-253">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b2c27-253">Related topics</span></span>

* [<span data-ttu-id="b2c27-254">Interface ID2D1Effect</span><span class="sxs-lookup"><span data-stu-id="b2c27-254">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
