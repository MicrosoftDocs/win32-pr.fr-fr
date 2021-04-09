---
title: État de l’appel asynchrone
description: Cette page décrit l’état d’appel asynchrone pour les appels RPC.
ms.assetid: 4a594dad-a8a1-44e9-8648-ddc2539c234c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96331a18b267b2e44072840727c8fd06afd11d6b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840854"
---
# <a name="asynchronous-call-state"></a><span data-ttu-id="47bef-103">État de l’appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="47bef-103">Asynchronous Call State</span></span>

<span data-ttu-id="47bef-104">Cette page décrit l’état d’appel asynchrone pour les appels RPC.</span><span class="sxs-lookup"><span data-stu-id="47bef-104">This page describes the Asynchronous Call State for RPC calls.</span></span>

## <a name="client-behavior"></a><span data-ttu-id="47bef-105">Comportement du client</span><span class="sxs-lookup"><span data-stu-id="47bef-105">Client Behavior</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="47bef-106">State</span><span class="sxs-lookup"><span data-stu-id="47bef-106">State</span></span></th>
<th><span data-ttu-id="47bef-107">Nom de l’état</span><span class="sxs-lookup"><span data-stu-id="47bef-107">State name</span></span></th>
<th><span data-ttu-id="47bef-108">Action</span><span class="sxs-lookup"><span data-stu-id="47bef-108">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="47bef-109">C</span><span class="sxs-lookup"><span data-stu-id="47bef-109">C</span></span></td>
<td><span data-ttu-id="47bef-110">Effectuer l’appel</span><span class="sxs-lookup"><span data-stu-id="47bef-110">Make the call</span></span></td>
<td><span data-ttu-id="47bef-111">Rendre le RPC</span><span class="sxs-lookup"><span data-stu-id="47bef-111">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="47bef-112">En cas de réussite, accédez à l’État WComp</span><span class="sxs-lookup"><span data-stu-id="47bef-112">On success go to state WComp</span></span></li>
<li><span data-ttu-id="47bef-113">En cas d’exception, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="47bef-113">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="47bef-114">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="47bef-114">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47bef-115">Puissiez</span><span class="sxs-lookup"><span data-stu-id="47bef-115">Can</span></span></td>
<td><span data-ttu-id="47bef-116">Annuler l’appel</span><span class="sxs-lookup"><span data-stu-id="47bef-116">Cancel the call</span></span></td>
<td><span data-ttu-id="47bef-117">Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp</span><span class="sxs-lookup"><span data-stu-id="47bef-117">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47bef-118">WComp</span><span class="sxs-lookup"><span data-stu-id="47bef-118">WComp</span></span></td>
<td><span data-ttu-id="47bef-119">Attendre la fin de l’opération</span><span class="sxs-lookup"><span data-stu-id="47bef-119">Wait for completion</span></span></td>
<td><span data-ttu-id="47bef-120">Attendre la réception de la notification notificationCall-Complete</span><span class="sxs-lookup"><span data-stu-id="47bef-120">Wait for notificationCall-complete notification should be received</span></span><br/> <span data-ttu-id="47bef-121">Aller à la comp.</span><span class="sxs-lookup"><span data-stu-id="47bef-121">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="47bef-122">Conformes</span><span class="sxs-lookup"><span data-stu-id="47bef-122">Comp</span></span></td>
<td><span data-ttu-id="47bef-123">Completion</span><span class="sxs-lookup"><span data-stu-id="47bef-123">Completion</span></span></td>
<td><span data-ttu-id="47bef-124">Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin</span><span class="sxs-lookup"><span data-stu-id="47bef-124">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="47bef-125">End</span><span class="sxs-lookup"><span data-stu-id="47bef-125">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="server-behavior"></a><span data-ttu-id="47bef-126">Comportement du serveur</span><span class="sxs-lookup"><span data-stu-id="47bef-126">Server Behavior</span></span>



| <span data-ttu-id="47bef-127">State</span><span class="sxs-lookup"><span data-stu-id="47bef-127">State</span></span> | <span data-ttu-id="47bef-128">Nom de l’état</span><span class="sxs-lookup"><span data-stu-id="47bef-128">State name</span></span>     | <span data-ttu-id="47bef-129">Action</span><span class="sxs-lookup"><span data-stu-id="47bef-129">Action</span></span>                                                                                                                                                                                                              |
|-------|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47bef-130">D</span><span class="sxs-lookup"><span data-stu-id="47bef-130">D</span></span>     | <span data-ttu-id="47bef-131">Dispatch</span><span class="sxs-lookup"><span data-stu-id="47bef-131">Dispatch</span></span>       | <span data-ttu-id="47bef-132">L’appel est distribué par le runtimeProcess RPC</span><span class="sxs-lookup"><span data-stu-id="47bef-132">The call is dispatched by the RPC runtimeProcess</span></span><br/> <span data-ttu-id="47bef-133">Aller à la comp.</span><span class="sxs-lookup"><span data-stu-id="47bef-133">Go to Comp</span></span><br/> <span data-ttu-id="47bef-134">Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="47bef-134">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="47bef-135">Pour échouer correctement : accédez à un</span><span class="sxs-lookup"><span data-stu-id="47bef-135">To fail gracefully: go to A</span></span><br/> |
| <span data-ttu-id="47bef-136">Un</span><span class="sxs-lookup"><span data-stu-id="47bef-136">A</span></span>     | <span data-ttu-id="47bef-137">Abandonner l’appel</span><span class="sxs-lookup"><span data-stu-id="47bef-137">Abort the call</span></span> | <span data-ttu-id="47bef-138">Appeler [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)aller à la fin</span><span class="sxs-lookup"><span data-stu-id="47bef-138">Call [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)Go to End</span></span><br/>                                                                                                                                             |
| <span data-ttu-id="47bef-139">Conformes</span><span class="sxs-lookup"><span data-stu-id="47bef-139">Comp</span></span>  | <span data-ttu-id="47bef-140">Completion</span><span class="sxs-lookup"><span data-stu-id="47bef-140">Completion</span></span>     | <span data-ttu-id="47bef-141">Problème [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)aller à la fin</span><span class="sxs-lookup"><span data-stu-id="47bef-141">Issue [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)Go to End</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="47bef-142">End</span><span class="sxs-lookup"><span data-stu-id="47bef-142">End</span></span>   |                |                                                                                                                                                                                                                     |



 

 

 





