---
title: SV_GroupIndex
description: Le \ 0034 ; aplati \ 0034 ; index d’un thread de nuanceur de calcul dans un groupe de threads, qui transforme le SV multidimensionnel \_ GroupThreadID en valeur 1D. SV \_ GroupIndex varie de 0 à (numthreadsX \ numthreadsY \ numThreadsZ) \ 8211 ; 1,0.
ms.assetid: e793be10-7c83-478c-859a-4b0a2c537570
keywords:
- SV_GroupIndex HLSL
topic_type:
- apiref
api_name:
- SV_GroupIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 952a94378a0570d5bb7bc4f08959074bc8a4da4d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103728180"
---
# <a name="sv_groupindex"></a><span data-ttu-id="400e9-105">SV \_ GroupIndex</span><span class="sxs-lookup"><span data-stu-id="400e9-105">SV\_GroupIndex</span></span>

<span data-ttu-id="400e9-106">Index « aplati » d’un thread de nuanceur de calcul dans un groupe de threads, qui convertit le SV multidimensionnel \_ GroupThreadID en valeur 1D.</span><span class="sxs-lookup"><span data-stu-id="400e9-106">The "flattened" index of a compute shader thread within a thread group, which turns the multi-dimensional SV\_GroupThreadID into a 1D value.</span></span> <span data-ttu-id="400e9-107">SV \_ GroupIndex varie de 0 à (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span><span class="sxs-lookup"><span data-stu-id="400e9-107">SV\_GroupIndex varies from 0 to (numthreadsX \* numthreadsY \* numThreadsZ) – 1.</span></span>

## <a name="type"></a><span data-ttu-id="400e9-108">Type</span><span class="sxs-lookup"><span data-stu-id="400e9-108">Type</span></span>



| <span data-ttu-id="400e9-109">Type</span><span class="sxs-lookup"><span data-stu-id="400e9-109">Type</span></span> |
|------|
| <span data-ttu-id="400e9-110">uint</span><span class="sxs-lookup"><span data-stu-id="400e9-110">uint</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="400e9-111">Notes</span><span class="sxs-lookup"><span data-stu-id="400e9-111">Remarks</span></span>


```
SV_GroupIndex = SV_GroupThreadID.z*dimx*dimy + 
                      SV_GroupThreadID.y*dimx + 
                      SV_GroupThreadID.x
```



<span data-ttu-id="400e9-112">où dimx et Dimy sont les dimensions spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) pour le point d’entrée.</span><span class="sxs-lookup"><span data-stu-id="400e9-112">where dimx and dimy are the dimensions specified in the [numthreads](sm5-attributes-numthreads.md) attribute for the entry point.</span></span>

<span data-ttu-id="400e9-113">Cette valeur système est facultative.</span><span class="sxs-lookup"><span data-stu-id="400e9-113">This system value is optional.</span></span> <span data-ttu-id="400e9-114">Toutefois, son utilisation garantit qu’un thread écrit uniquement dans la région de mémoire qui lui est assignée dans la variable groupshared.</span><span class="sxs-lookup"><span data-stu-id="400e9-114">However, its use ensures that a thread only writes to its assigned region of memory in the groupshared variable.</span></span>

<span data-ttu-id="400e9-115">L’illustration suivante montre la relation entre les paramètres passés à [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads (SV GroupIndex, SV DispatchThreadID, SV \_ ,[SV \_ GroupID](sv-groupid.md)).[ \_](sv-dispatchthreadid.md)[ \_](sv-groupthreadid.md)</span><span class="sxs-lookup"><span data-stu-id="400e9-115">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values (SV\_GroupIndex,[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

<span data-ttu-id="400e9-117">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="400e9-117">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="400e9-118">Sommet</span><span class="sxs-lookup"><span data-stu-id="400e9-118">Vertex</span></span> | <span data-ttu-id="400e9-119">Forme</span><span class="sxs-lookup"><span data-stu-id="400e9-119">Hull</span></span> | <span data-ttu-id="400e9-120">Domain</span><span class="sxs-lookup"><span data-stu-id="400e9-120">Domain</span></span> | <span data-ttu-id="400e9-121">Géométrie</span><span class="sxs-lookup"><span data-stu-id="400e9-121">Geometry</span></span> | <span data-ttu-id="400e9-122">Pixel</span><span class="sxs-lookup"><span data-stu-id="400e9-122">Pixel</span></span> | <span data-ttu-id="400e9-123">Compute</span><span class="sxs-lookup"><span data-stu-id="400e9-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="400e9-124">x</span><span class="sxs-lookup"><span data-stu-id="400e9-124">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="400e9-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="400e9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400e9-126">Sémantique</span><span class="sxs-lookup"><span data-stu-id="400e9-126">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="400e9-127">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="400e9-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 