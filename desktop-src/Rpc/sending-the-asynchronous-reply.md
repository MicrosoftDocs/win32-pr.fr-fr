---
title: Envoi de la réponse asynchrone
description: Lorsque l’appel asynchrone est terminé, le serveur envoie une réponse au client en appelant la fonction RpcAsyncCompleteCall et en lui passant le handle asynchrone.
ms.assetid: 458bc476-963e-4812-b4c2-9074ff0a8284
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06f861c3f2a1befdb85435f5275176c82e23bb06
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029661"
---
# <a name="sending-the-asynchronous-reply"></a><span data-ttu-id="5f9bd-103">Envoi de la réponse asynchrone</span><span class="sxs-lookup"><span data-stu-id="5f9bd-103">Sending the Asynchronous Reply</span></span>

<span data-ttu-id="5f9bd-104">Lorsque l’appel asynchrone est terminé, le serveur envoie une réponse au client en appelant la fonction [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) et en lui passant le handle asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-104">When the asynchronous call is complete, the server sends a reply to the client by calling the [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) function and passing it the asynchronous handle.</span></span> <span data-ttu-id="5f9bd-105">Cet appel est nécessaire même si l’appel asynchrone a une valeur de retour void et \[ aucun \] paramètre de sortie.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-105">This call is necessary even if the asynchronous call has a void return value and no \[out\] parameters.</span></span> <span data-ttu-id="5f9bd-106">Si la fonction a une valeur de retour, elle est passée par référence à **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-106">If the function has a return value, it is passed by reference to **RpcAsyncCompleteCall**.</span></span>

<span data-ttu-id="5f9bd-107">Quand le serveur appelle [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) ou **RpcAsyncAbortCall**, ou qu’un appel se termine parce qu’une exception a été levée dans la routine du gestionnaire de serveur, la bibliothèque Runtime RPC détruit automatiquement le handle asynchrone du serveur.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-107">When the server calls [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) or **RpcAsyncAbortCall**, or a call completes because an exception was raised in the server-manager routine, the RPC run-time library automatically destroys the server's asynchronous handle.</span></span>

> [!Note]  
> <span data-ttu-id="5f9bd-108">Le serveur doit terminer la mise à jour des \[ paramètres in, out \] et \[ out \] avant d’appeler **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-108">The server must finish updating the \[in, out\] and \[out\] parameters before calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="5f9bd-109">Aucune modification ne peut être apportée à ces paramètres ou au handle asynchrone après l’appel de **RpcAsyncCompleteCall**.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-109">No changes can be made to those parameters or to the asynchronous handle after calling **RpcAsyncCompleteCall**.</span></span> <span data-ttu-id="5f9bd-110">Si l’appel de fonction **RpcAsyncCompleteCall** échoue, le runtime RPC libère les paramètres.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-110">If the **RpcAsyncCompleteCall** function call fails, the RPC runtime frees the parameters.</span></span>

 

<span data-ttu-id="5f9bd-111">L’exemple suivant illustre un appel de procédure asynchrone simple.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-111">The following example demonstrates a simple asynchronous procedure call.</span></span>


```C++
#define DEFAULT_ASYNC_DELAY 20;
#define ASYNC_CANCEL_CHECK 100;

void AsyncFunc(IN PRPC_ASYNC_STATE pAsync,
               IN RPC_BINDING_HANDLE hBinding,
               IN OUT unsigned long nAsychDelay)
{
    int nReply = 1;
    RPC_STATUS status;
    unsigned long nTmpAsychDelay;
    int i;
 
    if (nAsychDelay < 0){
        nAsychDelay = DEFAULT_ASYNC_DELAY;
    }else if (nAsychDelay < 100){
        nAsychDelay = 100;
    }

    // We only call RpcServerTestCancel if the call
    // takes longer than ASYNC_CANCEL_CHECK ms
    if(nAsychDelay > ASYNC_CANCEL_CHECK){
        
        nTmpAsychDelay = nAsychDelay/100;
 
        for (i = 0; i < 100; i++){
            Sleep(nTmpAsychDelay);
 
            if (i%5 == 0){
                fprintf(stderr, 
                        "\rRunning AsyncFunc (%lu ms) (%d%c) ... ",
                        nAsychDelay, i+5, PERCENT);
 
                status = 
                    RpcServerTestCancel(
                        RpcAsyncGetCallHandle(pAsync));
                if (status == RPC_S_OK){
                    fprintf(stderr, 
                            "\nAsyncFunc has been canceled!!!\n");
                    break;
                }else if (status != RPC_S_CALL_IN_PROGRESS){
                    printf(
                        "RpcAsyncInitializeHandle returned 0x%x\n", 
                        status);
                    exit(status); 
                }
            }
        }
    }else{
        Sleep(nAsychDelay);
    }
 
    printf("\nCalling RpcAsyncCompleteCall\n");
    status = RpcAsyncCompleteCall(pAsync, &nReply);
    printf("RpcAsyncCompleteCall returned 0x%x\n", status);
    if (status){
        exit(status);
    }
}
```



<span data-ttu-id="5f9bd-112">Par souci de simplicité, cette routine de serveur asynchrone ne traite pas les données réelles.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-112">For the sake of simplicity, this asynchronous server routine does not process actual data.</span></span> <span data-ttu-id="5f9bd-113">Il se met tout simplement en veille pendant un certain temps.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-113">It simply puts itself to sleep for awhile.</span></span>

> [!Note]  
> <span data-ttu-id="5f9bd-114">La fonction **RpcAsyncCompleteCall** peut être appelée sur le thread qui a reçu l’appel ou sur tout autre thread du processus.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-114">The **RpcAsyncCompleteCall** function can be called either on the thread that received the call, or on any other thread in the process.</span></span> <span data-ttu-id="5f9bd-115">Si toutes les données nécessaires pour terminer l’appel sont immédiatement disponibles, le serveur peut les remplir sur le même thread et appeler **RpcAsyncCompleteCall** sur le même thread.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-115">If all the data necessary to complete the call are readily available, the server may fill them in on the same thread, and call the **RpcAsyncCompleteCall** on the same thread.</span></span> <span data-ttu-id="5f9bd-116">Cette approche permet d’économiser un changement de contexte et d’améliorer les performances.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-116">This approach saves some context switching and improves performance.</span></span> <span data-ttu-id="5f9bd-117">De tels appels sont appelés associer façon opportuniste asynchrones.</span><span class="sxs-lookup"><span data-stu-id="5f9bd-117">Such calls are called opportunistically asynchronous.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="5f9bd-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5f9bd-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f9bd-119">**\_état RPC asynchrone \_**</span><span class="sxs-lookup"><span data-stu-id="5f9bd-119">**RPC\_ASYNC\_STATE**</span></span>](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[<span data-ttu-id="5f9bd-120">**RpcAsyncCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="5f9bd-120">**RpcAsyncCompleteCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[<span data-ttu-id="5f9bd-121">**RpcAsyncAbortCall**</span><span class="sxs-lookup"><span data-stu-id="5f9bd-121">**RpcAsyncAbortCall**</span></span>](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[<span data-ttu-id="5f9bd-122">**RpcServerTestCancel**</span><span class="sxs-lookup"><span data-stu-id="5f9bd-122">**RpcServerTestCancel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




