---
description: Décrit une mémoire tampon de vertex.
ms.assetid: 0ae8f976-d0ca-4d55-b6db-5be85fa3c799
title: Structure D3DVERTEXBUFFER_DESC (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DVERTEXBUFFER_DESC
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: b2c0838743f8190eeb0e5c825e7125d2e48c0b6c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530987"
---
# <a name="d3dvertexbuffer_desc-structure"></a><span data-ttu-id="9d6f5-103">D3DVERTEXBUFFER \_ desc, structure</span><span class="sxs-lookup"><span data-stu-id="9d6f5-103">D3DVERTEXBUFFER\_DESC structure</span></span>

<span data-ttu-id="9d6f5-104">Décrit une mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="9d6f5-104">Describes a vertex buffer.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d6f5-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d6f5-105">Syntax</span></span>


```C++
typedef struct D3DVERTEXBUFFER_DESC {
  D3DFORMAT       Format;
  D3DRESOURCETYPE Type;
  DWORD           Usage;
  D3DPOOL         Pool;
  UINT            Size;
  DWORD           FVF;
} D3DVERTEXBUFFER_DESC, *LPD3DVERTEXBUFFER_DESC;
```



## <a name="members"></a><span data-ttu-id="9d6f5-106">Membres</span><span class="sxs-lookup"><span data-stu-id="9d6f5-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d6f5-107">**Format**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-107">**Format**</span></span>
</dt> <dd>

<span data-ttu-id="9d6f5-108">Type : **[D3DFORMAT](d3dformat.md)**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-108">Type: **[D3DFORMAT](d3dformat.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d6f5-109">Membre du type énuméré [D3DFORMAT](d3dformat.md) , décrivant le format de surface des données de la mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="9d6f5-109">Member of the [D3DFORMAT](d3dformat.md) enumerated type, describing the surface format of the vertex buffer data.</span></span>

</dd> <dt>

<span data-ttu-id="9d6f5-110">**Type**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-110">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="9d6f5-111">Type : **[ **D3DRESOURCETYPE**](./d3dresourcetype.md)**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-111">Type: **[**D3DRESOURCETYPE**](./d3dresourcetype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d6f5-112">Membre du type énuméré [**D3DRESOURCETYPE**](./d3dresourcetype.md) , identifiant cette ressource comme une mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="9d6f5-112">Member of the [**D3DRESOURCETYPE**](./d3dresourcetype.md) enumerated type, identifying this resource as a vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9d6f5-113">**Utilisation**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-113">**Usage**</span></span>
</dt> <dd>

<span data-ttu-id="9d6f5-114">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d6f5-115">Combinaison d’un ou plusieurs indicateurs [**D3DUSAGE**](d3dusage.md) .</span><span class="sxs-lookup"><span data-stu-id="9d6f5-115">Combination of one or more [**D3DUSAGE**](d3dusage.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="9d6f5-116">**Pool**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-116">**Pool**</span></span>
</dt> <dd>

<span data-ttu-id="9d6f5-117">Type : **[ **D3DPOOL**](./d3dpool.md)**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-117">Type: **[**D3DPOOL**](./d3dpool.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d6f5-118">Membre du type énuméré [**D3DPOOL**](./d3dpool.md) , spécifiant la classe de mémoire allouée pour cette mémoire tampon de vertex.</span><span class="sxs-lookup"><span data-stu-id="9d6f5-118">Member of the [**D3DPOOL**](./d3dpool.md) enumerated type, specifying the class of memory allocated for this vertex buffer.</span></span>

</dd> <dt>

<span data-ttu-id="9d6f5-119">**Taille**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-119">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="9d6f5-120">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-120">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d6f5-121">Taille de la mémoire tampon de vertex, en octets.</span><span class="sxs-lookup"><span data-stu-id="9d6f5-121">Size of the vertex buffer, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="9d6f5-122">**CLOS**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-122">**FVF**</span></span>
</dt> <dd>

<span data-ttu-id="9d6f5-123">Type : **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-123">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="9d6f5-124">Combinaison de [D3DFVF](d3dfvf.md) qui décrit le format de vertex des vertex dans cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="9d6f5-124">Combination of [D3DFVF](d3dfvf.md) that describes the vertex format of the vertices in this buffer.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d6f5-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d6f5-125">Requirements</span></span>



| <span data-ttu-id="9d6f5-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d6f5-126">Requirement</span></span> | <span data-ttu-id="9d6f5-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d6f5-127">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d6f5-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d6f5-128">Header</span></span><br/> | <dl> <span data-ttu-id="9d6f5-129"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d6f5-129"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d6f5-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d6f5-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6f5-131">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="9d6f5-131">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="9d6f5-132">**GetDesc**</span><span class="sxs-lookup"><span data-stu-id="9d6f5-132">**GetDesc**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dvertexbuffer9-getdesc)
</dt> <dt>

[<span data-ttu-id="9d6f5-133">Mémoires tampons de vertex (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="9d6f5-133">Vertex Buffers (Direct3D 9)</span></span>](vertex-buffers.md)
</dt> </dl>

 

 
