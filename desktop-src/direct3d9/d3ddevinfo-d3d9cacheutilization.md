---
description: Mesurez les performances du taux d’accès au cache pour les textures et les vertex indexés.
ms.assetid: 70bc4e93-0a34-485b-bdcc-028c24b52f62
title: Structure D3DDEVINFO_D3D9CACHEUTILIZATION (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9CACHEUTILIZATION
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 94f77549d0ea2a9c59d7de8367a6133085cc2771
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "104530867"
---
# <a name="d3ddevinfo_d3d9cacheutilization-structure"></a><span data-ttu-id="eeabb-103">D3DDEVINFO \_ D3D9CACHEUTILIZATION, structure</span><span class="sxs-lookup"><span data-stu-id="eeabb-103">D3DDEVINFO\_D3D9CACHEUTILIZATION structure</span></span>

<span data-ttu-id="eeabb-104">Mesurez les performances du taux d’accès au cache pour les textures et les vertex indexés.</span><span class="sxs-lookup"><span data-stu-id="eeabb-104">Measure the cache hit rate performance for textures and indexed vertices.</span></span>

## <a name="syntax"></a><span data-ttu-id="eeabb-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="eeabb-105">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9CACHEUTILIZATION {
  FLOAT TextureCacheHitRate;
  FLOAT PostTransformVertexCacheHitRate;
} D3DDEVINFO_D3D9CACHEUTILIZATION, *LPD3DDEVINFO_D3D9CACHEUTILIZATION;
```



## <a name="members"></a><span data-ttu-id="eeabb-106">Membres</span><span class="sxs-lookup"><span data-stu-id="eeabb-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="eeabb-107">**TextureCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="eeabb-107">**TextureCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="eeabb-108">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eeabb-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eeabb-109">Taux d’accès pour la recherche d’une texture dans le cache de texture.</span><span class="sxs-lookup"><span data-stu-id="eeabb-109">The hit rate for finding a texture in the texture cache.</span></span> <span data-ttu-id="eeabb-110">Cela suppose qu’il existe un cache de texture.</span><span class="sxs-lookup"><span data-stu-id="eeabb-110">This assumes there is a texture cache.</span></span> <span data-ttu-id="eeabb-111">L’amélioration du niveau de détail pour utiliser la texture la plus détaillée, l’utilisation de nombreuses textures volumineuses ou la génération d’un modèle d’accès de texture presque aléatoire sur les textures volumineuses avec un code de nuanceur personnalisé peut avoir un impact considérable sur le taux d’accès au cache de texture.</span><span class="sxs-lookup"><span data-stu-id="eeabb-111">Increasing the level-of-detail bias to use the most detailed texture, using many large textures, or producing a near random texture access pattern on large textures with custom shader code can dramatically affect the texture cache hit rate.</span></span>

</dd> <dt>

<span data-ttu-id="eeabb-112">**PostTransformVertexCacheHitRate**</span><span class="sxs-lookup"><span data-stu-id="eeabb-112">**PostTransformVertexCacheHitRate**</span></span>
</dt> <dd>

<span data-ttu-id="eeabb-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="eeabb-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="eeabb-114">Taux d’accès pour la recherche des vertex transformés dans le cache de vertex.</span><span class="sxs-lookup"><span data-stu-id="eeabb-114">The hit rate for finding transformed vertices in the vertex cache.</span></span> <span data-ttu-id="eeabb-115">Le GPU est conçu pour transformer des vertex indexés et peut les stocker dans un cache de vertex.</span><span class="sxs-lookup"><span data-stu-id="eeabb-115">The GPU is designed to transform indexed vertices and may store them in a vertex cache.</span></span> <span data-ttu-id="eeabb-116">Si vous utilisez des mailles, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) ou [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) peut entraîner une meilleure utilisation du cache de vertex.</span><span class="sxs-lookup"><span data-stu-id="eeabb-116">If you are using meshes, [**D3DXOptimizeFaces**](d3dxoptimizefaces.md) or [**D3DXOptimizeVertices**](d3dxoptimizevertices.md) may result in better vertex cache utilization.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="eeabb-117">Notes</span><span class="sxs-lookup"><span data-stu-id="eeabb-117">Remarks</span></span>

<span data-ttu-id="eeabb-118">Un cache efficace est généralement plus proche d’un taux d’accès de 90% et un cache inefficace est généralement plus proche d’un taux d’accès de 10% (même si un faible pourcentage n’est pas nécessairement un problème).</span><span class="sxs-lookup"><span data-stu-id="eeabb-118">An efficient cache is typically closer to a 90 percent hit rate, and an inefficient cache is typically closer to a 10 percent hit rate (although a low percentage is not necessarily a problem).</span></span>

## <a name="requirements"></a><span data-ttu-id="eeabb-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="eeabb-119">Requirements</span></span>



| <span data-ttu-id="eeabb-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="eeabb-120">Requirement</span></span> | <span data-ttu-id="eeabb-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="eeabb-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eeabb-122">En-tête</span><span class="sxs-lookup"><span data-stu-id="eeabb-122">Header</span></span><br/> | <dl> <span data-ttu-id="eeabb-123"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="eeabb-123"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eeabb-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="eeabb-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eeabb-125">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="eeabb-125">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="eeabb-126">**GetData**</span><span class="sxs-lookup"><span data-stu-id="eeabb-126">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
