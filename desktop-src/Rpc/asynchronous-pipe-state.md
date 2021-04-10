---
title: État du canal asynchrone
description: Cette page décrit l’état du canal asynchrone pour les appels RPC.
ms.assetid: af937eba-6b70-447a-af76-a8e27f5754e3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8396b08c7ef7b8152457d9426883645fab39bdef
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030813"
---
# <a name="asynchronous-pipe-state"></a><span data-ttu-id="b46da-103">État du canal asynchrone</span><span class="sxs-lookup"><span data-stu-id="b46da-103">Asynchronous Pipe State</span></span>

<span data-ttu-id="b46da-104">Cette page décrit l’état du canal asynchrone pour les appels RPC.</span><span class="sxs-lookup"><span data-stu-id="b46da-104">This page describes the Asynchronous Pipe State for RPC calls.</span></span>

## <a name="in-pipe"></a><span data-ttu-id="b46da-105">DANS le canal</span><span class="sxs-lookup"><span data-stu-id="b46da-105">IN Pipe</span></span>

<span data-ttu-id="b46da-106">Comportement du client</span><span class="sxs-lookup"><span data-stu-id="b46da-106">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b46da-107">State</span><span class="sxs-lookup"><span data-stu-id="b46da-107">State</span></span></th>
<th><span data-ttu-id="b46da-108">Nom d’état</span><span class="sxs-lookup"><span data-stu-id="b46da-108">State Name</span></span></th>
<th><span data-ttu-id="b46da-109">Action</span><span class="sxs-lookup"><span data-stu-id="b46da-109">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b46da-110">C</span><span class="sxs-lookup"><span data-stu-id="b46da-110">C</span></span></td>
<td><span data-ttu-id="b46da-111">Effectuer l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-111">Make the call</span></span></td>
<td><span data-ttu-id="b46da-112">Rendre le RPC</span><span class="sxs-lookup"><span data-stu-id="b46da-112">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="b46da-113">En cas de réussite, accédez à l’État WS</span><span class="sxs-lookup"><span data-stu-id="b46da-113">On success go to state WS</span></span></li>
<li><span data-ttu-id="b46da-114">En cas d’exception, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-114">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="b46da-115">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-115">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-116">P</span><span class="sxs-lookup"><span data-stu-id="b46da-116">P</span></span></td>
<td><span data-ttu-id="b46da-117">Envoi de données (push)</span><span class="sxs-lookup"><span data-stu-id="b46da-117">Push</span></span></td>
<td><span data-ttu-id="b46da-118">Créer un push</span><span class="sxs-lookup"><span data-stu-id="b46da-118">Make a push</span></span>
<ul>
<li><span data-ttu-id="b46da-119">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-119">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-120">En cas de réussite, accédez à WS</span><span class="sxs-lookup"><span data-stu-id="b46da-120">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="b46da-121">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-121">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-122">WS</span><span class="sxs-lookup"><span data-stu-id="b46da-122">WS</span></span></td>
<td><span data-ttu-id="b46da-123">Attendre l’envoi</span><span class="sxs-lookup"><span data-stu-id="b46da-123">Wait for Send</span></span></td>
<td><span data-ttu-id="b46da-124">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-124">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-125">En cas d’échec d’une notification, accédez à CAN</span><span class="sxs-lookup"><span data-stu-id="b46da-125">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="b46da-126">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à P</span><span class="sxs-lookup"><span data-stu-id="b46da-126">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="b46da-127">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</span><span class="sxs-lookup"><span data-stu-id="b46da-127">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b46da-128">Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> est reçue, Go COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-128">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b46da-129">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-129">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-130">NP</span><span class="sxs-lookup"><span data-stu-id="b46da-130">NP</span></span></td>
<td><span data-ttu-id="b46da-131">Push null</span><span class="sxs-lookup"><span data-stu-id="b46da-131">Null Push</span></span></td>
<td><span data-ttu-id="b46da-132">Push 0 octets (push null)</span><span class="sxs-lookup"><span data-stu-id="b46da-132">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="b46da-133">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-133">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-134">En cas de réussite, accédez à WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-134">On success go to WComp</span></span></li>
</ul>
<span data-ttu-id="b46da-135">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-135">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-136">Puissiez</span><span class="sxs-lookup"><span data-stu-id="b46da-136">Can</span></span></td>
<td><span data-ttu-id="b46da-137">Annuler l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-137">Cancel the Call</span></span></td>
<td><span data-ttu-id="b46da-138">Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-138">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-139">WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-139">WComp</span></span></td>
<td><span data-ttu-id="b46da-140">Attendre la fin de l’opération</span><span class="sxs-lookup"><span data-stu-id="b46da-140">Wait for Completion</span></span></td>
<td><span data-ttu-id="b46da-141">L’attente de la notification de fin de notificationCall doit être reçue.</span><span class="sxs-lookup"><span data-stu-id="b46da-141">Wait for notificationCall-complete notification should be received.</span></span><br/> <span data-ttu-id="b46da-142">Aller à la comp.</span><span class="sxs-lookup"><span data-stu-id="b46da-142">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-143">Conformes</span><span class="sxs-lookup"><span data-stu-id="b46da-143">Comp</span></span></td>
<td><span data-ttu-id="b46da-144">Completion</span><span class="sxs-lookup"><span data-stu-id="b46da-144">Completion</span></span></td>
<td><span data-ttu-id="b46da-145">Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-145">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-146">End</span><span class="sxs-lookup"><span data-stu-id="b46da-146">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="b46da-147">Comportement du serveur</span><span class="sxs-lookup"><span data-stu-id="b46da-147">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b46da-148">State</span><span class="sxs-lookup"><span data-stu-id="b46da-148">State</span></span></th>
<th><span data-ttu-id="b46da-149">Nom d’état</span><span class="sxs-lookup"><span data-stu-id="b46da-149">State Name</span></span></th>
<th><span data-ttu-id="b46da-150">Action</span><span class="sxs-lookup"><span data-stu-id="b46da-150">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b46da-151">D</span><span class="sxs-lookup"><span data-stu-id="b46da-151">D</span></span></td>
<td><span data-ttu-id="b46da-152">Dispatch</span><span class="sxs-lookup"><span data-stu-id="b46da-152">Dispatch</span></span></td>
<td><span data-ttu-id="b46da-153">L’appel est distribué par le runtime RPC accéder à P</span><span class="sxs-lookup"><span data-stu-id="b46da-153">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="b46da-154">Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-154">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="b46da-155">Pour échouer correctement : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-155">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-156">P</span><span class="sxs-lookup"><span data-stu-id="b46da-156">P</span></span></td>
<td><span data-ttu-id="b46da-157">Extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-157">Pull</span></span></td>
<td><span data-ttu-id="b46da-158">Créer une extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-158">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b46da-159">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-159">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-160">En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accéder à P</span><span class="sxs-lookup"><span data-stu-id="b46da-160">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b46da-161">En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), atteindre la comp.</span><span class="sxs-lookup"><span data-stu-id="b46da-161">On success and synchronous completion with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="b46da-162">En cas de réussite et d’achèvement asynchrone (retournée ERROR_IO_PENDING), accédez à WP</span><span class="sxs-lookup"><span data-stu-id="b46da-162">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="b46da-163">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-163">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-164">WP</span><span class="sxs-lookup"><span data-stu-id="b46da-164">WP</span></span></td>
<td><span data-ttu-id="b46da-165">Attendre l’extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-165">Wait for Pull</span></span></td>
<td><span data-ttu-id="b46da-166">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-166">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-167">En cas d’échec de la saisie semi-automatique, accédez à</span><span class="sxs-lookup"><span data-stu-id="b46da-167">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b46da-168">Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-168">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="b46da-169">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, aller à P</span><span class="sxs-lookup"><span data-stu-id="b46da-169">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b46da-170">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet de lecture (extraction null), atteindre la comp.</span><span class="sxs-lookup"><span data-stu-id="b46da-170">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="b46da-171">Si une défaillance est reçue, accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-171">If a failure is received go to A</span></span></li>
</ul>
<span data-ttu-id="b46da-172">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-172">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-173">Un</span><span class="sxs-lookup"><span data-stu-id="b46da-173">A</span></span></td>
<td><span data-ttu-id="b46da-174">Abandonner l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-174">Abort the Call</span></span></td>
<td><span data-ttu-id="b46da-175">Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-175">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-176">Conformes</span><span class="sxs-lookup"><span data-stu-id="b46da-176">Comp</span></span></td>
<td><span data-ttu-id="b46da-177">Completion</span><span class="sxs-lookup"><span data-stu-id="b46da-177">Completion</span></span></td>
<td><span data-ttu-id="b46da-178">Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-178">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-179">End</span><span class="sxs-lookup"><span data-stu-id="b46da-179">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="out-pipe"></a><span data-ttu-id="b46da-180">Canal de sortie</span><span class="sxs-lookup"><span data-stu-id="b46da-180">OUT Pipe</span></span>

<span data-ttu-id="b46da-181">Comportement du client</span><span class="sxs-lookup"><span data-stu-id="b46da-181">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b46da-182">State</span><span class="sxs-lookup"><span data-stu-id="b46da-182">State</span></span></th>
<th><span data-ttu-id="b46da-183">Nom d’état</span><span class="sxs-lookup"><span data-stu-id="b46da-183">State Name</span></span></th>
<th><span data-ttu-id="b46da-184">Action</span><span class="sxs-lookup"><span data-stu-id="b46da-184">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b46da-185">C</span><span class="sxs-lookup"><span data-stu-id="b46da-185">C</span></span></td>
<td><span data-ttu-id="b46da-186">Effectuer l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-186">Make the call</span></span></td>
<td><span data-ttu-id="b46da-187">Rendre le RPC</span><span class="sxs-lookup"><span data-stu-id="b46da-187">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="b46da-188">En cas de réussite, accédez à P</span><span class="sxs-lookup"><span data-stu-id="b46da-188">On success go to P</span></span></li>
<li><span data-ttu-id="b46da-189">En cas d’échec, accédez à COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-189">On failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="b46da-190">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-190">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-191">P</span><span class="sxs-lookup"><span data-stu-id="b46da-191">P</span></span></td>
<td><span data-ttu-id="b46da-192">Extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-192">Pull</span></span></td>
<td><span data-ttu-id="b46da-193">Créer une extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-193">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b46da-194">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-194">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-195">En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accéder à P</span><span class="sxs-lookup"><span data-stu-id="b46da-195">On success and synchronous completion with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b46da-196">En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-196">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="b46da-197">En cas de réussite et d’achèvement asynchrone (retournée ERROR_IO_PENDING), accédez à WP</span><span class="sxs-lookup"><span data-stu-id="b46da-197">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WP</span></span></li>
</ul>
<span data-ttu-id="b46da-198">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-198">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-199">WP</span><span class="sxs-lookup"><span data-stu-id="b46da-199">WP</span></span></td>
<td><span data-ttu-id="b46da-200">Attendre l’extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-200">Wait for Pull</span></span></td>
<td><span data-ttu-id="b46da-201">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-201">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-202">En cas d’échec de la saisie semi-automatique, accédez à CAN</span><span class="sxs-lookup"><span data-stu-id="b46da-202">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="b46da-203">Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accéder à peut</span><span class="sxs-lookup"><span data-stu-id="b46da-203">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="b46da-204">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, aller à P</span><span class="sxs-lookup"><span data-stu-id="b46da-204">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to P</span></span></li>
<li><span data-ttu-id="b46da-205">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet de lecture (extraction null), atteindre la comp.</span><span class="sxs-lookup"><span data-stu-id="b46da-205">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read (null pull) go to Comp</span></span></li>
<li><span data-ttu-id="b46da-206">Si une défaillance est reçue, Go peut</span><span class="sxs-lookup"><span data-stu-id="b46da-206">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="b46da-207">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-207">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-208">Puissiez</span><span class="sxs-lookup"><span data-stu-id="b46da-208">Can</span></span></td>
<td><span data-ttu-id="b46da-209">Annuler l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-209">Cancel the Call</span></span></td>
<td><span data-ttu-id="b46da-210">Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-210">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-211">WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-211">WComp</span></span></td>
<td><span data-ttu-id="b46da-212">Attendre la fin de l’opération</span><span class="sxs-lookup"><span data-stu-id="b46da-212">Wait for Completion</span></span></td>
<td><span data-ttu-id="b46da-213">Attendre la notification.</span><span class="sxs-lookup"><span data-stu-id="b46da-213">Wait for notification.</span></span> <span data-ttu-id="b46da-214">La notification de fin d’appel doit être reçue.</span><span class="sxs-lookup"><span data-stu-id="b46da-214">Call-complete notification should be received.</span></span><br/> <span data-ttu-id="b46da-215">Aller à la comp.</span><span class="sxs-lookup"><span data-stu-id="b46da-215">Go to Comp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-216">Conformes</span><span class="sxs-lookup"><span data-stu-id="b46da-216">Comp</span></span></td>
<td><span data-ttu-id="b46da-217">Completion</span><span class="sxs-lookup"><span data-stu-id="b46da-217">Completion</span></span></td>
<td><span data-ttu-id="b46da-218">Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-218">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-219">End</span><span class="sxs-lookup"><span data-stu-id="b46da-219">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="b46da-220">Comportement du serveur</span><span class="sxs-lookup"><span data-stu-id="b46da-220">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b46da-221">State</span><span class="sxs-lookup"><span data-stu-id="b46da-221">State</span></span></th>
<th><span data-ttu-id="b46da-222">Nom d’état</span><span class="sxs-lookup"><span data-stu-id="b46da-222">State Name</span></span></th>
<th><span data-ttu-id="b46da-223">Action</span><span class="sxs-lookup"><span data-stu-id="b46da-223">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b46da-224">D</span><span class="sxs-lookup"><span data-stu-id="b46da-224">D</span></span></td>
<td><span data-ttu-id="b46da-225">Dispatch</span><span class="sxs-lookup"><span data-stu-id="b46da-225">Dispatch</span></span></td>
<td><span data-ttu-id="b46da-226">L’appel est distribué par le runtime RPC accéder à P</span><span class="sxs-lookup"><span data-stu-id="b46da-226">The call is dispatched by the RPC runtime Go to P</span></span><br/> <span data-ttu-id="b46da-227">Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-227">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="b46da-228">Pour échouer correctement : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-228">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-229">P</span><span class="sxs-lookup"><span data-stu-id="b46da-229">P</span></span></td>
<td><span data-ttu-id="b46da-230">Envoi de données (push)</span><span class="sxs-lookup"><span data-stu-id="b46da-230">Push</span></span></td>
<td><span data-ttu-id="b46da-231">Créer un push</span><span class="sxs-lookup"><span data-stu-id="b46da-231">Make a push</span></span>
<ul>
<li><span data-ttu-id="b46da-232">En cas de réussite, accédez à WP</span><span class="sxs-lookup"><span data-stu-id="b46da-232">On success go to WP</span></span></li>
<li><span data-ttu-id="b46da-233">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-233">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="b46da-234">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-234">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-235">WP</span><span class="sxs-lookup"><span data-stu-id="b46da-235">WP</span></span></td>
<td><span data-ttu-id="b46da-236">Attendre la notification push</span><span class="sxs-lookup"><span data-stu-id="b46da-236">Wait for Push</span></span></td>
<td><span data-ttu-id="b46da-237">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-237">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-238">En cas d’échec de la saisie semi-automatique, accédez à</span><span class="sxs-lookup"><span data-stu-id="b46da-238">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b46da-239">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à P</span><span class="sxs-lookup"><span data-stu-id="b46da-239">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to P</span></span></li>
<li><span data-ttu-id="b46da-240">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</span><span class="sxs-lookup"><span data-stu-id="b46da-240">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b46da-241">Si une défaillance est reçue, cliquez sur COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-241">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b46da-242">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-242">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-243">NP</span><span class="sxs-lookup"><span data-stu-id="b46da-243">NP</span></span></td>
<td><span data-ttu-id="b46da-244">Push null</span><span class="sxs-lookup"><span data-stu-id="b46da-244">Null Push</span></span></td>
<td><span data-ttu-id="b46da-245">Pousser 0 octets</span><span class="sxs-lookup"><span data-stu-id="b46da-245">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="b46da-246">en cas de réussite, accédez à WNP</span><span class="sxs-lookup"><span data-stu-id="b46da-246">on success go to WNP</span></span></li>
<li><span data-ttu-id="b46da-247">en cas d’échec, accédez à COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-247">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="b46da-248">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-248">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-249">WNP</span><span class="sxs-lookup"><span data-stu-id="b46da-249">WNP</span></span></td>
<td><span data-ttu-id="b46da-250">Attendre une notification push null</span><span class="sxs-lookup"><span data-stu-id="b46da-250">Wait for Null Push</span></span></td>
<td><span data-ttu-id="b46da-251">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-251">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-252">En cas d’échec de la saisie semi-automatique, accédez à</span><span class="sxs-lookup"><span data-stu-id="b46da-252">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b46da-253">Si une défaillance est reçue, cliquez sur COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-253">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="b46da-254">Si une réussite est reçue, Go COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-254">If a success is received go Comp</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-255">Un</span><span class="sxs-lookup"><span data-stu-id="b46da-255">A</span></span></td>
<td><span data-ttu-id="b46da-256">Abandonner l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-256">Abort the Call</span></span></td>
<td><span data-ttu-id="b46da-257">Appelez <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-257">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-258">Conformes</span><span class="sxs-lookup"><span data-stu-id="b46da-258">Comp</span></span></td>
<td><span data-ttu-id="b46da-259">Completion</span><span class="sxs-lookup"><span data-stu-id="b46da-259">Completion</span></span></td>
<td><span data-ttu-id="b46da-260">Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-260">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-261">End</span><span class="sxs-lookup"><span data-stu-id="b46da-261">End</span></span></td>


</tr>
</tbody>
</table>



 

## <a name="in-out-pipe"></a><span data-ttu-id="b46da-262">Canal de sortie</span><span class="sxs-lookup"><span data-stu-id="b46da-262">IN-OUT Pipe</span></span>

<span data-ttu-id="b46da-263">Comportement du client</span><span class="sxs-lookup"><span data-stu-id="b46da-263">Client Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b46da-264">State</span><span class="sxs-lookup"><span data-stu-id="b46da-264">State</span></span></th>
<th><span data-ttu-id="b46da-265">Nom d’état</span><span class="sxs-lookup"><span data-stu-id="b46da-265">State Name</span></span></th>
<th><span data-ttu-id="b46da-266">Action</span><span class="sxs-lookup"><span data-stu-id="b46da-266">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b46da-267">C</span><span class="sxs-lookup"><span data-stu-id="b46da-267">C</span></span></td>
<td><span data-ttu-id="b46da-268">Effectuer l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-268">Make the call</span></span></td>
<td><span data-ttu-id="b46da-269">Rendre le RPC</span><span class="sxs-lookup"><span data-stu-id="b46da-269">Make the RPC</span></span>
<ul>
<li><span data-ttu-id="b46da-270">En cas de réussite, accédez à WS</span><span class="sxs-lookup"><span data-stu-id="b46da-270">On success go to WS</span></span></li>
<li><span data-ttu-id="b46da-271">En cas d’exception, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-271">On exception go to End</span></span></li>
</ul>
<span data-ttu-id="b46da-272">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-272">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-273">PS</span><span class="sxs-lookup"><span data-stu-id="b46da-273">PS</span></span></td>
<td><span data-ttu-id="b46da-274">Envoi de données (push)</span><span class="sxs-lookup"><span data-stu-id="b46da-274">Push</span></span></td>
<td><span data-ttu-id="b46da-275">Créer un push</span><span class="sxs-lookup"><span data-stu-id="b46da-275">Make a push</span></span>
<ul>
<li><span data-ttu-id="b46da-276">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-276">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-277">En cas de réussite, accédez à WS</span><span class="sxs-lookup"><span data-stu-id="b46da-277">On success go to WS</span></span></li>
</ul>
<span data-ttu-id="b46da-278">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-278">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-279">WS</span><span class="sxs-lookup"><span data-stu-id="b46da-279">WS</span></span></td>
<td><span data-ttu-id="b46da-280">Attendre l’envoi</span><span class="sxs-lookup"><span data-stu-id="b46da-280">Wait for Send</span></span></td>
<td><span data-ttu-id="b46da-281">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-281">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-282">En cas d’échec d’une notification, accédez à CAN</span><span class="sxs-lookup"><span data-stu-id="b46da-282">On failure to get a notification go to Can</span></span></li>
<li><span data-ttu-id="b46da-283">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à PS</span><span class="sxs-lookup"><span data-stu-id="b46da-283">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="b46da-284">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</span><span class="sxs-lookup"><span data-stu-id="b46da-284">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b46da-285">Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> est reçue, Go COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-285">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcCallComplete</strong></a> is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b46da-286">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-286">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-287">NP</span><span class="sxs-lookup"><span data-stu-id="b46da-287">NP</span></span></td>
<td><span data-ttu-id="b46da-288">Push null</span><span class="sxs-lookup"><span data-stu-id="b46da-288">Null Push</span></span></td>
<td><span data-ttu-id="b46da-289">Push 0 octets (push null)</span><span class="sxs-lookup"><span data-stu-id="b46da-289">Push 0 bytes (null push)</span></span>
<ul>
<li><span data-ttu-id="b46da-290">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-290">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-291">En cas de réussite, accédez à PL</span><span class="sxs-lookup"><span data-stu-id="b46da-291">On success go to PL</span></span></li>
</ul>
<span data-ttu-id="b46da-292">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-292">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-293">PL</span><span class="sxs-lookup"><span data-stu-id="b46da-293">PL</span></span></td>
<td><span data-ttu-id="b46da-294">Extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-294">Pull</span></span></td>
<td><span data-ttu-id="b46da-295">Créer une extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-295">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b46da-296">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-296">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-297">En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accédez à PL</span><span class="sxs-lookup"><span data-stu-id="b46da-297">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b46da-298">En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-298">On success and synchronous completion with zero bytes read (null pull) go to WComp</span></span></li>
<li><span data-ttu-id="b46da-299">En cas de réussite et d’achèvement asynchrone (ERROR_IO_PENDING est retourné), accédez à WPL</span><span class="sxs-lookup"><span data-stu-id="b46da-299">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="b46da-300">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-300">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-301">WPL</span><span class="sxs-lookup"><span data-stu-id="b46da-301">WPL</span></span></td>
<td><span data-ttu-id="b46da-302">Attendre l’extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-302">Wait for Pull</span></span></td>
<td><span data-ttu-id="b46da-303">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-303">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-304">En cas d’échec de la saisie semi-automatique, accédez à CAN</span><span class="sxs-lookup"><span data-stu-id="b46da-304">On failure to get a completion go to Can</span></span></li>
<li><span data-ttu-id="b46da-305">Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accéder à peut</span><span class="sxs-lookup"><span data-stu-id="b46da-305">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to Can</span></span></li>
<li><span data-ttu-id="b46da-306">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, accédez à pl</span><span class="sxs-lookup"><span data-stu-id="b46da-306">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b46da-307">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet lu atteindre la comp.</span><span class="sxs-lookup"><span data-stu-id="b46da-307">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to Comp</span></span></li>
<li><span data-ttu-id="b46da-308">Si une défaillance est reçue, Go peut</span><span class="sxs-lookup"><span data-stu-id="b46da-308">If a failure is received go Can</span></span></li>
</ul>
<span data-ttu-id="b46da-309">Pour échec : atteindre peut</span><span class="sxs-lookup"><span data-stu-id="b46da-309">To fail: go to Can</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-310">Puissiez</span><span class="sxs-lookup"><span data-stu-id="b46da-310">Can</span></span></td>
<td><span data-ttu-id="b46da-311">Annuler l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-311">Cancel the Call</span></span></td>
<td><span data-ttu-id="b46da-312">Appeler <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>accéder à WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-312">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall"><strong>RpcAsyncCancelCall</strong></a>Go to WComp</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-313">WComp</span><span class="sxs-lookup"><span data-stu-id="b46da-313">WComp</span></span></td>
<td><span data-ttu-id="b46da-314">Attendre la fin de l’opération</span><span class="sxs-lookup"><span data-stu-id="b46da-314">Wait for Completion</span></span></td>
<td><span data-ttu-id="b46da-315">Attendre la notification.</span><span class="sxs-lookup"><span data-stu-id="b46da-315">Wait for notification.</span></span> <span data-ttu-id="b46da-316">La notification CallComplete doit être reçue.</span><span class="sxs-lookup"><span data-stu-id="b46da-316">CallComplete notification should be received.</span></span><br/> <span data-ttu-id="b46da-317">Aller à la comp.</span><span class="sxs-lookup"><span data-stu-id="b46da-317">Go to Comp</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-318">Conformes</span><span class="sxs-lookup"><span data-stu-id="b46da-318">Comp</span></span></td>
<td><span data-ttu-id="b46da-319">Completion</span><span class="sxs-lookup"><span data-stu-id="b46da-319">Completion</span></span></td>
<td><span data-ttu-id="b46da-320">Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-320">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>Go to End</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-321">End</span><span class="sxs-lookup"><span data-stu-id="b46da-321">End</span></span></td>


</tr>
</tbody>
</table>



 

<span data-ttu-id="b46da-322">Comportement du serveur</span><span class="sxs-lookup"><span data-stu-id="b46da-322">Server Behavior</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b46da-323">State</span><span class="sxs-lookup"><span data-stu-id="b46da-323">State</span></span></th>
<th><span data-ttu-id="b46da-324">Nom d’état</span><span class="sxs-lookup"><span data-stu-id="b46da-324">State Name</span></span></th>
<th><span data-ttu-id="b46da-325">Action</span><span class="sxs-lookup"><span data-stu-id="b46da-325">Action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b46da-326">D</span><span class="sxs-lookup"><span data-stu-id="b46da-326">D</span></span></td>
<td><span data-ttu-id="b46da-327">Dispatch</span><span class="sxs-lookup"><span data-stu-id="b46da-327">Dispatch</span></span></td>
<td><span data-ttu-id="b46da-328">L’appel est distribué par le runtimeGo RPC à PL</span><span class="sxs-lookup"><span data-stu-id="b46da-328">The call is dispatched by the RPC runtimeGo to PL</span></span><br/> <span data-ttu-id="b46da-329">Pour échouer irrémédiablement (lors de l’exécution sur le thread RPC) : lever l’exception ; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-329">To fail fatally (while executing on the RPC thread): Raise exception; go to End</span></span><br/> <span data-ttu-id="b46da-330">Pour échouer correctement : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-330">To fail gracefully: Go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-331">PL</span><span class="sxs-lookup"><span data-stu-id="b46da-331">PL</span></span></td>
<td><span data-ttu-id="b46da-332">Extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-332">Pull</span></span></td>
<td><span data-ttu-id="b46da-333">Créer une extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-333">Make a pull</span></span>
<ul>
<li><span data-ttu-id="b46da-334">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-334">On failure go to End</span></span></li>
<li><span data-ttu-id="b46da-335">En cas de réussite et d’achèvement synchrone avec des octets non nuls lus, accédez à PL</span><span class="sxs-lookup"><span data-stu-id="b46da-335">On success and synchronous completion with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b46da-336">En cas de réussite et d’achèvement synchrone avec zéro octet de lecture (extraction null), accédez à PS</span><span class="sxs-lookup"><span data-stu-id="b46da-336">On success and synchronous completion with zero bytes read (null pull) go to PS</span></span></li>
<li><span data-ttu-id="b46da-337">En cas de réussite et d’achèvement asynchrone (ERROR_IO_PENDING est retourné), accédez à WPL</span><span class="sxs-lookup"><span data-stu-id="b46da-337">On success and asynchronous completion (ERROR_IO_PENDING is returned) go to WPL</span></span></li>
</ul>
<span data-ttu-id="b46da-338">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-338">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-339">WPL</span><span class="sxs-lookup"><span data-stu-id="b46da-339">WPL</span></span></td>
<td><span data-ttu-id="b46da-340">Attendre l’extraction</span><span class="sxs-lookup"><span data-stu-id="b46da-340">Wait for Pull</span></span></td>
<td><span data-ttu-id="b46da-341">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-341">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-342">En cas d’échec de la saisie semi-automatique, accédez à</span><span class="sxs-lookup"><span data-stu-id="b46da-342">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b46da-343">Si une erreur <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> est reçue, accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-343">If a failure <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received go to A</span></span></li>
<li><span data-ttu-id="b46da-344">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec des octets non nuls lus, accédez à pl</span><span class="sxs-lookup"><span data-stu-id="b46da-344">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with non-zero bytes read go to PL</span></span></li>
<li><span data-ttu-id="b46da-345">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> de réussite est reçu avec zéro octet lu, accédez à PS</span><span class="sxs-lookup"><span data-stu-id="b46da-345">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcReceiveComplete</strong></a> is received with zero bytes read go to PS</span></span></li>
<li><span data-ttu-id="b46da-346">Si une défaillance est reçue, accédez à</span><span class="sxs-lookup"><span data-stu-id="b46da-346">If a failure is received go A</span></span></li>
</ul>
<span data-ttu-id="b46da-347">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-347">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-348">PS</span><span class="sxs-lookup"><span data-stu-id="b46da-348">PS</span></span></td>
<td><span data-ttu-id="b46da-349">Envoi de données (push)</span><span class="sxs-lookup"><span data-stu-id="b46da-349">Push</span></span></td>
<td><span data-ttu-id="b46da-350">Créer un push</span><span class="sxs-lookup"><span data-stu-id="b46da-350">Make a push</span></span>
<ul>
<li><span data-ttu-id="b46da-351">En cas de réussite, accédez à WPS</span><span class="sxs-lookup"><span data-stu-id="b46da-351">On success go to WPS</span></span></li>
<li><span data-ttu-id="b46da-352">En cas d’échec, aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-352">On failure go to End</span></span></li>
</ul>
<span data-ttu-id="b46da-353">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-353">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-354">WP</span><span class="sxs-lookup"><span data-stu-id="b46da-354">WPS</span></span></td>
<td><span data-ttu-id="b46da-355">Attendre la notification push</span><span class="sxs-lookup"><span data-stu-id="b46da-355">Wait for Push</span></span></td>
<td><span data-ttu-id="b46da-356">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-356">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-357">En cas d’échec de la saisie semi-automatique, accédez à</span><span class="sxs-lookup"><span data-stu-id="b46da-357">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b46da-358">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données doivent être envoyées, accédez à PS</span><span class="sxs-lookup"><span data-stu-id="b46da-358">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data needs to be sent go to PS</span></span></li>
<li><span data-ttu-id="b46da-359">Si un <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> de réussite est reçu et que davantage de données n’ont pas besoin d’être envoyées, accédez à NP</span><span class="sxs-lookup"><span data-stu-id="b46da-359">If a success <a href="/windows/desktop/api/Rpcasync/ne-rpcasync-rpc_async_event"><strong>RpcSendComplete</strong></a> is received and more data does not need to be sent go to NP</span></span></li>
<li><span data-ttu-id="b46da-360">Si une défaillance est reçue, cliquez sur COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-360">If a failure is received go Comp</span></span></li>
</ul>
<span data-ttu-id="b46da-361">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-361">To fail: go to A</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-362">NP</span><span class="sxs-lookup"><span data-stu-id="b46da-362">NP</span></span></td>
<td><span data-ttu-id="b46da-363">Push null</span><span class="sxs-lookup"><span data-stu-id="b46da-363">Null Push</span></span></td>
<td><span data-ttu-id="b46da-364">Pousser 0 octets</span><span class="sxs-lookup"><span data-stu-id="b46da-364">Push 0 bytes</span></span>
<ul>
<li><span data-ttu-id="b46da-365">en cas de réussite, accédez à WNP</span><span class="sxs-lookup"><span data-stu-id="b46da-365">on success go to WNP</span></span></li>
<li><span data-ttu-id="b46da-366">en cas d’échec, accédez à COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-366">on failure go to Comp</span></span></li>
</ul>
<span data-ttu-id="b46da-367">Pour faire échouer : accédez à un</span><span class="sxs-lookup"><span data-stu-id="b46da-367">To fail: go to A</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-368">WNP</span><span class="sxs-lookup"><span data-stu-id="b46da-368">WNP</span></span></td>
<td><span data-ttu-id="b46da-369">Attendre une notification push null</span><span class="sxs-lookup"><span data-stu-id="b46da-369">Wait for Null Push</span></span></td>
<td><span data-ttu-id="b46da-370">Attendre la notification</span><span class="sxs-lookup"><span data-stu-id="b46da-370">Wait for notification</span></span>
<ul>
<li><span data-ttu-id="b46da-371">En cas d’échec de la saisie semi-automatique, accédez à</span><span class="sxs-lookup"><span data-stu-id="b46da-371">On failure to get a completion go to A</span></span></li>
<li><span data-ttu-id="b46da-372">Si une défaillance est reçue, cliquez sur COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-372">If a failure is received go Comp</span></span></li>
<li><span data-ttu-id="b46da-373">Si une réussite est reçue, Go COMP</span><span class="sxs-lookup"><span data-stu-id="b46da-373">If a success is received go Comp</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-374">Un</span><span class="sxs-lookup"><span data-stu-id="b46da-374">A</span></span></td>
<td><span data-ttu-id="b46da-375">Abandonner l’appel</span><span class="sxs-lookup"><span data-stu-id="b46da-375">Abort the Call</span></span></td>
<td><span data-ttu-id="b46da-376">Appelez <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-376">Call <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall"><strong>RpcAsyncAbortCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b46da-377">Conformes</span><span class="sxs-lookup"><span data-stu-id="b46da-377">Comp</span></span></td>
<td><span data-ttu-id="b46da-378">Completion</span><span class="sxs-lookup"><span data-stu-id="b46da-378">Completion</span></span></td>
<td><span data-ttu-id="b46da-379">Problème <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; aller à la fin</span><span class="sxs-lookup"><span data-stu-id="b46da-379">Issue <a href="/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall"><strong>RpcAsyncCompleteCall</strong></a>; go to End</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b46da-380">End</span><span class="sxs-lookup"><span data-stu-id="b46da-380">End</span></span></td>


</tr>
</tbody>
</table>



 

 

 





