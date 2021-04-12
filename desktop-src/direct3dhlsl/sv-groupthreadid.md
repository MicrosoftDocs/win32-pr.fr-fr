---
title: SV_GroupThreadID
description: Indices pour lesquels un thread individuel dans un groupe de threads est en cours d’exécution dans un nuanceur de calcul.
ms.assetid: be944592-c4ea-43c9-88bc-98a9a190a437
keywords:
- SV_GroupThreadID HLSL
topic_type:
- apiref
api_name:
- SV_GroupThreadID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3d4d35766bdbdc2d69c98983a85f336ab784d24d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316266"
---
# <a name="sv_groupthreadid"></a><span data-ttu-id="7a00c-104">SV \_ GroupThreadID</span><span class="sxs-lookup"><span data-stu-id="7a00c-104">SV\_GroupThreadID</span></span>

<span data-ttu-id="7a00c-105">Indices pour lesquels un thread individuel dans un groupe de threads est en cours d’exécution dans un nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="7a00c-105">Indices for which an individual thread within a thread group a compute shader is executing in.</span></span> <span data-ttu-id="7a00c-106">SV \_ GroupThreadID varie dans la plage spécifiée pour le nuanceur de calcul dans l’attribut [numThreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="7a00c-106">SV\_GroupThreadID varies across the range specified for the compute shader in the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span> <span data-ttu-id="7a00c-107">Par exemple, si numThreads (3, 2, 1) a été spécifié, les valeurs possibles pour la \_ valeur d’entrée de SV GroupThreadID sont comprises dans cette plage de valeurs (0-2, 0-1, 0).</span><span class="sxs-lookup"><span data-stu-id="7a00c-107">For example if numthreads(3,2,1) was specified possible values for the SV\_GroupThreadID input value have this range of values (0-2,0-1,0).</span></span>

## <a name="type"></a><span data-ttu-id="7a00c-108">Type</span><span class="sxs-lookup"><span data-stu-id="7a00c-108">Type</span></span>



|       |
|-------|
| <span data-ttu-id="7a00c-109">Type</span><span class="sxs-lookup"><span data-stu-id="7a00c-109">Type</span></span>  |
| <span data-ttu-id="7a00c-110">uint3</span><span class="sxs-lookup"><span data-stu-id="7a00c-110">uint3</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7a00c-111">Notes</span><span class="sxs-lookup"><span data-stu-id="7a00c-111">Remarks</span></span>

<span data-ttu-id="7a00c-112">Cette valeur système est facultative et est toujours dans les limites des valeurs passées à l’attribut [numThreads](sm5-attributes-numthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="7a00c-112">This system value is optional, and is always within the bounds of the values passed into the [numthreads](sm5-attributes-numthreads.md) attribute.</span></span>

<span data-ttu-id="7a00c-113">L’illustration suivante montre la relation entre les paramètres transmis à [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut [numThreads](sm5-attributes-numthreads.md) , numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système liées aux threads ([SV \_ GroupIndex](sv-groupindex.md),[SV \_ DispatchThreadID](sv-dispatchthreadid.md), SV \_ GroupThreadID,[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="7a00c-113">The following illustration shows the relationship between the parameters passed to [**Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the [numthreads](sm5-attributes-numthreads.md) attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread-related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),SV\_GroupThreadID,[SV\_GroupID](sv-groupid.md)).</span></span>

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

<span data-ttu-id="7a00c-115">Cette fonction est prise en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="7a00c-115">This function is supported in the following types of shaders:</span></span>



|        |      |        |          |       |         |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="7a00c-116">Sommet</span><span class="sxs-lookup"><span data-stu-id="7a00c-116">Vertex</span></span> | <span data-ttu-id="7a00c-117">Forme</span><span class="sxs-lookup"><span data-stu-id="7a00c-117">Hull</span></span> | <span data-ttu-id="7a00c-118">Domain</span><span class="sxs-lookup"><span data-stu-id="7a00c-118">Domain</span></span> | <span data-ttu-id="7a00c-119">Géométrie</span><span class="sxs-lookup"><span data-stu-id="7a00c-119">Geometry</span></span> | <span data-ttu-id="7a00c-120">Pixel</span><span class="sxs-lookup"><span data-stu-id="7a00c-120">Pixel</span></span> | <span data-ttu-id="7a00c-121">Compute</span><span class="sxs-lookup"><span data-stu-id="7a00c-121">Compute</span></span> |
|        |      |        |          |       | <span data-ttu-id="7a00c-122">x</span><span class="sxs-lookup"><span data-stu-id="7a00c-122">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="7a00c-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7a00c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a00c-124">Sémantique</span><span class="sxs-lookup"><span data-stu-id="7a00c-124">Semantics</span></span>](dx-graphics-hlsl-semantics.md)
</dt> <dt>

[<span data-ttu-id="7a00c-125">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="7a00c-125">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 