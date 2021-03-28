---
title: numThreads
description: Définit le nombre de threads à exécuter dans un groupe de threads unique lorsqu’un nuanceur de calcul est distribué (consultez ID3D11DeviceContext Dispatch).
ms.assetid: ec6b751c-d81c-4221-ae80-166d2a3707fe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: abcca751b58bc88ba984ac5c2210a563591d592e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382736"
---
# <a name="numthreads"></a><span data-ttu-id="5a852-103">numThreads</span><span class="sxs-lookup"><span data-stu-id="5a852-103">numthreads</span></span>

<span data-ttu-id="5a852-104">Définit le nombre de threads à exécuter dans un groupe de threads unique lorsqu’un nuanceur de calcul est distribué (consultez [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span><span class="sxs-lookup"><span data-stu-id="5a852-104">Defines the number of threads to be executed in a single thread group when a compute shader is dispatched (see [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch)).</span></span>


```
numthreads(X, Y, Z)    
```



<span data-ttu-id="5a852-105">Les valeurs X, Y et Z indiquent la taille du groupe de threads dans une direction particulière et le total de X \* Y \* Z indique le nombre de threads dans le groupe.</span><span class="sxs-lookup"><span data-stu-id="5a852-105">The X, Y and Z values indicate the size of the thread group in a particular direction and the total of X\*Y\*Z gives the number of threads in the group.</span></span> <span data-ttu-id="5a852-106">La possibilité de spécifier la taille du groupe de threads sur trois dimensions permet d’accéder à des threads individuels d’une manière logique pour les structures de données 2D et 3D.</span><span class="sxs-lookup"><span data-stu-id="5a852-106">The ability to specify the size of the thread group across three dimensions allows individual threads to be accessed in a manner that logically 2D and 3D data structures.</span></span>

<span data-ttu-id="5a852-107">Par exemple, si un nuanceur de calcul effectue une addition de matrice 4x4, numThreads peut être défini sur numThreads (4, 4, 1) et l’indexation dans les threads individuels correspond automatiquement aux entrées de la matrice.</span><span class="sxs-lookup"><span data-stu-id="5a852-107">For example, if a compute shader is doing 4x4 matrix addition then numthreads could be set to numthreads(4,4,1) and the indexing in the individual threads would automatically match the matrix entries.</span></span> <span data-ttu-id="5a852-108">Le nuanceur de calcul peut également déclarer un groupe de threads avec le même nombre de threads (16) à l’aide de numThreads (16, 1, 1), mais il doit alors calculer l’entrée de la matrice actuelle en fonction du numéro de thread actuel.</span><span class="sxs-lookup"><span data-stu-id="5a852-108">The compute shader could also declare a thread group with the same number of threads (16) using numthreads(16,1,1), however it would then have to calculate the current matrix entry based on the current thread number.</span></span>

<span data-ttu-id="5a852-109">Les valeurs de paramètre autorisées pour **numThreads** dépendent de la version du nuanceur de calcul.</span><span class="sxs-lookup"><span data-stu-id="5a852-109">The allowable parameter values for **numthreads** depends on the compute shader version.</span></span>



| <span data-ttu-id="5a852-110">Nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="5a852-110">Compute Shader</span></span> | <span data-ttu-id="5a852-111">Z maximal</span><span class="sxs-lookup"><span data-stu-id="5a852-111">Maximum Z</span></span> | <span data-ttu-id="5a852-112">Nombre maximal de threads (X \* Y \* Z)</span><span class="sxs-lookup"><span data-stu-id="5a852-112">Maximum Threads (X\*Y\*Z)</span></span> |
|----------------|-----------|---------------------------|
| <span data-ttu-id="5a852-113">CS \_ 4 \_ x</span><span class="sxs-lookup"><span data-stu-id="5a852-113">cs\_4\_x</span></span>       | <span data-ttu-id="5a852-114">1</span><span class="sxs-lookup"><span data-stu-id="5a852-114">1</span></span>         | <span data-ttu-id="5a852-115">768</span><span class="sxs-lookup"><span data-stu-id="5a852-115">768</span></span>                       |
| <span data-ttu-id="5a852-116">CS \_ 5 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5a852-116">cs\_5\_0</span></span>       | <span data-ttu-id="5a852-117">64</span><span class="sxs-lookup"><span data-stu-id="5a852-117">64</span></span>        | <span data-ttu-id="5a852-118">1 024</span><span class="sxs-lookup"><span data-stu-id="5a852-118">1024</span></span>                      |



 

<span data-ttu-id="5a852-119">L’illustration suivante montre la relation entre les paramètres passés à [**ID3D11DeviceContext ::D ispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch (5, 3, 2), les valeurs spécifiées dans l’attribut numThreads, numThreads (10, 8, 3) et les valeurs qui seront transmises au nuanceur de calcul pour les valeurs système associées aux threads ([SV \_ GroupIndex](sv-groupindex.md),[SV \_](sv-dispatchthreadid.md)DispatchThreadID, VP [ \_ GroupThreadID](sv-groupthreadid.md),[SV \_ GroupID](sv-groupid.md)).</span><span class="sxs-lookup"><span data-stu-id="5a852-119">The following illustration shows the relationship between the parameters passed to [**ID3D11DeviceContext::Dispatch**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-dispatch), Dispatch(5,3,2), the values specified in the numthreads attribute, numthreads(10,8,3), and values that will passed to the compute shader for the thread related system values ([SV\_GroupIndex](sv-groupindex.md),[SV\_DispatchThreadID](sv-dispatchthreadid.md),[SV\_GroupThreadID](sv-groupthreadid.md),[SV\_GroupID](sv-groupid.md)).</span></span>

![illustration de la relation entre la répartition, les groupes de threads et les threads](images/threadgroupids.png)

<span data-ttu-id="5a852-121">Cet attribut est pris en charge dans les types de nuanceurs suivants :</span><span class="sxs-lookup"><span data-stu-id="5a852-121">This attribute is supported in the following types of shaders:</span></span>



| <span data-ttu-id="5a852-122">Sommet</span><span class="sxs-lookup"><span data-stu-id="5a852-122">Vertex</span></span> | <span data-ttu-id="5a852-123">Forme</span><span class="sxs-lookup"><span data-stu-id="5a852-123">Hull</span></span> | <span data-ttu-id="5a852-124">Domain</span><span class="sxs-lookup"><span data-stu-id="5a852-124">Domain</span></span> | <span data-ttu-id="5a852-125">Géométrie</span><span class="sxs-lookup"><span data-stu-id="5a852-125">Geometry</span></span> | <span data-ttu-id="5a852-126">Pixel</span><span class="sxs-lookup"><span data-stu-id="5a852-126">Pixel</span></span> | <span data-ttu-id="5a852-127">Compute</span><span class="sxs-lookup"><span data-stu-id="5a852-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="5a852-128">x</span><span class="sxs-lookup"><span data-stu-id="5a852-128">x</span></span>       |



 

## <a name="related-topics"></a><span data-ttu-id="5a852-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5a852-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a852-130">Attributs du modèle de nuanceur 5</span><span class="sxs-lookup"><span data-stu-id="5a852-130">Shader Model 5 Attributes</span></span>](d3d11-graphics-reference-sm5-attributes.md)
</dt> <dt>

[<span data-ttu-id="5a852-131">Shader, modèle 5</span><span class="sxs-lookup"><span data-stu-id="5a852-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 