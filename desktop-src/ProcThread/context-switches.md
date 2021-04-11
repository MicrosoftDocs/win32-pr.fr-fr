---
description: Le planificateur gère une file d’attente de threads exécutables pour chaque niveau de priorité.
ms.assetid: 82463d71-9cef-4608-b997-25dc9c1e1c0a
title: Commutateurs de contexte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7628ee9e659cdbc2369b5f69d25847e8864dbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202857"
---
# <a name="context-switches"></a><span data-ttu-id="2ef67-103">Commutateurs de contexte</span><span class="sxs-lookup"><span data-stu-id="2ef67-103">Context Switches</span></span>

<span data-ttu-id="2ef67-104">Le planificateur gère une file d’attente de threads exécutables pour chaque niveau de priorité.</span><span class="sxs-lookup"><span data-stu-id="2ef67-104">The scheduler maintains a queue of executable threads for each priority level.</span></span> <span data-ttu-id="2ef67-105">Il s’agit de *Threads prêts* à l’emploi.</span><span class="sxs-lookup"><span data-stu-id="2ef67-105">These are known as *ready threads*.</span></span> <span data-ttu-id="2ef67-106">Lorsqu’un processeur devient disponible, le système effectue un *changement de contexte*.</span><span class="sxs-lookup"><span data-stu-id="2ef67-106">When a processor becomes available, the system performs a *context switch*.</span></span> <span data-ttu-id="2ef67-107">Les étapes d’un changement de contexte sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ef67-107">The steps in a context switch are:</span></span>

1.  <span data-ttu-id="2ef67-108">Enregistrez le contexte du thread dont l’exécution vient d’être terminée.</span><span class="sxs-lookup"><span data-stu-id="2ef67-108">Save the context of the thread that just finished executing.</span></span>
2.  <span data-ttu-id="2ef67-109">Placez le thread qui vient d’être exécuté à la fin de la file d’attente pour sa priorité.</span><span class="sxs-lookup"><span data-stu-id="2ef67-109">Place the thread that just finished executing at the end of the queue for its priority.</span></span>
3.  <span data-ttu-id="2ef67-110">Recherche la file d’attente dont la priorité est la plus élevée et qui contient des threads prêts.</span><span class="sxs-lookup"><span data-stu-id="2ef67-110">Find the highest priority queue that contains ready threads.</span></span>
4.  <span data-ttu-id="2ef67-111">Supprimez le thread situé à l’en-tête de la file d’attente, chargez son contexte et exécutez-le.</span><span class="sxs-lookup"><span data-stu-id="2ef67-111">Remove the thread at the head of the queue, load its context, and execute it.</span></span>

<span data-ttu-id="2ef67-112">Les classes de threads suivantes ne sont pas des threads prêts.</span><span class="sxs-lookup"><span data-stu-id="2ef67-112">The following classes of threads are not ready threads.</span></span>

-   <span data-ttu-id="2ef67-113">Threads créés avec l' \_ indicateur de création suspendu</span><span class="sxs-lookup"><span data-stu-id="2ef67-113">Threads created with the CREATE\_SUSPENDED flag</span></span>
-   <span data-ttu-id="2ef67-114">Threads interrompus pendant l’exécution avec la fonction [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) ou [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread)</span><span class="sxs-lookup"><span data-stu-id="2ef67-114">Threads halted during execution with the [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) or [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) function</span></span>
-   <span data-ttu-id="2ef67-115">Threads en attente d’un objet ou d’une entrée de synchronisation.</span><span class="sxs-lookup"><span data-stu-id="2ef67-115">Threads waiting for a synchronization object or input.</span></span>

<span data-ttu-id="2ef67-116">Tant que les threads suspendus ou bloqués ne sont pas prêts à être exécutés, le planificateur n’alloue pas de temps processeur à eux, quelle que soit leur priorité.</span><span class="sxs-lookup"><span data-stu-id="2ef67-116">Until threads that are suspended or blocked become ready to run, the scheduler does not allocate any processor time to them, regardless of their priority.</span></span>

<span data-ttu-id="2ef67-117">Les raisons les plus courantes d’un changement de contexte sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="2ef67-117">The most common reasons for a context switch are:</span></span>

-   <span data-ttu-id="2ef67-118">La tranche de temps s’est écoulée.</span><span class="sxs-lookup"><span data-stu-id="2ef67-118">The time slice has elapsed.</span></span>
-   <span data-ttu-id="2ef67-119">Un thread avec une priorité plus élevée est prêt à être exécuté.</span><span class="sxs-lookup"><span data-stu-id="2ef67-119">A thread with a higher priority has become ready to run.</span></span>
-   <span data-ttu-id="2ef67-120">Un thread en cours d’exécution doit attendre.</span><span class="sxs-lookup"><span data-stu-id="2ef67-120">A running thread needs to wait.</span></span>

<span data-ttu-id="2ef67-121">Quand un thread en cours d’exécution doit attendre, il abandonne le reste de sa tranche de temps.</span><span class="sxs-lookup"><span data-stu-id="2ef67-121">When a running thread needs to wait, it relinquishes the remainder of its time slice.</span></span>

 

 
