---
title: En attente de la réponse asynchrone
description: Ce que fait le client lorsqu’il attend d’être informé d’une réponse du serveur dépend du mécanisme de notification qu’il sélectionne.
ms.assetid: b1d4ea54-26bc-49f9-8cc1-a74fd4ffced3
keywords:
- Appel de procédure distante RPC, tâches, attente de réponses asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0890b3024a05bb704f7b5a803c4b1e517c65ee21
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315887"
---
# <a name="waiting-for-the-asynchronous-reply"></a><span data-ttu-id="bb17f-104">En attente de la réponse asynchrone</span><span class="sxs-lookup"><span data-stu-id="bb17f-104">Waiting for the Asynchronous Reply</span></span>

<span data-ttu-id="bb17f-105">Ce que fait le client lorsqu’il attend d’être informé d’une réponse du serveur dépend du mécanisme de notification qu’il sélectionne.</span><span class="sxs-lookup"><span data-stu-id="bb17f-105">What the client does while it waits to be notified of a reply from the server depends on the notification mechanism it selects.</span></span>

<span data-ttu-id="bb17f-106">Si le client utilise un événement pour la notification, il appelle généralement la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ou la fonction [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) .</span><span class="sxs-lookup"><span data-stu-id="bb17f-106">If the client uses an event for notification, it will typically call the [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function or the [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) function.</span></span> <span data-ttu-id="bb17f-107">Le client entre dans un État bloqué lorsqu’il appelle l’une de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="bb17f-107">The client enters a blocked state when it calls either of these functions.</span></span> <span data-ttu-id="bb17f-108">Cela est efficace, car le client n’utilise pas de cycles d’exécution du processeur pendant qu’il est bloqué.</span><span class="sxs-lookup"><span data-stu-id="bb17f-108">This is efficient because the client does not consume CPU run cycles while it is blocked.</span></span>

<span data-ttu-id="bb17f-109">Lorsqu’il utilise l’interrogation pour attendre ses résultats, le programme client entre dans une boucle qui appelle à plusieurs reprises la fonction [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span><span class="sxs-lookup"><span data-stu-id="bb17f-109">When it uses polling to wait for its results, the client program enters a loop that repeatedly calls the function [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="bb17f-110">Il s’agit d’une méthode efficace pour attendre si votre programme client effectue d’autres traitements dans la boucle d’interrogation.</span><span class="sxs-lookup"><span data-stu-id="bb17f-110">This is an efficient method of waiting if your client program does other processing in the polling loop.</span></span> <span data-ttu-id="bb17f-111">Par exemple, il peut préparer des données en petits segments pour un appel de procédure distante asynchrone suivant.</span><span class="sxs-lookup"><span data-stu-id="bb17f-111">For instance, it can prepare data in small chunks for a subsequent asynchronous remote procedure call.</span></span> <span data-ttu-id="bb17f-112">Une fois chaque segment terminé, votre client peut interroger l’appel de procédure distante asynchrone en suspens pour déterminer s’il est terminé.</span><span class="sxs-lookup"><span data-stu-id="bb17f-112">After each chunk is finished, your client can poll the outstanding asynchronous remote procedure call to see if it is complete.</span></span>

<span data-ttu-id="bb17f-113">Votre programme client peut fournir un appel de procédure asynchrone (APC), qui est un type de fonction de rappel que la bibliothèque Runtime RPC appellera lorsque l’appel de procédure distante asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="bb17f-113">Your client program can provide an asynchronous procedure call (APC), which is a type of callback function that the RPC run-time library will invoke when the asynchronous remote procedure call completes.</span></span> <span data-ttu-id="bb17f-114">Votre programme client doit être dans un état d’attente averti.</span><span class="sxs-lookup"><span data-stu-id="bb17f-114">Your client program must be in an alertable wait state.</span></span> <span data-ttu-id="bb17f-115">Cela signifie généralement que le client appelle une fonction d’API Windows pour se placer dans un État bloqué.</span><span class="sxs-lookup"><span data-stu-id="bb17f-115">This typically means that the client calls a Windows API function to put itself in a blocked state.</span></span> <span data-ttu-id="bb17f-116">Pour plus d’informations, consultez [appels de procédures asynchrones](/windows/desktop/Sync/asynchronous-procedure-calls).</span><span class="sxs-lookup"><span data-stu-id="bb17f-116">For more information, see [Asynchronous Procedure Calls](/windows/desktop/Sync/asynchronous-procedure-calls).</span></span>

> [!Note]  
> <span data-ttu-id="bb17f-117">La notification d’achèvement ne sera pas retournée à partir d’une routine RPC asynchrone si une exception RPC est levée lors d’un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bb17f-117">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during a asynchronous call.</span></span>

 

<span data-ttu-id="bb17f-118">Si votre programme client utilise un port de terminaison d’e/s pour recevoir la notification d’achèvement, il doit appeler la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) .</span><span class="sxs-lookup"><span data-stu-id="bb17f-118">If your client program uses an I/O completion port to receive completion notification, it must call the [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) function.</span></span> <span data-ttu-id="bb17f-119">Dans ce cas, il peut attendre indéfiniment une réponse ou continuer à effectuer d’autres traitements.</span><span class="sxs-lookup"><span data-stu-id="bb17f-119">When it does, it can either wait indefinitely for a response or continue to do other processing.</span></span> <span data-ttu-id="bb17f-120">S’il effectue un autre traitement pendant qu’il attend une réponse, il doit interroger le port de terminaison avec la fonction **GetQueuedCompletionStatus** .</span><span class="sxs-lookup"><span data-stu-id="bb17f-120">If it does other processing while it waits for a reply, it must poll the completion port with the **GetQueuedCompletionStatus** function.</span></span> <span data-ttu-id="bb17f-121">Dans ce cas, elle doit généralement définir le *dwMilliseconds* sur zéro.</span><span class="sxs-lookup"><span data-stu-id="bb17f-121">In this case, it typically needs to set the *dwMilliseconds* to zero.</span></span> <span data-ttu-id="bb17f-122">Cela entraîne le retour immédiat de **GetQueuedCompletionStatus** , même si l’appel asynchrone n’est pas terminé.</span><span class="sxs-lookup"><span data-stu-id="bb17f-122">This causes **GetQueuedCompletionStatus** to return immediately, even if the asynchronous call has not completed.</span></span>

<span data-ttu-id="bb17f-123">Les programmes clients peuvent également recevoir des notifications de fin d’exécution par le biais de leurs files d’attente de messages de fenêtre.</span><span class="sxs-lookup"><span data-stu-id="bb17f-123">Client programs can also receive completion notification through their window message queues.</span></span> <span data-ttu-id="bb17f-124">Dans ce cas, ils traitent simplement le message d’achèvement comme tout message Windows.</span><span class="sxs-lookup"><span data-stu-id="bb17f-124">In this situation, they simply process the completion message as they would any Windows message.</span></span>

<span data-ttu-id="bb17f-125">Dans une application multithread, un appel asynchrone peut être annulé par le client uniquement après que le thread à l’origine de l’appel a été retourné avec succès à partir de l’appel.</span><span class="sxs-lookup"><span data-stu-id="bb17f-125">In a multithreaded application, an asynchronous call can be canceled by the client only after the thread that originated the call has returned successfully from the call.</span></span> <span data-ttu-id="bb17f-126">Cela garantit que l’appel n’est pas annulé de manière asynchrone par un autre thread après l’échec d’un appel synchrone.</span><span class="sxs-lookup"><span data-stu-id="bb17f-126">This ensures that the call is not canceled asynchronously by another thread after it failed a synchronous call.</span></span> <span data-ttu-id="bb17f-127">Comme pratique standard, un appel asynchrone qui échoue de façon synchrone ne doit pas être annulé de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bb17f-127">As standard practice, an asynchronous call that fails synchronously should not be canceled asynchronously.</span></span> <span data-ttu-id="bb17f-128">L’application cliente doit observer ce comportement si des appels peuvent être émis et annulés sur des threads différents.</span><span class="sxs-lookup"><span data-stu-id="bb17f-128">The client application must observe this behavior if calls may be issued and canceled on different threads.</span></span> <span data-ttu-id="bb17f-129">De même, après l’annulation de l’appel, le code client doit attendre la notification d’achèvement et terminer l’appel.</span><span class="sxs-lookup"><span data-stu-id="bb17f-129">Also, after the call is canceled, the client code must wait for the completion notification and complete the call.</span></span> <span data-ttu-id="bb17f-130">La fonction [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) touche simplement la notification d’achèvement. ce n’est pas un substitut pour terminer l’appel.</span><span class="sxs-lookup"><span data-stu-id="bb17f-130">The [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) function simply rushes the completion notification; it is not a substitute for completing the call.</span></span>

<span data-ttu-id="bb17f-131">Le fragment de code suivant montre comment un programme client peut utiliser un événement pour attendre une réponse asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bb17f-131">The following code fragment illustrates how a client program can use an event to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="bb17f-132">Les programmes clients qui utilisent un APC pour recevoir la notification d’une réponse asynchrone se placent généralement dans un État bloqué.</span><span class="sxs-lookup"><span data-stu-id="bb17f-132">Client programs that use an APC to receive notification of an asynchronous reply typically put themselves into a blocked state.</span></span> <span data-ttu-id="bb17f-133">Le fragment de code suivant illustre cela.</span><span class="sxs-lookup"><span data-stu-id="bb17f-133">The following code fragment shows this.</span></span>


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="bb17f-134">Dans ce cas, le programme client passe en mode veille, en consommant aucun cycle de processeur, jusqu’à ce que la bibliothèque Runtime RPC appelle l’APC (non affiché).</span><span class="sxs-lookup"><span data-stu-id="bb17f-134">In this case, the client program goes to sleep, consuming no CPU cycles, until the RPC run-time library calls the APC (not shown).</span></span>

<span data-ttu-id="bb17f-135">L’exemple suivant illustre un client qui utilise un port de terminaison d’e/s pour attendre une réponse asynchrone.</span><span class="sxs-lookup"><span data-stu-id="bb17f-135">The next example demonstrates a client that uses an I/O completion port to wait for an asynchronous reply.</span></span>


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (!GetQueuedCompletionStatus(
         Async.u.IOC.hIOPort,
         &Async.u.IOC.dwNumberOfBytesTransferred,
         &Async.u.IOC.dwCompletionKey,
         &Async.u.IOC.lpOverlapped,
         INFINITE))
{
    RpcRaiseException(APP_ERROR);
}
```



<span data-ttu-id="bb17f-136">Dans l’exemple précédent, l’appel à [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) attend indéfiniment jusqu’à ce que l’appel de procédure distante asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="bb17f-136">In the preceding example, the call to [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) waits indefinitely until the asynchronous remote procedure call completes.</span></span>

<span data-ttu-id="bb17f-137">Un piège potentiel se produit lors de l’écriture d’applications multithread.</span><span class="sxs-lookup"><span data-stu-id="bb17f-137">One potential pitfall occurs when writing multithreaded applications.</span></span> <span data-ttu-id="bb17f-138">Si un thread appelle un appel de procédure distante et se termine avant de recevoir une notification indiquant que l’envoi est terminé, l’appel de procédure distante peut échouer et le stub client peut fermer la connexion au serveur.</span><span class="sxs-lookup"><span data-stu-id="bb17f-138">If a thread invokes a remote procedure call and then terminates before it receives notification that the send completed, the remote procedure call may fail and the client stub may close the connection to the server.</span></span> <span data-ttu-id="bb17f-139">Par conséquent, les threads qui appellent une procédure distante ne doivent pas se terminer avant que l’appel soit terminé ou annulé lorsque le comportement n’est pas souhaitable.</span><span class="sxs-lookup"><span data-stu-id="bb17f-139">Therefore, threads that call a remote procedure should not terminate before the call is completed or canceled when behavior is undesirable.</span></span>

 

 