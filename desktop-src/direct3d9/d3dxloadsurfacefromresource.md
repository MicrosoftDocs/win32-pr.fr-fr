---
description: Charge une surface à partir d’une ressource.
ms.assetid: 16d49f61-8c84-4e15-aacc-1d26099e65e0
title: D3DXLoadSurfaceFromResource, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ae802a1b7e18ce5f2b0a11c6679628ea1deb25aa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103953800"
---
# <a name="d3dxloadsurfacefromresource-function"></a><span data-ttu-id="ebc4e-103">D3DXLoadSurfaceFromResource fonction)</span><span class="sxs-lookup"><span data-stu-id="ebc4e-103">D3DXLoadSurfaceFromResource function</span></span>

<span data-ttu-id="ebc4e-104">Charge une surface à partir d’une ressource.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-104">Loads a surface from a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebc4e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebc4e-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromResource(
  _In_          LPDIRECT3DSURFACE9 pDestSurface,
  _In_    const PALETTEENTRY       *pDestPalette,
  _In_    const RECT               *pDestRect,
  _In_          HMODULE            hSrcModule,
  _In_          LPCTSTR            pSrcResource,
  _In_    const RECT               *pSrcRect,
  _In_          DWORD              Filter,
  _In_          D3DCOLOR           ColorKey,
  _Inout_       D3DXIMAGE_INFO     *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ebc4e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebc4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebc4e-107">*pDestSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-108">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="ebc4e-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="ebc4e-109">Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="ebc4e-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="ebc4e-110">Spécifie la surface de destination, qui reçoit l’image.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ebc4e-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ebc4e-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-114">*pDestRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-115">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ebc4e-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ebc4e-116">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ebc4e-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ebc4e-117">Spécifie le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="ebc4e-118">Affectez la valeur **null** à ce paramètre pour spécifier la surface entière.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-119">*hSrcModule* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-119">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-120">Type : **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc4e-120">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ebc4e-121">Handle vers le module dans lequel se trouve la ressource, ou **null** pour le module associé à l’image que le système d’exploitation a utilisé pour créer le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-121">Handle to the module where the resource is located, or **NULL** for module associated with the image the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-122">*pSrcResource* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-122">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-123">Type : **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc4e-123">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ebc4e-124">Pointeur vers une chaîne qui spécifie le nom de la ressource.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-124">Pointer to a string that specifies the resource name.</span></span> <span data-ttu-id="ebc4e-125">Si les paramètres du compilateur requièrent Unicode, le type de données LPCTSTR est résolu en LPCWSTR.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-125">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="ebc4e-126">Dans le cas contraire, le type de données String est résolu en LPCSTR.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-126">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="ebc4e-127">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-127">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-128">*pSrcRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-128">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-129">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ebc4e-129">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ebc4e-130">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ebc4e-130">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ebc4e-131">Spécifie le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-131">Specifies the source rectangle.</span></span> <span data-ttu-id="ebc4e-132">Affectez la valeur **null** à ce paramètre pour spécifier la totalité de l’image.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-132">Set this parameter to **NULL** to specify the entire image.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-133">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-133">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-134">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc4e-134">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ebc4e-135">Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-135">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ebc4e-136">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ebc4e-136">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-137">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-137">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-138">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ebc4e-138">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ebc4e-139">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-139">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ebc4e-140">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-140">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ebc4e-141">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaque donc, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-141">Alpha is significant and should usually be set to FF for opaque color keys Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> <dt>

<span data-ttu-id="ebc4e-142">*pSrcInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="ebc4e-142">*pSrcInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="ebc4e-143">Type : **[ **D3DXIMAGE \_ info**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ebc4e-143">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ebc4e-144">Pointeur vers une structure d' [**\_ informations D3DXIMAGE**](d3dximage-info.md) à remplir avec une description des données dans le fichier image source, ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-144">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with a description of the data in the source image file, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebc4e-145">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebc4e-145">Return value</span></span>

<span data-ttu-id="ebc4e-146">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebc4e-146">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebc4e-147">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-147">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ebc4e-148">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-148">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ebc4e-149">Notes</span><span class="sxs-lookup"><span data-stu-id="ebc4e-149">Remarks</span></span>

<span data-ttu-id="ebc4e-150">Le paramètre du compilateur détermine également la version de la fonction.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-150">The compiler setting also determines the function version.</span></span> <span data-ttu-id="ebc4e-151">Si Unicode est défini, l’appel de fonction est résolu en D3DXLoadSurfaceFromResourceW.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-151">If Unicode is defined, the function call resolves to D3DXLoadSurfaceFromResourceW.</span></span> <span data-ttu-id="ebc4e-152">Dans le cas contraire, l’appel de fonction est résolu en D3DXLoadSurfaceFromResourceA, car les chaînes ANSI sont utilisées.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-152">Otherwise, the function call resolves to D3DXLoadSurfaceFromResourceA because ANSI strings are being used.</span></span>

<span data-ttu-id="ebc4e-153">La ressource en cours de chargement doit être de type RT \_ bitmap ou RT \_ RCDATA.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-153">The resource being loaded must be of type RT\_BITMAP or RT\_RCDATA.</span></span> <span data-ttu-id="ebc4e-154">Le type de ressource « RT \_ RCDATA » est utilisé pour charger des formats autres que des bitmaps (tels que. TGA,. jpg et. DDS).</span><span class="sxs-lookup"><span data-stu-id="ebc4e-154">Resource type RT\_RCDATA is used to load formats other than bitmaps (such as .tga, .jpg, and .dds).</span></span>

<span data-ttu-id="ebc4e-155">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-155">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="ebc4e-156">L’écriture sur une surface non-niveau zéro n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-156">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="ebc4e-157">Si [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sur l’aire.</span><span class="sxs-lookup"><span data-stu-id="ebc4e-157">If [**D3DXLoadSurfaceFromFile**](d3dxloadsurfacefromfile.md) is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebc4e-158">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebc4e-158">Requirements</span></span>



| <span data-ttu-id="ebc4e-159">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebc4e-159">Requirement</span></span> | <span data-ttu-id="ebc4e-160">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebc4e-160">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ebc4e-161">En-tête</span><span class="sxs-lookup"><span data-stu-id="ebc4e-161">Header</span></span><br/>  | <dl> <span data-ttu-id="ebc4e-162"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebc4e-162"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ebc4e-163">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ebc4e-163">Library</span></span><br/> | <dl> <span data-ttu-id="ebc4e-164"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebc4e-164"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ebc4e-165">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebc4e-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebc4e-166">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ebc4e-166">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
