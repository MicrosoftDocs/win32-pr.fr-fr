---
description: Charge un volume à partir de la mémoire.
ms.assetid: 9f74fcc0-f935-4466-865b-e798711a1f2f
title: D3DXLoadVolumeFromMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7d6c3f1bdfe40f19eeb57b4f0d8a38c40a239404
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522335"
---
# <a name="d3dxloadvolumefrommemory-function"></a><span data-ttu-id="f9d2e-103">D3DXLoadVolumeFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="f9d2e-103">D3DXLoadVolumeFromMemory function</span></span>

<span data-ttu-id="f9d2e-104">Charge un volume à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-104">Loads a volume from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9d2e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f9d2e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromMemory(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCVOID           pSrcMemory,
  _In_       D3DFORMAT         SrcFormat,
  _In_       UINT              SrcRowPitch,
  _In_       UINT              SrcSlicePitch,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="f9d2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f9d2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9d2e-107">*pDestVolume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-108">Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="f9d2e-109">Pointeur vers une interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="f9d2e-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="f9d2e-110">Spécifie le volume de destination, qui reçoit l’image.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="f9d2e-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="f9d2e-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-114">*pDestBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-115">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="f9d2e-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="f9d2e-116">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="f9d2e-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="f9d2e-117">Spécifie la zone de destination.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-117">Specifies the destination box.</span></span> <span data-ttu-id="f9d2e-118">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-119">*pSrcMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-120">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9d2e-121">Pointeur vers l’angle supérieur gauche du volume source en mémoire.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-121">Pointer to the top-left corner of the source volume in memory.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-122">*SrcFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-123">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="f9d2e-124">Membre du type énuméré [D3DFORMAT](d3dformat.md) , format de pixel du volume source.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-125">*SrcRowPitch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-125">*SrcRowPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9d2e-127">Hauteur de l’image source, en octets.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="f9d2e-128">Pour les formats DXT (formats de texture compressés), ce nombre doit représenter la taille d’une ligne de cellules, en octets.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-128">For DXT formats (compressed texture formats), this number should represent the size of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-129">*SrcSlicePitch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-129">*SrcSlicePitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-130">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-130">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9d2e-131">Hauteur de l’image source, en octets.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-131">Pitch of source image, in bytes.</span></span> <span data-ttu-id="f9d2e-132">Pour les formats DXT (formats de texture compressés), ce nombre doit représenter la taille d’une tranche de cellules, en octets.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-132">For DXT formats (compressed texture formats), this number should represent the size of one slice of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-133">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-133">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-134">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="f9d2e-134">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="f9d2e-135">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette source de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-135">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-136">*pSrcBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-136">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-137">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="f9d2e-137">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="f9d2e-138">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="f9d2e-138">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="f9d2e-139">Spécifie la zone source.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-139">Specifies the source box.</span></span> <span data-ttu-id="f9d2e-140">**Null** n’est pas une valeur valide pour ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-140">**NULL** is not a valid value for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-141">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-141">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-142">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-142">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f9d2e-143">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-143">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="f9d2e-144">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="f9d2e-144">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="f9d2e-145">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f9d2e-145">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9d2e-146">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-146">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="f9d2e-147">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-147">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="f9d2e-148">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-148">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="f9d2e-149">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-149">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="f9d2e-150">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-150">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9d2e-151">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f9d2e-151">Return value</span></span>

<span data-ttu-id="f9d2e-152">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-152">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f9d2e-153">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-153">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f9d2e-154">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-154">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9d2e-155">Notes</span><span class="sxs-lookup"><span data-stu-id="f9d2e-155">Remarks</span></span>

<span data-ttu-id="f9d2e-156">L’écriture sur une surface non-niveau zéro de la texture du volume n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-156">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="f9d2e-157">Si **D3DXLoadVolumeFromMemory** est appelé et que la texture n’a pas déjà été modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**IDirect3DVolumeTexture9 :: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sur la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="f9d2e-157">If **D3DXLoadVolumeFromMemory** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="f9d2e-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f9d2e-158">Requirements</span></span>



| <span data-ttu-id="f9d2e-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f9d2e-159">Requirement</span></span> | <span data-ttu-id="f9d2e-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="f9d2e-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f9d2e-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="f9d2e-161">Header</span></span><br/>  | <dl> <span data-ttu-id="f9d2e-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9d2e-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="f9d2e-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f9d2e-163">Library</span></span><br/> | <dl> <span data-ttu-id="f9d2e-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f9d2e-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="f9d2e-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f9d2e-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9d2e-166">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-166">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="f9d2e-167">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-167">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="f9d2e-168">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="f9d2e-168">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="f9d2e-169">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="f9d2e-169">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
