---
description: Les e/s alertables sont la méthode par laquelle les threads d’application traitent les demandes d’e/s asynchrones uniquement lorsqu’elles sont dans un État alerté.
ms.assetid: d996f1cc-eeab-456b-818b-5307a79effd9
title: E/s alertables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fb830dfadb97051c47b2472eb3e7a3c2d6a0bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518133"
---
# <a name="alertable-io"></a><span data-ttu-id="9712f-103">E/s alertables</span><span class="sxs-lookup"><span data-stu-id="9712f-103">Alertable I/O</span></span>

<span data-ttu-id="9712f-104">Les e/s alertables sont la méthode par laquelle les threads d’application traitent les demandes d’e/s asynchrones uniquement lorsqu’elles sont dans un État alerté.</span><span class="sxs-lookup"><span data-stu-id="9712f-104">Alertable I/O is the method by which application threads process asynchronous I/O requests only when they are in an alertable state.</span></span>

<span data-ttu-id="9712f-105">Pour comprendre quand un thread est dans un état d’alerte, envisagez le scénario suivant :</span><span class="sxs-lookup"><span data-stu-id="9712f-105">To understand when a thread is in an alertable state, consider the following scenario:</span></span>

1.  <span data-ttu-id="9712f-106">Un thread lance une requête de lecture asynchrone en appelant [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) avec un pointeur vers une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="9712f-106">A thread initiates an asynchronous read request by calling [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) with a pointer to a callback function.</span></span>
2.  <span data-ttu-id="9712f-107">Le thread lance une demande d’écriture asynchrone en appelant [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) avec un pointeur vers une fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="9712f-107">The thread initiates an asynchronous write request by calling [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) with a pointer to a callback function.</span></span>
3.  <span data-ttu-id="9712f-108">Le thread appelle une fonction qui extrait une ligne de données à partir d’un serveur de base de données distant.</span><span class="sxs-lookup"><span data-stu-id="9712f-108">The thread calls a function that fetches a row of data from a remote database server.</span></span>

<span data-ttu-id="9712f-109">Dans ce scénario, les appels à [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) seront probablement retournés avant l’appel de fonction à l’étape 3.</span><span class="sxs-lookup"><span data-stu-id="9712f-109">In this scenario, the calls to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex) will most likely return before the function call in step 3.</span></span> <span data-ttu-id="9712f-110">Dans ce cas, le noyau place les pointeurs vers les fonctions de rappel dans la file d’attente d’appels de procédure asynchrone (APC) du thread.</span><span class="sxs-lookup"><span data-stu-id="9712f-110">When they do, the kernel places the pointers to the callback functions on the thread's Asynchronous Procedure Call (APC) queue.</span></span> <span data-ttu-id="9712f-111">Le noyau gère cette file d’attente spécifiquement pour conserver les données de requête d’e/s renvoyées jusqu’à ce qu’elle puisse être traitée par le thread correspondant.</span><span class="sxs-lookup"><span data-stu-id="9712f-111">The kernel maintains this queue specifically to hold returned I/O request data until it can be processed by the corresponding thread.</span></span>

<span data-ttu-id="9712f-112">Lorsque l’extraction de lignes est terminée et que le thread retourne de la fonction, sa priorité la plus élevée consiste à traiter les demandes d’e/s renvoyées sur la file d’attente en appelant les fonctions de rappel.</span><span class="sxs-lookup"><span data-stu-id="9712f-112">When the row fetch is complete and the thread returns from the function, its highest priority is to process the returned I/O requests on the queue by calling the callback functions.</span></span> <span data-ttu-id="9712f-113">Pour ce faire, il doit entrer un état d’alerte.</span><span class="sxs-lookup"><span data-stu-id="9712f-113">To do this, it must enter an alertable state.</span></span> <span data-ttu-id="9712f-114">Un thread ne peut le faire qu’en appelant l’une des fonctions suivantes avec les indicateurs appropriés :</span><span class="sxs-lookup"><span data-stu-id="9712f-114">A thread can only do this by calling one of the following functions with the appropriate flags:</span></span>

-   [<span data-ttu-id="9712f-115">**SleepEx**</span><span class="sxs-lookup"><span data-stu-id="9712f-115">**SleepEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-sleepex)
-   [<span data-ttu-id="9712f-116">**WaitForSingleObjectEx**</span><span class="sxs-lookup"><span data-stu-id="9712f-116">**WaitForSingleObjectEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex)
-   [<span data-ttu-id="9712f-117">**WaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="9712f-117">**WaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjectsex)
-   [<span data-ttu-id="9712f-118">**SignalObjectAndWait**</span><span class="sxs-lookup"><span data-stu-id="9712f-118">**SignalObjectAndWait**</span></span>](/windows/win32/api/synchapi/nf-synchapi-signalobjectandwait)
-   [<span data-ttu-id="9712f-119">**MsgWaitForMultipleObjectsEx**</span><span class="sxs-lookup"><span data-stu-id="9712f-119">**MsgWaitForMultipleObjectsEx**</span></span>](/windows/desktop/api/winuser/nf-winuser-msgwaitformultipleobjectsex)

<span data-ttu-id="9712f-120">Lorsque le thread entre dans un état d’alerte, les événements suivants se produisent :</span><span class="sxs-lookup"><span data-stu-id="9712f-120">When the thread enters an alertable state, the following events occur:</span></span>

1.  <span data-ttu-id="9712f-121">Le noyau vérifie la file d’attente APC du thread.</span><span class="sxs-lookup"><span data-stu-id="9712f-121">The kernel checks the thread's APC queue.</span></span> <span data-ttu-id="9712f-122">Si la file d’attente contient des pointeurs de fonction de rappel, le noyau supprime le pointeur de la file d’attente et l’envoie au thread.</span><span class="sxs-lookup"><span data-stu-id="9712f-122">If the queue contains callback function pointers, the kernel removes the pointer from the queue and sends it to the thread.</span></span>
2.  <span data-ttu-id="9712f-123">Le thread exécute la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="9712f-123">The thread executes the callback function.</span></span>
3.  <span data-ttu-id="9712f-124">Les étapes 1 et 2 sont répétées pour chaque pointeur restant dans la file d’attente.</span><span class="sxs-lookup"><span data-stu-id="9712f-124">Steps 1 and 2 are repeated for each pointer remaining in the queue.</span></span>
4.  <span data-ttu-id="9712f-125">Lorsque la file d’attente est vide, le thread retourne de la fonction qui l’a placée dans un état d’alerte.</span><span class="sxs-lookup"><span data-stu-id="9712f-125">When the queue is empty, the thread returns from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="9712f-126">Dans ce scénario, une fois que le thread entre dans un état d’alerte, il appellera les fonctions de rappel envoyées à [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) et [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), puis le retour de la fonction qui l’a placée dans un état d’alerte.</span><span class="sxs-lookup"><span data-stu-id="9712f-126">In this scenario, once the thread enters an alertable state it will call the callback functions sent to [**ReadFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-readfileex) and [**WriteFileEx**](/windows/desktop/api/FileAPI/nf-fileapi-writefileex), then return from the function that placed it in an alertable state.</span></span>

<span data-ttu-id="9712f-127">Si un thread entre dans un état d’alerte alors que sa file d’attente APC est vide, l’exécution du thread est suspendue par le noyau jusqu’à ce que l’un des éléments suivants se produise :</span><span class="sxs-lookup"><span data-stu-id="9712f-127">If a thread enters an alertable state while its APC queue is empty, the thread's execution will be suspended by the kernel until one of the following occurs:</span></span>

-   <span data-ttu-id="9712f-128">L’objet de noyau attendu est signalé.</span><span class="sxs-lookup"><span data-stu-id="9712f-128">The kernel object that is being waited on becomes signaled.</span></span>
-   <span data-ttu-id="9712f-129">Un pointeur de fonction de rappel est placé dans la file d’attente APC.</span><span class="sxs-lookup"><span data-stu-id="9712f-129">A callback function pointer is placed in the APC queue.</span></span>

<span data-ttu-id="9712f-130">Un thread qui utilise des e/s alertables traite les demandes d’e/s asynchrones plus efficacement que lorsqu’il attend simplement l’indicateur d’événement dans la structure [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) à définir, et le mécanisme d’e/s d’alerte est moins compliqué que les [ports de terminaison d’e/s](i-o-completion-ports.md) à utiliser.</span><span class="sxs-lookup"><span data-stu-id="9712f-130">A thread that uses alertable I/O processes asynchronous I/O requests more efficiently than when they simply wait on the event flag in the [**OVERLAPPED**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) structure to be set, and the alertable I/O mechanism is less complicated than [I/O completion ports](i-o-completion-ports.md) to use.</span></span> <span data-ttu-id="9712f-131">Toutefois, les e/s alertables renvoient le résultat de la requête d’e/s uniquement au thread qui l’a lancée.</span><span class="sxs-lookup"><span data-stu-id="9712f-131">However, alertable I/O returns the result of the I/O request only to the thread that initiated it.</span></span> <span data-ttu-id="9712f-132">Les ports de terminaison d’e/s n’ont pas cette limitation.</span><span class="sxs-lookup"><span data-stu-id="9712f-132">I/O completion ports do not have this limitation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9712f-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9712f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9712f-134">Appels de procédure asynchrone</span><span class="sxs-lookup"><span data-stu-id="9712f-134">Asynchronous Procedure Calls</span></span>](/windows/desktop/Sync/asynchronous-procedure-calls)
</dt> </dl>

 

 
