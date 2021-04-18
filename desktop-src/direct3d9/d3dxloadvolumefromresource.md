---
description: Charge un volume à partir d’une ressource.
ms.assetid: 3fa1243b-5e31-4737-8d3c-08852d6528d9
title: D3DXLoadVolumeFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9d57ce492db24ac9920662d4de5baed4650dd801
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522566"
---
# <a name="d3dxloadvolumefromresource-function"></a><span data-ttu-id="627f4-103">D3DXLoadVolumeFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="627f4-103">D3DXLoadVolumeFromResource function</span></span>

<span data-ttu-id="627f4-104">Charge un volume à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="627f4-104">Loads a volume from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="627f4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="627f4-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromResource(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       HMODULE           hSrcModule,
  _In_       LPCSTR            pSrcResource,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="627f4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="627f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="627f4-107">*pDestVolume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-108">Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="627f4-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="627f4-109">Pointeur vers une interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="627f4-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="627f4-110">Spécifie le volume de destination.</span><span class="sxs-lookup"><span data-stu-id="627f4-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="627f4-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="627f4-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="627f4-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-114">*pDestBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-115">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="627f4-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="627f4-116">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="627f4-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="627f4-117">Spécifie la zone de destination.</span><span class="sxs-lookup"><span data-stu-id="627f4-117">Specifies the destination box.</span></span> <span data-ttu-id="627f4-118">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="627f4-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-119">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-120">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="627f4-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="627f4-121">Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="627f4-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-122">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-123">Type : **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="627f4-123">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="627f4-124">Pointeur vers une chaîne qui spécifie le nom de fichier de l’image source.</span><span class="sxs-lookup"><span data-stu-id="627f4-124">Pointer to a string that specifies the file name of the source image.</span></span> <span data-ttu-id="627f4-125">Si UNICODE ou \_ Unicode sont définis, ce type de paramètre est LPCWSTR, sinon, le type est LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="627f4-125">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-126">*pSrcBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-126">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-127">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="627f4-127">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="627f4-128">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="627f4-128">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="627f4-129">Spécifie la zone source.</span><span class="sxs-lookup"><span data-stu-id="627f4-129">Specifies the source box.</span></span> <span data-ttu-id="627f4-130">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="627f4-130">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-131">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-131">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-132">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="627f4-132">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="627f4-133">Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md), contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="627f4-133">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="627f4-134">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="627f4-134">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-135">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-135">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-136">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="627f4-136">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="627f4-137">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="627f4-137">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="627f4-138">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="627f4-138">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="627f4-139">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="627f4-139">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="627f4-140">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="627f4-140">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="627f4-141">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="627f4-141">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="627f4-142">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="627f4-142">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="627f4-143">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="627f4-143">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="627f4-144">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="627f4-144">Return value</span></span>

<span data-ttu-id="627f4-145">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="627f4-145">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="627f4-146">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="627f4-146">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="627f4-147">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="627f4-147">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="627f4-148">Notes</span><span class="sxs-lookup"><span data-stu-id="627f4-148">Remarks</span></span>

<span data-ttu-id="627f4-149">La ressource en cours de chargement doit être une ressource bitmap (RT \_ bitmap).</span><span class="sxs-lookup"><span data-stu-id="627f4-149">The resource being loaded must be a bitmap resource(RT\_BITMAP).</span></span>

<span data-ttu-id="627f4-150">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="627f4-150">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="627f4-151">L’écriture sur une surface non-niveau zéro de la texture du volume n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="627f4-151">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="627f4-152">Si [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) est appelé et que la texture n’a pas déjà été modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**IDirect3DVolumeTexture9 :: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sur la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="627f4-152">If [**D3DXLoadVolumeFromFile**](d3dxloadvolumefromfile.md) is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

<span data-ttu-id="627f4-153">Cette fonction prend en charge les chaînes Unicode et ANSI.</span><span class="sxs-lookup"><span data-stu-id="627f4-153">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="627f4-154">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="627f4-154">Requirements</span></span>



| <span data-ttu-id="627f4-155">Condition requise</span><span class="sxs-lookup"><span data-stu-id="627f4-155">Requirement</span></span> | <span data-ttu-id="627f4-156">Valeur</span><span class="sxs-lookup"><span data-stu-id="627f4-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="627f4-157">En-tête</span><span class="sxs-lookup"><span data-stu-id="627f4-157">Header</span></span><br/>  | <dl> <span data-ttu-id="627f4-158"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="627f4-158"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="627f4-159">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="627f4-159">Library</span></span><br/> | <dl> <span data-ttu-id="627f4-160"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="627f4-160"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="627f4-161">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="627f4-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="627f4-162">**D3DXLoadVolumeFromFile**</span><span class="sxs-lookup"><span data-stu-id="627f4-162">**D3DXLoadVolumeFromFile**</span></span>](d3dxloadvolumefromfile.md)
</dt> <dt>

[<span data-ttu-id="627f4-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="627f4-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="627f4-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="627f4-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="627f4-165">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="627f4-165">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="627f4-166">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="627f4-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
