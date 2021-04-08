---
description: Charge une surface à partir de la mémoire.
ms.assetid: 9a36e395-fd00-47fe-8df1-cda8c80182ef
title: D3DXLoadSurfaceFromMemory, fonction (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXLoadSurfaceFromMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ffb7be05301ae807505242153be902ab30eecf14
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043084"
---
# <a name="d3dxloadsurfacefrommemory-function"></a><span data-ttu-id="ba1e5-103">D3DXLoadSurfaceFromMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="ba1e5-103">D3DXLoadSurfaceFromMemory function</span></span>

<span data-ttu-id="ba1e5-104">Charge une surface à partir de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-104">Loads a surface from memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba1e5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ba1e5-105">Syntax</span></span>


```C++
HRESULT D3DXLoadSurfaceFromMemory(
  _In_       LPDIRECT3DSURFACE9 pDestSurface,
  _In_ const PALETTEENTRY       *pDestPalette,
  _In_ const RECT               *pDestRect,
  _In_       LPCVOID            pSrcMemory,
  _In_       D3DFORMAT          SrcFormat,
  _In_       UINT               SrcPitch,
  _In_ const PALETTEENTRY       *pSrcPalette,
  _In_ const RECT               *pSrcRect,
  _In_       DWORD              Filter,
  _In_       D3DCOLOR           ColorKey
);
```



## <a name="parameters"></a><span data-ttu-id="ba1e5-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ba1e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba1e5-107">*pDestSurface* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-107">*pDestSurface* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-108">Type : **[ **LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-108">Type: **[**LPDIRECT3DSURFACE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9)**</span></span>

<span data-ttu-id="ba1e5-109">Pointeur vers une interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) .</span><span class="sxs-lookup"><span data-stu-id="ba1e5-109">Pointer to an [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface.</span></span> <span data-ttu-id="ba1e5-110">Spécifie la surface de destination, qui reçoit l’image.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-110">Specifies the destination surface, which receives the image.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-111">*pDestPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-111">*pDestPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-112">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ba1e5-112">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ba1e5-113">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette de destination de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-113">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the destination palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-114">*pDestRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-114">*pDestRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-115">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ba1e5-115">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ba1e5-116">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ba1e5-116">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ba1e5-117">Spécifie le rectangle de destination.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-117">Specifies the destination rectangle.</span></span> <span data-ttu-id="ba1e5-118">Affectez la valeur **null** à ce paramètre pour spécifier la surface entière.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-118">Set this parameter to **NULL** to specify the entire surface.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-119">*pSrcMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-119">*pSrcMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-120">Type : **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-120">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba1e5-121">Pointeur vers l’angle supérieur gauche de l’image source en mémoire.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-121">Pointer to the upper left corner of the source image in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-122">*SrcFormat* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-122">*SrcFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-123">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-123">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

<span data-ttu-id="ba1e5-124">Membre du type énuméré [D3DFORMAT](d3dformat.md) , format de pixel de l’image source.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-124">Member of the [D3DFORMAT](d3dformat.md) enumerated type, the pixel format of the source image.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-125">*SrcPitch* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-125">*SrcPitch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-126">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-126">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba1e5-127">Hauteur de l’image source, en octets.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-127">Pitch of source image, in bytes.</span></span> <span data-ttu-id="ba1e5-128">Pour les formats DXT, ce nombre doit représenter la largeur d’une ligne de cellules, en octets.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-128">For DXT formats, this number should represent the width of one row of cells, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-129">*pSrcPalette* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-129">*pSrcPalette* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-130">Type : **const [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***</span><span class="sxs-lookup"><span data-stu-id="ba1e5-130">Type: **const [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry)\***</span></span>

<span data-ttu-id="ba1e5-131">Pointeur vers une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , la palette source de 256 couleurs ou **null**.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-131">Pointer to a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure, the source palette of 256 colors or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-132">*pSrcRect* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-132">*pSrcRect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-133">Type : **const [**Rect**](/previous-versions//dd162897(v=vs.85)) \***</span><span class="sxs-lookup"><span data-stu-id="ba1e5-133">Type: **const [**RECT**](/previous-versions//dd162897(v=vs.85))\***</span></span>

<span data-ttu-id="ba1e5-134">Pointeur vers une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ba1e5-134">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ba1e5-135">Spécifie les dimensions de l’image source en mémoire.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-135">Specifies the dimensions of the source image in memory.</span></span> <span data-ttu-id="ba1e5-136">Cette valeur ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-136">This value cannot be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-137">*Filtre* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-137">*Filter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-138">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-138">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba1e5-139">Combinaison d’un ou de [plusieurs \_ filtres D3DX](d3dx-filter.md) contrôlant la façon dont l’image est filtrée.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-139">Combination of one or more [D3DX\_FILTER](d3dx-filter.md) controlling how the image is filtered.</span></span> <span data-ttu-id="ba1e5-140">La spécification \_ de la valeur D3DX par défaut pour ce paramètre revient à spécifier la valeur de filtre du \_ triangle de filtre D3DX \_ \| \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ba1e5-140">Specifying D3DX\_DEFAULT for this parameter is the equivalent of specifying D3DX\_FILTER\_TRIANGLE \| D3DX\_FILTER\_DITHER.</span></span>

</dd> <dt>

<span data-ttu-id="ba1e5-141">*ColorKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ba1e5-141">*ColorKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba1e5-142">Type : **[ **D3DCOLOR**](d3dcolor.md)**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-142">Type: **[**D3DCOLOR**](d3dcolor.md)**</span></span>

<span data-ttu-id="ba1e5-143">Valeur [**D3DCOLOR**](d3dcolor.md) à remplacer par le noir transparent, ou 0 pour désactiver le ColorKey.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-143">[**D3DCOLOR**](d3dcolor.md) value to replace with transparent black, or 0 to disable the colorkey.</span></span> <span data-ttu-id="ba1e5-144">Il s’agit toujours d’une couleur ARVB de 32 bits, indépendante du format d’image source.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-144">This is always a 32-bit ARGB color, independent of the source image format.</span></span> <span data-ttu-id="ba1e5-145">Alpha est significatif et doit généralement être défini sur FF pour les clés de couleur opaques.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-145">Alpha is significant and should usually be set to FF for opaque color keys.</span></span> <span data-ttu-id="ba1e5-146">Ainsi, pour le noir opaque, la valeur est égale à 0xFF000000.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-146">Thus, for opaque black, the value would be equal to 0xFF000000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba1e5-147">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ba1e5-147">Return value</span></span>

<span data-ttu-id="ba1e5-148">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba1e5-148">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba1e5-149">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-149">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ba1e5-150">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-150">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba1e5-151">Notes</span><span class="sxs-lookup"><span data-stu-id="ba1e5-151">Remarks</span></span>

<span data-ttu-id="ba1e5-152">Cette fonction gère la conversion vers et à partir des formats de texture compressés.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-152">This function handles conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="ba1e5-153">L’écriture sur une surface non-niveau zéro n’entraîne pas la mise à jour du rectangle de modification.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-153">Writing to a non-level-zero surface will not cause the dirty rectangle to be updated.</span></span> <span data-ttu-id="ba1e5-154">Si **D3DXLoadSurfaceFromMemory** est appelé et que la surface n’était pas encore modifiée (ce qui est peu probable dans les scénarios d’utilisation normale), l’application doit appeler explicitement [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) sur l’aire.</span><span class="sxs-lookup"><span data-stu-id="ba1e5-154">If **D3DXLoadSurfaceFromMemory** is called and the surface was not already dirty (this is unlikely under normal usage scenarios), the application needs to explicitly call [**AddDirtyRect**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-adddirtyrect) on the surface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba1e5-155">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ba1e5-155">Requirements</span></span>



| <span data-ttu-id="ba1e5-156">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ba1e5-156">Requirement</span></span> | <span data-ttu-id="ba1e5-157">Valeur</span><span class="sxs-lookup"><span data-stu-id="ba1e5-157">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ba1e5-158">En-tête</span><span class="sxs-lookup"><span data-stu-id="ba1e5-158">Header</span></span><br/>  | <dl> <span data-ttu-id="ba1e5-159"><dt>D3dx9tex. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba1e5-159"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ba1e5-160">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ba1e5-160">Library</span></span><br/> | <dl> <span data-ttu-id="ba1e5-161"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba1e5-161"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ba1e5-162">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ba1e5-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba1e5-163">Fonctions de texture dans D3DX 9</span><span class="sxs-lookup"><span data-stu-id="ba1e5-163">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
