---
description: Les indicateurs suivants sont utilisés pour spécifier les canaux à utiliser dans une texture.
ms.assetid: 0317b857-2512-4ad7-b6e3-82afdda7ea10
title: D3DX_FILTER
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6e1ab3ab51a73277da685b7ac562e84d1b94a9
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997326"
---
# <a name="d3dx_filter"></a><span data-ttu-id="f6f53-103">\_Filtre D3DX</span><span class="sxs-lookup"><span data-stu-id="f6f53-103">D3DX\_FILTER</span></span>

<span data-ttu-id="f6f53-104">Les indicateurs suivants sont utilisés pour spécifier les canaux à utiliser dans une texture.</span><span class="sxs-lookup"><span data-stu-id="f6f53-104">The following flags are used to specify which channels in a texture to operate on.</span></span>



| <span data-ttu-id="f6f53-105">\#définition</span><span class="sxs-lookup"><span data-stu-id="f6f53-105">\#define</span></span>                | <span data-ttu-id="f6f53-106">Description</span><span class="sxs-lookup"><span data-stu-id="f6f53-106">Description</span></span>                                                                                                                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6f53-107">Filtre D3DX, \_ \_ aucun</span><span class="sxs-lookup"><span data-stu-id="f6f53-107">D3DX\_FILTER\_NONE</span></span>      | <span data-ttu-id="f6f53-108">Aucune mise à l’échelle ou aucun filtrage n’aura lieu.</span><span class="sxs-lookup"><span data-stu-id="f6f53-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="f6f53-109">Les pixels en dehors des limites de l’image source sont supposés être en noir transparent.</span><span class="sxs-lookup"><span data-stu-id="f6f53-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>                                                                                 |
| <span data-ttu-id="f6f53-110">\_Point de filtre D3DX \_</span><span class="sxs-lookup"><span data-stu-id="f6f53-110">D3DX\_FILTER\_POINT</span></span>     | <span data-ttu-id="f6f53-111">Chaque pixel de destination est calculé en échantillonnant le pixel le plus proche de l’image source.</span><span class="sxs-lookup"><span data-stu-id="f6f53-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>                                                                                                                     |
| <span data-ttu-id="f6f53-112">D3DX- \_ filtre \_ linéaire</span><span class="sxs-lookup"><span data-stu-id="f6f53-112">D3DX\_FILTER\_LINEAR</span></span>    | <span data-ttu-id="f6f53-113">Chaque pixel de destination est calculé en échantillonnant les quatre pixels les plus proches de l’image source.</span><span class="sxs-lookup"><span data-stu-id="f6f53-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="f6f53-114">Ce filtre fonctionne mieux lorsque la mise à l’échelle sur les deux axes est inférieure à deux.</span><span class="sxs-lookup"><span data-stu-id="f6f53-114">This filter works best when the scale on both axes is less than two.</span></span>                                          |
| <span data-ttu-id="f6f53-115">\_Triangle de filtre D3DX \_</span><span class="sxs-lookup"><span data-stu-id="f6f53-115">D3DX\_FILTER\_TRIANGLE</span></span>  | <span data-ttu-id="f6f53-116">Chaque pixel de l’image source contribue de manière égale à l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="f6f53-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="f6f53-117">Il s’agit de la plus lente des filtres.</span><span class="sxs-lookup"><span data-stu-id="f6f53-117">This is the slowest of the filters.</span></span>                                                                                           |
| <span data-ttu-id="f6f53-118">\_Zone de filtre D3DX \_</span><span class="sxs-lookup"><span data-stu-id="f6f53-118">D3DX\_FILTER\_BOX</span></span>       | <span data-ttu-id="f6f53-119">Chaque pixel est calculé en calculant la moyenne d’une zone de pixels 2x2 (x2) à partir de l’image source.</span><span class="sxs-lookup"><span data-stu-id="f6f53-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="f6f53-120">Ce filtre fonctionne uniquement lorsque les dimensions de la destination sont la moitié de la source, comme c’est le cas avec des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="f6f53-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span> |
| <span data-ttu-id="f6f53-121">D3DX \_ Filtrer \_ en miroir \_ U</span><span class="sxs-lookup"><span data-stu-id="f6f53-121">D3DX\_FILTER\_MIRROR\_U</span></span> | <span data-ttu-id="f6f53-122">Les pixels du bord de la texture sur l’axe u doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="f6f53-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="f6f53-123">Filtre D3DX- \_ \_ miroir \_ V</span><span class="sxs-lookup"><span data-stu-id="f6f53-123">D3DX\_FILTER\_MIRROR\_V</span></span> | <span data-ttu-id="f6f53-124">Les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="f6f53-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="f6f53-125">\_ \_ Mise en miroir du filtre D3DX \_ W</span><span class="sxs-lookup"><span data-stu-id="f6f53-125">D3DX\_FILTER\_MIRROR\_W</span></span> | <span data-ttu-id="f6f53-126">Les pixels du bord de la texture sur l’axe des w doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="f6f53-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>                                                                                                                           |
| <span data-ttu-id="f6f53-127">\_ \_ Mise en miroir du filtre D3DX</span><span class="sxs-lookup"><span data-stu-id="f6f53-127">D3DX\_FILTER\_MIRROR</span></span>    | <span data-ttu-id="f6f53-128">La spécification de cet indicateur revient à spécifier les \_ indicateurs de filtre D3DX en miroir \_ \_ U, D3DX \_ Filter \_ miroir \_ V et D3DX \_ Filter- \_ MIRROR \_ W.</span><span class="sxs-lookup"><span data-stu-id="f6f53-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>                                                                     |
| <span data-ttu-id="f6f53-129">Filtre D3DX, \_ \_ trame</span><span class="sxs-lookup"><span data-stu-id="f6f53-129">D3DX\_FILTER\_DITHER</span></span>    | <span data-ttu-id="f6f53-130">L’image résultante doit être tramée à l’aide d’un algorithme de trame trié 4x4.</span><span class="sxs-lookup"><span data-stu-id="f6f53-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span>                                                                                                                                  |
| <span data-ttu-id="f6f53-131">\_Filtre \_ de D3DX sRVB \_ dans</span><span class="sxs-lookup"><span data-stu-id="f6f53-131">D3DX\_FILTER\_SRGB\_IN</span></span>  | <span data-ttu-id="f6f53-132">Les données d’entrée se trouvent dans l’espace de couleurs sRGB (gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="f6f53-132">Input data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                              |
| <span data-ttu-id="f6f53-133">Filtre de D3DX en \_ \_ \_ sortie</span><span class="sxs-lookup"><span data-stu-id="f6f53-133">D3DX\_FILTER\_SRGB\_OUT</span></span> | <span data-ttu-id="f6f53-134">Les données de sortie se trouvent dans l’espace de couleurs sRGB (gamma 2,2).</span><span class="sxs-lookup"><span data-stu-id="f6f53-134">The output data is in sRGB (gamma 2.2) color space.</span></span>                                                                                                                                                         |
| <span data-ttu-id="f6f53-135">Filtre de D3DX \_ \_ sRVB</span><span class="sxs-lookup"><span data-stu-id="f6f53-135">D3DX\_FILTER\_SRGB</span></span>      | <span data-ttu-id="f6f53-136">Identique à la spécification \_ de la fonction de filtre D3DX \_ sRVB \_ dans le \| \_ filtre D3DX \_ \_ out.</span><span class="sxs-lookup"><span data-stu-id="f6f53-136">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span>                                                                                                                                       |



 

<span data-ttu-id="f6f53-137">Chaque filtre valide doit contenir exactement l’un des indicateurs suivants : D3DX \_ filtre \_ None, D3DX \_ Filter \_ point, D3DX \_ Filter \_ Linear, D3DX \_ Filter \_ triangle ou D3DX \_ Filter \_ Box.</span><span class="sxs-lookup"><span data-stu-id="f6f53-137">Each valid filter must contain exactly one of the following flags: D3DX\_FILTER\_NONE, D3DX\_FILTER\_POINT, D3DX\_FILTER\_LINEAR, D3DX\_FILTER\_TRIANGLE, or D3DX\_FILTER\_BOX.</span></span> <span data-ttu-id="f6f53-138">En outre, vous pouvez utiliser l’opérateur OR pour spécifier zéro, un ou plusieurs des indicateurs facultatifs suivants avec un filtre valide : D3DX \_ Filter \_ miroir \_ U, D3DX \_ Filter \_ MIRROR \_ V, D3DX \_ filtre \_ MIRROR \_ avec, D3DX Filter \_ \_ miroir, D3DX \_ Filter \_ juxtaposition, D3DX \_ Filter \_ sRVB \_ in, D3DX \_ Filter sRVB \_ \_ out ou D3DX \_ Filter \_ sRGB.</span><span class="sxs-lookup"><span data-stu-id="f6f53-138">In addition, you can use the OR operator to specify zero or more of the following optional flags with a valid filter: D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, D3DX\_FILTER\_MIRROR\_W, D3DX\_FILTER\_MIRROR, D3DX\_FILTER\_DITHER, D3DX\_FILTER\_SRGB\_IN, D3DX\_FILTER\_SRGB\_OUT or D3DX\_FILTER\_SRGB.</span></span>

<span data-ttu-id="f6f53-139">La spécification de \_ la valeur D3DX par défaut pour ce paramètre est généralement l’équivalent de la spécification de la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f6f53-139">Specifying D3DX\_DEFAULT for this parameter is usually the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span> <span data-ttu-id="f6f53-140">Toutefois, D3DX \_ default peut avoir différentes significations, en fonction de la méthode qui utilise le filtre.</span><span class="sxs-lookup"><span data-stu-id="f6f53-140">However, D3DX\_DEFAULT can have different meanings, depending on which method uses the filter.</span></span> <span data-ttu-id="f6f53-141">Par exemple :</span><span class="sxs-lookup"><span data-stu-id="f6f53-141">For example:</span></span>

-   <span data-ttu-id="f6f53-142">Quand vous utilisez [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), la \_ valeur par défaut de D3DX est mappée au triangle de filtre D3DX de filtre \_ \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f6f53-142">When using [**D3DXCreateTextureFromFileEx**](d3dxcreatetexturefromfileex.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>
-   <span data-ttu-id="f6f53-143">Quand vous utilisez [**D3DXFilterTexture**](d3dxfiltertexture.md), \_ la valeur par défaut de D3DX est mappée à \_ la zone de filtre D3DX \_ si la taille de la texture est une puissance de deux et le filtre de la zone de filtre D3DX dans le \_ \_ \| \_ \_ cas contraire.</span><span class="sxs-lookup"><span data-stu-id="f6f53-143">When using [**D3DXFilterTexture**](d3dxfiltertexture.md), D3DX\_DEFAULT maps to D3DX\_FILTER\_BOX if the texture size is a power of two, and D3DX\_FILTER\_BOX \| D3DX\_FILTER\_DITHER otherwise.</span></span>

<span data-ttu-id="f6f53-144">Référencez chaque méthode pour rechercher des informations sur la façon dont le \_ filtre par défaut D3DX est mappé.</span><span class="sxs-lookup"><span data-stu-id="f6f53-144">Reference each method to check for information about how D3DX\_DEFAULT filter is mapped.</span></span>

## <a name="constant-information"></a><span data-ttu-id="f6f53-145">Informations constantes</span><span class="sxs-lookup"><span data-stu-id="f6f53-145">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f6f53-146">En-tête</span><span class="sxs-lookup"><span data-stu-id="f6f53-146">Header</span></span>                   | <span data-ttu-id="f6f53-147">d3dx9tex. h</span><span class="sxs-lookup"><span data-stu-id="f6f53-147">d3dx9tex.h</span></span> |
| <span data-ttu-id="f6f53-148">Système d’exploitation minimal</span><span class="sxs-lookup"><span data-stu-id="f6f53-148">Minimum operating system</span></span> | <span data-ttu-id="f6f53-149">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f6f53-149">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f6f53-150">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6f53-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6f53-151">Constantes D3DX</span><span class="sxs-lookup"><span data-stu-id="f6f53-151">D3DX Constants</span></span>](dx9-graphics-reference-d3dx-constants.md)
</dt> </dl>

 

 



