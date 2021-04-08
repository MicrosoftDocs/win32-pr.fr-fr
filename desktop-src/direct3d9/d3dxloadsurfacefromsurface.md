---
description: Charge une surface à partir d’une autre surface avec la conversion de couleurs.
ms.assetid: eddb420d-fd32-4c09-afec-435887c4e905
title: D3DXLoadSurfaceFromSurface, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromSurface
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b5138ddf540c3e4a87fe65f29938cb3557b2360
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762187"
---
# <a name="d3dxloadsurfacefromsurface-function"></a><span data-ttu-id="e7f5c-103">D3DXLoadSurfaceFromSurface fonction)</span><span class="sxs-lookup"><span data-stu-id="e7f5c-103">D3DXLoadSurfaceFromSurface function</span></span>

<span data-ttu-id="e7f5c-104">Charge une surface à partir d’une autre surface avec la conversion de couleurs.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-104">Loads a surface from another surface with color conversion.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f5c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7f5c-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromSurface(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPDIRECT3DSURFACE9 pSrcSurface,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="e7f5c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7f5c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7f5c-107">*pDestSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-108">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e7f5c-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e7f5c-109">Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="e7f5c-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="e7f5c-110">Spécifie la surface de destination, qui reçoit l’image.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="e7f5c-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e7f5c-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e7f5c-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7f5c-114">*pDestRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-115">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e7f5c-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e7f5c-116">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e7f5c-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e7f5c-117">Spécifie le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="e7f5c-118">Affectez la valeur **null** à ce paramètre pour spécifier la surface entière.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="e7f5c-119">*pSrcSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-119">*pSrcSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-120">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="e7f5c-120">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="e7f5c-121">Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) représentant la surface source.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-121">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the source surface.</span></span>

</dd> <dt>

<span data-ttu-id="e7f5c-122">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-122">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-123">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="e7f5c-123">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="e7f5c-124">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette source de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-124">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e7f5c-125">*pSrcRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-125">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-126">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="e7f5c-126">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="e7f5c-127">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="e7f5c-127">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="e7f5c-128">Spécifie le rectangle source.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-128">Specifies the source rectangle.</span></span> <span data-ttu-id="e7f5c-129">Affectez la valeur **null** à ce paramètre pour spécifier la surface entière.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-129">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="e7f5c-130">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-130">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-131">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e7f5c-131">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e7f5c-132">Combinaison d’un ou de plusieurs [ \_ filtres D3DX](d3dx-filter.md), qui contrôle la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-132">A combination of one or more [D3DX\_FILTER](d3dx-filter.md), controlling how the image is filtered.</span></span> <span data-ttu-id="e7f5c-133">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="e7f5c-133">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="e7f5c-134">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7f5c-134">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7f5c-135">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="e7f5c-135">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="e7f5c-136">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-136">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="e7f5c-137">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-137">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="e7f5c-138">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-138">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="e7f5c-139">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-139">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7f5c-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7f5c-140">Return value</span></span>

<span data-ttu-id="e7f5c-141">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e7f5c-141">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e7f5c-142">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-142">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e7f5c-143">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-143">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7f5c-144">Notes</span><span class="sxs-lookup"><span data-stu-id="e7f5c-144">Remarks</span></span>

<span data-ttu-id="e7f5c-145">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-145">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="e7f5c-146">L’écriture sur une surface non-niveau zéro n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-146">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="e7f5c-147">Si **D3DXLoadSurfaceFromSurface** est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sur l’aire.</span><span class="sxs-lookup"><span data-stu-id="e7f5c-147">If **D3DXLoadSurfaceFromSurface** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7f5c-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7f5c-148">Requirements</span></span>



| <span data-ttu-id="e7f5c-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7f5c-149">Requirement</span></span> | <span data-ttu-id="e7f5c-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7f5c-150">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e7f5c-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7f5c-151">Header</span></span><br/>  | <dl> <span data-ttu-id="e7f5c-152"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7f5c-152"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="e7f5c-153">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7f5c-153">Library</span></span><br/> | <dl> <span data-ttu-id="e7f5c-154"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7f5c-154"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e7f5c-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7f5c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7f5c-156">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="e7f5c-156">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
