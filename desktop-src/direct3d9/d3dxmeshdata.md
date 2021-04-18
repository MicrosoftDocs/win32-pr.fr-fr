---
description: Structure des données de maillage.
ms.assetid: 9164b956-95b7-4bc0-bf7e-feed2e3b4a2b
title: D3DXMESHDATA, structure (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMESHDATA
api_type:
- HeaderDef
api_location:
- D3dx9anim.h
ms.openlocfilehash: 785284ba1330c957813a099eb6cf1c74521d3c90
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104322646"
---
# <a name="d3dxmeshdata-structure"></a><span data-ttu-id="1ff03-103">D3DXMESHDATA, structure</span><span class="sxs-lookup"><span data-stu-id="1ff03-103">D3DXMESHDATA structure</span></span>

<span data-ttu-id="1ff03-104">Structure des données de maillage.</span><span class="sxs-lookup"><span data-stu-id="1ff03-104">Mesh data structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ff03-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="1ff03-105">Syntax</span></span>


```C++
typedef struct D3DXMESHDATA {
  D3DXMESHDATATYPE Type;
  union {
    LPD3DXMESH      pMesh;
    LPD3DXPATCHMESH pPatchMesh;
  };
} D3DXMESHDATA, *LPD3DXMESHDATA;
```



## <a name="members"></a><span data-ttu-id="1ff03-106">Membres</span><span class="sxs-lookup"><span data-stu-id="1ff03-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1ff03-107">**Type**</span><span class="sxs-lookup"><span data-stu-id="1ff03-107">**Type**</span></span>
</dt> <dd>

<span data-ttu-id="1ff03-108">Type : **[ **D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span><span class="sxs-lookup"><span data-stu-id="1ff03-108">Type: **[**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1ff03-109">Définit le type de données de maillage.</span><span class="sxs-lookup"><span data-stu-id="1ff03-109">Defines the mesh data type.</span></span> <span data-ttu-id="1ff03-110">Consultez [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span><span class="sxs-lookup"><span data-stu-id="1ff03-110">See [**D3DXMESHDATATYPE**](./d3dxmeshdatatype.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ff03-111">**pMesh**</span><span class="sxs-lookup"><span data-stu-id="1ff03-111">**pMesh**</span></span>
</dt> <dd>

<span data-ttu-id="1ff03-112">Type : **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="1ff03-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

</dd> <dd>

<span data-ttu-id="1ff03-113">Pointeur vers une maille.</span><span class="sxs-lookup"><span data-stu-id="1ff03-113">Pointer to a mesh.</span></span> <span data-ttu-id="1ff03-114">Consultez [**ID3DXMesh**](id3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="1ff03-114">See [**ID3DXMesh**](id3dxmesh.md).</span></span>

</dd> <dt>

<span data-ttu-id="1ff03-115">**pPatchMesh**</span><span class="sxs-lookup"><span data-stu-id="1ff03-115">**pPatchMesh**</span></span>
</dt> <dd>

<span data-ttu-id="1ff03-116">Type : **LPD3DXPATCHMESH**</span><span class="sxs-lookup"><span data-stu-id="1ff03-116">Type: **LPD3DXPATCHMESH**</span></span>

</dd> <dd>

<span data-ttu-id="1ff03-117">Pointeur vers un filet de correction.</span><span class="sxs-lookup"><span data-stu-id="1ff03-117">Pointer to a patch mesh.</span></span> <span data-ttu-id="1ff03-118">Consultez [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span><span class="sxs-lookup"><span data-stu-id="1ff03-118">See [**ID3DXPatchMesh**](id3dxpatchmesh.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1ff03-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="1ff03-119">Requirements</span></span>



| <span data-ttu-id="1ff03-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="1ff03-120">Requirement</span></span> | <span data-ttu-id="1ff03-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="1ff03-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ff03-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="1ff03-122">Header</span></span><br/> | <dl> <span data-ttu-id="1ff03-123"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ff03-123"><dt>D3dx9anim.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ff03-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="1ff03-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ff03-125">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="1ff03-125">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="1ff03-126">**D3DXMESHCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="1ff03-126">**D3DXMESHCONTAINER**</span></span>](d3dxmeshcontainer.md)
</dt> </dl>

 

 
