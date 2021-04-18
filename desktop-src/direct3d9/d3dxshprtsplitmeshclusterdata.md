---
description: D3DXSHPRTSPLITMESHCLUSTERDATA, structure
ms.assetid: 6a53420c-06bc-4f52-ac2e-5adda5e34cb2
title: D3DXSHPRTSPLITMESHCLUSTERDATA, structure (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHPRTSPLITMESHCLUSTERDATA
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: e7b1bc23606dbf08f5a924860e12c9c09d719287
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106522947"
---
# <a name="d3dxshprtsplitmeshclusterdata-structure"></a><span data-ttu-id="e3ab1-103">D3DXSHPRTSPLITMESHCLUSTERDATA, structure</span><span class="sxs-lookup"><span data-stu-id="e3ab1-103">D3DXSHPRTSPLITMESHCLUSTERDATA structure</span></span>

## <a name="syntax"></a><span data-ttu-id="e3ab1-104">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e3ab1-104">Syntax</span></span>


```C++
typedef struct D3DXSHPRTSPLITMESHCLUSTERDATA {
  UINT uVertStart;
  UINT uVertLength;
  UINT uFaceStart;
  UINT uFaceLength;
  UINT uClusterStart;
  UINT uClusterLength;
} D3DXSHPRTSPLITMESHCLUSTERDATA, *LPD3DXSHPRTSPLITMESHCLUSTERDATA;
```



## <a name="members"></a><span data-ttu-id="e3ab1-105">Membres</span><span class="sxs-lookup"><span data-stu-id="e3ab1-105">Members</span></span>

<dl> <dt>

<span data-ttu-id="e3ab1-106">**uVertStart**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-106">**uVertStart**</span></span>
</dt> <dd>

<span data-ttu-id="e3ab1-107">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-107">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3ab1-108">Sommet initial dans le tableau de vertex remappé.</span><span class="sxs-lookup"><span data-stu-id="e3ab1-108">Initial vertex into remapped vertex array.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab1-109">**uVertLength**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-109">**uVertLength**</span></span>
</dt> <dd>

<span data-ttu-id="e3ab1-110">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3ab1-111">Nombre de vertex dans ce supercluster.</span><span class="sxs-lookup"><span data-stu-id="e3ab1-111">Number of vertices in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab1-112">**uFaceStart**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-112">**uFaceStart**</span></span>
</dt> <dd>

<span data-ttu-id="e3ab1-113">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-113">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3ab1-114">Index initial dans le tableau de faces.</span><span class="sxs-lookup"><span data-stu-id="e3ab1-114">Initial index into face array.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab1-115">**uFaceLength**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-115">**uFaceLength**</span></span>
</dt> <dd>

<span data-ttu-id="e3ab1-116">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-116">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3ab1-117">Nombre de visages dans ce supercluster.</span><span class="sxs-lookup"><span data-stu-id="e3ab1-117">Number of faces in this supercluster.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab1-118">**uClusterStart**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-118">**uClusterStart**</span></span>
</dt> <dd>

<span data-ttu-id="e3ab1-119">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3ab1-120">Index initial dans le groupe de clusters.</span><span class="sxs-lookup"><span data-stu-id="e3ab1-120">Initial index into cluster array.</span></span>

</dd> <dt>

<span data-ttu-id="e3ab1-121">**uClusterLength**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-121">**uClusterLength**</span></span>
</dt> <dd>

<span data-ttu-id="e3ab1-122">Type : **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="e3ab1-123">Nombre de clusters dans ce groupe supercluster.</span><span class="sxs-lookup"><span data-stu-id="e3ab1-123">Number of clusters in this supercluster array.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3ab1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e3ab1-124">Requirements</span></span>



| <span data-ttu-id="e3ab1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e3ab1-125">Requirement</span></span> | <span data-ttu-id="e3ab1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="e3ab1-126">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e3ab1-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="e3ab1-127">Header</span></span><br/> | <dl> <span data-ttu-id="e3ab1-128"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e3ab1-128"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3ab1-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e3ab1-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3ab1-130">Structures D3DX</span><span class="sxs-lookup"><span data-stu-id="e3ab1-130">D3DX Structures</span></span>](dx9-graphics-reference-d3dx-structures.md)
</dt> <dt>

[<span data-ttu-id="e3ab1-131">**D3DXSHPRTCompSplitMeshSC**</span><span class="sxs-lookup"><span data-stu-id="e3ab1-131">**D3DXSHPRTCompSplitMeshSC**</span></span>](d3dxshprtcompsplitmeshsc.md)
</dt> </dl>

 

 
