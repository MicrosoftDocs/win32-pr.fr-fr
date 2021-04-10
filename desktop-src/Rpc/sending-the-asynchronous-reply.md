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
# <a name="sending-the-asynchronous-reply"></a>Envoi de la réponse asynchrone

Lorsque l’appel asynchrone est terminé, le serveur envoie une réponse au client en appelant la fonction [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) et en lui passant le handle asynchrone. Cet appel est nécessaire même si l’appel asynchrone a une valeur de retour void et \[ aucun \] paramètre de sortie. Si la fonction a une valeur de retour, elle est passée par référence à **RpcAsyncCompleteCall**.

Quand le serveur appelle [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) ou **RpcAsyncAbortCall**, ou qu’un appel se termine parce qu’une exception a été levée dans la routine du gestionnaire de serveur, la bibliothèque Runtime RPC détruit automatiquement le handle asynchrone du serveur.

> [!Note]  
> Le serveur doit terminer la mise à jour des \[ paramètres in, out \] et \[ out \] avant d’appeler **RpcAsyncCompleteCall**. Aucune modification ne peut être apportée à ces paramètres ou au handle asynchrone après l’appel de **RpcAsyncCompleteCall**. Si l’appel de fonction **RpcAsyncCompleteCall** échoue, le runtime RPC libère les paramètres.

 

L’exemple suivant illustre un appel de procédure asynchrone simple.


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



Par souci de simplicité, cette routine de serveur asynchrone ne traite pas les données réelles. Il se met tout simplement en veille pendant un certain temps.

> [!Note]  
> La fonction **RpcAsyncCompleteCall** peut être appelée sur le thread qui a reçu l’appel ou sur tout autre thread du processus. Si toutes les données nécessaires pour terminer l’appel sont immédiatement disponibles, le serveur peut les remplir sur le même thread et appeler **RpcAsyncCompleteCall** sur le même thread. Cette approche permet d’économiser un changement de contexte et d’améliorer les performances. De tels appels sont appelés associer façon opportuniste asynchrones.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**\_état RPC asynchrone \_**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state)
</dt> <dt>

[**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall)
</dt> <dt>

[**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)
</dt> <dt>

[**RpcServerTestCancel**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcservertestcancel)
</dt> </dl>

 

 




