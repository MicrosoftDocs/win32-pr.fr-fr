---
description: Charge une surface à partir d’un fichier en mémoire.
ms.assetid: 436a6151-2819-44eb-bd56-1b3777f709e5
title: D3DXLoadSurfaceFromFileInMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a447c4c5b65e3085d84e26ef202283cf0c31c6b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762332"
---
# <a name="d3dxloadsurfacefromfileinmemory-function"></a><span data-ttu-id="a173e-103">D3DXLoadSurfaceFromFileInMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="a173e-103">D3DXLoadSurfaceFromFileInMemory function</span></span>

<span data-ttu-id="a173e-104">Charge une surface à partir d’un fichier en mémoire.</span><span class="sxs-lookup"><span data-stu-id="a173e-104">Loads a surface from a file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="a173e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a173e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromFileInMemory(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          LPCVOID            pSrcData,
  _In_          UINT               SrcData,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a173e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a173e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a173e-107">*pDestSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-108">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="a173e-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="a173e-109">Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="a173e-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="a173e-110">Spécifie la surface de destination, qui reçoit l’image.</span><span class="sxs-lookup"><span data-stu-id="a173e-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="a173e-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="a173e-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="a173e-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-114">*pDestRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-115">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="a173e-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="a173e-116">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a173e-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="a173e-117">Spécifie le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="a173e-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="a173e-118">Affectez la valeur **null** à ce paramètre pour spécifier la surface entière.</span><span class="sxs-lookup"><span data-stu-id="a173e-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-119">*pSrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-119">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-120">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a173e-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a173e-121">Pointeur vers le fichier en mémoire à partir duquel charger l’aire.</span><span class="sxs-lookup"><span data-stu-id="a173e-121">Pointer to the file in memory from which to load the surface.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-122">*SrcData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-122">*SrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-123">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a173e-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a173e-124">Taille du fichier en mémoire, en octets.</span><span class="sxs-lookup"><span data-stu-id="a173e-124">Size of the file in memory, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-125">*pSrcRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-126">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="a173e-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="a173e-127">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="a173e-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="a173e-128">Spécifie le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="a173e-128">Specifies the source rectangle.</span></span> <span data-ttu-id="a173e-129">Affectez la valeur **null** à ce paramètre pour spécifier la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="a173e-129">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-130">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a173e-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a173e-132">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="a173e-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="a173e-133">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a173e-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-134">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a173e-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-135">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="a173e-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="a173e-136">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="a173e-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="a173e-137">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="a173e-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="a173e-138">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="a173e-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="a173e-139">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="a173e-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="a173e-140">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a173e-140">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a173e-141">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="a173e-141">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="a173e-142">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source ou **null**.</span><span class="sxs-lookup"><span data-stu-id="a173e-142">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a173e-143">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a173e-143">Return value</span></span>

<span data-ttu-id="a173e-144">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a173e-144">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a173e-145">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a173e-145">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a173e-146">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="a173e-146">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="a173e-147">Notes</span><span class="sxs-lookup"><span data-stu-id="a173e-147">Remarks</span></span>

<span data-ttu-id="a173e-148">Cette fonction gère la conversion vers et à partir des formats de texture compressés et prend en charge les formats de fichier suivants :. bmp,. DDS,. dib,. HDR,. jpg,. PFM,. png,. ppm et. tga.</span><span class="sxs-lookup"><span data-stu-id="a173e-148">This function handles conversion to and from compressed texture formats and supports the following file formats: .bmp, .dds, .dib, .hdr, .jpg, .pfm, .png, .ppm, and .tga.</span></span> <span data-ttu-id="a173e-149">Consultez [**D3DXIMAGE \_ FILEFORMAT**](./d3dximage-fileformat.md).</span><span class="sxs-lookup"><span data-stu-id="a173e-149">See [**D3DXIMAGE\_FILEFORMAT**](./d3dximage-fileformat.md).</span></span>

<span data-ttu-id="a173e-150">L’écriture sur une surface non-niveau zéro n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="a173e-150">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="a173e-151">Si **D3DXLoadSurfaceFromFileInMemory** est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sur l’aire.</span><span class="sxs-lookup"><span data-stu-id="a173e-151">If **D3DXLoadSurfaceFromFileInMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="a173e-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a173e-152">Requirements</span></span>



| <span data-ttu-id="a173e-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a173e-153">Requirement</span></span> | <span data-ttu-id="a173e-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="a173e-154">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a173e-155">En-tête</span><span class="sxs-lookup"><span data-stu-id="a173e-155">Header</span></span><br/>  | <dl> <span data-ttu-id="a173e-156"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="a173e-156"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="a173e-157">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="a173e-157">Library</span></span><br/> | <dl> <span data-ttu-id="a173e-158"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a173e-158"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a173e-159">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a173e-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a173e-160">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="a173e-160">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
