---
description: Windows comprend les nouveaux éléments de programmation suivants pour la synchronisation.
ms.assetid: 16cd98d2-adc5-4a14-ad39-a0c5b4cc00cc
title: Nouveautés de la synchronisation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4702ba10126d9c0eeeb85462195680b074918584
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203025"
---
# <a name="whats-new-in-synchronization"></a><span data-ttu-id="fe698-103">Nouveautés de la synchronisation</span><span class="sxs-lookup"><span data-stu-id="fe698-103">What's New in Synchronization</span></span>

<span data-ttu-id="fe698-104">Windows comprend les nouveaux éléments de programmation suivants pour la synchronisation.</span><span class="sxs-lookup"><span data-stu-id="fe698-104">Windows includes the following new programming elements for synchronization.</span></span>

## <a name="windows-8"></a><span data-ttu-id="fe698-105">Windows 8</span><span class="sxs-lookup"><span data-stu-id="fe698-105">Windows 8</span></span>

### <a name="new-functions"></a><span data-ttu-id="fe698-106">Nouvelles fonctions</span><span class="sxs-lookup"><span data-stu-id="fe698-106">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="fe698-107">**DeleteSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="fe698-107">**DeleteSynchronizationBarrier**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-deletesynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="fe698-108">Supprime une barrière de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="fe698-108">Deletes a synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-109">**EnterSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="fe698-109">**EnterSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="fe698-110">Fait en sorte que le thread appelant attende une barrière de synchronisation jusqu’à ce que le nombre maximal de threads soit entré dans le cloisonnement.</span><span class="sxs-lookup"><span data-stu-id="fe698-110">Causes the calling thread to wait at a synchronization barrier until the maximum number of threads have entered the barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-111">**GetOverlappedResultEx**</span><span class="sxs-lookup"><span data-stu-id="fe698-111">**GetOverlappedResultEx**</span></span>](/windows/desktop/api/Ioapiset/nf-ioapiset-getoverlappedresultex)
</dt> <dd>

<span data-ttu-id="fe698-112">Récupère les résultats d’une opération avec chevauchement sur le fichier spécifié, le canal nommé ou l’appareil de communication dans l’intervalle de délai d’attente spécifié.</span><span class="sxs-lookup"><span data-stu-id="fe698-112">Retrieves the results of an overlapped operation on the specified file, named pipe, or communications device within the specified time-out interval.</span></span> <span data-ttu-id="fe698-113">Le thread appelant peut effectuer une attente signalable.</span><span class="sxs-lookup"><span data-stu-id="fe698-113">The calling thread can perform an alertable wait.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-114">**InitializeSynchronizationBarrier**</span><span class="sxs-lookup"><span data-stu-id="fe698-114">**InitializeSynchronizationBarrier**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-entersynchronizationbarrier)
</dt> <dd>

<span data-ttu-id="fe698-115">Spécifie le nombre maximal de threads et le nombre de spins pour une nouvelle barrière de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="fe698-115">Specifies the maximum number of threads and spin count for a new synchronization barrier.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-116">**WaitOnAddress**</span><span class="sxs-lookup"><span data-stu-id="fe698-116">**WaitOnAddress**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-waitonaddress)
</dt> <dd>

<span data-ttu-id="fe698-117">Attend la modification de la valeur à l’adresse spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fe698-117">Waits for the value at the specified address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-118">**WakeByAddressAll**</span><span class="sxs-lookup"><span data-stu-id="fe698-118">**WakeByAddressAll**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddressall)
</dt> <dd>

<span data-ttu-id="fe698-119">Sort tous les threads en attente de la modification de la valeur d’une adresse.</span><span class="sxs-lookup"><span data-stu-id="fe698-119">Wakes all threads that are waiting for the value of an address to change.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-120">**WakeByAddressSingle**</span><span class="sxs-lookup"><span data-stu-id="fe698-120">**WakeByAddressSingle**</span></span>](/windows/desktop/api/SynchAPI/nf-synchapi-wakebyaddresssingle)
</dt> <dd>

<span data-ttu-id="fe698-121">Sort un thread en attente de la modification de la valeur d’une adresse.</span><span class="sxs-lookup"><span data-stu-id="fe698-121">Wakes one thread that is waiting for the value of an address to change.</span></span>

</dd> </dl>

### <a name="new-interlocked-functions"></a><span data-ttu-id="fe698-122">Nouvelles fonctions verrouillées</span><span class="sxs-lookup"><span data-stu-id="fe698-122">New Interlocked Functions</span></span>

<dl> <dt>

<span data-ttu-id="fe698-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-123">[**InterlockedAddNoFence**](/previous-versions/windows/desktop/legacy/hh972629(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-124">Effectue une opération d’addition atomique sur les valeurs **longues** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-124">Performs an atomic addition operation on the specified **LONG** values.</span></span> <span data-ttu-id="fe698-125">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-125">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-126">[**InterlockedAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972630(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-127">Effectue une opération d’addition atomique sur les valeurs **LongLong** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-127">Performs an atomic addition operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="fe698-128">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-128">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-129">[**InterlockedAndNoFence**](/previous-versions/windows/desktop/legacy/hh972634(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-130">Effectue une opération atomique et sur les valeurs **longues** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-130">Performs an atomic AND operation on the specified **LONG** values.</span></span> <span data-ttu-id="fe698-131">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-131">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-132">[**InterlockedAnd8NoFence**](/previous-versions/windows/desktop/legacy/hh972633(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-133">Effectue une opération atomique et sur les valeurs **char** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-133">Performs an atomic AND operation on the specified **char** values.</span></span> <span data-ttu-id="fe698-134">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-134">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-135">[**InterlockedAnd16NoFence**](/previous-versions/windows/desktop/legacy/hh972631(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-136">Effectue une opération atomique et sur les valeurs **courtes** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-136">Performs an atomic AND operation on the specified **SHORT** values.</span></span> <span data-ttu-id="fe698-137">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-137">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-138">[**InterlockedAnd64NoFence**](/previous-versions/windows/desktop/legacy/hh972632(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-139">Effectue une opération atomique et sur les valeurs **LongLong** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-139">Performs an atomic AND operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="fe698-140">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-140">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-141">[**InterlockedBitTestAndComplement64**](/previous-versions/windows/desktop/legacy/hh972635(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-142">Teste le bit spécifié de la valeur **LONG64** spécifiée et le complète.</span><span class="sxs-lookup"><span data-stu-id="fe698-142">Tests the specified bit of the specified **LONG64** value and complements it.</span></span> <span data-ttu-id="fe698-143">L'opération est atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-143">The operation is atomic.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-144">[**InterlockedBitTestAndResetAcquire**](/previous-versions/windows/desktop/legacy/hh972636(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-145">Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="fe698-145">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="fe698-146">L’opération est atomique et est effectuée avec la sémantique d’acquisition de mémoire acquise.</span><span class="sxs-lookup"><span data-stu-id="fe698-146">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-147">[**InterlockedBitTestAndResetRelease**](/previous-versions/windows/desktop/legacy/hh972637(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-148">Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="fe698-148">Tests the specified bit of the specified **LONG** value and sets it to 0.</span></span> <span data-ttu-id="fe698-149">L’opération est atomique et est effectuée à l’aide de la sémantique de libération de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-149">The operation is atomic, and it is performed using memory release semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-150">[**InterlockedBitTestAndSetAcquire**](/previous-versions/windows/desktop/legacy/hh972638(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-151">Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="fe698-151">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="fe698-152">L’opération est atomique et est effectuée avec la sémantique d’acquisition de mémoire acquise.</span><span class="sxs-lookup"><span data-stu-id="fe698-152">The operation is atomic, and it is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-153">[**InterlockedBitTestAndSetRelease**](/previous-versions/windows/desktop/legacy/hh972639(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-154">Teste le bit spécifié de la valeur **longue** spécifiée et lui affecte la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="fe698-154">Tests the specified bit of the specified **LONG** value and sets it to 1.</span></span> <span data-ttu-id="fe698-155">L’opération est atomique et est effectuée avec la sémantique d’ordonnancement de mémoire de version.</span><span class="sxs-lookup"><span data-stu-id="fe698-155">The operation is atomic, and it is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-156">[**InterlockedCompareExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972645(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-157">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-157">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-158">La fonction compare deux valeurs 32 bits spécifiées et échange avec une autre valeur 32 bits en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-158">The function compares two specified 32-bit values and exchanges with another 32-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="fe698-159">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-159">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-160">**InterlockedCompareExchange16**</span><span class="sxs-lookup"><span data-stu-id="fe698-160">**InterlockedCompareExchange16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange16)
</dt> <dd>

<span data-ttu-id="fe698-161">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-161">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-162">La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-162">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-163">[**InterlockedCompareExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972642(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-164">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-164">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-165">La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-165">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="fe698-166">L’opération est effectuée avec la sémantique d’acquisition de mémoire acquise.</span><span class="sxs-lookup"><span data-stu-id="fe698-166">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-167">[**InterlockedCompareExchange16Release**](/previous-versions/windows/desktop/legacy/hh972644(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-168">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-168">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-169">La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-169">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="fe698-170">L’échange est effectué avec la sémantique d’ordonnancement de mémoire de version.</span><span class="sxs-lookup"><span data-stu-id="fe698-170">The exchange is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-171">[**InterlockedCompareExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972643(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-172">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-172">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-173">La fonction compare deux valeurs 16 bits spécifiées et échange avec une autre valeur de 16 bits en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-173">The function compares two specified 16-bit values and exchanges with another 16-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="fe698-174">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-174">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-175">[**InterlockedCompareExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972646(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-176">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-176">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-177">La fonction compare deux valeurs 64 bits spécifiées et échange avec une autre valeur 64 bits en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-177">The function compares two specified 64-bit values and exchanges with another 64-bit value based on the outcome of the comparison.</span></span> <span data-ttu-id="fe698-178">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-178">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-179">**InterlockedCompareExchange128**</span><span class="sxs-lookup"><span data-stu-id="fe698-179">**InterlockedCompareExchange128**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedcompareexchange128)
</dt> <dd>

<span data-ttu-id="fe698-180">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-180">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-181">La fonction compare deux valeurs 128 bits spécifiées et échange avec une autre valeur 128 bits en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-181">The function compares two specified 128-bit values and exchanges with another 128-bit value based on the outcome of the comparison.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-182">[**InterlockedCompareExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972647(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-183">Effectue une opération atomique de comparaison et d’échange sur les valeurs spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-183">Performs an atomic compare-and-exchange operation on the specified values.</span></span> <span data-ttu-id="fe698-184">La fonction compare deux valeurs de pointeur spécifiées et échange avec une autre valeur de pointeur en fonction du résultat de la comparaison.</span><span class="sxs-lookup"><span data-stu-id="fe698-184">The function compares two specified pointer values and exchanges with another pointer value based on the outcome of the comparison.</span></span> <span data-ttu-id="fe698-185">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-185">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-186">[**InterlockedDecrementNoFence**](/previous-versions/windows/desktop/legacy/hh972652(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-187">Décrémente (réduit d’une unité) la valeur de la variable 32 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-187">Decrements (decreases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-188">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-188">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-189">**InterlockedDecrement16**</span><span class="sxs-lookup"><span data-stu-id="fe698-189">**InterlockedDecrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockeddecrement16)
</dt> <dd>

<span data-ttu-id="fe698-190">Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-190">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-191">[**InterlockedDecrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972649(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-192">Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-192">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-193">L’opération est effectuée avec la sémantique d’acquisition de mémoire acquise.</span><span class="sxs-lookup"><span data-stu-id="fe698-193">The operation is performed with acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-194">[**InterlockedDecrement16Release**](/previous-versions/windows/desktop/legacy/hh972651(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-195">Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-195">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-196">L’opération est effectuée avec la sémantique d’ordonnancement de mémoire de version.</span><span class="sxs-lookup"><span data-stu-id="fe698-196">The operation is performed with release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-197">[**InterlockedDecrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972650(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-198">Décrémente (réduit d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-198">Decrements (decreases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-199">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-199">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-200">[**InterlockedDecrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972653(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-201">Décrémente (réduit d’une unité) la valeur de la variable 64 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-201">Decrements (decreases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-202">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-202">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-203">[**InterlockedExchangeNoFence**](/previous-versions/windows/desktop/legacy/hh972659(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-204">Affecte à une variable 64 bits la valeur spécifiée sous la forme d’une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-204">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="fe698-205">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-205">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-206">**InterlockedExchange8**</span><span class="sxs-lookup"><span data-stu-id="fe698-206">**InterlockedExchange8**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedexchange8)
</dt> <dd>

<span data-ttu-id="fe698-207">Définit une variable 8 bits à la valeur spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-207">Sets an 8-bit variable to the specified value as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-208">[**InterlockedExchange16Acquire**](/previous-versions/windows/desktop/legacy/hh972654(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-209">Définit une variable de 16 bits à la valeur spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-209">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="fe698-210">L’opération est effectuée à l’aide d’une sémantique d’ordonnancement de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-210">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-211">[**InterlockedExchange16NoFence**](/previous-versions/windows/desktop/legacy/hh972655(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-212">Définit une variable de 16 bits à la valeur spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-212">Sets a 16-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="fe698-213">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-213">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-214">[**InterlockedExchangeNoFence64**](/previous-versions/windows/desktop/legacy/hh972660(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-215">Affecte à une variable 64 bits la valeur spécifiée sous la forme d’une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-215">Sets a 64-bit variable to the specified value as an atomic operation.</span></span> <span data-ttu-id="fe698-216">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-216">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-217">[**InterlockedExchangePointerNoFence**](/previous-versions/windows/desktop/legacy/hh972661(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-218">Échange atomiquement une paire d’adresses.</span><span class="sxs-lookup"><span data-stu-id="fe698-218">Atomically exchanges a pair of addresses.</span></span> <span data-ttu-id="fe698-219">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-219">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-220">[**InterlockedExchangeAddNoFence**](/previous-versions/windows/desktop/legacy/hh972657(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-221">Effectue un ajout atomique de valeurs 2 32 bits.</span><span class="sxs-lookup"><span data-stu-id="fe698-221">Performs an atomic addition of two 32-bit values.</span></span> <span data-ttu-id="fe698-222">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-222">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-223">[**InterlockedExchangeAddNoFence64**](/previous-versions/windows/desktop/legacy/hh972658(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-224">Effectue un ajout atomique de valeurs 2 64 bits.</span><span class="sxs-lookup"><span data-stu-id="fe698-224">Performs an atomic addition of two 64-bit values.</span></span> <span data-ttu-id="fe698-225">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-225">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-226">[**InterlockedIncrementNoFence**](/previous-versions/windows/desktop/legacy/hh972667(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-227">Incrémente (augmente d’une unité) la valeur de la variable 32 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-227">Increments (increases by one) the value of the specified 32-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-228">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-228">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-229">**InterlockedIncrement16**</span><span class="sxs-lookup"><span data-stu-id="fe698-229">**InterlockedIncrement16**</span></span>](/windows/desktop/api/Winnt/nf-winnt-interlockedincrement16)
</dt> <dd>

<span data-ttu-id="fe698-230">Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-230">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-231">[**InterlockedIncrement16Acquire**](/previous-versions/windows/desktop/legacy/hh972663(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-232">Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-232">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-233">L’opération est effectuée à l’aide d’une sémantique d’ordonnancement de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-233">The operation is performed using acquire memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-234">[**InterlockedIncrement16Release**](/previous-versions/windows/desktop/legacy/hh972665(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-235">Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-235">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-236">L’opération est effectuée à l’aide de la sémantique d’ordonnancement de mémoire Release.</span><span class="sxs-lookup"><span data-stu-id="fe698-236">The operation is performed using release memory ordering semantics.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-237">[**InterlockedIncrement16NoFence**](/previous-versions/windows/desktop/legacy/hh972664(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-238">Incrémente (augmente d’une unité) la valeur de la variable 16 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-238">Increments (increases by one) the value of the specified 16-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-239">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-239">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-240">[**InterlockedIncrementNoFence64**](/previous-versions/windows/desktop/legacy/hh972668(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-241">Incrémente (augmente d’une unité) la valeur de la variable 64 bits spécifiée comme une opération atomique.</span><span class="sxs-lookup"><span data-stu-id="fe698-241">Increments (increases by one) the value of the specified 64-bit variable as an atomic operation.</span></span> <span data-ttu-id="fe698-242">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-242">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-243">[**InterlockedOrNoFence**](/previous-versions/windows/desktop/legacy/hh972672(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-244">Effectue une opération atomique ou sur les valeurs **longues** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-244">Performs an atomic OR operation on the specified **LONG** values.</span></span> <span data-ttu-id="fe698-245">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-245">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-246">[**InterlockedOr8NoFence**](/previous-versions/windows/desktop/legacy/hh972671(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-247">Effectue une opération atomique ou sur les valeurs **char** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-247">Performs an atomic OR operation on the specified **char** values.</span></span> <span data-ttu-id="fe698-248">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-248">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-249">[**InterlockedOr16NoFence**](/previous-versions/windows/desktop/legacy/hh972669(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-250">Effectue une opération atomique ou sur les valeurs **courtes** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-250">Performs an atomic OR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="fe698-251">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-251">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-252">[**InterlockedOr64NoFence**](/previous-versions/windows/desktop/legacy/hh972670(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-253">Effectue une opération atomique ou sur les valeurs **LongLong** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-253">Performs an atomic OR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="fe698-254">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-254">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-255">**InterlockedPushListSListEx**</span><span class="sxs-lookup"><span data-stu-id="fe698-255">**InterlockedPushListSListEx**</span></span>](/windows/desktop/api/interlockedapi/nf-interlockedapi-interlockedpushlistslistex)
</dt> <dd>

<span data-ttu-id="fe698-256">Insère une liste à liaison unique à l’avant d’une autre liste à liaison unique.</span><span class="sxs-lookup"><span data-stu-id="fe698-256">Inserts a singly-linked list at the front of another singly linked list.</span></span> <span data-ttu-id="fe698-257">L’accès aux listes est synchronisé sur un système multiprocesseur.</span><span class="sxs-lookup"><span data-stu-id="fe698-257">Access to the lists is synchronized on a multiprocessor system.</span></span> <span data-ttu-id="fe698-258">Cette version de la méthode n’utilise pas la Convention d’appel [ \_ \_ fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) .</span><span class="sxs-lookup"><span data-stu-id="fe698-258">This version of the method does not use the [\_\_fastcall](https://msdn.microsoft.com/library/6xa169sk(v=VS.71).aspx) calling convention.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-259">[**InterlockedXorNoFence**](/previous-versions/windows/desktop/legacy/hh972677(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-260">Effectue une opération atomique XOR sur les valeurs **longues** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-260">Performs an atomic XOR operation on the specified **LONG** values.</span></span> <span data-ttu-id="fe698-261">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-261">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-262">[**InterlockedXor8NoFence**](/previous-versions/windows/desktop/legacy/hh972676(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-263">Effectue une opération Atomic XOR sur les valeurs **char** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-263">Performs an atomic XOR operation on the specified **char** values.</span></span> <span data-ttu-id="fe698-264">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-264">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-265">[**InterlockedXor16NoFence**](/previous-versions/windows/desktop/legacy/hh972674(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-266">Effectue une opération atomique XOR sur les valeurs **courtes** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-266">Performs an atomic XOR operation on the specified **SHORT** values.</span></span> <span data-ttu-id="fe698-267">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-267">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> <dt>

<span data-ttu-id="fe698-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="fe698-268">[**InterlockedXor64NoFence**](/previous-versions/windows/desktop/legacy/hh972675(v=vs.85))</span></span>
</dt> <dd>

<span data-ttu-id="fe698-269">Effectue une opération Atomic XOR sur les valeurs **LongLong** spécifiées.</span><span class="sxs-lookup"><span data-stu-id="fe698-269">Performs an atomic XOR operation on the specified **LONGLONG** values.</span></span> <span data-ttu-id="fe698-270">L’opération est effectuée atomiquement, mais sans utiliser de barrières de mémoire.</span><span class="sxs-lookup"><span data-stu-id="fe698-270">The operation is performed atomically, but without using memory barriers.</span></span>

</dd> </dl>

## <a name="windows-7"></a><span data-ttu-id="fe698-271">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fe698-271">Windows 7</span></span>

### <a name="new-functions"></a><span data-ttu-id="fe698-272">Nouvelles fonctions</span><span class="sxs-lookup"><span data-stu-id="fe698-272">New Functions</span></span>

<dl> <dt>

[<span data-ttu-id="fe698-273">**SetWaitableTimerEx**</span><span class="sxs-lookup"><span data-stu-id="fe698-273">**SetWaitableTimerEx**</span></span>](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex)
</dt> <dd>

<span data-ttu-id="fe698-274">Active le minuteur attendu spécifié et fournit des informations de contexte pour le minuteur.</span><span class="sxs-lookup"><span data-stu-id="fe698-274">Activates the specified waitable timer and provides context information for the timer.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-275">**TryAcquireSRWLockExclusive**</span><span class="sxs-lookup"><span data-stu-id="fe698-275">**TryAcquireSRWLockExclusive**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockexclusive)
</dt> <dd>

<span data-ttu-id="fe698-276">Tente d’acquérir un verrou SRW (Slim Reader/Writer) en mode exclusif.</span><span class="sxs-lookup"><span data-stu-id="fe698-276">Attempts to acquire a slim reader/writer (SRW) lock in exclusive mode.</span></span> <span data-ttu-id="fe698-277">Si l’appel réussit, le thread appelant prend la propriété du verrou.</span><span class="sxs-lookup"><span data-stu-id="fe698-277">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> <dt>

[<span data-ttu-id="fe698-278">**TryAcquireSRWLockShared**</span><span class="sxs-lookup"><span data-stu-id="fe698-278">**TryAcquireSRWLockShared**</span></span>](/windows/win32/api/synchapi/nf-synchapi-tryacquiresrwlockshared)
</dt> <dd>

<span data-ttu-id="fe698-279">Tente d’acquérir un verrou SRW (Slim Reader/Writer) en mode partagé.</span><span class="sxs-lookup"><span data-stu-id="fe698-279">Attempts to acquire a slim reader/writer (SRW) lock in shared mode.</span></span> <span data-ttu-id="fe698-280">Si l’appel réussit, le thread appelant prend la propriété du verrou.</span><span class="sxs-lookup"><span data-stu-id="fe698-280">If the call is successful, the calling thread takes ownership of the lock.</span></span>

</dd> </dl>

### <a name="new-structures"></a><span data-ttu-id="fe698-281">Nouvelles structures</span><span class="sxs-lookup"><span data-stu-id="fe698-281">New Structures</span></span>

<dl> <dt>

[<span data-ttu-id="fe698-282">**contexte de la raison \_**</span><span class="sxs-lookup"><span data-stu-id="fe698-282">**REASON\_CONTEXT**</span></span>](/windows/win32/api/minwinbase/ns-minwinbase-reason_context)
</dt> <dd>

<span data-ttu-id="fe698-283">Contient les informations de contexte pour une minuterie activée avec [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span><span class="sxs-lookup"><span data-stu-id="fe698-283">Contains context information for a timer activated with [**SetWaitableTimerEx**](/windows/win32/api/synchapi/nf-synchapi-setwaitabletimerex).</span></span>

</dd> </dl>

 

 
