---
title: Exécution de l’appel asynchrone
description: Avant de pouvoir effectuer un appel distant asynchrone, le client doit initialiser le handle asynchrone. Les programmes client et serveur utilisent des pointeurs vers \_ la \_ structure d’état asynchrone RPC pour les handles asynchrones.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Appel de procédure distante RPC, tâches, appels asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa06f60b43a7dff3a29223ff1d8e9ad726c0e938
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106510270"
---
# <a name="making-the-asynchronous-call"></a><span data-ttu-id="189a4-105">Exécution de l’appel asynchrone</span><span class="sxs-lookup"><span data-stu-id="189a4-105">Making the Asynchronous Call</span></span>

<span data-ttu-id="189a4-106">Avant de pouvoir effectuer un appel distant asynchrone, le client doit initialiser le handle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="189a4-106">Before it can make an asynchronous remote call, the client must initialize the asynchronous handle.</span></span> <span data-ttu-id="189a4-107">Les programmes client et serveur utilisent des pointeurs vers la structure d' [**\_ \_ état asynchrone RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) pour les handles asynchrones.</span><span class="sxs-lookup"><span data-stu-id="189a4-107">Client and server programs use pointers to the [**RPC\_ASYNC\_STATE**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) structure for asynchronous handles.</span></span>

<span data-ttu-id="189a4-108">Chaque appel en suspens doit avoir son propre handle asynchrone unique.</span><span class="sxs-lookup"><span data-stu-id="189a4-108">Every outstanding call must have its own unique asynchronous handle.</span></span> <span data-ttu-id="189a4-109">Le client crée le descripteur et le passe à la fonction [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) .</span><span class="sxs-lookup"><span data-stu-id="189a4-109">The client creates the handle and passes it to the [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) function.</span></span> <span data-ttu-id="189a4-110">Pour que l’appel se termine correctement, le client doit s’assurer que la mémoire pour le descripteur n’est pas libérée jusqu’à ce qu’il reçoive la réponse asynchrone du serveur.</span><span class="sxs-lookup"><span data-stu-id="189a4-110">For the call to complete correctly, the client must ensure that the memory for the handle is not released until it receives the server's asynchronous reply.</span></span> <span data-ttu-id="189a4-111">En outre, avant d’effectuer un autre appel sur un handle asynchrone existant, le client doit réinitialiser le descripteur.</span><span class="sxs-lookup"><span data-stu-id="189a4-111">Also, before making another call on an existing asynchronous handle, the client must reinitialize the handle.</span></span> <span data-ttu-id="189a4-112">Si vous ne le faites pas, le stub client lève une exception pendant l’appel.</span><span class="sxs-lookup"><span data-stu-id="189a4-112">Failure to do this can cause the client stub to raise an exception during the call.</span></span> <span data-ttu-id="189a4-113">Le client doit également s’assurer que les tampons fournis pour les \[ paramètres [**out**](/windows/desktop/Midl/out-idl) \] et \[ [**dans**](/windows/desktop/Midl/in), les paramètres **out** \] à une procédure distante asynchrone restent alloués jusqu’à ce qu’il ait reçu la réponse du serveur.</span><span class="sxs-lookup"><span data-stu-id="189a4-113">The client must also ensure that the buffers it supplies for \[[**out**](/windows/desktop/Midl/out-idl)\] parameters and \[[**in**](/windows/desktop/Midl/in), **out**\] parameters to an asynchronous remote procedure remain allocated until it has received the reply from the server.</span></span>

<span data-ttu-id="189a4-114">Lorsqu’il appelle une procédure distante asynchrone, le client doit sélectionner la méthode qui sera utilisée par la bibliothèque Runtime RPC pour l’informer de la fin de l’appel.</span><span class="sxs-lookup"><span data-stu-id="189a4-114">When it invokes an asynchronous remote procedure, the client must select the method that the RPC run-time library will use to notify it of the call's completion.</span></span> <span data-ttu-id="189a4-115">Le client peut recevoir cette notification de l’une des manières suivantes :</span><span class="sxs-lookup"><span data-stu-id="189a4-115">The client can receive this notification in any one of the following ways:</span></span>

-   <span data-ttu-id="189a4-116">Événement.</span><span class="sxs-lookup"><span data-stu-id="189a4-116">Event.</span></span> <span data-ttu-id="189a4-117">Le client peut spécifier un événement à déclencher lorsque l’appel est terminé.</span><span class="sxs-lookup"><span data-stu-id="189a4-117">The client can specify an event to be fired when the call has completed.</span></span> <span data-ttu-id="189a4-118">Pour plus d’informations, consultez [objets d’événement](/windows/desktop/Sync/event-objects).</span><span class="sxs-lookup"><span data-stu-id="189a4-118">For details, see [Event Objects](/windows/desktop/Sync/event-objects).</span></span>
-   <span data-ttu-id="189a4-119">Interrogation.</span><span class="sxs-lookup"><span data-stu-id="189a4-119">Polling.</span></span> <span data-ttu-id="189a4-120">Le client peut appeler [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)de façon répétée.</span><span class="sxs-lookup"><span data-stu-id="189a4-120">The client can repeatedly call [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus).</span></span> <span data-ttu-id="189a4-121">Si la valeur de retour est différente de l' \_ \_ appel Async RPC S \_ \_ en attente, l’appel est terminé.</span><span class="sxs-lookup"><span data-stu-id="189a4-121">If the return value is anything other than RPC\_S\_ASYNC\_CALL\_PENDING, the call is complete.</span></span> <span data-ttu-id="189a4-122">Cette méthode utilise plus de temps processeur que les autres méthodes décrites ici.</span><span class="sxs-lookup"><span data-stu-id="189a4-122">This method uses more CPU time than the other methods described here.</span></span>
-   <span data-ttu-id="189a4-123">APC.</span><span class="sxs-lookup"><span data-stu-id="189a4-123">APC.</span></span> <span data-ttu-id="189a4-124">Le client peut spécifier un [appel de procédure asynchrone (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) qui est appelé lorsque l’appel est terminé.</span><span class="sxs-lookup"><span data-stu-id="189a4-124">The client can specify an [asynchronous procedure call (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) that gets called when the call completes.</span></span> <span data-ttu-id="189a4-125">Pour le prototype de la fonction APC, consultez [**\_ routine RPCNOTIFICATION**](/previous-versions/aa375808(v=vs.80)).</span><span class="sxs-lookup"><span data-stu-id="189a4-125">For the prototype of the APC function, see [**RPCNOTIFICATION\_ROUTINE**](/previous-versions/aa375808(v=vs.80)).</span></span> <span data-ttu-id="189a4-126">L’APC est appelé avec le paramètre d’événement défini sur RpcCallComplete.</span><span class="sxs-lookup"><span data-stu-id="189a4-126">The APC is called with its Event parameter set to RpcCallComplete.</span></span> <span data-ttu-id="189a4-127">Pour que les APC soient distribués, le thread client doit se trouver dans un état d’attente averti.</span><span class="sxs-lookup"><span data-stu-id="189a4-127">For APCs to get dispatched, the client thread must be in an alertable wait state.</span></span>

    <span data-ttu-id="189a4-128">Si le champ **hThread** du descripteur asynchrone a la valeur 0, les APC sont mis en file d’attente sur le thread qui a effectué l’appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="189a4-128">If the **hThread** field in the asynchronous handle is set to 0, the APCs are queued on the thread that made the asynchronous call.</span></span> <span data-ttu-id="189a4-129">Si la valeur est différente de zéro, les APC sont mis en file d’attente sur le thread spécifié par m.</span><span class="sxs-lookup"><span data-stu-id="189a4-129">If it is nonzero, the APCs are queued on the thread specified by m.</span></span>

-   <span data-ttu-id="189a4-130">IOC.</span><span class="sxs-lookup"><span data-stu-id="189a4-130">IOC.</span></span> <span data-ttu-id="189a4-131">Le port de terminaison d’e/s est notifié avec les paramètres spécifiés dans le handle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="189a4-131">The I/O completion port is notified with the parameters specified in the asynchronous handle.</span></span> <span data-ttu-id="189a4-132">Pour plus d’informations, consultez [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span><span class="sxs-lookup"><span data-stu-id="189a4-132">For more information, see [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).</span></span>
-   <span data-ttu-id="189a4-133">Handle Windows.</span><span class="sxs-lookup"><span data-stu-id="189a4-133">Windows handle.</span></span> <span data-ttu-id="189a4-134">Un message est publié dans le handle de fenêtre (HWND) spécifié.</span><span class="sxs-lookup"><span data-stu-id="189a4-134">A message is posted to the specified window handle (HWND).</span></span>

<span data-ttu-id="189a4-135">Le fragment de code suivant montre les étapes essentielles requises pour initialiser un handle asynchrone et l’utiliser pour effectuer un appel de procédure distante asynchrone.</span><span class="sxs-lookup"><span data-stu-id="189a4-135">The following code fragment shows the essential steps required for initializing an asynchronous handle and using it to make an asynchronous remote procedure call.</span></span>


```C++
RPC_ASYNC_STATE Async;
RPC_STATUS status;
 
// Initialize the handle.
status = RpcAsyncInitializeHandle(&Async, sizeof(RPC_ASYNC_STATE));
if (status)
{
    // Code to handle the error goes here.
}
 
Async.UserInfo = NULL;
Async.NotificationType = RpcNotificationTypeEvent;
 
Async.u.hEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
if (Async.u.hEvent == 0)
{
    // Code to handle the error goes here.
}
// Call an asynchronous RPC routine here
RpcTryExcept
{
    printf("\nCalling the remote procedure 'AsyncFunc'\n");
    AsyncFunc(&Async, AsyncRPC_ClientIfHandle, nAsychDelay);
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("AsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
 
// Call a synchronous routine while
// the asynchronous procedure is still running
RpcTryExcept
{
    printf("\nCalling the remote procedure 'NonAsyncFunc'\n");
    NonAsyncFunc(AsyncRPC_ClientIfHandle, pszMessage);
    fprintf(stderr, 
            "While 'AsyncFunc' is running asynchronously,\n"
            "we still can send message to the server in the mean "
            "time.\n\n");
}
RpcExcept(1)
{
    ulCode = RpcExceptionCode();
    printf("NonAsyncFunc: Run time reported exception 0x%lx = %ld\n", 
            ulCode, ulCode);
}
RpcEndExcept
```



<span data-ttu-id="189a4-136">Comme le montre cet exemple, votre programme client peut exécuter des appels de procédure distante synchrone alors qu’un appel de procédure asynchrone est toujours en attente.</span><span class="sxs-lookup"><span data-stu-id="189a4-136">As this example demonstrates, your client program can execute synchronous remote procedure calls while an asynchronous procedure call is still pending.</span></span> <span data-ttu-id="189a4-137">Ce client crée un objet d’événement pour la bibliothèque Runtime RPC à utiliser pour l’avertir lorsque l’appel asynchrone se termine.</span><span class="sxs-lookup"><span data-stu-id="189a4-137">This client creates an event object for the RPC run-time library to use to notify it when the asynchronous call completes.</span></span>

> [!Note]  
> <span data-ttu-id="189a4-138">La notification d’achèvement ne sera pas retournée à partir d’une routine RPC asynchrone si une exception RPC est levée lors d’un appel asynchrone.</span><span class="sxs-lookup"><span data-stu-id="189a4-138">Notification of completion will not be returned from an asynchronous RPC routine if an RPC exception is raised during an asynchronous call.</span></span>

 

 

 