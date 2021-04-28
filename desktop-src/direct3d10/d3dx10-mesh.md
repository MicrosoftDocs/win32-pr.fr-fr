---
description: D3DX10_MESH énumération-indicateurs utilisés pour spécifier les options de création d’une maille.
ms.assetid: 1a5a6b3f-34f4-4338-9ffe-8f95f6f0c385
title: Énumération D3DX10_MESH (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESH
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 2659783b0443396508465f9498eec86950f825bc
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105437"
---
# <a name="d3dx10_mesh-enumeration"></a><span data-ttu-id="c2821-103">D3DX10 \_ , énumération</span><span class="sxs-lookup"><span data-stu-id="c2821-103">D3DX10\_MESH enumeration</span></span>

<span data-ttu-id="c2821-104">Indicateurs utilisés pour spécifier les options de création d’une maille.</span><span class="sxs-lookup"><span data-stu-id="c2821-104">Flags used to specify creation options for a mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2821-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c2821-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESH { 
  D3DX10_MESH_32_BIT        = 0x001,
  D3DX10_MESH_GS_ADJACENCY  = 0x004
} D3DX10_MESH, *LPD3DX10_MESH;
```



## <a name="constants"></a><span data-ttu-id="c2821-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c2821-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c2821-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10 \_ maille \_ 32 \_ bits**</span><span class="sxs-lookup"><span data-stu-id="c2821-107"><span id="D3DX10_MESH_32_BIT"></span><span id="d3dx10_mesh_32_bit"></span>**D3DX10\_MESH\_32\_BIT**</span></span>
</dt> <dd>

<span data-ttu-id="c2821-108">Le maillage a des index 32 bits plutôt que des index 16 bits.</span><span class="sxs-lookup"><span data-stu-id="c2821-108">The mesh has 32-bit indices instead of 16-bit indices.</span></span> <span data-ttu-id="c2821-109">Consultez la section Notes.</span><span class="sxs-lookup"><span data-stu-id="c2821-109">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c2821-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10 \_ maille \_ GS \_**</span><span class="sxs-lookup"><span data-stu-id="c2821-110"><span id="D3DX10_MESH_GS_ADJACENCY"></span><span id="d3dx10_mesh_gs_adjacency"></span>**D3DX10\_MESH\_GS\_ADJACENCY**</span></span>
</dt> <dd>

<span data-ttu-id="c2821-111">Signale que le maillage contient des données d’adjacence de nuanceur Geometry.</span><span class="sxs-lookup"><span data-stu-id="c2821-111">Signals that the mesh contains geometry shader adjacency data.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c2821-112">Notes </span><span class="sxs-lookup"><span data-stu-id="c2821-112">Remarks</span></span>

<span data-ttu-id="c2821-113">Une maille 32 bits (D3DXMESH \_ 32 bits) peut théoriquement prendre en charge (2 ³ ²)-1 face et vertex.</span><span class="sxs-lookup"><span data-stu-id="c2821-113">A 32-bit mesh (D3DXMESH\_32BIT) can theoretically support (2³²)-1 faces and vertices.</span></span> <span data-ttu-id="c2821-114">Toutefois, l’allocation de mémoire pour une maille qui est importante sur un système d’exploitation 32 bits n’est pas pratique.</span><span class="sxs-lookup"><span data-stu-id="c2821-114">However, allocating memory for a mesh that large on a 32-bit operating system is not practical.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2821-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c2821-115">Requirements</span></span>



| <span data-ttu-id="c2821-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c2821-116">Requirement</span></span> | <span data-ttu-id="c2821-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="c2821-117">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2821-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="c2821-118">Header</span></span><br/> | <dl> <span data-ttu-id="c2821-119"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2821-119"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2821-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c2821-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2821-121">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="c2821-121">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




