---
description: Tessellates la maille donnée à l’aide du schéma de pavage N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: D3DXTessellateNPatches, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523817"
---
# <a name="d3dxtessellatenpatches-function"></a><span data-ttu-id="11319-103">D3DXTessellateNPatches fonction)</span><span class="sxs-lookup"><span data-stu-id="11319-103">D3DXTessellateNPatches function</span></span>

<span data-ttu-id="11319-104">Tessellates la maille donnée à l’aide du schéma de pavage N-patch.</span><span class="sxs-lookup"><span data-stu-id="11319-104">Tessellates the given mesh using the N-patch tessellation scheme.</span></span>

## <a name="syntax"></a><span data-ttu-id="11319-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="11319-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a><span data-ttu-id="11319-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="11319-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11319-107">*pMeshIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11319-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11319-108">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="11319-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="11319-109">Pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) , qui représente le maillage à paver.</span><span class="sxs-lookup"><span data-stu-id="11319-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="11319-110">*pAdjacencyIn* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11319-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11319-111">Type : **const const DWORD \***</span><span class="sxs-lookup"><span data-stu-id="11319-111">Type: **const CONST DWORD\***</span></span>

<span data-ttu-id="11319-112">Pointeur vers un tableau de trois DWORD par visage qui spécifient les trois voisins pour chaque visage dans le maillage source.</span><span class="sxs-lookup"><span data-stu-id="11319-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="11319-113">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="11319-113">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11319-114">*NumSegs* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11319-114">*NumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11319-115">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11319-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11319-116">Nombre de segments par périphérie à paver.</span><span class="sxs-lookup"><span data-stu-id="11319-116">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="11319-117">*QuadraticInterpNormals* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="11319-117">*QuadraticInterpNormals* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11319-118">Type : **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="11319-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="11319-119">Affectez la valeur **true** pour utiliser l’interpolation quadratique pour les normales ; Affectez la valeur **false** à l’interpolation linéaire.</span><span class="sxs-lookup"><span data-stu-id="11319-119">Set to **TRUE** to use quadratic interpolation for normals; set to **FALSE** for linear interpolation.</span></span>

</dd> <dt>

<span data-ttu-id="11319-120">*ppMeshOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11319-120">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11319-121">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="11319-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="11319-122">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant le maillage fractionné retourné.</span><span class="sxs-lookup"><span data-stu-id="11319-122">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned tessellated mesh.</span></span>

</dd> <dt>

<span data-ttu-id="11319-123">*ppAdjacencyOut* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="11319-123">*ppAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11319-124">Type : **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="11319-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="11319-125">Adresse d’un pointeur vers une interface [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="11319-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="11319-126">Si la valeur de ce paramètre n’est pas définie sur **null**, cette mémoire tampon contient un tableau de trois DWORDS par visage qui spécifient les trois voisins pour chaque visage dans le maillage de sortie.</span><span class="sxs-lookup"><span data-stu-id="11319-126">If the value of this parameter is not set to **NULL**, this buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="11319-127">Ce paramètre peut avoir la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="11319-127">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11319-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="11319-128">Return value</span></span>

<span data-ttu-id="11319-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="11319-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="11319-130">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="11319-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="11319-131">Si la fonction échoue, la valeur de retour peut être l’une des valeurs suivantes : D3DERR \_ INVALIDCALL, D3DXERR \_ sera déplacé, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="11319-131">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="11319-132">Notes</span><span class="sxs-lookup"><span data-stu-id="11319-132">Remarks</span></span>

<span data-ttu-id="11319-133">Cette fonction tessellates à l’aide de l’algorithme N-patch.</span><span class="sxs-lookup"><span data-stu-id="11319-133">This function tessellates by using the N-patch algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="11319-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="11319-134">Requirements</span></span>



| <span data-ttu-id="11319-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="11319-135">Requirement</span></span> | <span data-ttu-id="11319-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="11319-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="11319-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="11319-137">Header</span></span><br/>  | <dl> <span data-ttu-id="11319-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="11319-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="11319-139">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="11319-139">Library</span></span><br/> | <dl> <span data-ttu-id="11319-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11319-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="11319-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="11319-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11319-142">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="11319-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
