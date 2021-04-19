---
description: Pourcentage de temps de traitement des données de nuanceur.
ms.assetid: 388bb943-c25f-4b50-b7e4-d6259f1186c2
title: Structure D3DDEVINFO_D3D9STAGETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9STAGETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: cf8c9522decfcbb09a60aff0bee65ca05a0f5eeb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106538320"
---
# <a name="d3ddevinfo_d3d9stagetimings-structure"></a><span data-ttu-id="34631-103">D3DDEVINFO \_ D3D9STAGETIMINGS, structure</span><span class="sxs-lookup"><span data-stu-id="34631-103">D3DDEVINFO\_D3D9STAGETIMINGS structure</span></span>

<span data-ttu-id="34631-104">Pourcentage de temps de traitement des données de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="34631-104">Percent of time processing shader data.</span></span>

## <a name="syntax"></a><span data-ttu-id="34631-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="34631-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9STAGETIMINGS {
  FLOAT MemoryProcessingPercent;
  FLOAT ComputationProcessingPercent;
} D3DDEVINFO_D3D9STAGETIMINGS, *LPD3DDEVINFO_D3D9STAGETIMINGS;
```



## <a name="members"></a><span data-ttu-id="34631-106">Membres</span><span class="sxs-lookup"><span data-stu-id="34631-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="34631-107">**MemoryProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="34631-107">**MemoryProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="34631-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34631-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34631-109">Pourcentage de temps passé par le nuanceur aux accès mémoire.</span><span class="sxs-lookup"><span data-stu-id="34631-109">Percent of time in shader spent on memory accesses.</span></span>

</dd> <dt>

<span data-ttu-id="34631-110">**ComputationProcessingPercent**</span><span class="sxs-lookup"><span data-stu-id="34631-110">**ComputationProcessingPercent**</span></span>
</dt> <dd>

<span data-ttu-id="34631-111">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="34631-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="34631-112">Pourcentage de traitement du temps (déplacement des données dans les registres ou opérations mathématiques).</span><span class="sxs-lookup"><span data-stu-id="34631-112">Percent of time processing (moving data around in registers or doing mathematical operations).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="34631-113">Notes</span><span class="sxs-lookup"><span data-stu-id="34631-113">Remarks</span></span>

<span data-ttu-id="34631-114">Pour des performances optimales, il est recommandé de disposer d’une charge équilibrée.</span><span class="sxs-lookup"><span data-stu-id="34631-114">For best performance, a balanced load is recommended.</span></span>

## <a name="requirements"></a><span data-ttu-id="34631-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="34631-115">Requirements</span></span>



| <span data-ttu-id="34631-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="34631-116">Requirement</span></span> | <span data-ttu-id="34631-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="34631-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="34631-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="34631-118">Header</span></span><br/> | <dl> <span data-ttu-id="34631-119"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="34631-119"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34631-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="34631-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34631-121">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="34631-121">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="34631-122">**GetData**</span><span class="sxs-lookup"><span data-stu-id="34631-122">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
