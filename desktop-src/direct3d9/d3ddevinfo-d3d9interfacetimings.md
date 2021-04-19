---
description: Pourcentage de temps de traitement des données dans le pilote. Ces statistiques peuvent aider à identifier les cas où le pilote attend d’autres ressources.
ms.assetid: 2c613349-61eb-44aa-aa7b-3161dd1fc95e
title: Structure D3DDEVINFO_D3D9INTERFACETIMINGS (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DDEVINFO_D3D9INTERFACETIMINGS
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: dfd6303f3682e29090db41fa83b38fc67f99121e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/15/2021
ms.locfileid: "106524846"
---
# <a name="d3ddevinfo_d3d9interfacetimings-structure"></a><span data-ttu-id="c37bc-104">D3DDEVINFO \_ D3D9INTERFACETIMINGS, structure</span><span class="sxs-lookup"><span data-stu-id="c37bc-104">D3DDEVINFO\_D3D9INTERFACETIMINGS structure</span></span>

<span data-ttu-id="c37bc-105">Pourcentage de temps de traitement des données dans le pilote.</span><span class="sxs-lookup"><span data-stu-id="c37bc-105">Percent of time processing data in the driver.</span></span> <span data-ttu-id="c37bc-106">Ces statistiques peuvent aider à identifier les cas où le pilote attend d’autres ressources.</span><span class="sxs-lookup"><span data-stu-id="c37bc-106">These statistics may help identify cases when the driver is waiting for other resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="c37bc-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c37bc-107">Syntax</span></span>


```C++
typedef struct D3DDEVINFO_D3D9INTERFACETIMINGS {
  FLOAT WaitingForGPUToUseApplicationResourceTimePercent;
  FLOAT WaitingForGPUToAcceptMoreCommandsTimePercent;
  FLOAT WaitingForGPUToStayWithinLatencyTimePercent;
  FLOAT WaitingForGPUExclusiveResourceTimePercent;
  FLOAT WaitingForGPUOtherTimePercent;
} D3DDEVINFO_D3D9INTERFACETIMINGS, *LPD3DDEVINFO_D3D9INTERFACETIMINGS;
```



## <a name="members"></a><span data-ttu-id="c37bc-108">Membres</span><span class="sxs-lookup"><span data-stu-id="c37bc-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="c37bc-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c37bc-109">**WaitingForGPUToUseApplicationResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c37bc-110">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c37bc-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c37bc-111">Pourcentage de temps passé par le pilote à attendre la fin du GPU à l’aide d’une ressource verrouillée (et [D3DLOCK \_ DONOTWAIT](d3dlock.md) n’a pas été spécifié).</span><span class="sxs-lookup"><span data-stu-id="c37bc-111">Percentage of time the driver spent waiting for the GPU to finish using a locked resource (and [D3DLOCK\_DONOTWAIT](d3dlock.md) wasn't specified).</span></span>

</dd> <dt>

<span data-ttu-id="c37bc-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c37bc-112">**WaitingForGPUToAcceptMoreCommandsTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c37bc-113">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c37bc-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c37bc-114">Pourcentage de temps passé par le pilote à attendre que le GPU termine le traitement de certaines commandes avant que le pilote puisse en envoyer davantage.</span><span class="sxs-lookup"><span data-stu-id="c37bc-114">Percentage of time the driver spent waiting for the GPU to finish processing some commands before the driver could send more.</span></span> <span data-ttu-id="c37bc-115">Cela indique que le pilote n’a plus suffisamment de place pour envoyer des commandes au GPU.</span><span class="sxs-lookup"><span data-stu-id="c37bc-115">This indicates the driver has run out of room to send commands to the GPU.</span></span>

</dd> <dt>

<span data-ttu-id="c37bc-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c37bc-116">**WaitingForGPUToStayWithinLatencyTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c37bc-117">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c37bc-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c37bc-118">Pourcentage de temps passé par le pilote à attendre la latence du GPU pour réduire à moins de trois frames de rendu.</span><span class="sxs-lookup"><span data-stu-id="c37bc-118">Percentage of time the driver spent waiting for the GPU latency to reduce to less than three rendering frames.</span></span>

<span data-ttu-id="c37bc-119">Si une application est limitée par GPU, le pilote doit bloquer l’UC jusqu’à ce que le GPU soit dans trois frames.</span><span class="sxs-lookup"><span data-stu-id="c37bc-119">If an application is GPU-limited, the driver must stall the CPU until the GPU gets within three frames.</span></span> <span data-ttu-id="c37bc-120">Cela empêche une application de mettre en file d’attente de nombreuses secondes les appels de rendu, ce qui peut augmenter considérablement la latence entre le moment où l’utilisateur entre de nouvelles données et le moment où l’utilisateur voit les résultats de cette entrée.</span><span class="sxs-lookup"><span data-stu-id="c37bc-120">This prevents an application from queuing up many seconds' worth of rendering calls which may dramatically increase the latency between when the user inputs new data and when the user sees the results of that input.</span></span> <span data-ttu-id="c37bc-121">En général, le pilote peut effectuer le suivi du nombre de fois où l’élément [**présent**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) est appelé pour empêcher la mise en file d’attente de plus de trois frames de travail de rendu.</span><span class="sxs-lookup"><span data-stu-id="c37bc-121">In general, the driver can track the number of times [**Present**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) is called to prevent queuing up more than three frames of rendering work.</span></span>

</dd> <dt>

<span data-ttu-id="c37bc-122">**WaitingForGPUExclusiveResourceTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c37bc-122">**WaitingForGPUExclusiveResourceTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c37bc-123">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c37bc-123">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c37bc-124">Pourcentage de temps passé par le pilote à attendre une ressource qui ne peut pas être canalisée (qui est exécutée en parallèle).</span><span class="sxs-lookup"><span data-stu-id="c37bc-124">Percentage of time the driver spent waiting for a resource that cannot be pipelined (that is operated in parallel).</span></span> <span data-ttu-id="c37bc-125">Une application peut souhaiter éviter d’utiliser une ressource non pipeline pour des raisons de performances.</span><span class="sxs-lookup"><span data-stu-id="c37bc-125">An application may want to avoid using a non-pipelined resource for performance reasons.</span></span>

</dd> <dt>

<span data-ttu-id="c37bc-126">**WaitingForGPUOtherTimePercent**</span><span class="sxs-lookup"><span data-stu-id="c37bc-126">**WaitingForGPUOtherTimePercent**</span></span>
</dt> <dd>

<span data-ttu-id="c37bc-127">Type : **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c37bc-127">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

</dd> <dd>

<span data-ttu-id="c37bc-128">Pourcentage de temps passé par le pilote à attendre un autre traitement GPU.</span><span class="sxs-lookup"><span data-stu-id="c37bc-128">Percentage of time the driver spent waiting for other GPU processing.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c37bc-129">Notes</span><span class="sxs-lookup"><span data-stu-id="c37bc-129">Remarks</span></span>

<span data-ttu-id="c37bc-130">Ces mesures permettent d’identifier le moment où un pilote est en attente et ce qu’il attend.</span><span class="sxs-lookup"><span data-stu-id="c37bc-130">These metrics help identify when a driver is waiting and what it is waiting for.</span></span> <span data-ttu-id="c37bc-131">Les pourcentages élevés ne sont pas nécessairement un problème.</span><span class="sxs-lookup"><span data-stu-id="c37bc-131">High percentages are not necessarily a problem.</span></span>

<span data-ttu-id="c37bc-132">Ces métriques globales du système peuvent ou non être implémentées.</span><span class="sxs-lookup"><span data-stu-id="c37bc-132">These system-global metrics may or may not be implemented.</span></span> <span data-ttu-id="c37bc-133">En fonction du matériel spécifique, ces métriques peuvent ne pas prendre en charge plusieurs requêtes simultanément.</span><span class="sxs-lookup"><span data-stu-id="c37bc-133">Depending on the specific hardware, these metrics may not support multiple queries simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="c37bc-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c37bc-134">Requirements</span></span>



| <span data-ttu-id="c37bc-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c37bc-135">Requirement</span></span> | <span data-ttu-id="c37bc-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="c37bc-136">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="c37bc-137">En-tête</span><span class="sxs-lookup"><span data-stu-id="c37bc-137">Header</span></span><br/> | <dl> <span data-ttu-id="c37bc-138"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="c37bc-138"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c37bc-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c37bc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37bc-140">Structures Direct3D</span><span class="sxs-lookup"><span data-stu-id="c37bc-140">Direct3D Structures</span></span>](dx9-graphics-reference-d3d-structures.md)
</dt> <dt>

[<span data-ttu-id="c37bc-141">**GetData**</span><span class="sxs-lookup"><span data-stu-id="c37bc-141">**GetData**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata)
</dt> </dl>

 

 
