---
title: SV_GroupID
description: Index pour le groupe de threads dans lequel un nuanceur de calcul s’exécute.
ms.assetid: 1b90ca74-a2b6-4a5f-aa4a-1ec879360593
keywords:
- SV_GroupID HLSL
topic_type:
- apiref
api_name:
- SV_GroupID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ab94cef0a9a33f23947e11b93a5487c65eee3890
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/09/2021
ms.locfileid: "111827038"
---
# <a name="sv_groupid"></a><span data-ttu-id="4e9a1-104">\_GROUPID vs</span><span class="sxs-lookup"><span data-stu-id="4e9a1-104">SV\_GroupID</span></span>

<span data-ttu-id="4e9a1-105">Index pour le groupe de threads dans lequel un nuanceur de calcul s’exécute.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-105">Indices for which thread group a compute shader is executing in.</span></span> <span data-ttu-id="4e9a1-106">Les index concernent l’ensemble du groupe et non un thread individuel.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-106">The indices are to the whole group and not an individual thread.</span></span> <span data-ttu-id="4e9a1-107">Les valeurs possibles varient au sein de la plage passée comme paramètres à la [**distribution**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span><span class="sxs-lookup"><span data-stu-id="4e9a1-107">Possible values vary across the range passed as parameters to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch).</span></span> <span data-ttu-id="4e9a1-108">Par exemple, l’appel de dispatch (2, 1, 1) donne les valeurs possibles 0, 0, 0 et 1, 0, 0.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-108">For example calling Dispatch(2,1,1) results in possible values of 0,0,0 and 1,0,0.</span></span>

<span data-ttu-id="4e9a1-109">Définit l’offset de groupe dans un appel de [**distribution**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) , par dimension de l’appel de répartition.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-109">Defines the group offset within a [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) call, per dimension of the dispatch call.</span></span>

## <a name="type"></a><span data-ttu-id="4e9a1-110">Type</span><span class="sxs-lookup"><span data-stu-id="4e9a1-110">Type</span></span>



| <span data-ttu-id="4e9a1-111">Type</span><span class="sxs-lookup"><span data-stu-id="4e9a1-111">Type</span></span>      |
|-------|
| <span data-ttu-id="4e9a1-112">uint3</span><span class="sxs-lookup"><span data-stu-id="4e9a1-112">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="4e9a1-113">Remarques</span><span class="sxs-lookup"><span data-stu-id="4e9a1-113">Remarks</span></span>

<span data-ttu-id="4e9a1-114">Cette valeur système est facultative.</span><span class="sxs-lookup"><span data-stu-id="4e9a1-114">This system value is optional.</span></span>

<span data-ttu-id="4e9a1-115">L’illustration suivante montre la relation entre les paramètres transmis à [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md),[SV \_ GroupThreadID](sv-groupthreadid.md), SV \_ GroupId).</span><span class="sxs-lookup"><span data-stu-id="4e9a1-115">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),SV\_GroupID).</span></span>

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

<span data-ttu-id="4e9a1-117">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="4e9a1-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4e9a1-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="4e9a1-118">Vertex</span></span> | <span data-ttu-id="4e9a1-119">Forme</span><span class="sxs-lookup"><span data-stu-id="4e9a1-119">Hull</span></span> | <span data-ttu-id="4e9a1-120">Domaine</span><span class="sxs-lookup"><span data-stu-id="4e9a1-120">Domain</span></span> | <span data-ttu-id="4e9a1-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="4e9a1-121">Geometry</span></span> | <span data-ttu-id="4e9a1-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="4e9a1-122">Pixel</span></span> | <span data-ttu-id="4e9a1-123">Compute</span><span class="sxs-lookup"><span data-stu-id="4e9a1-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="4e9a1-124">x</span><span class="sxs-lookup"><span data-stu-id="4e9a1-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4e9a1-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4e9a1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e9a1-126">Sémantique</span><span class="sxs-lookup"><span data-stu-id="4e9a1-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="4e9a1-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="4e9a1-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 
