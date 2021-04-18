---
description: Les applications peuvent rencontrer des problèmes lorsqu’elles sont exécutées sur des systèmes multiprocesseurs en raison d’hypothèses qu’elles rendent valides uniquement sur les systèmes à un seul processeur.
ms.assetid: b20a1d2c-b795-4ed8-ac33-539a347020c8
title: Problèmes de synchronisation et de multiprocesseur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3896dc240e76f1506bac2a6a2e95f101b05beca7
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/21/2021
ms.locfileid: "106520209"
---
# <a name="synchronization-and-multiprocessor-issues"></a><span data-ttu-id="f6ad5-103">Problèmes de synchronisation et de multiprocesseur</span><span class="sxs-lookup"><span data-stu-id="f6ad5-103">Synchronization and Multiprocessor Issues</span></span>

<span data-ttu-id="f6ad5-104">Les applications peuvent rencontrer des problèmes lorsqu’elles sont exécutées sur des systèmes multiprocesseurs en raison d’hypothèses qu’elles rendent valides uniquement sur les systèmes à un seul processeur.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-104">Applications may encounter problems when run on multiprocessor systems due to assumptions they make which are valid only on single-processor systems.</span></span>

## <a name="thread-priorities"></a><span data-ttu-id="f6ad5-105">Priorités des threads</span><span class="sxs-lookup"><span data-stu-id="f6ad5-105">Thread Priorities</span></span>

<span data-ttu-id="f6ad5-106">Prenons l’exemple d’un programme avec deux threads, l’un avec une priorité plus élevée que l’autre.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-106">Consider a program with two threads, one with a higher priority than the other.</span></span> <span data-ttu-id="f6ad5-107">Sur un système à processeur unique, le thread dont la priorité est la plus élevée n’abandonne pas le contrôle au thread de priorité inférieure, car le planificateur donne la préférence aux threads de priorité plus élevée.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-107">On a single-processor system, the higher priority thread will not relinquish control to the lower priority thread because the scheduler gives preference to higher priority threads.</span></span> <span data-ttu-id="f6ad5-108">Sur un système multiprocesseur, les deux threads peuvent s’exécuter simultanément, chacun sur son propre processeur.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-108">On a multiprocessor system, both threads can run simultaneously, each on its own processor.</span></span>

<span data-ttu-id="f6ad5-109">Les applications doivent synchroniser l’accès aux structures de données pour éviter les conditions de concurrence.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-109">Applications should synchronize access to data structures to avoid race conditions.</span></span> <span data-ttu-id="f6ad5-110">Le code qui suppose que les threads de priorité plus élevée sont exécutés sans interférence de threads de priorité inférieure échouera sur les systèmes multiprocesseurs.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-110">Code that assumes that higher priority threads run without interference from lower priority threads will fail on multiprocessor systems.</span></span>

## <a name="memory-ordering"></a><span data-ttu-id="f6ad5-111">Ordonnancement de mémoire</span><span class="sxs-lookup"><span data-stu-id="f6ad5-111">Memory Ordering</span></span>

<span data-ttu-id="f6ad5-112">Lorsqu’un processeur écrit dans un emplacement de mémoire, la valeur est mise en cache pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-112">When a processor writes to a memory location, the value is cached to improve performance.</span></span> <span data-ttu-id="f6ad5-113">De même, le processeur tente de répondre aux demandes de lecture à partir du cache pour améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-113">Similarly, the processor attempts to satisfy read requests from the cache to improve performance.</span></span> <span data-ttu-id="f6ad5-114">En outre, les processeurs commencent à extraire les valeurs de la mémoire avant d’être demandées par l’application.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-114">Furthermore, processors begin to fetch values from memory before they are requested by the application.</span></span> <span data-ttu-id="f6ad5-115">Cela peut se produire dans le cadre d’une exécution spéculative ou en raison de problèmes de ligne de cache.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-115">This can happen as part of speculative execution or due to cache line issues.</span></span>

<span data-ttu-id="f6ad5-116">Les caches de l’UC peuvent être partitionnés en banques accessibles en parallèle.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-116">CPU caches can be partitioned into banks that can be accessed in parallel.</span></span> <span data-ttu-id="f6ad5-117">Cela signifie que les opérations de mémoire peuvent être effectuées dans le désordre.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-117">This means that memory operations can be completed out of order.</span></span> <span data-ttu-id="f6ad5-118">Pour garantir que les opérations de mémoire sont effectuées dans l’ordre, la plupart des processeurs fournissent des instructions de barrière de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-118">To ensure that memory operations are completed in order, most processors provide memory-barrier instructions.</span></span> <span data-ttu-id="f6ad5-119">Une *barrière de mémoire complète* garantit que les opérations de lecture et d’écriture de la mémoire qui s’affichent avant l’instruction de barrière de mémoire sont validées dans la mémoire avant toute opération de lecture et d’écriture de mémoire qui s’affiche après l’instruction de barrière de mémoire.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-119">A *full memory barrier* ensures that memory read and write operations that appear before the memory barrier instruction are committed to memory before any memory read and write operations that appear after the memory barrier instruction.</span></span> <span data-ttu-id="f6ad5-120">Une *barrière de lecture* de la mémoire ordonne uniquement les opérations de lecture de la mémoire et une *barrière d’écriture* de la mémoire ne commande que les opérations d’écriture de la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-120">A *read memory barrier* orders only the memory read operations and a *write memory barrier* orders only the memory write operations.</span></span> <span data-ttu-id="f6ad5-121">Ces instructions garantissent également que le compilateur désactive toutes les optimisations qui pourraient réorganiser les opérations de mémoire sur les barrières.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-121">These instructions also ensure that the compiler disables any optimizations that could reorder memory operations across the barriers.</span></span>

<span data-ttu-id="f6ad5-122">Les processeurs peuvent prendre en charge des instructions pour les barrières de mémoire avec les sémantiques Acquire, Release et CLOTURE.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-122">Processors can support instructions for memory barriers with acquire, release, and fence semantics.</span></span> <span data-ttu-id="f6ad5-123">Ces sémantiques décrivent l’ordre dans lequel les résultats d’une opération sont disponibles.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-123">These semantics describe the order in which results of an operation become available.</span></span> <span data-ttu-id="f6ad5-124">Avec la sémantique Acquire, les résultats de l’opération sont disponibles avant les résultats de toute opération qui s’affiche après dans le code.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-124">With acquire semantics, the results of the operation are available before the results of any operation that appears after it in code.</span></span> <span data-ttu-id="f6ad5-125">Avec la sémantique de version, les résultats de l’opération sont disponibles après les résultats de toute opération qui s’affiche avant dans le code.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-125">With release semantics, the results of the operation are available after the results of any operation that appears before it in code.</span></span> <span data-ttu-id="f6ad5-126">Les sémantiques de clôture combinent les sémantiques Acquire et Release.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-126">Fence semantics combine acquire and release semantics.</span></span> <span data-ttu-id="f6ad5-127">Les résultats d’une opération avec la sémantique de clôture sont disponibles avant ceux de toute opération qui s’affiche après dans le code et après ceux de toute opération qui s’affiche avant.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-127">The results of an operation with fence semantics are available before those of any operation that appears after it in code and after those of any operation that appears before it.</span></span>

<span data-ttu-id="f6ad5-128">Sur les processeurs x86 et x64 qui prennent en charge SSE2, les instructions sont **mfence** (barrière de mémoire), **lfence** (barrière de charge) et **sfence** (clôture de magasin).</span><span class="sxs-lookup"><span data-stu-id="f6ad5-128">On x86 and x64 processors that support SSE2, the instructions are **mfence** (memory fence), **lfence** (load fence), and **sfence** (store fence).</span></span> <span data-ttu-id="f6ad5-129">Sur les processeurs ARM, les injambess sont **DMB** et **ORD**.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-129">On ARM processors, the instrutions are **dmb** and **dsb**.</span></span> <span data-ttu-id="f6ad5-130">Pour plus d’informations, consultez la documentation du processeur.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-130">For more information, see the documentation for the processor.</span></span>

<span data-ttu-id="f6ad5-131">Les fonctions de synchronisation suivantes utilisent les barrières appropriées pour garantir l’ordonnancement de mémoire :</span><span class="sxs-lookup"><span data-stu-id="f6ad5-131">The following synchronization functions use the appropriate barriers to ensure memory ordering:</span></span>

-   <span data-ttu-id="f6ad5-132">Fonctions qui entrent ou laissent des sections critiques</span><span class="sxs-lookup"><span data-stu-id="f6ad5-132">Functions that enter or leave critical sections</span></span>
-   <span data-ttu-id="f6ad5-133">Fonctions qui acquièrent ou libèrent des verrous SRW</span><span class="sxs-lookup"><span data-stu-id="f6ad5-133">Functions that acquire or release SRW locks</span></span>
-   <span data-ttu-id="f6ad5-134">Début et fin de l’initialisation unique</span><span class="sxs-lookup"><span data-stu-id="f6ad5-134">One-time initialization begin and completion</span></span>
-   <span data-ttu-id="f6ad5-135">**EnterSynchronizationBarrier** fonction)</span><span class="sxs-lookup"><span data-stu-id="f6ad5-135">**EnterSynchronizationBarrier** function</span></span>
-   <span data-ttu-id="f6ad5-136">Fonctions qui signalent des objets de synchronisation</span><span class="sxs-lookup"><span data-stu-id="f6ad5-136">Functions that signal synchronization objects</span></span>
-   <span data-ttu-id="f6ad5-137">Fonctions Wait</span><span class="sxs-lookup"><span data-stu-id="f6ad5-137">Wait functions</span></span>
-   <span data-ttu-id="f6ad5-138">Fonctions verrouillées (à l’exception des fonctions avec un suffixe _nolimite_ ou des intrinsèques avec le suffixe _\_ NF_ )</span><span class="sxs-lookup"><span data-stu-id="f6ad5-138">Interlocked functions (except functions with _NoFence_ suffix, or intrinsics with _\_nf_ suffix)</span></span>

## <a name="fixing-a-race-condition"></a><span data-ttu-id="f6ad5-139">Correction d’une condition de concurrence critique</span><span class="sxs-lookup"><span data-stu-id="f6ad5-139">Fixing a Race Condition</span></span>

<span data-ttu-id="f6ad5-140">Le code suivant présente une condition de concurrence sur les systèmes multiprocesseurs, car le processeur qui s’exécute `CacheComputedValue` pour la première fois peut écrire `fValueHasBeenComputed` dans la mémoire principale avant `iValue` d’écrire dans la mémoire principale.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-140">The following code has a race condition on a multiprocessor systems because the processor that executes `CacheComputedValue` the first time may write `fValueHasBeenComputed` to main memory before writing `iValue` to main memory.</span></span> <span data-ttu-id="f6ad5-141">Par conséquent, un deuxième processeur `FetchComputedValue` s’exécutant en même temps lit la valeur `fValueHasBeenComputed` **true**, mais la nouvelle valeur de `iValue` est toujours dans le cache du premier processeur et n’a pas été écrite dans la mémoire.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-141">Consequently, a second processor executing `FetchComputedValue` at the same time reads `fValueHasBeenComputed` as **TRUE**, but the new value of `iValue` is still in the first processor's cache and has not been written to memory.</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="f6ad5-142">Cette condition de concurrence peut être réparée à l’aide du mot clé **volatile** ou de la fonction [**interlockedexchang**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) pour garantir que la valeur de `iValue` est mise à jour pour tous les processeurs avant que la valeur de `fValueHasBeenComputed` soit définie sur **true**.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-142">This race condition above can be repaired by using the **volatile** keyword or the [**InterlockedExchange**](/windows/desktop/api/winnt/nf-winnt-interlockedexchange.md) function to ensure that the value of `iValue` is updated for all processors before the value of `fValueHasBeenComputed` is set to **TRUE**.</span></span>

<span data-ttu-id="f6ad5-143">À partir de Visual Studio 2005, s’il est compilé en mode **/volatile : ms** , le compilateur utilise la sémantique Acquire pour les opérations de lecture sur les variables **volatiles** et la sémantique de libération pour les opérations d’écriture sur les variables **volatiles** (lorsqu’elles sont prises en charge par l’UC).</span><span class="sxs-lookup"><span data-stu-id="f6ad5-143">Starting Visual Studio 2005, if compiled in **/volatile:ms** mode, the compiler uses acquire semantics for read operations on **volatile** variables and release semantics for write operations on **volatile** variables (when supported by the CPU).</span></span> <span data-ttu-id="f6ad5-144">Par conséquent, vous pouvez corriger l’exemple comme suit :</span><span class="sxs-lookup"><span data-stu-id="f6ad5-144">Therefore, you can correct the example as follows:</span></span>

``` syntax
volatile int iValue;
volatile BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (!fValueHasBeenComputed) 
  {
    iValue = ComputeValue();
    fValueHasBeenComputed = TRUE;
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (fValueHasBeenComputed) 
  {
    *piResult = iValue;
    return TRUE;
  } 

  else return FALSE;
}
```

<span data-ttu-id="f6ad5-145">Avec Visual Studio 2003, les références **volatiles** à **volatiles** sont triées ; le compilateur ne réorganise pas l’accès aux variables **volatiles** .</span><span class="sxs-lookup"><span data-stu-id="f6ad5-145">With Visual Studio 2003, **volatile** to **volatile** references are ordered; the compiler will not re-order **volatile** variable access.</span></span> <span data-ttu-id="f6ad5-146">Toutefois, ces opérations peuvent être réorganisées par le processeur.</span><span class="sxs-lookup"><span data-stu-id="f6ad5-146">However, these operations could be re-ordered by the processor.</span></span> <span data-ttu-id="f6ad5-147">Par conséquent, vous pouvez corriger l’exemple comme suit :</span><span class="sxs-lookup"><span data-stu-id="f6ad5-147">Therefore, you can correct the example as follows:</span></span>

``` syntax
int iValue;
BOOL fValueHasBeenComputed = FALSE;
extern int ComputeValue();

void CacheComputedValue()
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          FALSE, FALSE)==FALSE) 
  {
    InterlockedExchange ((LONG*)&iValue, (LONG)ComputeValue());
    InterlockedExchange ((LONG*)&fValueHasBeenComputed, TRUE);
  }
}
 
BOOL FetchComputedValue(int *piResult)
{
  if (InterlockedCompareExchange((LONG*)&fValueHasBeenComputed, 
          TRUE, TRUE)==TRUE) 
  {
    InterlockedExchange((LONG*)piResult, (LONG)iValue);
    return TRUE;
  } 

  else return FALSE;
}
```

## <a name="related-topics"></a><span data-ttu-id="f6ad5-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f6ad5-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6ad5-149">Objets de section critique</span><span class="sxs-lookup"><span data-stu-id="f6ad5-149">Critical Section Objects</span></span>](critical-section-objects.md)
</dt> <dt>

[<span data-ttu-id="f6ad5-150">Accès aux variables verrouillées</span><span class="sxs-lookup"><span data-stu-id="f6ad5-150">Interlocked Variable Access</span></span>](interlocked-variable-access.md)
</dt> <dt>

[<span data-ttu-id="f6ad5-151">Fonctions Wait</span><span class="sxs-lookup"><span data-stu-id="f6ad5-151">Wait Functions</span></span>](wait-functions.md)
</dt> </dl>

 

 



