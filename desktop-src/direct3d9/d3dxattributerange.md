---
description: Stocke une entrée de table d’attributs.
ms.assetid: b9f13b12-35ba-4e4c-93ac-3dd44d611b47
title: D3DXATTRIBUTERANGE, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXATTRIBUTERANGE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a842bbf41847f4b4e65c975e11f3e160cea1422d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106523197"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="f4633-103">D3DXATTRIBUTERANGE, structure</span><span class="sxs-lookup"><span data-stu-id="f4633-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="f4633-104">Stocke une entrée de table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="f4633-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4633-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4633-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="f4633-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f4633-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="f4633-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="f4633-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="f4633-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4633-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4633-109">Identificateur de la table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="f4633-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f4633-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="f4633-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="f4633-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4633-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4633-112">Début de la face.</span><span class="sxs-lookup"><span data-stu-id="f4633-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="f4633-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="f4633-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="f4633-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4633-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4633-115">Nombre de visages.</span><span class="sxs-lookup"><span data-stu-id="f4633-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="f4633-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="f4633-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="f4633-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4633-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4633-118">Sommet de départ.</span><span class="sxs-lookup"><span data-stu-id="f4633-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="f4633-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="f4633-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="f4633-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f4633-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="f4633-121">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="f4633-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4633-122">Notes</span><span class="sxs-lookup"><span data-stu-id="f4633-122">Remarks</span></span>

<span data-ttu-id="f4633-123">Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc.</span><span class="sxs-lookup"><span data-stu-id="f4633-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="f4633-124">En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas un identificateur d’attribut (AttribId) donné lors du dessin du frame.</span><span class="sxs-lookup"><span data-stu-id="f4633-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="f4633-125">Le type LPD3DXATTRIBUTERANGE est défini en tant que pointeur vers la structure **D3DXATTRIBUTERANGE** .</span><span class="sxs-lookup"><span data-stu-id="f4633-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="f4633-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4633-126">Requirements</span></span>



| <span data-ttu-id="f4633-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4633-127">Requirement</span></span> | <span data-ttu-id="f4633-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4633-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4633-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="f4633-129">Header</span></span><br/> | <dl> <span data-ttu-id="f4633-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4633-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4633-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4633-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4633-132">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="f4633-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
