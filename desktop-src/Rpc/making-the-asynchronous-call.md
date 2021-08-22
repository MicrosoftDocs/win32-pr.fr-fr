---
title: Exécution de l’appel asynchrone
description: Avant de pouvoir effectuer un appel distant asynchrone, le client doit initialiser le handle asynchrone. Les programmes client et serveur utilisent des pointeurs vers \_ la \_ structure d’état asynchrone RPC pour les handles asynchrones.
ms.assetid: b40308ef-88ae-4c80-9118-29c5ffee77ad
keywords:
- Appel de procédure distante RPC, tâches, appels asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93d8399071cae6ea39aaac3f966e7e799b2c93b32a152048a7d18282b465f929
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928375"
---
# <a name="making-the-asynchronous-call"></a>Exécution de l’appel asynchrone

Avant de pouvoir effectuer un appel distant asynchrone, le client doit initialiser le handle asynchrone. Les programmes client et serveur utilisent des pointeurs vers la structure d' [**\_ \_ état asynchrone RPC**](/windows/desktop/api/Rpcasync/ns-rpcasync-rpc_async_state) pour les handles asynchrones.

Chaque appel en suspens doit avoir son propre handle asynchrone unique. Le client crée le descripteur et le passe à la fonction [**RpcAsyncInitializeHandle**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncinitializehandle) . Pour que l’appel se termine correctement, le client doit s’assurer que la mémoire pour le descripteur n’est pas libérée jusqu’à ce qu’il reçoive la réponse asynchrone du serveur. En outre, avant d’effectuer un autre appel sur un handle asynchrone existant, le client doit réinitialiser le descripteur. Si vous ne le faites pas, le stub client lève une exception pendant l’appel. Le client doit également s’assurer que les tampons fournis pour les \[ paramètres [**out**](/windows/desktop/Midl/out-idl) \] et \[ [**dans**](/windows/desktop/Midl/in), les paramètres **out** \] à une procédure distante asynchrone restent alloués jusqu’à ce qu’il ait reçu la réponse du serveur.

Lorsqu’il appelle une procédure distante asynchrone, le client doit sélectionner la méthode qui sera utilisée par la bibliothèque Runtime RPC pour l’informer de la fin de l’appel. Le client peut recevoir cette notification de l’une des manières suivantes :

-   Événement. Le client peut spécifier un événement à déclencher lorsque l’appel est terminé. Pour plus d’informations, consultez [objets d’événement](/windows/desktop/Sync/event-objects).
-   Interrogation. Le client peut appeler [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus)de façon répétée. Si la valeur de retour est différente de l' \_ \_ appel Async RPC S \_ \_ en attente, l’appel est terminé. Cette méthode utilise plus de temps processeur que les autres méthodes décrites ici.
-   APC. Le client peut spécifier un [appel de procédure asynchrone (APC)](/windows/desktop/Sync/asynchronous-procedure-calls) qui est appelé lorsque l’appel est terminé. Pour le prototype de la fonction APC, consultez [**\_ routine RPCNOTIFICATION**](/previous-versions/aa375808(v=vs.80)). L’APC est appelé avec le paramètre d’événement défini sur RpcCallComplete. Pour que les APC soient distribués, le thread client doit se trouver dans un état d’attente averti.

    Si le champ **hThread** du descripteur asynchrone a la valeur 0, les APC sont mis en file d’attente sur le thread qui a effectué l’appel asynchrone. Si la valeur est différente de zéro, les APC sont mis en file d’attente sur le thread spécifié par m.

-   IOC. Le port de terminaison d’e/s est notifié avec les paramètres spécifiés dans le handle asynchrone. Pour plus d’informations, consultez [**CreateIoCompletionPort**](/windows/desktop/FileIO/createiocompletionport).
-   handle de Windows. Un message est publié dans le handle de fenêtre (HWND) spécifié.

Le fragment de code suivant montre les étapes essentielles requises pour initialiser un handle asynchrone et l’utiliser pour effectuer un appel de procédure distante asynchrone.


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



Comme le montre cet exemple, votre programme client peut exécuter des appels de procédure distante synchrone alors qu’un appel de procédure asynchrone est toujours en attente. Ce client crée un objet d’événement pour la bibliothèque Runtime RPC à utiliser pour l’avertir lorsque l’appel asynchrone se termine.

> [!Note]  
> La notification d’achèvement ne sera pas retournée à partir d’une routine RPC asynchrone si une exception RPC est levée lors d’un appel asynchrone.

 

 

 