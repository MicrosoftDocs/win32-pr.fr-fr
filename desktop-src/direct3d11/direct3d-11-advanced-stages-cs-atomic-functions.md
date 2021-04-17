---
title: Atomic, fonctions
description: Pour accéder à un nouveau type de ressource ou à une mémoire partagée, utilisez une fonction intrinsèque verrouillée. Il est garanti que les fonctions interverrouillées fonctionnent de manière atomique. Autrement dit, il est garanti qu’ils se produisent dans l’ordre programmé. Cette section répertorie les fonctions atomiques.
ms.assetid: de75482f-2919-4761-82d7-c8a8811046bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1b152560eeb97e1e8d3daf69edb7a094fd04b7d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104508025"
---
# <a name="atomic-functions"></a><span data-ttu-id="c25bf-106">Atomic, fonctions</span><span class="sxs-lookup"><span data-stu-id="c25bf-106">Atomic Functions</span></span>

<span data-ttu-id="c25bf-107">Pour accéder à un nouveau type de ressource ou à une mémoire partagée, utilisez une fonction intrinsèque verrouillée.</span><span class="sxs-lookup"><span data-stu-id="c25bf-107">To access a new resource type or shared memory, use an interlocked intrinsic function.</span></span> <span data-ttu-id="c25bf-108">Il est garanti que les fonctions interverrouillées fonctionnent de manière atomique.</span><span class="sxs-lookup"><span data-stu-id="c25bf-108">Interlocked functions are guaranteed to operate atomically.</span></span> <span data-ttu-id="c25bf-109">Autrement dit, il est garanti qu’ils se produisent dans l’ordre programmé.</span><span class="sxs-lookup"><span data-stu-id="c25bf-109">That is, they are guaranteed to occur in the order programmed.</span></span> <span data-ttu-id="c25bf-110">Cette section répertorie les fonctions atomiques.</span><span class="sxs-lookup"><span data-stu-id="c25bf-110">This section lists the atomic functions.</span></span>

-   [<span data-ttu-id="c25bf-111">**InterlockedAdd**</span><span class="sxs-lookup"><span data-stu-id="c25bf-111">**InterlockedAdd**</span></span>](/windows/desktop/direct3dhlsl/interlockedadd)
-   [<span data-ttu-id="c25bf-112">**InterlockedMin**</span><span class="sxs-lookup"><span data-stu-id="c25bf-112">**InterlockedMin**</span></span>](/windows/desktop/direct3dhlsl/interlockedmin)
-   [<span data-ttu-id="c25bf-113">**InterlockedMax**</span><span class="sxs-lookup"><span data-stu-id="c25bf-113">**InterlockedMax**</span></span>](/windows/desktop/direct3dhlsl/interlockedmax)
-   [<span data-ttu-id="c25bf-114">**Interverrouiller**</span><span class="sxs-lookup"><span data-stu-id="c25bf-114">**InterlockedOr**</span></span>](/windows/desktop/direct3dhlsl/interlockedor)
-   [<span data-ttu-id="c25bf-115">**InterlockedAnd**</span><span class="sxs-lookup"><span data-stu-id="c25bf-115">**InterlockedAnd**</span></span>](/windows/desktop/direct3dhlsl/interlockedand)
-   [<span data-ttu-id="c25bf-116">**InterlockedXor**</span><span class="sxs-lookup"><span data-stu-id="c25bf-116">**InterlockedXor**</span></span>](/windows/desktop/direct3dhlsl/interlockedxor)
-   [<span data-ttu-id="c25bf-117">**InterlockedCompareStore**</span><span class="sxs-lookup"><span data-stu-id="c25bf-117">**InterlockedCompareStore**</span></span>](/windows/desktop/direct3dhlsl/interlockedcomparestore)
-   [<span data-ttu-id="c25bf-118">**InterlockedCompareExchange**</span><span class="sxs-lookup"><span data-stu-id="c25bf-118">**InterlockedCompareExchange**</span></span>](/windows/desktop/direct3dhlsl/interlockedcompareexchange)
-   [<span data-ttu-id="c25bf-119">**Interlockedexchang**</span><span class="sxs-lookup"><span data-stu-id="c25bf-119">**InterlockedExchange**</span></span>](/windows/desktop/direct3dhlsl/interlockedexchange)

## <a name="related-topics"></a><span data-ttu-id="c25bf-120">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c25bf-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c25bf-121">Vue d’ensemble du nuanceur de calcul</span><span class="sxs-lookup"><span data-stu-id="c25bf-121">Compute Shader Overview</span></span>](direct3d-11-advanced-stages-compute-shader.md)
</dt> </dl>

 

 