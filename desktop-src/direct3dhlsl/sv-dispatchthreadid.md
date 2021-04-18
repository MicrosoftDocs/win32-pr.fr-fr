---
title: SV_DispatchThreadID
description: Index pour lesquels un nuanceur de calcul et un groupe de threads combinés sont en cours d’exécution.
ms.assetid: bad697f6-26d9-47cd-93e5-127621a161e8
keywords:
- SV_DispatchThreadID HLSL
topic_type:
- apiref
api_name:
- SV_DispatchThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d55fcf7e291c561ecb51dd32dfac135c563974c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104557950"
---
# <a name="sv_dispatchthreadid"></a><span data-ttu-id="0e5a1-104">SV \_ DispatchThreadID</span><span class="sxs-lookup"><span data-stu-id="0e5a1-104">SV\_DispatchThreadID</span></span>

<span data-ttu-id="0e5a1-105">Index pour lesquels un nuanceur de calcul et un groupe de threads combinés sont en cours d’exécution.</span><span class="sxs-lookup"><span data-stu-id="0e5a1-105">Indices for which combined thread and thread group a compute shader is executing in.</span></span> <span data-ttu-id="0e5a1-106">SV \_ DispatchThreadID est la somme de SV \_ GroupID \* numThreads et GroupThreadID.</span><span class="sxs-lookup"><span data-stu-id="0e5a1-106">SV\_DispatchThreadID is the sum of SV\_GroupID \* numthreads and GroupThreadID.</span></span> <span data-ttu-id="0e5a1-107">Elle varie selon la plage spécifiée dans [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) et [numThreads](sm5-attributes-numthreads.md).</span><span class="sxs-lookup"><span data-stu-id="0e5a1-107">It varies across the range specified in [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch) and [numthreads](sm5-attributes-numthreads.md).</span></span> <span data-ttu-id="0e5a1-108">Par exemple, si Dispatch (2, 2, 2) est appelé sur un nuanceur de calcul avec numThreads (3, 3, 3) SV \_ DispatchThreadID aura une plage de 0.. 5 pour chaque dimension.</span><span class="sxs-lookup"><span data-stu-id="0e5a1-108">For example if Dispatch(2,2,2) is called on a compute shader with numthreads(3,3,3) SV\_DispatchThreadID will have a range of 0..5 for each dimension.</span></span>

## <a name="type"></a><span data-ttu-id="0e5a1-109">Type</span><span class="sxs-lookup"><span data-stu-id="0e5a1-109">Type</span></span>



|       |
|-------|
| <span data-ttu-id="0e5a1-110">Type</span><span class="sxs-lookup"><span data-stu-id="0e5a1-110">Type</span></span>  |
| <span data-ttu-id="0e5a1-111">uint3</span><span class="sxs-lookup"><span data-stu-id="0e5a1-111">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="0e5a1-112">Notes</span><span class="sxs-lookup"><span data-stu-id="0e5a1-112">Remarks</span></span>

<span data-ttu-id="0e5a1-113">Cette valeur système est facultative.</span><span class="sxs-lookup"><span data-stu-id="0e5a1-113">This system value is optional.</span></span>

<span data-ttu-id="0e5a1-114">L’illustration suivante montre la relation entre les paramètres transmis à [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads ([SV \_ GroupIndex](sv-groupindex.md), SV \_ DispatchThreadID,[SV \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="0e5a1-114">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),SV\_DispatchThreadID,[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

<span data-ttu-id="0e5a1-116">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="0e5a1-116">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0e5a1-117">Sommet</span><span class="sxs-lookup"><span data-stu-id="0e5a1-117">Vertex</span></span> | <span data-ttu-id="0e5a1-118">Forme</span><span class="sxs-lookup"><span data-stu-id="0e5a1-118">Hull</span></span> | <span data-ttu-id="0e5a1-119">Domain</span><span class="sxs-lookup"><span data-stu-id="0e5a1-119">Domain</span></span> | <span data-ttu-id="0e5a1-120">Géométrie</span><span class="sxs-lookup"><span data-stu-id="0e5a1-120">Geometry</span></span> | <span data-ttu-id="0e5a1-121">Pixel</span><span class="sxs-lookup"><span data-stu-id="0e5a1-121">Pixel</span></span> | <span data-ttu-id="0e5a1-122">Compute</span><span class="sxs-lookup"><span data-stu-id="0e5a1-122">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="0e5a1-123">x</span><span class="sxs-lookup"><span data-stu-id="0e5a1-123">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="0e5a1-124">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0e5a1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e5a1-125">Sémantique</span><span class="sxs-lookup"><span data-stu-id="0e5a1-125">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="0e5a1-126">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="0e5a1-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 