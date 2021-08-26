---
title: Gestion de canal asynchrone côté serveur
description: La routine Manager d’une fonction asynchrone reçoit toujours le descripteur asynchrone en tant que premier paramètre.
ms.assetid: ddf9c319-6c4d-4de1-ab29-0ef9b76531ba
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b879cad9b3bde57798a3ebd3c04f7c9a76cb0d1ed055d219195db51cbed4a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017789"
---
# <a name="server-side-asynchronous-pipe-handling"></a>Gestion de canal asynchrone côté serveur

La routine Manager d’une fonction asynchrone reçoit toujours le descripteur asynchrone en tant que premier paramètre. Le serveur utilise ce handle pour envoyer la réponse et envoyer les données du canal de communication sortant dès qu’elles sont disponibles. Le descripteur reste valide jusqu’à ce que [**RpcAsyncCompleteCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccompletecall) soit appelé dessus, l’appel est abandonné par [**RpcAsyncAbortCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncabortcall)ou une exception se produit dans la routine du gestionnaire. L’application doit effectuer le suivi de tous les pointeurs de niveau supérieur \[ **pour les** \] paramètres out et \[ **in, out** \] , afin de les mettre à jour avant d’effectuer l’appel. L’application doit également effectuer le suivi des \[ canaux d' [**in**](/windows/desktop/Midl/in) \] et de \[ [**sortie**](/windows/desktop/Midl/out-idl) \] .

Le serveur envoie des données de canal asynchrones de la même manière que le client. Consultez [gestion des canaux asynchrones côté client](client-side-asynchronous-pipe-handling.md).

Le serveur reçoit les données de canal asynchrones de la même manière que le client. Si le mécanisme de réception est un appel de procédure asynchrone (APC), le serveur doit spécifier un handle de thread (dans pAsync->u. APC. hThread) et inscrire le handle asynchrone avec la bibliothèque Runtime.

## <a name="example"></a>Exemple

Dans cet exemple, la routine du gestionnaire de serveur, MyAsyncPipeFunc, gère l’appel de procédure distante à partir du client.


```C++
typedef struct 
{
    PRPC_ASYNC_STATE pAsync;
    ASYNC_INTPIPE *inpipe;
    ASYNC_INTPIPE *outpipe;
    int i;
    int *b;
    int PipeBuffer[ASYNC_CHUNK_SIZE];
} PIPE_CALL_COOKIE;
 
void MyAsyncPipeFunc(
    IN PRPC_ASYNC_STATE pAsync,
    IN RPC_BINDING_HANDLE hBinding,
    IN int a,
    IN ASYNC_INTPIPE *inpipe,
    OUT ASYNC_INTPIPE *outpipe,
    OUT int *b)
{
    unsigned long ThreadIdentifier;
    HANDLE HandleToThread;
    PIPE_CALL_COOKIE *PipeCallCookie;
 
    PipeCallCookie = new PIPE_CALL_COOKIE;
    PipeCallCookie->pAsync = pAsync;
    PipeCallCookie->inpipe = inpipe;
    PipeCallCookie->outpipe = outpipe;
    PipeCallCookie->b = b;
 
    pAsync->u.APC.hThread = 0;
    pAsync->u.APC.hThread = CreateThread(
                                0, DefaultThreadStackSize,
                                (LPTHREAD_START_ROUTINE)   
                                ThreadProcPipes,
                                PipeCallCookie, 0,
                                &ThreadIdentifier);
}// endMyAsyncPipeFunc
 
//Sending pipe data
//This APC routine is called when a pipe send completes, 
//or when an asynchronous call completes. 
 
//This thread routine receives pipe data, processes the call, 
//sends the reply back to the client, and 
//completes the asynchronous call.
 
void ThreadProcPipes(IN PIPE_CALL_COOKIE  *Cookie)
{
    int *ptr ;
    int  n ;
    int retval ;
 
    while (pAsync->u.APC.hThread == 0)
    {
        Sleep(10);
    }
 
    pAsync->Flags = RPC_C_NOTIFY_ON_SEND_COMPLETE;
    pAsync->UserInfo = (void *) PipeCallCookie;
    pAsync->NotificationType = RpcNotificationTypeApc;
    pAsync->u.APC.NotificationRoutine = MyAsyncPipeAPCRoutine;
    pAsync->u.APC.hThread = HandleToThread;
 
    RpcAsyncRegisterHandle(pAsync);
 
    while (!fDone)
    {
        Cookie->inpipe->pull(
            Cookie->inpipe.state,
            (int *) Cookie->PipeBuffer,
            ASYNC_CHUNK_SIZE,
            &num_elements);
        switch (Status)
        {
            case RPC_S_ASYNC_CALL_PENDING:
                if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
                {
                    RpcRaiseException(APP_ERROR) ;
                }
            break;
 
            case RPC_S_OK:
                if (num_elements == 0)
                {
                    fDone = 1;
                }
                else
                {
                    // process the received data
                }
            break;
 
            default:
                fDone = 1;
            break;
        }
    }
 
    Cookie->i = 1;
    Cookie->outpipe->push(
        Cookie->outpipe.state,
        0,
        Cookie->PipeBuffer,
        ASYNC_CHUNK_SIZE) ;
 
    while (Cookie->i < ASYNC_NUM_CHUNKS+1)
    {
        if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
        {
            RpcRaiseException (APP_ERROR);
        }
    }
    // sending non pipe reply
    *(Cookie->b) = 10;
    Status = RpcAsyncCompleteCall (Cookie->pAsync, &retval);
}
 
void MyAsyncPipeAPCRoutine (
    IN PRPC_ASYNC_STATE pAsync,
    IN void *Context,
    IN unsigned int Flags)
{
    PIPE_CALL_COOKIE *Cookie = (PIPE_CALL_COOKIE *) pAsync->UserInfo;
 
    if (Flags & RPC_ASYNC_PIPE_SEND_COMPLETE)
    {
        if (Cookie->i & ASYNC_NUM_CHUNKS)
        {
            Cookie->outpipe->push(
                Cookie->outpipe.state,
                0,
                (int *) Cookie->PipeBuffer,
                ASYNC_CHUNK_SIZE);
            Cookie->i++ ;
        }
        else
        {
            pAsync->Flags = 0;
            Cookie->outpipe->push(Cookie->outpipe.state, 0, 0, 0);
            Cookie->i++;
        }
    }
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Canaux](pipes.md)
</dt> <dt>

[MIDL asynchrone](/windows/desktop/Midl/async)
</dt> <dt>

[RPC asynchrone côté serveur](server-side-asynchronous-rpc.md)
</dt> </dl>

 

 