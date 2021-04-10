---
description: Utilise un système de coordonnées droitier pour créer une maille contenant un cylindre.
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: D3DXCreateCylinder, fonction (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762091"
---
# <a name="d3dxcreatecylinder-function"></a><span data-ttu-id="1d160-103">D3DXCreateCylinder fonction)</span><span class="sxs-lookup"><span data-stu-id="1d160-103">D3DXCreateCylinder function</span></span>

<span data-ttu-id="1d160-104">Utilise un système de coordonnées droitier pour créer une maille contenant un cylindre.</span><span class="sxs-lookup"><span data-stu-id="1d160-104">Uses a left-handed coordinate system to create a mesh containing a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d160-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1d160-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="1d160-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="1d160-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d160-107">*pDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d160-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-108">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1d160-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1d160-109">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , représentant l’appareil associé au maillage de cylindre créé.</span><span class="sxs-lookup"><span data-stu-id="1d160-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created cylinder mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1d160-110">*Radius1* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d160-110">*Radius1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d160-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d160-112">Rayon à l’extrémité Z négative.</span><span class="sxs-lookup"><span data-stu-id="1d160-112">Radius at the negative Z end.</span></span> <span data-ttu-id="1d160-113">La valeur doit être supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="1d160-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1d160-114">*Radius2* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d160-114">*Radius2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d160-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d160-116">Rayon à l’extrémité Z positive.</span><span class="sxs-lookup"><span data-stu-id="1d160-116">Radius at the positive Z end.</span></span> <span data-ttu-id="1d160-117">La valeur doit être supérieure ou égale à 0.0 f.</span><span class="sxs-lookup"><span data-stu-id="1d160-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1d160-118">*Longueur* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d160-118">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-119">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d160-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d160-120">Longueur du cylindre le long de l’axe z.</span><span class="sxs-lookup"><span data-stu-id="1d160-120">Length of the cylinder along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1d160-121">*Tranches* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d160-121">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d160-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d160-123">Nombre de tranches relatives à l’axe principal.</span><span class="sxs-lookup"><span data-stu-id="1d160-123">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="1d160-124">*Piles* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="1d160-124">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-125">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1d160-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1d160-126">Nombre de piles le long de l’axe principal.</span><span class="sxs-lookup"><span data-stu-id="1d160-126">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="1d160-127">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d160-127">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-128">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d160-128">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1d160-129">Adresse d’un pointeur vers la forme de sortie, une interface [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="1d160-129">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1d160-130">*ppAdjacency* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="1d160-130">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d160-131">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1d160-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1d160-132">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1d160-132">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="1d160-133">Quand la méthode est retournée, ce paramètre est rempli avec un tableau de trois DWORDs par visage qui spécifient les trois voisins pour chaque visage de la maille.</span><span class="sxs-lookup"><span data-stu-id="1d160-133">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="1d160-134">La **valeur null** peut être spécifiée.</span><span class="sxs-lookup"><span data-stu-id="1d160-134">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d160-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="1d160-135">Return value</span></span>

<span data-ttu-id="1d160-136">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1d160-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1d160-137">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="1d160-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1d160-138">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1d160-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d160-139">Notes</span><span class="sxs-lookup"><span data-stu-id="1d160-139">Remarks</span></span>

<span data-ttu-id="1d160-140">Le cylindre créé est centré au niveau de l’origine et son axe est aligné avec l’axe z.</span><span class="sxs-lookup"><span data-stu-id="1d160-140">The created cylinder is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="1d160-141">Cette fonction crée une maille avec l' \_ option de création managée D3DXMESH et [D3DFVF \_ xyz \| D3DFVF \_ ](d3dfvf.md) le format de vertex flexible normal.</span><span class="sxs-lookup"><span data-stu-id="1d160-141">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="1d160-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1d160-142">Requirements</span></span>



| <span data-ttu-id="1d160-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1d160-143">Requirement</span></span> | <span data-ttu-id="1d160-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="1d160-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d160-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="1d160-145">Header</span></span><br/>  | <dl> <span data-ttu-id="1d160-146"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d160-146"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="1d160-147">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="1d160-147">Library</span></span><br/> | <dl> <span data-ttu-id="1d160-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1d160-148"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1d160-149">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1d160-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d160-150">Fonctions de dessin de forme</span><span class="sxs-lookup"><span data-stu-id="1d160-150">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
