---
description: Définit les opérations à effectuer sur les vertex en préparation du nettoyage du maillage.
ms.assetid: f222acaa-fa82-4591-b7c2-b520cb648ed5
title: Énumération D3DXCLEANTYPE (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCLEANTYPE
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: b38578d0f50521def552b8bd6608c2696b405d0f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104211805"
---
# <a name="d3dxcleantype-enumeration"></a><span data-ttu-id="b6283-103">Énumération D3DXCLEANTYPE</span><span class="sxs-lookup"><span data-stu-id="b6283-103">D3DXCLEANTYPE enumeration</span></span>

<span data-ttu-id="b6283-104">Définit les opérations à effectuer sur les vertex en préparation du nettoyage du maillage.</span><span class="sxs-lookup"><span data-stu-id="b6283-104">Defines operations to perform on vertices in preparation for mesh cleaning.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6283-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b6283-105">Syntax</span></span>


```C++
typedef enum D3DXCLEANTYPE { 
  D3DXCLEAN_BACKFACING      = 1,
  D3DXCLEAN_BOWTIES         = 2,
  D3DXCLEAN_SKINNING        = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_OPTIMIZATION    = D3DXCLEAN_BACKFACING,
  D3DXCLEAN_SIMPLIFICATION  = D3DXCLEAN_BACKFACING | D3DXCLEAN_BOWTIES
} D3DXCLEANTYPE, *LPD3DXCLEANTYPE;
```



## <a name="constants"></a><span data-ttu-id="b6283-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="b6283-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b6283-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="b6283-107"><span id="D3DXCLEAN_BACKFACING"></span><span id="d3dxclean_backfacing"></span>**D3DXCLEAN\_BACKFACING**</span></span>
</dt> <dd>

<span data-ttu-id="b6283-108">Les triangles de fusion qui partagent les mêmes index de vertex mais qui ont des normales de visage pointent dans des directions opposées (triangles de face arrière).</span><span class="sxs-lookup"><span data-stu-id="b6283-108">Merge triangles that share the same vertex indices but have face normals pointing in opposite directions (back-facing triangles).</span></span> <span data-ttu-id="b6283-109">À moins que les triangles ne soient pas fractionnés par l’ajout d’un vertex répliqué, les données d’adjacence de maillage des deux triangles peuvent entrer en conflit.</span><span class="sxs-lookup"><span data-stu-id="b6283-109">Unless the triangles are not split by adding a replicated vertex, mesh adjacency data from the two triangles may conflict.</span></span>

</dd> <dt>

<span data-ttu-id="b6283-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN \_ BOWTIES**</span><span class="sxs-lookup"><span data-stu-id="b6283-110"><span id="D3DXCLEAN_BOWTIES"></span><span id="d3dxclean_bowties"></span>**D3DXCLEAN\_BOWTIES**</span></span>
</dt> <dd>

<span data-ttu-id="b6283-111">Si un vertex est l’apex de deux ventilateurs triangulaires (un nœud papillon) et que les opérations de maillage affectent l’un des ventilateurs, vous fractionnez ensuite le vertex partagé en deux nouveaux sommets.</span><span class="sxs-lookup"><span data-stu-id="b6283-111">If a vertex is the apex of two triangle fans (a bowtie) and mesh operations will affect one of the fans, then split the shared vertex into two new vertices.</span></span> <span data-ttu-id="b6283-112">Bowties peut provoquer des problèmes pour les opérations telles que la simplification du maillage qui suppriment des vertex, car la suppression d’un vertex affecte deux ensembles distincts de triangles.</span><span class="sxs-lookup"><span data-stu-id="b6283-112">Bowties can cause problems for operations such as mesh simplification that remove vertices, because removing one vertex affects two distinct sets of triangles.</span></span>

</dd> <dt>

<span data-ttu-id="b6283-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN l' \_ apparence**</span><span class="sxs-lookup"><span data-stu-id="b6283-113"><span id="D3DXCLEAN_SKINNING"></span><span id="d3dxclean_skinning"></span>**D3DXCLEAN\_SKINNING**</span></span>
</dt> <dd>

<span data-ttu-id="b6283-114">Utilisez cet indicateur pour empêcher les boucles infinies pendant l’apparence des opérations de maillage d’installation.</span><span class="sxs-lookup"><span data-stu-id="b6283-114">Use this flag to prevent infinite loops during skinning setup mesh operations.</span></span>

</dd> <dt>

<span data-ttu-id="b6283-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**Optimisation de D3DXCLEAN \_**</span><span class="sxs-lookup"><span data-stu-id="b6283-115"><span id="D3DXCLEAN_OPTIMIZATION"></span><span id="d3dxclean_optimization"></span>**D3DXCLEAN\_OPTIMIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="b6283-116">Utilisez cet indicateur pour empêcher les boucles infinies pendant les opérations d’optimisation de maillage.</span><span class="sxs-lookup"><span data-stu-id="b6283-116">Use this flag to prevent infinite loops during mesh optimization operations.</span></span>

</dd> <dt>

<span data-ttu-id="b6283-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**\_Simplification D3DXCLEAN**</span><span class="sxs-lookup"><span data-stu-id="b6283-117"><span id="D3DXCLEAN_SIMPLIFICATION"></span><span id="d3dxclean_simplification"></span>**D3DXCLEAN\_SIMPLIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="b6283-118">Utilisez cet indicateur pour empêcher les boucles infinies pendant les opérations de simplification du maillage.</span><span class="sxs-lookup"><span data-stu-id="b6283-118">Use this flag to prevent infinite loops during mesh simplification operations.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6283-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b6283-119">Requirements</span></span>



| <span data-ttu-id="b6283-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b6283-120">Requirement</span></span> | <span data-ttu-id="b6283-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="b6283-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b6283-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="b6283-122">Header</span></span><br/> | <dl> <span data-ttu-id="b6283-123"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="b6283-123"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b6283-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b6283-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6283-125">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="b6283-125">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




