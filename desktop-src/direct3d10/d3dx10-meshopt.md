---
description: 'Énumération D3DX10_MESHOPT : spécifie le type d’optimisation de maillage à effectuer.'
ms.assetid: 20d1da8c-8c3d-4045-9a37-d534a8682716
title: Énumération D3DX10_MESHOPT (D3DX10Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10_MESHOPT
api_type:
- HeaderDef
api_location:
- D3DX10Mesh.h
ms.openlocfilehash: 7b3085cf9970f2c1f6fe3748cc4db8f4fb2b2a78
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105447"
---
# <a name="d3dx10_meshopt-enumeration"></a><span data-ttu-id="c9bab-103">D3DX10 \_ MESHOPT, énumération</span><span class="sxs-lookup"><span data-stu-id="c9bab-103">D3DX10\_MESHOPT enumeration</span></span>

<span data-ttu-id="c9bab-104">Spécifie le type d’optimisation de maillage à effectuer.</span><span class="sxs-lookup"><span data-stu-id="c9bab-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9bab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9bab-105">Syntax</span></span>


```C++
typedef enum D3DX10_MESHOPT { 
  D3DX10_MESHOPT_COMPACT             = 0x01000000,
  D3DX10_MESHOPT_ATTR_SORT           = 0x02000000,
  D3DX10_MESHOPT_VERTEX_CACHE        = 0x04000000,
  D3DX10_MESHOPT_STRIP_REORDER       = 0x08000000,
  D3DX10_MESHOPT_IGNORE_VERTS        = 0x10000000,
  D3DX10_MESHOPT_DO_NOT_SPLIT        = 0x20000000,
  D3DX10_MESHOPT_DEVICE_INDEPENDENT  = 0x00400000
} D3DX10_MESHOPT, *LPD3DX10_MESHOPT;
```



## <a name="constants"></a><span data-ttu-id="c9bab-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="c9bab-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c9bab-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10 \_ MESHOPT \_ compact**</span><span class="sxs-lookup"><span data-stu-id="c9bab-107"><span id="D3DX10_MESHOPT_COMPACT"></span><span id="d3dx10_meshopt_compact"></span>**D3DX10\_MESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="c9bab-108">Réorganise les visages pour supprimer les sommets et les faces inutilisés.</span><span class="sxs-lookup"><span data-stu-id="c9bab-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="c9bab-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10 \_ MESHOPT \_ attr \_ sort**</span><span class="sxs-lookup"><span data-stu-id="c9bab-109"><span id="D3DX10_MESHOPT_ATTR_SORT"></span><span id="d3dx10_meshopt_attr_sort"></span>**D3DX10\_MESHOPT\_ATTR\_SORT**</span></span>
</dt> <dd>

<span data-ttu-id="c9bab-110">Réorganise les visages pour optimiser le nombre de modifications d’état de groupe d’attributs et les performances améliorées de DrawSubset.</span><span class="sxs-lookup"><span data-stu-id="c9bab-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced DrawSubset performance.</span></span>

</dd> <dt>

<span data-ttu-id="c9bab-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**\_Cache de \_ vertex d3dx10 MESHOPT \_**</span><span class="sxs-lookup"><span data-stu-id="c9bab-111"><span id="D3DX10_MESHOPT_VERTEX_CACHE"></span><span id="d3dx10_meshopt_vertex_cache"></span>**D3DX10\_MESHOPT\_VERTEX\_CACHE**</span></span>
</dt> <dd>

<span data-ttu-id="c9bab-112">Réorganise les visages pour augmenter le taux d’accès au cache des caches de vertex.</span><span class="sxs-lookup"><span data-stu-id="c9bab-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="c9bab-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**Réorganisation de la \_ bande d3dx10 MESHOPT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="c9bab-113"><span id="D3DX10_MESHOPT_STRIP_REORDER"></span><span id="d3dx10_meshopt_strip_reorder"></span>**D3DX10\_MESHOPT\_STRIP\_REORDER**</span></span>
</dt> <dd>

<span data-ttu-id="c9bab-114">Réorganise les visages pour maximiser la longueur des triangles adjacents.</span><span class="sxs-lookup"><span data-stu-id="c9bab-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="c9bab-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10 \_ MESHOPT \_ Ignorer les \_ basculements**</span><span class="sxs-lookup"><span data-stu-id="c9bab-115"><span id="D3DX10_MESHOPT_IGNORE_VERTS"></span><span id="d3dx10_meshopt_ignore_verts"></span>**D3DX10\_MESHOPT\_IGNORE\_VERTS**</span></span>
</dt> <dd>

<span data-ttu-id="c9bab-116">Optimiser les visages uniquement ; n’optimisez pas les vertex.</span><span class="sxs-lookup"><span data-stu-id="c9bab-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="c9bab-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10 \_ MESHOPT \_ ne \_ pas \_ fractionner**</span><span class="sxs-lookup"><span data-stu-id="c9bab-117"><span id="D3DX10_MESHOPT_DO_NOT_SPLIT"></span><span id="d3dx10_meshopt_do_not_split"></span>**D3DX10\_MESHOPT\_DO\_NOT\_SPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="c9bab-118">Lors du tri des attributs, ne fractionnez pas les vertex partagés entre les groupes d’attributs.</span><span class="sxs-lookup"><span data-stu-id="c9bab-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="c9bab-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10 \_ MESHOPT \_ appareil \_ indépendant**</span><span class="sxs-lookup"><span data-stu-id="c9bab-119"><span id="D3DX10_MESHOPT_DEVICE_INDEPENDENT"></span><span id="d3dx10_meshopt_device_independent"></span>**D3DX10\_MESHOPT\_DEVICE\_INDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="c9bab-120">Affecte la taille du cache de vertex.</span><span class="sxs-lookup"><span data-stu-id="c9bab-120">Affects the vertex cache size.</span></span> <span data-ttu-id="c9bab-121">L’utilisation de cet indicateur spécifie une taille de cache de vertex par défaut qui fonctionne bien sur le matériel hérité.</span><span class="sxs-lookup"><span data-stu-id="c9bab-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9bab-122">Notes </span><span class="sxs-lookup"><span data-stu-id="c9bab-122">Remarks</span></span>

<span data-ttu-id="c9bab-123">Les \_ indicateurs d’optimisation D3DXMESHOPT STRIPREORDER et D3DXMESHOPT \_ VERTEXCACHE s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="c9bab-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="c9bab-124">L' \_ indicateur D3DXMESHOPT SHAREVB a été supprimé de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="c9bab-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="c9bab-125">Utilisez le \_ partage VB D3DXMESH \_ à la place, dans D3DXMESH.</span><span class="sxs-lookup"><span data-stu-id="c9bab-125">Use D3DXMESH\_VB\_SHARE instead, in D3DXMESH.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9bab-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9bab-126">Requirements</span></span>



| <span data-ttu-id="c9bab-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9bab-127">Requirement</span></span> | <span data-ttu-id="c9bab-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9bab-128">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9bab-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9bab-129">Header</span></span><br/> | <dl> <span data-ttu-id="c9bab-130"><dt>D3DX10Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9bab-130"><dt>D3DX10Mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9bab-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c9bab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9bab-132">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="c9bab-132">D3DX Enumerations</span></span>](d3d10-graphics-reference-d3dx10-enums.md)
</dt> </dl>

 

 




