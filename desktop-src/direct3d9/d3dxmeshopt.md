---
description: Énumération D3DXMESHOPT-spécifie le type d’optimisation de maillage à effectuer.
ms.assetid: 32ef227a-b299-47c4-96b8-c0ea7bf549e1
title: Énumération D3DXMESHOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _D3DXMESHOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: db7c2a2411d1c846c7369fc1d925a8e5569df3b1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114347"
---
# <a name="d3dxmeshopt-enumeration"></a><span data-ttu-id="dab3f-103">Énumération D3DXMESHOPT</span><span class="sxs-lookup"><span data-stu-id="dab3f-103">D3DXMESHOPT enumeration</span></span>

<span data-ttu-id="dab3f-104">Spécifie le type d’optimisation de maillage à effectuer.</span><span class="sxs-lookup"><span data-stu-id="dab3f-104">Specifies the type of mesh optimization to be performed.</span></span>

## <a name="syntax"></a><span data-ttu-id="dab3f-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dab3f-105">Syntax</span></span>


```C++
enum _D3DXMESHOPT {
  D3DXMESHOPT_COMPACT            = 0x01000000, 
  D3DXMESHOPT_ATTRSORT           = 0x02000000, 
  D3DXMESHOPT_VERTEXCACHE        = 0x04000000, 
  D3DXMESHOPT_STRIPREORDER       = 0x08000000, 
  D3DXMESHOPT_IGNOREVERTS        = 0x10000000, 
  D3DXMESHOPT_DONOTSPLIT         = 0x20000000, 
  D3DXMESHOPT_DEVICEINDEPENDENT  = 0x40000000 

};
```



## <a name="constants"></a><span data-ttu-id="dab3f-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="dab3f-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dab3f-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT \_ compact**</span><span class="sxs-lookup"><span data-stu-id="dab3f-107"><span id="D3DXMESHOPT_COMPACT"></span><span id="d3dxmeshopt_compact"></span>**D3DXMESHOPT\_COMPACT**</span></span>
</dt> <dd>

<span data-ttu-id="dab3f-108">Réorganise les visages pour supprimer les sommets et les faces inutilisés.</span><span class="sxs-lookup"><span data-stu-id="dab3f-108">Reorders faces to remove unused vertices and faces.</span></span>

</dd> <dt>

<span data-ttu-id="dab3f-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT \_ ATTRSORT**</span><span class="sxs-lookup"><span data-stu-id="dab3f-109"><span id="D3DXMESHOPT_ATTRSORT"></span><span id="d3dxmeshopt_attrsort"></span>**D3DXMESHOPT\_ATTRSORT**</span></span>
</dt> <dd>

<span data-ttu-id="dab3f-110">Réorganise les visages pour optimiser le nombre de modifications d’état de groupe d’attributs et les ID3DXBaseMesh améliorées [**::D**](id3dxbasemesh--drawsubset.md) les performances rawsubset.</span><span class="sxs-lookup"><span data-stu-id="dab3f-110">Reorders faces to optimize for fewer attribute bundle state changes and enhanced [**ID3DXBaseMesh::DrawSubset**](id3dxbasemesh--drawsubset.md) performance.</span></span>

</dd> <dt>

<span data-ttu-id="dab3f-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT \_ VERTEXCACHE**</span><span class="sxs-lookup"><span data-stu-id="dab3f-111"><span id="D3DXMESHOPT_VERTEXCACHE"></span><span id="d3dxmeshopt_vertexcache"></span>**D3DXMESHOPT\_VERTEXCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="dab3f-112">Réorganise les visages pour augmenter le taux d’accès au cache des caches de vertex.</span><span class="sxs-lookup"><span data-stu-id="dab3f-112">Reorders faces to increase the cache hit rate of vertex caches.</span></span>

</dd> <dt>

<span data-ttu-id="dab3f-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT \_ STRIPREORDER**</span><span class="sxs-lookup"><span data-stu-id="dab3f-113"><span id="D3DXMESHOPT_STRIPREORDER"></span><span id="d3dxmeshopt_stripreorder"></span>**D3DXMESHOPT\_STRIPREORDER**</span></span>
</dt> <dd>

<span data-ttu-id="dab3f-114">Réorganise les visages pour maximiser la longueur des triangles adjacents.</span><span class="sxs-lookup"><span data-stu-id="dab3f-114">Reorders faces to maximize length of adjacent triangles.</span></span>

</dd> <dt>

<span data-ttu-id="dab3f-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT \_ IGNOREVERTS**</span><span class="sxs-lookup"><span data-stu-id="dab3f-115"><span id="D3DXMESHOPT_IGNOREVERTS"></span><span id="d3dxmeshopt_ignoreverts"></span>**D3DXMESHOPT\_IGNOREVERTS**</span></span>
</dt> <dd>

<span data-ttu-id="dab3f-116">Optimiser les visages uniquement ; n’optimisez pas les vertex.</span><span class="sxs-lookup"><span data-stu-id="dab3f-116">Optimize the faces only; do not optimize the vertices.</span></span>

</dd> <dt>

<span data-ttu-id="dab3f-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT \_ DONOTSPLIT**</span><span class="sxs-lookup"><span data-stu-id="dab3f-117"><span id="D3DXMESHOPT_DONOTSPLIT"></span><span id="d3dxmeshopt_donotsplit"></span>**D3DXMESHOPT\_DONOTSPLIT**</span></span>
</dt> <dd>

<span data-ttu-id="dab3f-118">Lors du tri des attributs, ne fractionnez pas les vertex partagés entre les groupes d’attributs.</span><span class="sxs-lookup"><span data-stu-id="dab3f-118">While attribute sorting, do not split vertices that are shared between attribute groups.</span></span>

</dd> <dt>

<span data-ttu-id="dab3f-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT \_ DEVICEINDEPENDENT**</span><span class="sxs-lookup"><span data-stu-id="dab3f-119"><span id="D3DXMESHOPT_DEVICEINDEPENDENT"></span><span id="d3dxmeshopt_deviceindependent"></span>**D3DXMESHOPT\_DEVICEINDEPENDENT**</span></span>
</dt> <dd>

<span data-ttu-id="dab3f-120">Affecte la taille du cache de vertex.</span><span class="sxs-lookup"><span data-stu-id="dab3f-120">Affects the vertex cache size.</span></span> <span data-ttu-id="dab3f-121">L’utilisation de cet indicateur spécifie une taille de cache de vertex par défaut qui fonctionne bien sur le matériel hérité.</span><span class="sxs-lookup"><span data-stu-id="dab3f-121">Using this flag specifies a default vertex cache size that works well on legacy hardware.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="dab3f-122">Notes </span><span class="sxs-lookup"><span data-stu-id="dab3f-122">Remarks</span></span>

<span data-ttu-id="dab3f-123">Les \_ indicateurs d’optimisation D3DXMESHOPT STRIPREORDER et D3DXMESHOPT \_ VERTEXCACHE s’excluent mutuellement.</span><span class="sxs-lookup"><span data-stu-id="dab3f-123">The D3DXMESHOPT\_STRIPREORDER and D3DXMESHOPT\_VERTEXCACHE optimization flags are mutually exclusive.</span></span>

<span data-ttu-id="dab3f-124">L' \_ indicateur D3DXMESHOPT SHAREVB a été supprimé de cette énumération.</span><span class="sxs-lookup"><span data-stu-id="dab3f-124">The D3DXMESHOPT\_SHAREVB flag has been removed from this enumeration.</span></span> <span data-ttu-id="dab3f-125">Utilisez le \_ partage VB D3DXMESH \_ à la place, dans [**D3DXMESH**](./d3dxmesh.md).</span><span class="sxs-lookup"><span data-stu-id="dab3f-125">Use D3DXMESH\_VB\_SHARE instead, in [**D3DXMESH**](./d3dxmesh.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="dab3f-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dab3f-126">Requirements</span></span>



| <span data-ttu-id="dab3f-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dab3f-127">Requirement</span></span> | <span data-ttu-id="dab3f-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="dab3f-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dab3f-129">En-tête</span><span class="sxs-lookup"><span data-stu-id="dab3f-129">Header</span></span><br/> | <dl> <span data-ttu-id="dab3f-130"><dt>D3dx9mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="dab3f-130"><dt>D3dx9mesh.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dab3f-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dab3f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dab3f-132">Énumérations D3DX</span><span class="sxs-lookup"><span data-stu-id="dab3f-132">D3DX Enumerations</span></span>](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 
