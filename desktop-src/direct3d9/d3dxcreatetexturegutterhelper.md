---
description: Crée un objet ID3DXTextureGutterHelper à partir d’une maille d’entrée et de données de texture.
ms.assetid: 1696fc3d-5b35-48cc-a79b-c0d4ed44e420
title: D3DXCreateTextureGutterHelper, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTextureGutterHelper
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 8957649f3cef6ea67932579918163613160ee993
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106527107"
---
# <a name="d3dxcreatetexturegutterhelper-function"></a><span data-ttu-id="59fdc-103">D3DXCreateTextureGutterHelper fonction)</span><span class="sxs-lookup"><span data-stu-id="59fdc-103">D3DXCreateTextureGutterHelper function</span></span>

<span data-ttu-id="59fdc-104">Crée un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à partir d’une maille d’entrée et de données de texture.</span><span class="sxs-lookup"><span data-stu-id="59fdc-104">Creates an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object from an input mesh and texture data.</span></span>

## <a name="syntax"></a><span data-ttu-id="59fdc-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="59fdc-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTextureGutterHelper(
  _In_    UINT                      Width,
  _In_    UINT                      Height,
  _In_    LPD3DXMESH                pMesh,
  _In_    FLOAT                     GutterSize,
  _Inout_ LPD3DXTEXTUREGUTTERHELPER *ppBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="59fdc-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="59fdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59fdc-107">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59fdc-107">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fdc-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59fdc-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59fdc-109">Largeur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="59fdc-109">Width of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="59fdc-110">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59fdc-110">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fdc-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59fdc-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59fdc-112">Hauteur de la texture, en pixels.</span><span class="sxs-lookup"><span data-stu-id="59fdc-112">Height of the texture, in pixels.</span></span>

</dd> <dt>

<span data-ttu-id="59fdc-113">*pMesh* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59fdc-113">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fdc-114">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="59fdc-114">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="59fdc-115">Pointeur vers un objet de maillage [**ID3DXMesh**](id3dxmesh.md) d’entrée.</span><span class="sxs-lookup"><span data-stu-id="59fdc-115">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object.</span></span>

</dd> <dt>

<span data-ttu-id="59fdc-116">*GutterSize* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="59fdc-116">*GutterSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fdc-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="59fdc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="59fdc-118">Nombre de texels permettant de suréchantillonner la texture et de créer la région de la reliure.</span><span class="sxs-lookup"><span data-stu-id="59fdc-118">Number of texels by which to over-sample the texture and create the gutter region.</span></span> <span data-ttu-id="59fdc-119">Doit être au moins égal à 1.</span><span class="sxs-lookup"><span data-stu-id="59fdc-119">Must be at least 1.</span></span>

</dd> <dt>

<span data-ttu-id="59fdc-120">*ppBuffer* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="59fdc-120">*ppBuffer* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="59fdc-121">Type : **[ **LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span><span class="sxs-lookup"><span data-stu-id="59fdc-121">Type: **[**LPD3DXTEXTUREGUTTERHELPER**](id3dxtexturegutterhelper.md)\***</span></span>

<span data-ttu-id="59fdc-122">Pointeur vers un objet [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) à créer.</span><span class="sxs-lookup"><span data-stu-id="59fdc-122">Pointer to an [**ID3DXTextureGutterHelper**](id3dxtexturegutterhelper.md) object to be created.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59fdc-123">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="59fdc-123">Return value</span></span>

<span data-ttu-id="59fdc-124">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="59fdc-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="59fdc-125">Si la fonction est réussie, la valeur de retour est S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="59fdc-125">If the function succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="59fdc-126">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="59fdc-126">If the function fails, the return value can be one of these: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="59fdc-127">Notes</span><span class="sxs-lookup"><span data-stu-id="59fdc-127">Remarks</span></span>

<span data-ttu-id="59fdc-128">Utilisez [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) pour transformer une scène en nouvelles coordonnées.</span><span class="sxs-lookup"><span data-stu-id="59fdc-128">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to transform a scene to new coordinates.</span></span>

## <a name="requirements"></a><span data-ttu-id="59fdc-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="59fdc-129">Requirements</span></span>



| <span data-ttu-id="59fdc-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="59fdc-130">Requirement</span></span> | <span data-ttu-id="59fdc-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="59fdc-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="59fdc-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="59fdc-132">Header</span></span><br/>  | <dl> <span data-ttu-id="59fdc-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="59fdc-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="59fdc-134">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="59fdc-134">Library</span></span><br/> | <dl> <span data-ttu-id="59fdc-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="59fdc-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="59fdc-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="59fdc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fdc-137">Fonctions de transfert luminance précalculées</span><span class="sxs-lookup"><span data-stu-id="59fdc-137">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
