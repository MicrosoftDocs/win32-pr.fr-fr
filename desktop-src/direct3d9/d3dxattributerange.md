---
description: 'Structure D3DXATTRIBUTERANGE : stocke une entrée de table d’attributs.'
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
ms.openlocfilehash: 7dfdf15f653fda77b1ca8c9a14cd32decee9658e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116007"
---
# <a name="d3dxattributerange-structure"></a><span data-ttu-id="53d24-103">D3DXATTRIBUTERANGE, structure</span><span class="sxs-lookup"><span data-stu-id="53d24-103">D3DXATTRIBUTERANGE structure</span></span>

<span data-ttu-id="53d24-104">Stocke une entrée de table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="53d24-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="53d24-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53d24-105">Syntax</span></span>


```C++
typedef struct D3DXATTRIBUTERANGE {
  DWORD AttribId;
  DWORD FaceStart;
  DWORD FaceCount;
  DWORD VertexStart;
  DWORD VertexCount;
} D3DXATTRIBUTERANGE, *LPD3DXATTRIBUTERANGE;
```



## <a name="members"></a><span data-ttu-id="53d24-106">Membres</span><span class="sxs-lookup"><span data-stu-id="53d24-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="53d24-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="53d24-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="53d24-108">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53d24-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53d24-109">Identificateur de la table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="53d24-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="53d24-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="53d24-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="53d24-111">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53d24-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53d24-112">Début de la face.</span><span class="sxs-lookup"><span data-stu-id="53d24-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="53d24-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="53d24-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="53d24-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53d24-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53d24-115">Nombre de visages.</span><span class="sxs-lookup"><span data-stu-id="53d24-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="53d24-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="53d24-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="53d24-117">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53d24-117">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53d24-118">Sommet de départ.</span><span class="sxs-lookup"><span data-stu-id="53d24-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="53d24-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="53d24-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="53d24-120">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53d24-120">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="53d24-121">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="53d24-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="53d24-122">Notes </span><span class="sxs-lookup"><span data-stu-id="53d24-122">Remarks</span></span>

<span data-ttu-id="53d24-123">Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc.</span><span class="sxs-lookup"><span data-stu-id="53d24-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="53d24-124">En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas un identificateur d’attribut (AttribId) donné lors du dessin du frame.</span><span class="sxs-lookup"><span data-stu-id="53d24-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="53d24-125">Le type LPD3DXATTRIBUTERANGE est défini en tant que pointeur vers la structure **D3DXATTRIBUTERANGE** .</span><span class="sxs-lookup"><span data-stu-id="53d24-125">The LPD3DXATTRIBUTERANGE type is defined as a pointer to the **D3DXATTRIBUTERANGE** structure.</span></span>


```
typedef D3DXATTRIBUTERANGE* LPD3DXATTRIBUTERANGE;
```



## <a name="requirements"></a><span data-ttu-id="53d24-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53d24-126">Requirements</span></span>



| <span data-ttu-id="53d24-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53d24-127">Requirement</span></span> | <span data-ttu-id="53d24-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="53d24-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53d24-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="53d24-129">Header</span></span><br/> | <dl> <span data-ttu-id="53d24-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="53d24-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53d24-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53d24-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53d24-132">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="53d24-132">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> </dl>

 

 
