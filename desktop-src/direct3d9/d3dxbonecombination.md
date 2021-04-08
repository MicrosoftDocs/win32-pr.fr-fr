---
description: Décrit un sous-ensemble de la maille qui a la même combinaison d’attributs et de segments.
ms.assetid: e6a4b3bb-d28d-44c2-a6df-f60f0412a70e
title: D3DXBONECOMBINATION, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXBONECOMBINATION
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: 3553ba37d0d9376fa5912143fb58849f03c5a83a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104043121"
---
# <a name="d3dxbonecombination-structure"></a><span data-ttu-id="c9261-103">D3DXBONECOMBINATION, structure</span><span class="sxs-lookup"><span data-stu-id="c9261-103">D3DXBONECOMBINATION structure</span></span>

<span data-ttu-id="c9261-104">Décrit un sous-ensemble de la maille qui a la même combinaison d’attributs et de segments.</span><span class="sxs-lookup"><span data-stu-id="c9261-104">Describes a subset of the mesh that has the same attribute and bone combination.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9261-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9261-105">Syntax</span></span>


```C++
typedef struct D3DXBONECOMBINATION {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
  DWORD *BoneId;
} D3DXBONECOMBINATION, *LPD3DXBONECOMBINATION;
```



## <a name="members"></a><span data-ttu-id="c9261-106">Membres</span><span class="sxs-lookup"><span data-stu-id="c9261-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="c9261-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="c9261-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="c9261-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9261-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9261-109">Identificateur de la table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c9261-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="c9261-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="c9261-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="c9261-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9261-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9261-112">Début de la face.</span><span class="sxs-lookup"><span data-stu-id="c9261-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="c9261-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="c9261-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="c9261-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9261-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9261-115">Nombre de visages.</span><span class="sxs-lookup"><span data-stu-id="c9261-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="c9261-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="c9261-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="c9261-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9261-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9261-118">Sommet de départ.</span><span class="sxs-lookup"><span data-stu-id="c9261-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="c9261-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="c9261-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="c9261-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c9261-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c9261-121">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="c9261-121">Vertex count.</span></span>

</dd> <dt>

<span data-ttu-id="c9261-122">**BoneId**</span><span class="sxs-lookup"><span data-stu-id="c9261-122">**BoneId**</span></span>
</dt> <dd>

<span data-ttu-id="c9261-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="c9261-123">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

</dd> <dd>

<span data-ttu-id="c9261-124">Pointeur vers un tableau de valeurs qui identifient chacun des segments qui peuvent être dessinés dans un appel de dessin unique.</span><span class="sxs-lookup"><span data-stu-id="c9261-124">Pointer to an array of values that identify each of the bones that can be drawn in a single drawing call.</span></span> <span data-ttu-id="c9261-125">Notez que le tableau peut être de longueur variable pour prendre en charge les combinaisons de longueur variable des segments de [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span><span class="sxs-lookup"><span data-stu-id="c9261-125">Note that the array can be of variable length to accommodate variable length bone combinations of [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md).</span></span>

<span data-ttu-id="c9261-126">La taille du tableau varie en fonction du type de maillage généré.</span><span class="sxs-lookup"><span data-stu-id="c9261-126">The size of the array varies based on the type of mesh generated.</span></span> <span data-ttu-id="c9261-127">Une taille de tableau de maillage non indexée est égale au nombre de poids par vertex (pMaxVertexInfl dans [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="c9261-127">A non-indexed mesh array size is equal to the number of weights per vertex (pMaxVertexInfl in [**ConvertToBlendedMesh**](id3dxskininfo--converttoblendedmesh.md)).</span></span> <span data-ttu-id="c9261-128">La taille d’un tableau de maillage indexé est égale au nombre d’entrées de palette de matrices osseuses (paletteSize dans [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span><span class="sxs-lookup"><span data-stu-id="c9261-128">An indexed mesh array size is equal to the number of bone matrix palette entries (paletteSize in [**ConvertToIndexedBlendedMesh**](id3dxskininfo--converttoindexedblendedmesh.md)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9261-129">Notes</span><span class="sxs-lookup"><span data-stu-id="c9261-129">Remarks</span></span>

<span data-ttu-id="c9261-130">Le sous-ensemble de la maille décrit par **D3DXBONECOMBINATION** peut être rendu dans un appel de dessin unique.</span><span class="sxs-lookup"><span data-stu-id="c9261-130">The subset of the mesh described by **D3DXBONECOMBINATION** can be rendered in a single drawing call.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9261-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9261-131">Requirements</span></span>



| <span data-ttu-id="c9261-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9261-132">Requirement</span></span> | <span data-ttu-id="c9261-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9261-133">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9261-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9261-134">Header</span></span><br/> | <dl> <span data-ttu-id="c9261-135"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9261-135"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9261-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9261-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9261-137">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="c9261-137">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
