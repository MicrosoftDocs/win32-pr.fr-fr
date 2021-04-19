---
description: Définit les modes de filtrage de texture pour une étape de texture.
ms.assetid: 4e0420fa-ac76-4be4-90d7-944d8d5a5de1
title: Énumération D3DTEXTUREFILTERTYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREFILTERTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 212fd05755ebf554c3c57e7ac45dcf8947f2d753
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522341"
---
# <a name="d3dtexturefiltertype-enumeration"></a><span data-ttu-id="dd099-103">Énumération D3DTEXTUREFILTERTYPE</span><span class="sxs-lookup"><span data-stu-id="dd099-103">D3DTEXTUREFILTERTYPE enumeration</span></span>

<span data-ttu-id="dd099-104">Définit les modes de filtrage de texture pour une étape de texture.</span><span class="sxs-lookup"><span data-stu-id="dd099-104">Defines texture filtering modes for a texture stage.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd099-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dd099-105">Syntax</span></span>


```C++
typedef enum D3DTEXTUREFILTERTYPE { 
  D3DTEXF_NONE             = 0,
  D3DTEXF_POINT            = 1,
  D3DTEXF_LINEAR           = 2,
  D3DTEXF_ANISOTROPIC      = 3,
  D3DTEXF_PYRAMIDALQUAD    = 6,
  D3DTEXF_GAUSSIANQUAD     = 7,
  D3DTEXF_CONVOLUTIONMONO  = 8,
  D3DTEXF_FORCE_DWORD      = 0x7fffffff
} D3DTEXTUREFILTERTYPE, *LPD3DTEXTUREFILTERTYPE;
```



## <a name="constants"></a><span data-ttu-id="dd099-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="dd099-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dd099-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF \_ aucun**</span><span class="sxs-lookup"><span data-stu-id="dd099-107"><span id="D3DTEXF_NONE"></span><span id="d3dtexf_none"></span>**D3DTEXF\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-108">En cas d’utilisation avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md), désactive mappage MIP.</span><span class="sxs-lookup"><span data-stu-id="dd099-108">When used with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md), disables mipmapping.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**\_Point D3DTEXF**</span><span class="sxs-lookup"><span data-stu-id="dd099-109"><span id="D3DTEXF_POINT"></span><span id="d3dtexf_point"></span>**D3DTEXF\_POINT**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-110">Lorsqu’il est utilisé avec [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), spécifie que le filtrage de point doit être utilisé comme facteur d’agrandissement ou de réduction de la texture, respectivement.</span><span class="sxs-lookup"><span data-stu-id="dd099-110">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that point filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="dd099-111">En cas d’utilisation avec **D3DSAMP \_ MIPFILTER**, active mappage MIP et spécifie que le rastériseur choisit la couleur à partir de la texture du niveau MIP le plus proche.</span><span class="sxs-lookup"><span data-stu-id="dd099-111">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and specifies that the rasterizer chooses the color from the texel of the nearest mip level.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF \_ linéaire**</span><span class="sxs-lookup"><span data-stu-id="dd099-112"><span id="D3DTEXF_LINEAR"></span><span id="d3dtexf_linear"></span>**D3DTEXF\_LINEAR**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-113">Lorsqu’il est utilisé avec [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), spécifie que le filtrage linéaire doit être utilisé en tant que facteur d’agrandissement de texture ou de filtre de réduction, respectivement.</span><span class="sxs-lookup"><span data-stu-id="dd099-113">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that linear filtering is to be used as the texture magnification or minification filter respectively.</span></span> <span data-ttu-id="dd099-114">En cas d’utilisation avec **D3DSAMP \_ MIPFILTER**, active le filtrage mappage MIP et trilinéaire ; il spécifie que le rastériseur interpole entre les deux niveaux les plus proches.</span><span class="sxs-lookup"><span data-stu-id="dd099-114">When used with **D3DSAMP\_MIPFILTER**, enables mipmapping and trilinear filtering; it specifies that the rasterizer interpolates between the two nearest mip levels.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF \_ anisotrope**</span><span class="sxs-lookup"><span data-stu-id="dd099-115"><span id="D3DTEXF_ANISOTROPIC"></span><span id="d3dtexf_anisotropic"></span>**D3DTEXF\_ANISOTROPIC**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-116">Lorsqu’il est utilisé avec [**D3DSAMP \_ MAGFILTER**](./d3dsamplerstatetype.md) ou [**D3DSAMP \_ MINFILTER**](./d3dsamplerstatetype.md), spécifie que le filtrage de texture anisotrope est utilisé respectivement comme un facteur d’agrandissement de texture ou de réduction.</span><span class="sxs-lookup"><span data-stu-id="dd099-116">When used with [**D3DSAMP\_ MAGFILTER**](./d3dsamplerstatetype.md) or [**D3DSAMP\_MINFILTER**](./d3dsamplerstatetype.md), specifies that anisotropic texture filtering used as a texture magnification or minification filter respectively.</span></span> <span data-ttu-id="dd099-117">Compense la distorsion causée par la différence d’angle entre le polygone de texture et le plan de l’écran.</span><span class="sxs-lookup"><span data-stu-id="dd099-117">Compensates for distortion caused by the difference in angle between the texture polygon and the plane of the screen.</span></span> <span data-ttu-id="dd099-118">L’utilisation de avec **D3DSAMP \_ MIPFILTER** n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="dd099-118">Use with **D3DSAMP\_MIPFILTER** is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF \_ PYRAMIDALQUAD**</span><span class="sxs-lookup"><span data-stu-id="dd099-119"><span id="D3DTEXF_PYRAMIDALQUAD"></span><span id="d3dtexf_pyramidalquad"></span>**D3DTEXF\_PYRAMIDALQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-120">Filtre chevalet à 4 échantillons utilisé comme un zoom de texture ou un filtre de réduction.</span><span class="sxs-lookup"><span data-stu-id="dd099-120">A 4-sample tent filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="dd099-121">L’utilisation de avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="dd099-121">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF \_ GAUSSIANQUAD**</span><span class="sxs-lookup"><span data-stu-id="dd099-122"><span id="D3DTEXF_GAUSSIANQUAD"></span><span id="d3dtexf_gaussianquad"></span>**D3DTEXF\_GAUSSIANQUAD**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-123">Filtre gaussien à 4 échantillons utilisé comme un agrandissement de texture ou un filtre de réduction.</span><span class="sxs-lookup"><span data-stu-id="dd099-123">A 4-sample Gaussian filter used as a texture magnification or minification filter.</span></span> <span data-ttu-id="dd099-124">L’utilisation de avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="dd099-124">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF \_ CONVOLUTIONMONO**</span><span class="sxs-lookup"><span data-stu-id="dd099-125"><span id="D3DTEXF_CONVOLUTIONMONO"></span><span id="d3dtexf_convolutionmono"></span>**D3DTEXF\_CONVOLUTIONMONO**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-126">Filtre de convolution pour les textures monochromes.</span><span class="sxs-lookup"><span data-stu-id="dd099-126">Convolution filter for monochrome textures.</span></span> <span data-ttu-id="dd099-127">Consultez [D3DFMT \_ a1](d3dformat.md).</span><span class="sxs-lookup"><span data-stu-id="dd099-127">See [D3DFMT\_A1](d3dformat.md).</span></span>



|                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd099-128">Différences entre Direct3D 9 et Direct3D 9Ex :</span><span class="sxs-lookup"><span data-stu-id="dd099-128">Differences between Direct3D 9 and Direct3D 9Ex:</span></span><br/> <span data-ttu-id="dd099-129">Cet indicateur est disponible uniquement dans Direct3D 9Ex.</span><span class="sxs-lookup"><span data-stu-id="dd099-129">This flag is available in Direct3D 9Ex only.</span></span><br/> |



 

<span data-ttu-id="dd099-130">L’utilisation de avec [**D3DSAMP \_ MIPFILTER**](./d3dsamplerstatetype.md) n’est pas définie.</span><span class="sxs-lookup"><span data-stu-id="dd099-130">Use with [**D3DSAMP\_MIPFILTER**](./d3dsamplerstatetype.md) is undefined.</span></span>

</dd> <dt>

<span data-ttu-id="dd099-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF \_ forcer \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="dd099-131"><span id="D3DTEXF_FORCE_DWORD"></span><span id="d3dtexf_force_dword"></span>**D3DTEXF\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="dd099-132">Force cette énumération à se compiler à 32 bits de taille.</span><span class="sxs-lookup"><span data-stu-id="dd099-132">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="dd099-133">Sans cette valeur, certains compilateurs permettent à cette énumération de compiler à une taille autre que 32 bits.</span><span class="sxs-lookup"><span data-stu-id="dd099-133">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="dd099-134">Cette valeur n'est pas utilisée.</span><span class="sxs-lookup"><span data-stu-id="dd099-134">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dd099-135">Notes</span><span class="sxs-lookup"><span data-stu-id="dd099-135">Remarks</span></span>

<span data-ttu-id="dd099-136">D3DTEXTUREFILTERTYPE est utilisé par [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) pour définir les modes de filtrage de texture pour une étape de texture.</span><span class="sxs-lookup"><span data-stu-id="dd099-136">D3DTEXTUREFILTERTYPE is used by [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) along with [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md) to define texture filtering modes for a texture stage.</span></span>

<span data-ttu-id="dd099-137">Pour vérifier si un format prend en charge d’autres types de filtre de texture que \_ le point de D3DTEXF (qui est toujours pris en charge), appelez [**IDirect3D9 :: CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) avec le \_ filtre de requête D3DUSAGE \_ .</span><span class="sxs-lookup"><span data-stu-id="dd099-137">To check if a format supports texture filter types other than D3DTEXF\_POINT (which is always supported), call [**IDirect3D9::CheckDeviceFormat**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdeviceformat) with D3DUSAGE\_QUERY\_FILTER.</span></span>

<span data-ttu-id="dd099-138">Définissez le filtre d’agrandissement d’une étape de texture en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec la \_ valeur MAGFILTER D3DSAMP comme deuxième paramètre et un membre de cette énumération comme troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd099-138">Set a texture stage's magnification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MAGFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="dd099-139">Définissez le filtre de réduction d’une étape de texture en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec la \_ valeur MINFILTER D3DSAMP comme deuxième paramètre et un membre de cette énumération comme troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd099-139">Set a texture stage's minification filter by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MINFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="dd099-140">Définissez le filtre de texture à utiliser entre les niveaux de mipmap en appelant [**IDirect3DDevice9 :: SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) avec la \_ valeur MIPFILTER D3DSAMP comme deuxième paramètre et un membre de cette énumération comme troisième paramètre.</span><span class="sxs-lookup"><span data-stu-id="dd099-140">Set the texture filter to use between-mipmap levels by calling [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) with the D3DSAMP\_MIPFILTER value as the second parameter and one member of this enumeration as the third parameter.</span></span>

<span data-ttu-id="dd099-141">Tous les modes de filtrage valides pour un appareil ne s’appliquent pas aux mappages de volume.</span><span class="sxs-lookup"><span data-stu-id="dd099-141">Not all valid filtering modes for a device will apply to volume maps.</span></span> <span data-ttu-id="dd099-142">En général, \_ \_ les filtres d’agrandissement linéaire D3DTEXF point et D3DTEXF sont pris en charge pour les mappages de volume.</span><span class="sxs-lookup"><span data-stu-id="dd099-142">In general, D3DTEXF\_POINT and D3DTEXF\_LINEAR magnification filters will be supported for volume maps.</span></span> <span data-ttu-id="dd099-143">Si D3DPTEXTURECAPS \_ MIPVOLUMEMAP est défini, le \_ filtre MIPMAP point D3DTEXF et le \_ point D3DTEXF et les \_ filtres de minimisation linéaire D3DTEXF sont pris en charge pour les mappages de volume.</span><span class="sxs-lookup"><span data-stu-id="dd099-143">If D3DPTEXTURECAPS\_MIPVOLUMEMAP is set, then the D3DTEXF\_POINT mipmap filter and D3DTEXF\_POINT and D3DTEXF\_LINEAR minification filters will be supported for volume maps.</span></span> <span data-ttu-id="dd099-144">L’appareil peut ou non prendre en charge le \_ filtre mipmap linéaire D3DTEXF pour les mappages de volume.</span><span class="sxs-lookup"><span data-stu-id="dd099-144">The device may or may not support the D3DTEXF\_LINEAR mipmap filter for volume maps.</span></span> <span data-ttu-id="dd099-145">Les appareils qui prennent en charge le filtrage anisotrope pour les mappages 2D ne prennent pas nécessairement en charge le filtrage anisotrope pour les mappages de volume.</span><span class="sxs-lookup"><span data-stu-id="dd099-145">Devices that support anisotropic filtering for 2D maps do not necessarily support anisotropic filtering for volume maps.</span></span> <span data-ttu-id="dd099-146">Toutefois, les applications qui activent le filtrage anisotrope recevront le meilleur filtrage disponible (probablement linéaire) si le filtrage anisotrope n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="dd099-146">However, applications that enable anisotropic filtering will receive the best available filtering (probably linear) if anisotropic filtering is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd099-147">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dd099-147">Requirements</span></span>



| <span data-ttu-id="dd099-148">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dd099-148">Requirement</span></span> | <span data-ttu-id="dd099-149">Valeur</span><span class="sxs-lookup"><span data-stu-id="dd099-149">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd099-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="dd099-150">Header</span></span><br/> | <dl> <span data-ttu-id="dd099-151"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd099-151"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd099-152">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dd099-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd099-153">Énumérations Direct3D</span><span class="sxs-lookup"><span data-stu-id="dd099-153">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="dd099-154">**ID3DXPatchMesh::GetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="dd099-154">**ID3DXPatchMesh::GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="dd099-155">**ID3DXPatchMesh::SetDisplaceParam**</span><span class="sxs-lookup"><span data-stu-id="dd099-155">**ID3DXPatchMesh::SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)
</dt> <dt>

[<span data-ttu-id="dd099-156">**D3DSAMPLERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="dd099-156">**D3DSAMPLERSTATETYPE**</span></span>](./d3dsamplerstatetype.md)
</dt> <dt>

[<span data-ttu-id="dd099-157">**IDirect3DDevice9::SetSamplerState**</span><span class="sxs-lookup"><span data-stu-id="dd099-157">**IDirect3DDevice9::SetSamplerState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)
</dt> </dl>

 

 
