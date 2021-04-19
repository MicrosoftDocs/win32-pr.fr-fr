---
description: Crée un objet de maillage à l’aide d’un code de format de vertex flexible.
ms.assetid: 4681f181-8a16-42d4-bbfa-bdee5ed69fd3
title: D3DXCreateMeshFVF, fonction (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateMeshFVF
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9d5589b0f02bfcb85f9c0f0dc4dc5de69e2fb23
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106535841"
---
# <a name="d3dxcreatemeshfvf-function"></a><span data-ttu-id="c515f-103">D3DXCreateMeshFVF fonction)</span><span class="sxs-lookup"><span data-stu-id="c515f-103">D3DXCreateMeshFVF function</span></span>

<span data-ttu-id="c515f-104">Crée un objet de maillage à l’aide d’un code de format de vertex flexible.</span><span class="sxs-lookup"><span data-stu-id="c515f-104">Creates a mesh object using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="c515f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c515f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateMeshFVF(
  _In_  DWORD             NumFaces,
  _In_  DWORD             NumVertices,
  _In_  DWORD             Options,
  _In_  DWORD             FVF,
  _In_  LPDIRECT3DDEVICE9 pD3DDevice,
  _Out_ LPD3DXMESH        *ppMesh
);
```



## <a name="parameters"></a><span data-ttu-id="c515f-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c515f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c515f-107">*NumFaces* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c515f-107">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c515f-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c515f-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c515f-109">Nombre de faces de la maille.</span><span class="sxs-lookup"><span data-stu-id="c515f-109">Number of faces for the mesh.</span></span> <span data-ttu-id="c515f-110">La plage valide pour ce nombre est supérieure à 0, et une valeur inférieure à la valeur DWORD Max, généralement 2 ³ ²-1, car le dernier index est réservé.</span><span class="sxs-lookup"><span data-stu-id="c515f-110">The valid range for this number is greater than 0, and one less than the max DWORD value, typically 2³² - 1, because the last index is reserved.</span></span>

</dd> <dt>

<span data-ttu-id="c515f-111">*NumVertices* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c515f-111">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c515f-112">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c515f-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c515f-113">Nombre de vertex pour le maillage.</span><span class="sxs-lookup"><span data-stu-id="c515f-113">Number of vertices for the mesh.</span></span> <span data-ttu-id="c515f-114">Ce paramètre doit être supérieur à 0.</span><span class="sxs-lookup"><span data-stu-id="c515f-114">This parameter must be greater than 0.</span></span>

</dd> <dt>

<span data-ttu-id="c515f-115">*Options* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c515f-115">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c515f-116">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c515f-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c515f-117">Combinaison d’un ou de plusieurs indicateurs de l’énumération [**D3DXMESH**](./d3dxmesh.md) , en spécifiant les options de création du maillage.</span><span class="sxs-lookup"><span data-stu-id="c515f-117">Combination of one or more flags from the [**D3DXMESH**](./d3dxmesh.md) enumeration, specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c515f-118">*Commission* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c515f-118">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c515f-119">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c515f-119">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c515f-120">Combinaison de [D3DFVF](d3dfvf.md) qui décrit le format de vertex pour le maillage retourné.</span><span class="sxs-lookup"><span data-stu-id="c515f-120">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format for the returned mesh.</span></span> <span data-ttu-id="c515f-121">Cette fonction ne prend pas en charge D3DFVF \_ XYZRHW.</span><span class="sxs-lookup"><span data-stu-id="c515f-121">This function does not support D3DFVF\_XYZRHW.</span></span>

</dd> <dt>

<span data-ttu-id="c515f-122">*pD3DDevice* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c515f-122">*pD3DDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c515f-123">Type : **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="c515f-123">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="c515f-124">Pointeur vers une interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , l’objet appareil à associer à la maille.</span><span class="sxs-lookup"><span data-stu-id="c515f-124">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, the device object to be associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="c515f-125">*ppMesh* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c515f-125">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c515f-126">Type : **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="c515f-126">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="c515f-127">Adresse d’un pointeur vers une interface [**ID3DXMesh**](id3dxmesh.md) représentant l’objet de maillage créé.</span><span class="sxs-lookup"><span data-stu-id="c515f-127">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the created mesh object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c515f-128">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c515f-128">Return value</span></span>

<span data-ttu-id="c515f-129">Type : **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c515f-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c515f-130">Si la fonction est réussie, la valeur de retour est D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c515f-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c515f-131">Si la fonction échoue, la valeur de retour peut être l’une des suivantes : D3DERR \_ INVALIDCALL, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="c515f-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="requirements"></a><span data-ttu-id="c515f-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c515f-132">Requirements</span></span>



| <span data-ttu-id="c515f-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c515f-133">Requirement</span></span> | <span data-ttu-id="c515f-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="c515f-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c515f-135">En-tête</span><span class="sxs-lookup"><span data-stu-id="c515f-135">Header</span></span><br/>  | <dl> <span data-ttu-id="c515f-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c515f-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="c515f-137">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="c515f-137">Library</span></span><br/> | <dl> <span data-ttu-id="c515f-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c515f-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="c515f-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c515f-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c515f-140">Fonctions de maillage</span><span class="sxs-lookup"><span data-stu-id="c515f-140">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> <dt>

[<span data-ttu-id="c515f-141">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="c515f-141">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
