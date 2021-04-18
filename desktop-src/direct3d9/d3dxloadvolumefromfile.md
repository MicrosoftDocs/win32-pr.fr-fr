---
description: Charge un volume à partir d’un fichier.
ms.assetid: ea0fc588-094e-4488-bd82-54507ee0fc91
title: D3DXLoadVolumeFromFile, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadVolumeFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff427c58b62d99c2c4716081aab82bd94f146edd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106543149"
---
# <a name="d3dxloadvolumefromfile-function"></a><span data-ttu-id="1ea14-103">D3DXLoadVolumeFromFile fonction)</span><span class="sxs-lookup"><span data-stu-id="1ea14-103">D3DXLoadVolumeFromFile function</span></span>

<span data-ttu-id="1ea14-104">Charge un volume à partir d’un fichier.</span><span class="sxs-lookup"><span data-stu-id="1ea14-104">Loads a volume from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ea14-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ea14-105">Syntax</span></span>


```C++
HRESULT D3DXLoadVolumeFromFile(
  _In_       LPDIRECT3DVOLUME9 pDestVolume,
  _In_ const PALETTEENTRY      *pDestPalette,
  _In_ const D3DBOX            *pDestBox,
  _In_       LPCTSTR           pSrcFile,
  _In_ const D3DBOX            *pSrcBox,
  _In_       DWORD             Filter,
  _In_       D3DCOLOR          ColorKey,
  _In_       D3DXIMAGE_INFO    *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="1ea14-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1ea14-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ea14-107">*pDestVolume* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-107">*pDestVolume* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-108">Type : **[ **LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span><span class="sxs-lookup"><span data-stu-id="1ea14-108">Type: **[**LPDIRECT3DVOLUME9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9)**</span></span>

<span data-ttu-id="1ea14-109">Pointeur vers une interface [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) .</span><span class="sxs-lookup"><span data-stu-id="1ea14-109">Pointer to an [**IDirect3DVolume9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvolume9) interface.</span></span> <span data-ttu-id="1ea14-110">Spécifie le volume de destination.</span><span class="sxs-lookup"><span data-stu-id="1ea14-110">Specifies the destination volume.</span></span>

</dd> <dt>

<span data-ttu-id="1ea14-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="1ea14-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="1ea14-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="1ea14-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="1ea14-114">*pDestBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-114">*pDestBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-115">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ea14-115">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="1ea14-116">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea14-116">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="1ea14-117">Spécifie la zone de destination.</span><span class="sxs-lookup"><span data-stu-id="1ea14-117">Specifies the destination box.</span></span> <span data-ttu-id="1ea14-118">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="1ea14-118">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="1ea14-119">*pSrcFile* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-119">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-120">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ea14-120">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ea14-121">Pointeur vers une chaîne qui spécifie le nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="1ea14-121">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="1ea14-122">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="1ea14-122">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="1ea14-123">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="1ea14-123">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="1ea14-124">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="1ea14-124">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1ea14-125">*pSrcBox* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-125">*pSrcBox* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-126">Type : **const [**D3DBOX**](d3dbox.md) \***</span><span class="sxs-lookup"><span data-stu-id="1ea14-126">Type: **const [**D3DBOX**](d3dbox.md)\***</span></span>

<span data-ttu-id="1ea14-127">Pointeur vers une structure [**D3DBOX**](d3dbox.md) .</span><span class="sxs-lookup"><span data-stu-id="1ea14-127">Pointer to a [**D3DBOX**](d3dbox.md) structure.</span></span> <span data-ttu-id="1ea14-128">Spécifie la zone source.</span><span class="sxs-lookup"><span data-stu-id="1ea14-128">Specifies the source box.</span></span> <span data-ttu-id="1ea14-129">Affectez la valeur **null** à ce paramètre pour spécifier la totalité du volume.</span><span class="sxs-lookup"><span data-stu-id="1ea14-129">Set this parameter to **NULL** to specify the entire volume.</span></span>

</dd> <dt>

<span data-ttu-id="1ea14-130">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1ea14-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1ea14-132">Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md), contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="1ea14-132">Combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="1ea14-133">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1ea14-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="1ea14-134">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-135">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="1ea14-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="1ea14-136">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="1ea14-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="1ea14-137">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="1ea14-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="1ea14-138">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="1ea14-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="1ea14-139">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="1ea14-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="1ea14-140">*pSrcInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1ea14-140">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ea14-141">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1ea14-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="1ea14-142">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="1ea14-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1ea14-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1ea14-143">Return value</span></span>

<span data-ttu-id="1ea14-144">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1ea14-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1ea14-145">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1ea14-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1ea14-146">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="1ea14-146">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ea14-147">Notes</span><span class="sxs-lookup"><span data-stu-id="1ea14-147">Remarks</span></span>

<span data-ttu-id="1ea14-148">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="1ea14-148">The compiler setting also determines the function version.</span></span> <span data-ttu-id="1ea14-149">Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadVolumeFromFileW.</span><span class="sxs-lookup"><span data-stu-id="1ea14-149">If Unicode is defined, the function call resolves to D3DXLoadVolumeFromFileW.</span></span> <span data-ttu-id="1ea14-150">Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadVolumeFromFileA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="1ea14-150">Otherwise, the function call resolves to D3DXLoadVolumeFromFileA because ANSI strings are being used.</span></span>

<span data-ttu-id="1ea14-151">Cette fonction gère la conversion vers et à partir des formats de texture compressés et prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="1ea14-151">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="1ea14-152">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="1ea14-152">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="1ea14-153">L’écriture sur une surface non-niveau zéro de la texture du volume n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="1ea14-153">Writing to a non-level-zero surface of the volume texture will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="1ea14-154">Si **D3DXLoadVolumeFromFile** est appelé et que la texture n’a pas déjà été modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**IDirect3DVolumeTexture9 :: AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) sur la texture du volume.</span><span class="sxs-lookup"><span data-stu-id="1ea14-154">If **D3DXLoadVolumeFromFile** is called and the texture was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**IDirect3DVolumeTexture9::AddDirtyBox**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvolumetexture9-adddirtybox) on the volume texture.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ea14-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ea14-155">Requirements</span></span>



| <span data-ttu-id="1ea14-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ea14-156">Requirement</span></span> | <span data-ttu-id="1ea14-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ea14-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1ea14-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ea14-158">Header</span></span><br/>  | <dl> <span data-ttu-id="1ea14-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ea14-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="1ea14-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1ea14-160">Library</span></span><br/> | <dl> <span data-ttu-id="1ea14-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ea14-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="1ea14-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ea14-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ea14-163">**D3DXLoadVolumeFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="1ea14-163">**D3DXLoadVolumeFromFileInMemory**</span></span>](d3dxloadvolumefromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="1ea14-164">**D3DXLoadVolumeFromMemory**</span><span class="sxs-lookup"><span data-stu-id="1ea14-164">**D3DXLoadVolumeFromMemory**</span></span>](d3dxloadvolumefrommemory.md)
</dt> <dt>

[<span data-ttu-id="1ea14-165">**D3DXLoadVolumeFromResource**</span><span class="sxs-lookup"><span data-stu-id="1ea14-165">**D3DXLoadVolumeFromResource**</span></span>](d3dxloadvolumefromresource.md)
</dt> <dt>

[<span data-ttu-id="1ea14-166">**D3DXLoadVolumeFromVolume**</span><span class="sxs-lookup"><span data-stu-id="1ea14-166">**D3DXLoadVolumeFromVolume**</span></span>](d3dxloadvolumefromvolume.md)
</dt> <dt>

[<span data-ttu-id="1ea14-167">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="1ea14-167">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
