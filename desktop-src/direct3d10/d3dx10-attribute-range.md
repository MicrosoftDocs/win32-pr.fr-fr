---
description: Stocke une entrée de table d’attributs.
ms.assetid: 81c77dc9-e078-46a1-a435-4b241e36ec13
title: Structure D3DX10_ATTRIBUTE_RANGE (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_ATTRIBUTE_RANGE
api_type:
- HeaderDef
api_location:
- D3DX10.h
ms.openlocfilehash: ddf7f10882e08232467130b3abbc6fb723a843ed
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106531357"
---
# <a name="d3dx10_attribute_range-structure"></a><span data-ttu-id="21c7c-103">Structure de la \_ plage d’attributs d3dx10 \_</span><span class="sxs-lookup"><span data-stu-id="21c7c-103">D3DX10\_ATTRIBUTE\_RANGE structure</span></span>

<span data-ttu-id="21c7c-104">Stocke une entrée de table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="21c7c-104">Stores an attribute table entry.</span></span>

## <a name="syntax"></a><span data-ttu-id="21c7c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="21c7c-105">Syntax</span></span>


```C++
typedef struct D3DX10_ATTRIBUTE_RANGE {
  UINT AttribId;
  UINT FaceStart;
  UINT FaceCount;
  UINT VertexStart;
  UINT VertexCount;
} D3DX10_ATTRIBUTE_RANGE, *LPD3DX10_ATTRIBUTE_RANGE;
```



## <a name="members"></a><span data-ttu-id="21c7c-106">Membres</span><span class="sxs-lookup"><span data-stu-id="21c7c-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="21c7c-107">**AttribId**</span><span class="sxs-lookup"><span data-stu-id="21c7c-107">**AttribId**</span></span>
</dt> <dd>

<span data-ttu-id="21c7c-108">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c7c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="21c7c-109">Identificateur de la table d’attributs.</span><span class="sxs-lookup"><span data-stu-id="21c7c-109">Attribute table identifier.</span></span>

</dd> <dt>

<span data-ttu-id="21c7c-110">**FaceStart**</span><span class="sxs-lookup"><span data-stu-id="21c7c-110">**FaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="21c7c-111">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c7c-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="21c7c-112">Début de la face.</span><span class="sxs-lookup"><span data-stu-id="21c7c-112">Starting face.</span></span>

</dd> <dt>

<span data-ttu-id="21c7c-113">**FaceCount**</span><span class="sxs-lookup"><span data-stu-id="21c7c-113">**FaceCount**</span></span>
</dt> <dd>

<span data-ttu-id="21c7c-114">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c7c-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="21c7c-115">Nombre de visages.</span><span class="sxs-lookup"><span data-stu-id="21c7c-115">Face count.</span></span>

</dd> <dt>

<span data-ttu-id="21c7c-116">**VertexStart**</span><span class="sxs-lookup"><span data-stu-id="21c7c-116">**VertexStart**</span></span>
</dt> <dd>

<span data-ttu-id="21c7c-117">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c7c-117">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="21c7c-118">Sommet de départ.</span><span class="sxs-lookup"><span data-stu-id="21c7c-118">Starting vertex.</span></span>

</dd> <dt>

<span data-ttu-id="21c7c-119">**VertexCount**</span><span class="sxs-lookup"><span data-stu-id="21c7c-119">**VertexCount**</span></span>
</dt> <dd>

<span data-ttu-id="21c7c-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="21c7c-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="21c7c-121">Nombre de vertex.</span><span class="sxs-lookup"><span data-stu-id="21c7c-121">Vertex count.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="21c7c-122">Notes</span><span class="sxs-lookup"><span data-stu-id="21c7c-122">Remarks</span></span>

<span data-ttu-id="21c7c-123">Une table d’attributs permet d’identifier les zones de la maille qui doivent être dessinées avec différentes textures, États de rendu, matériaux, etc.</span><span class="sxs-lookup"><span data-stu-id="21c7c-123">An attribute table is used to identify areas of the mesh that need to be drawn with different textures, render states, materials, and so on.</span></span> <span data-ttu-id="21c7c-124">En outre, l’application peut utiliser la table d’attributs pour masquer des parties d’un maillage en ne dessinant pas un identificateur d’attribut (AttribId) donné lors du dessin du frame.</span><span class="sxs-lookup"><span data-stu-id="21c7c-124">In addition, the application can use the attribute table to hide portions of a mesh by not drawing a given attribute identifier (AttribId) when drawing the frame.</span></span>

<span data-ttu-id="21c7c-125">Le \_ type de \_ plage d’attributs LPD3DX est défini en tant que pointeur vers la \_ structure de plage d’attributs D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="21c7c-125">The LPD3DX\_ATTRIBUTE\_RANGE type is defined as a pointer to the D3DX\_ATTRIBUTE\_RANGE structure.</span></span>


```
typedef D3DX_ATTRIBUTE_RANGE* LPD3DX_ATTRIBUTE_RANGE;
```



## <a name="requirements"></a><span data-ttu-id="21c7c-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="21c7c-126">Requirements</span></span>



| <span data-ttu-id="21c7c-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="21c7c-127">Requirement</span></span> | <span data-ttu-id="21c7c-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="21c7c-128">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21c7c-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="21c7c-129">Header</span></span><br/> | <dl> <span data-ttu-id="21c7c-130"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="21c7c-130"><dt>D3DX10.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21c7c-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="21c7c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21c7c-132">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="21c7c-132">D3DX Structures</span></span>](d3d10-graphics-reference-d3dx10-structures.md)
</dt> </dl>

 

 
