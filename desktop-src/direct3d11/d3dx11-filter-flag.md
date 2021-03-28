---
title: Énumération D3DX11_FILTER_FLAG (D3DX11tex. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Indicateurs de filtrage de texture.'
ms.assetid: 083a6a19-1933-4831-9501-36d4867f3dce
keywords:
- Énumération D3DX11_FILTER_FLAG Direct3D 11
- Pointeur d’énumération LPD3DX11_FILTER_FLAG Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11_FILTER_FLAG
api_location:
- D3DX11tex.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f2105970efb7f2ec07464d8a902df49d8f75bc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982575"
---
# <a name="d3dx11_filter_flag-enumeration"></a><span data-ttu-id="c209f-106">\_Énumération de l’indicateur de filtre D3DX11 \_</span><span class="sxs-lookup"><span data-stu-id="c209f-106">D3DX11\_FILTER\_FLAG enumeration</span></span>

> [!Note]  
> <span data-ttu-id="c209f-107">La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.</span><span class="sxs-lookup"><span data-stu-id="c209f-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="c209f-108">Indicateurs de filtrage de texture.</span><span class="sxs-lookup"><span data-stu-id="c209f-108">Texture filtering flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="c209f-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c209f-109">Syntax</span></span>


```C++
typedef enum D3DX11_FILTER_FLAG { 
  D3DX11_FILTER_NONE              = (1 << 0),
  D3DX11_FILTER_POINT             = (2 << 0),
  D3DX11_FILTER_LINEAR            = (3 << 0),
  D3DX11_FILTER_TRIANGLE          = (4 << 0),
  D3DX11_FILTER_BOX               = (5 << 0),
  D3DX11_FILTER_MIRROR_U          = (1 << 16),
  D3DX11_FILTER_MIRROR_V          = (2 << 16),
  D3DX11_FILTER_MIRROR_W          = (4 << 16),
  D3DX11_FILTER_MIRROR            = (7 << 16),
  D3DX11_FILTER_DITHER            = (1 << 19),
  D3DX11_FILTER_DITHER_DIFFUSION  = (2 << 19),
  D3DX11_FILTER_SRGB_IN           = (1 << 21),
  D3DX11_FILTER_SRGB_OUT          = (2 << 21),
  D3DX11_FILTER_SRGB              = (3 << 21)
} D3DX11_FILTER_FLAG, *LPD3DX11_FILTER_FLAG;
```



## <a name="constants"></a><span data-ttu-id="c209f-110">Constantes</span><span class="sxs-lookup"><span data-stu-id="c209f-110">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c209f-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**\_Filtre D3DX11 \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="c209f-111"><span id="D3DX11_FILTER_NONE"></span><span id="d3dx11_filter_none"></span>**D3DX11\_FILTER\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-112">Aucune mise à l’échelle ou aucun filtrage n’aura lieu.</span><span class="sxs-lookup"><span data-stu-id="c209f-112">No scaling or filtering will take place.</span></span> <span data-ttu-id="c209f-113">Les pixels en dehors des limites de l’image source sont supposés être en noir transparent.</span><span class="sxs-lookup"><span data-stu-id="c209f-113">Pixels outside the bounds of the source image are assumed to be transparent black.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**\_Point de filtre D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="c209f-114"><span id="D3DX11_FILTER_POINT"></span><span id="d3dx11_filter_point"></span>**D3DX11\_FILTER\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-115">Chaque pixel de destination est calculé en échantillonnant le pixel le plus proche de l’image source.</span><span class="sxs-lookup"><span data-stu-id="c209f-115">Each destination pixel is computed by sampling the nearest pixel from the source image.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**\_Filtre \_ linéaire D3DX11**</span><span class="sxs-lookup"><span data-stu-id="c209f-116"><span id="D3DX11_FILTER_LINEAR"></span><span id="d3dx11_filter_linear"></span>**D3DX11\_FILTER\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-117">Chaque pixel de destination est calculé en échantillonnant les quatre pixels les plus proches de l’image source.</span><span class="sxs-lookup"><span data-stu-id="c209f-117">Each destination pixel is computed by sampling the four nearest pixels from the source image.</span></span> <span data-ttu-id="c209f-118">Ce filtre fonctionne mieux lorsque la mise à l’échelle sur les deux axes est inférieure à deux.</span><span class="sxs-lookup"><span data-stu-id="c209f-118">This filter works best when the scale on both axes is less than two.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**\_Triangle de filtre D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="c209f-119"><span id="D3DX11_FILTER_TRIANGLE"></span><span id="d3dx11_filter_triangle"></span>**D3DX11\_FILTER\_TRIANGLE**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-120">Chaque pixel de l’image source contribue de manière égale à l’image de destination.</span><span class="sxs-lookup"><span data-stu-id="c209f-120">Every pixel in the source image contributes equally to the destination image.</span></span> <span data-ttu-id="c209f-121">Il s’agit de la plus lente des filtres.</span><span class="sxs-lookup"><span data-stu-id="c209f-121">This is the slowest of the filters.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**\_Zone de filtre D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="c209f-122"><span id="D3DX11_FILTER_BOX"></span><span id="d3dx11_filter_box"></span>**D3DX11\_FILTER\_BOX**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-123">Chaque pixel est calculé en calculant la moyenne d’une zone de pixels 2x2 (x2) à partir de l’image source.</span><span class="sxs-lookup"><span data-stu-id="c209f-123">Each pixel is computed by averaging a 2x2(x2) box of pixels from the source image.</span></span> <span data-ttu-id="c209f-124">Ce filtre fonctionne uniquement lorsque les dimensions de la destination sont la moitié de la source, comme c’est le cas avec des mipmaps.</span><span class="sxs-lookup"><span data-stu-id="c209f-124">This filter works only when the dimensions of the destination are half those of the source, as is the case with mipmaps.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**\_Miroir de filtre D3DX11 \_ \_ U**</span><span class="sxs-lookup"><span data-stu-id="c209f-125"><span id="D3DX11_FILTER_MIRROR_U"></span><span id="d3dx11_filter_mirror_u"></span>**D3DX11\_FILTER\_MIRROR\_U**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-126">Les pixels du bord de la texture sur l’axe u doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="c209f-126">Pixels off the edge of the texture on the u-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**\_Miroir de filtre D3DX11 \_ \_ V**</span><span class="sxs-lookup"><span data-stu-id="c209f-127"><span id="D3DX11_FILTER_MIRROR_V"></span><span id="d3dx11_filter_mirror_v"></span>**D3DX11\_FILTER\_MIRROR\_V**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-128">Les pixels du bord de la texture sur l’axe v doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="c209f-128">Pixels off the edge of the texture on the v-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**\_Miroir de filtre D3DX11 \_ \_ W**</span><span class="sxs-lookup"><span data-stu-id="c209f-129"><span id="D3DX11_FILTER_MIRROR_W"></span><span id="d3dx11_filter_mirror_w"></span>**D3DX11\_FILTER\_MIRROR\_W**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-130">Les pixels du bord de la texture sur l’axe des w doivent être mis en miroir, et non encapsulés.</span><span class="sxs-lookup"><span data-stu-id="c209f-130">Pixels off the edge of the texture on the w-axis should be mirrored, not wrapped.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**\_Miroir de filtre D3DX11 \_**</span><span class="sxs-lookup"><span data-stu-id="c209f-131"><span id="D3DX11_FILTER_MIRROR"></span><span id="d3dx11_filter_mirror"></span>**D3DX11\_FILTER\_MIRROR**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-132">La spécification de cet indicateur revient à spécifier les \_ indicateurs de filtre D3DX en miroir \_ \_ U, D3DX \_ Filter \_ miroir \_ V et D3DX \_ Filter- \_ MIRROR \_ W.</span><span class="sxs-lookup"><span data-stu-id="c209f-132">Specifying this flag is the same as specifying the D3DX\_FILTER\_MIRROR\_U, D3DX\_FILTER\_MIRROR\_V, and D3DX\_FILTER\_MIRROR\_W flags.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**\_Filtre D3DX11 \_ tramé**</span><span class="sxs-lookup"><span data-stu-id="c209f-133"><span id="D3DX11_FILTER_DITHER"></span><span id="d3dx11_filter_dither"></span>**D3DX11\_FILTER\_DITHER**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-134">L’image résultante doit être tramée à l’aide d’un algorithme de trame trié 4x4.</span><span class="sxs-lookup"><span data-stu-id="c209f-134">The resulting image must be dithered using a 4x4 ordered dither algorithm.</span></span> <span data-ttu-id="c209f-135">Cela se produit lors de la conversion d’un format vers un autre.</span><span class="sxs-lookup"><span data-stu-id="c209f-135">This happens when converting from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11 \_ filtre de \_ diffusion en trame \_**</span><span class="sxs-lookup"><span data-stu-id="c209f-136"><span id="D3DX11_FILTER_DITHER_DIFFUSION"></span><span id="d3dx11_filter_dither_diffusion"></span>**D3DX11\_FILTER\_DITHER\_DIFFUSION**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-137">Effectuez un tramage diffus sur l’image lors du passage d’un format à un autre.</span><span class="sxs-lookup"><span data-stu-id="c209f-137">Do diffuse dithering on the image when changing from one format to another.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11 \_ filtre \_ sRVB \_ dans**</span><span class="sxs-lookup"><span data-stu-id="c209f-138"><span id="D3DX11_FILTER_SRGB_IN"></span><span id="d3dx11_filter_srgb_in"></span>**D3DX11\_FILTER\_SRGB\_IN**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-139">Les données d’entrée se trouvent dans l’espace de couleurs RVB standard (sRVB).</span><span class="sxs-lookup"><span data-stu-id="c209f-139">Input data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="c209f-140">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="c209f-140">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11 \_ filtre \_ en \_ grisé**</span><span class="sxs-lookup"><span data-stu-id="c209f-141"><span id="D3DX11_FILTER_SRGB_OUT"></span><span id="d3dx11_filter_srgb_out"></span>**D3DX11\_FILTER\_SRGB\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-142">Les données de sortie sont dans l’espace de couleurs RVB standard (sRVB).</span><span class="sxs-lookup"><span data-stu-id="c209f-142">Output data is in standard RGB (sRGB) color space.</span></span> <span data-ttu-id="c209f-143">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="c209f-143">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c209f-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11 \_ filtre \_ sRVB**</span><span class="sxs-lookup"><span data-stu-id="c209f-144"><span id="D3DX11_FILTER_SRGB"></span><span id="d3dx11_filter_srgb"></span>**D3DX11\_FILTER\_SRGB**</span></span>
</dt> <dd>

<span data-ttu-id="c209f-145">Identique à la spécification \_ de la fonction de filtre D3DX \_ sRVB \_ dans le \| \_ filtre D3DX \_ \_ out.</span><span class="sxs-lookup"><span data-stu-id="c209f-145">Same as specifying D3DX\_FILTER\_SRGB\_IN \| D3DX\_FILTER\_SRGB\_OUT.</span></span> <span data-ttu-id="c209f-146">Consultez la section Remarques.</span><span class="sxs-lookup"><span data-stu-id="c209f-146">See remarks.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c209f-147">Notes</span><span class="sxs-lookup"><span data-stu-id="c209f-147">Remarks</span></span>

<span data-ttu-id="c209f-148">D3DX11 effectue automatiquement une correction gamma (pour convertir les données de couleur de l’espace RVB en espace RVB standard) lors du chargement des données de texture.</span><span class="sxs-lookup"><span data-stu-id="c209f-148">D3DX11 automatically performs gamma correction (to convert color data from RGB space to standard RGB space) when loading texture data.</span></span> <span data-ttu-id="c209f-149">Cette opération est effectuée automatiquement par exemple lorsque les données RVB sont chargées à partir d’un fichier. png dans une texture sRVB.</span><span class="sxs-lookup"><span data-stu-id="c209f-149">This is automatically done for instance when RGB data is loaded from a .png file into an sRGB texture.</span></span> <span data-ttu-id="c209f-150">Utilisez les indicateurs de filtre sRVB pour indiquer si les données n’ont pas besoin d’être converties en espace sRVB.</span><span class="sxs-lookup"><span data-stu-id="c209f-150">Use the SRGB filter flags to indicate if the data does not need to be converted into sRGB space.</span></span>

## <a name="requirements"></a><span data-ttu-id="c209f-151">Spécifications</span><span class="sxs-lookup"><span data-stu-id="c209f-151">Requirements</span></span>



| <span data-ttu-id="c209f-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c209f-152">Requirement</span></span> | <span data-ttu-id="c209f-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="c209f-153">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c209f-154">En-tête</span><span class="sxs-lookup"><span data-stu-id="c209f-154">Header</span></span><br/> | <dl> <span data-ttu-id="c209f-155"><dt>D3DX11tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="c209f-155"><dt>D3DX11tex.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c209f-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c209f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c209f-157">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="c209f-157">D3DX Enumerations</span></span>](d3d11-graphics-reference-d3dx11-enums.md)
</dt> </dl>

 

 





