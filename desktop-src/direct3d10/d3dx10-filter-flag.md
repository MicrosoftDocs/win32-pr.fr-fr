---
description: Indicateurs de filtrage de texture.
ms.assetid: bc73d916-fe18-4b15-b507-7954e157ab9a
title: Énumération D3DX10_FILTER_FLAG (D3DX10Tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_FILTER_FLAG
api_type:
- HeaderDef
api_location:
- D3DX10Tex.h
ms.openlocfilehash: f12842cd07c55c33509ecfbb56fc804a6fc3b7c0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953976"
---
# <a name="d3dx10_filter_flag-enumeration"></a><span data-ttu-id="92051-103">\_Énumération de l’indicateur de filtre d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="92051-103">D3DX10\_FILTER\_FLAG enumeration</span></span>

<span data-ttu-id="92051-104">Indicateurs de filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="92051-104">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="92051-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="92051-105">Syntax</span></span>


```C++
typedef enum D3DX10_FILTER_FLAG { 
  D3DX10_FILTER_NONE              = (1 << 0),
  D3DX10_FILTER_POINT             = (2 << 0),
  D3DX10_FILTER_LINEAR            = (3 << 0),
  D3DX10_FILTER_TRIANGLE          = (4 << 0),
  D3DX10_FILTER_BOX               = (5 << 0),
  D3DX10_FILTER_MIRROR_U          = (1 << 16),
  D3DX10_FILTER_MIRROR_V          = (2 << 16),
  D3DX10_FILTER_MIRROR_W          = (4 << 16),
  D3DX10_FILTER_MIRROR            = (7 << 16),
  D3DX10_FILTER_DITHER            = (1 << 19),
  D3DX10_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX10_FILTER_SRGB_IN           = (1 << 21),
  D3DX10_FILTER_SRGB_OUT          = (2 << 21),
  D3DX10_FILTER_SRGB              = (3 << 21)
} D3DX10_FILTER_FLAG, *LPD3DX10_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="92051-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="92051-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="92051-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**\_Filtre d3dx10 \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="92051-107"><span id="D3DX10_FILTER_NONE"></span><span id="d3dx10_filter_none"></span>**D3DX10\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="92051-108">Aucune mise à l’échelle ou aucun filtrage n’aura lieu.</span><span class="sxs-lookup"><span data-stu-id="92051-108">No scaling or filtering will take place.</span></span> <span data-ttu-id="92051-109">Les pixels en dehors des limites de l’image source sont supposés être en noir transparent.</span><span class="sxs-lookup"><span data-stu-id="92051-109">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="92051-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**\_Point de filtre d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="92051-110"><span id="D3DX10_FILTER_POINT"></span><span id="d3dx10_filter_point"></span>**D3DX10\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="92051-111">Chaque pixel de destination est calculé en échantillonnant le pixel le plus proche de l’image source.</span><span class="sxs-lookup"><span data-stu-id="92051-111">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="92051-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**\_Filtre \_ linéaire d3dx10**</span><span class="sxs-lookup"><span data-stu-id="92051-112"><span id="D3DX10_FILTER_LINEAR"></span><span id="d3dx10_filter_linear"></span>**D3DX10\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="92051-113">Chaque pixel de destination est calculé en échantillonnant les quatre pixels les plus proches de l’image source.</span><span class="sxs-lookup"><span data-stu-id="92051-113">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="92051-114">Ce filtre fonctionne mieux lorsque la mise à l’échelle sur les deux axes est inférieure à deux.</span><span class="sxs-lookup"><span data-stu-id="92051-114">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="92051-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**\_Triangle de filtre d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="92051-115"><span id="D3DX10_FILTER_TRIANGLE"></span><span id="d3dx10_filter_triangle"></span>**D3DX10\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="92051-116">Chaque pixel de l’image source contribue de manière égale à l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="92051-116">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="92051-117">Il s’agit de la plus lente des filtres.</span><span class="sxs-lookup"><span data-stu-id="92051-117">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="92051-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**\_Zone de filtre d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="92051-118"><span id="D3DX10_FILTER_BOX"></span><span id="d3dx10_filter_box"></span>**D3DX10\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="92051-119">Chaque pixel est calculé en calculant la moyenne d’une zone de pixels 2x2 (x2) à partir de l’image source.</span><span class="sxs-lookup"><span data-stu-id="92051-119">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="92051-120">Ce filtre fonctionne uniquement lorsque les dimensions de la destination sont la moitié de la source, comme c’est le cas avec des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="92051-120">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="92051-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**\_Miroir de filtre d3dx10 \_ \_ U**</span><span class="sxs-lookup"><span data-stu-id="92051-121"><span id="D3DX10_FILTER_MIRROR_U"></span><span id="d3dx10_filter_mirror_u"></span>**D3DX10\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="92051-122">Les pixels du bord de la texture sur l’axe u doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="92051-122">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="92051-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**\_Miroir de filtre d3dx10 \_ \_ V**</span><span class="sxs-lookup"><span data-stu-id="92051-123"><span id="D3DX10_FILTER_MIRROR_V"></span><span id="d3dx10_filter_mirror_v"></span>**D3DX10\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="92051-124">Les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="92051-124">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="92051-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**\_Miroir de filtre d3dx10 \_ \_ W**</span><span class="sxs-lookup"><span data-stu-id="92051-125"><span id="D3DX10_FILTER_MIRROR_W"></span><span id="d3dx10_filter_mirror_w"></span>**D3DX10\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="92051-126">Les pixels du bord de la texture sur l’axe des w doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="92051-126">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="92051-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**\_Miroir de filtre d3dx10 \_**</span><span class="sxs-lookup"><span data-stu-id="92051-127"><span id="D3DX10_FILTER_MIRROR"></span><span id="d3dx10_filter_mirror"></span>**D3DX10\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="92051-128">La spécification de cet indicateur revient à spécifier les \_ indicateurs de filtre D3DX en miroir \_ \_ U, D3DX \_ Filter \_ miroir \_ V et D3DX \_ Filter- \_ MIRROR \_ W.</span><span class="sxs-lookup"><span data-stu-id="92051-128">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="92051-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**\_Filtre d3dx10 \_ tramé**</span><span class="sxs-lookup"><span data-stu-id="92051-129"><span id="D3DX10_FILTER_DITHER"></span><span id="d3dx10_filter_dither"></span>**D3DX10\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="92051-130">L’image résultante doit être tramée à l’aide d’un algorithme de trame trié 4x4.</span><span class="sxs-lookup"><span data-stu-id="92051-130">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="92051-131">Cela se produit lors de la conversion d’un format vers un autre.</span><span class="sxs-lookup"><span data-stu-id="92051-131">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="92051-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10 \_ filtre de \_ diffusion en trame \_**</span><span class="sxs-lookup"><span data-stu-id="92051-132"><span id="D3DX10_FILTER_DITHER_DIFFUSION"></span><span id="d3dx10_filter_dither_diffusion"></span>**D3DX10\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="92051-133">Effectuez un tramage diffus sur l’image lors du passage d’un format à un autre.</span><span class="sxs-lookup"><span data-stu-id="92051-133">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="92051-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10 \_ filtre \_ sRVB \_ dans**</span><span class="sxs-lookup"><span data-stu-id="92051-134"><span id="D3DX10_FILTER_SRGB_IN"></span><span id="d3dx10_filter_srgb_in"></span>**D3DX10\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="92051-135">Les données d’entrée se trouvent dans l’espace de couleurs RVB standard (sRVB).</span><span class="sxs-lookup"><span data-stu-id="92051-135">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="92051-136">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="92051-136">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="92051-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10 \_ filtre \_ en \_ grisé**</span><span class="sxs-lookup"><span data-stu-id="92051-137"><span id="D3DX10_FILTER_SRGB_OUT"></span><span id="d3dx10_filter_srgb_out"></span>**D3DX10\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="92051-138">Les données de sortie sont dans l’espace de couleurs RVB standard (sRVB).</span><span class="sxs-lookup"><span data-stu-id="92051-138">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="92051-139">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="92051-139">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="92051-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10 \_ filtre \_ sRVB**</span><span class="sxs-lookup"><span data-stu-id="92051-140"><span id="D3DX10_FILTER_SRGB"></span><span id="d3dx10_filter_srgb"></span>**D3DX10\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="92051-141">Identique à la spécification \_ de la fonction de filtre D3DX \_ sRVB \_ dans le \| \_ filtre D3DX \_ \_ out.</span><span class="sxs-lookup"><span data-stu-id="92051-141">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="92051-142">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="92051-142">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="92051-143">Notes</span><span class="sxs-lookup"><span data-stu-id="92051-143">Remarks</span></span>

<span data-ttu-id="92051-144">D3DX10 effectue automatiquement une correction gamma (pour convertir les données de couleur de l’espace RVB en espace RVB standard) lors du chargement des données de texture.</span><span class="sxs-lookup"><span data-stu-id="92051-144">D3DX10 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="92051-145">Cette opération est effectuée automatiquement par exemple lorsque les données RVB sont chargées à partir d’un fichier. png dans une texture sRVB.</span><span class="sxs-lookup"><span data-stu-id="92051-145">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="92051-146">Utilisez les indicateurs de filtre sRVB pour indiquer si les données n’ont pas besoin d’être converties en espace sRVB.</span><span class="sxs-lookup"><span data-stu-id="92051-146">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="92051-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="92051-147">Requirements</span></span>



| <span data-ttu-id="92051-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="92051-148">Requirement</span></span> | <span data-ttu-id="92051-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="92051-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="92051-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="92051-150">Header</span></span><br/> | <dl> <span data-ttu-id="92051-151"><dt>D3DX10Tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="92051-151"><dt>D3DX10Tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92051-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="92051-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92051-153">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="92051-153">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




