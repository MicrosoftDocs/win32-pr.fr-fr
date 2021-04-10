---
description: Charge un volume à partir d’un autre volume.
ms.assetid: bc162f91-feb7-4571-ae4a-abaa5e7953f6
title: D3DXLoadVolumeFromVolume, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromVolume
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: da2cedf42533fa1d170269e97a366f7e4a1a41f5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953944"
---
# <a name="d3dxloadvolumefromvolume-function"></a><span data-ttu-id="d5281-103">D3DXLoadVolumeFromVolume fonction)</span><span class="sxs-lookup"><span data-stu-id="d5281-103">D3DXLoadVolumeFromVolume function</span></span>

<span data-ttu-id="d5281-104">Charge un volume à partir d’un autre volume.</span><span class="sxs-lookup"><span data-stu-id="d5281-104">Loads a volume from another volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5281-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5281-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromVolume(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPDIRECT3DVOLUME9 pSrcVolume,
  _In_ const PALETTEENTRY      *pSrcPalette,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="d5281-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5281-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5281-107">*pDestVolume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-108">Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="d5281-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="d5281-109">Pointeur vers une interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="d5281-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="d5281-110">Spécifie le volume de destination, qui reçoit l’image.</span><span class="sxs-lookup"><span data-stu-id="d5281-110">Specifies the destination volume, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="d5281-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="d5281-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="d5281-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="d5281-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5281-114">*pDestBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-115">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5281-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="d5281-116">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="d5281-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="d5281-117">Spécifie la zone de destination.</span><span class="sxs-lookup"><span data-stu-id="d5281-117">Specifies the destination box.</span></span> <span data-ttu-id="d5281-118">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="d5281-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5281-119">*pSrcVolume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-119">*pSrcVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-120">Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="d5281-120">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="d5281-121">Pointeur vers une interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="d5281-121">A Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="d5281-122">Spécifie le volume source.</span><span class="sxs-lookup"><span data-stu-id="d5281-122">Specifies the source volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5281-123">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-123">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-124">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="d5281-124">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="d5281-125">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette source de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="d5281-125">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5281-126">*pSrcBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-127">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5281-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="d5281-128">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="d5281-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="d5281-129">Spécifie la zone source.</span><span class="sxs-lookup"><span data-stu-id="d5281-129">Specifies the source box.</span></span> <span data-ttu-id="d5281-130">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="d5281-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="d5281-131">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5281-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5281-133">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md), qui contrôle la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="d5281-133">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="d5281-134">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="d5281-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="d5281-135">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5281-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5281-136">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="d5281-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="d5281-137">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="d5281-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="d5281-138">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="d5281-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="d5281-139">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="d5281-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="d5281-140">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="d5281-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5281-141">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5281-141">Return value</span></span>

<span data-ttu-id="d5281-142">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5281-142">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5281-143">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d5281-143">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5281-144">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="d5281-144">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5281-145">Notes</span><span class="sxs-lookup"><span data-stu-id="d5281-145">Remarks</span></span>

<span data-ttu-id="d5281-146">L’écriture sur une surface non-niveau zéro de la texture du volume n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="d5281-146">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="d5281-147">Si **D3DXLoadVolumeFromVolume** est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**IDirect3DVolumeTexture9 :: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sur l’aire.</span><span class="sxs-lookup"><span data-stu-id="d5281-147">If **D3DXLoadVolumeFromVolume** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5281-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5281-148">Requirements</span></span>



| <span data-ttu-id="d5281-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5281-149">Requirement</span></span> | <span data-ttu-id="d5281-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5281-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d5281-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5281-151">Header</span></span><br/>  | <dl> <span data-ttu-id="d5281-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5281-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="d5281-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5281-153">Library</span></span><br/> | <dl> <span data-ttu-id="d5281-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5281-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="d5281-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5281-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5281-156">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="d5281-156">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="d5281-157">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="d5281-157">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="d5281-158">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="d5281-158">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="d5281-159">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="d5281-159">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="d5281-160">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="d5281-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
