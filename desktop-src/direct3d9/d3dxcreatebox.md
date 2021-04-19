---
description: Utilise un système de coordonnées droitier pour créer un maillage contenant une zone alignée sur l’axe.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: D3DXCreateBox, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 187c389dd2d90b4457237540026a63edc4ab4f4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535169"
---
# <a name="d3dxcreatebox-function"></a><span data-ttu-id="8d99a-103">D3DXCreateBox fonction)</span><span class="sxs-lookup"><span data-stu-id="8d99a-103">D3DXCreateBox function</span></span>

<span data-ttu-id="8d99a-104">Utilise un système de coordonnées droitier pour créer un maillage contenant une zone alignée sur l’axe.</span><span class="sxs-lookup"><span data-stu-id="8d99a-104">Uses a left-handed coordinate system to create a mesh containing an axis-aligned box.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d99a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d99a-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="8d99a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d99a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d99a-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d99a-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d99a-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="8d99a-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="8d99a-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé à la maille Box créée.</span><span class="sxs-lookup"><span data-stu-id="8d99a-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="8d99a-110">*Largeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d99a-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d99a-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d99a-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d99a-112">Largeur de la zone, le long de l’axe x.</span><span class="sxs-lookup"><span data-stu-id="8d99a-112">Width of the box, along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="8d99a-113">*Hauteur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d99a-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d99a-114">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d99a-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d99a-115">Hauteur de la zone, le long de l’axe y.</span><span class="sxs-lookup"><span data-stu-id="8d99a-115">Height of the box, along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="8d99a-116">*Profondeur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d99a-116">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d99a-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8d99a-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8d99a-118">Profondeur de la zone, le long de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="8d99a-118">Depth of the box, along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="8d99a-119">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d99a-119">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d99a-120">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d99a-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="8d99a-121">Adresse d’un pointeur vers la forme de sortie, une interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="8d99a-121">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="8d99a-122">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d99a-122">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d99a-123">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="8d99a-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="8d99a-124">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="8d99a-124">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="8d99a-125">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="8d99a-125">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="8d99a-126">La **valeur null** peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8d99a-126">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d99a-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d99a-127">Return value</span></span>

<span data-ttu-id="8d99a-128">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8d99a-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8d99a-129">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8d99a-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="8d99a-130">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="8d99a-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d99a-131">Notes</span><span class="sxs-lookup"><span data-stu-id="8d99a-131">Remarks</span></span>

<span data-ttu-id="8d99a-132">La zone créé est centrée à l’origine.</span><span class="sxs-lookup"><span data-stu-id="8d99a-132">The created box is centered at the origin.</span></span>

<span data-ttu-id="8d99a-133">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="8d99a-133">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="8d99a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d99a-134">Requirements</span></span>



| <span data-ttu-id="8d99a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d99a-135">Requirement</span></span> | <span data-ttu-id="8d99a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d99a-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d99a-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d99a-137">Header</span></span><br/>  | <dl> <span data-ttu-id="8d99a-138"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d99a-138"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="8d99a-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="8d99a-139">Library</span></span><br/> | <dl> <span data-ttu-id="8d99a-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8d99a-140"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="8d99a-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="8d99a-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8d99a-142">Fonctions de dessin de forme</span><span class="sxs-lookup"><span data-stu-id="8d99a-142">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
