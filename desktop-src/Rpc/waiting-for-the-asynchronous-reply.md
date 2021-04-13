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
# <a name="waiting-for-the-asynchronous-reply"></a>En attente de la réponse asynchrone

Ce que fait le client lorsqu’il attend d’être informé d’une réponse du serveur dépend du mécanisme de notification qu’il sélectionne.

Si le client utilise un événement pour la notification, il appelle généralement la fonction [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) ou la fonction [**WaitForSingleObjectEx**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex) . Le client entre dans un État bloqué lorsqu’il appelle l’une de ces fonctions. Cela est efficace, car le client n’utilise pas de cycles d’exécution du processeur pendant qu’il est bloqué.

Lorsqu’il utilise l’interrogation pour attendre ses résultats, le programme client entre dans une boucle qui appelle à plusieurs reprises la fonction [**RpcAsyncGetCallStatus**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasyncgetcallstatus). Il s’agit d’une méthode efficace pour attendre si votre programme client effectue d’autres traitements dans la boucle d’interrogation. Par exemple, il peut préparer des données en petits segments pour un appel de procédure distante asynchrone suivant. Une fois chaque segment terminé, votre client peut interroger l’appel de procédure distante asynchrone en suspens pour déterminer s’il est terminé.

Votre programme client peut fournir un appel de procédure asynchrone (APC), qui est un type de fonction de rappel que la bibliothèque Runtime RPC appellera lorsque l’appel de procédure distante asynchrone se termine. Votre programme client doit être dans un état d’attente averti. Cela signifie généralement que le client appelle une fonction d’API Windows pour se placer dans un État bloqué. Pour plus d’informations, consultez [appels de procédures asynchrones](/windows/desktop/Sync/asynchronous-procedure-calls).

> [!Note]  
> La notification d’achèvement ne sera pas retournée à partir d’une routine RPC asynchrone si une exception RPC est levée lors d’un appel asynchrone.

 

Si votre programme client utilise un port de terminaison d’e/s pour recevoir la notification d’achèvement, il doit appeler la fonction [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) . Dans ce cas, il peut attendre indéfiniment une réponse ou continuer à effectuer d’autres traitements. S’il effectue un autre traitement pendant qu’il attend une réponse, il doit interroger le port de terminaison avec la fonction **GetQueuedCompletionStatus** . Dans ce cas, elle doit généralement définir le *dwMilliseconds* sur zéro. Cela entraîne le retour immédiat de **GetQueuedCompletionStatus** , même si l’appel asynchrone n’est pas terminé.

Les programmes clients peuvent également recevoir des notifications de fin d’exécution par le biais de leurs files d’attente de messages de fenêtre. Dans ce cas, ils traitent simplement le message d’achèvement comme tout message Windows.

Dans une application multithread, un appel asynchrone peut être annulé par le client uniquement après que le thread à l’origine de l’appel a été retourné avec succès à partir de l’appel. Cela garantit que l’appel n’est pas annulé de manière asynchrone par un autre thread après l’échec d’un appel synchrone. Comme pratique standard, un appel asynchrone qui échoue de façon synchrone ne doit pas être annulé de manière asynchrone. L’application cliente doit observer ce comportement si des appels peuvent être émis et annulés sur des threads différents. De même, après l’annulation de l’appel, le code client doit attendre la notification d’achèvement et terminer l’appel. La fonction [**RpcAsyncCancelCall**](/windows/desktop/api/Rpcasync/nf-rpcasync-rpcasynccancelcall) touche simplement la notification d’achèvement. ce n’est pas un substitut pour terminer l’appel.

Le fragment de code suivant montre comment un programme client peut utiliser un événement pour attendre une réponse asynchrone.


```C++
// This code fragment assumes that Async is a valid asynchronous
// RPC handle.
if (WaitForSingleObject(Async.u.hEvent, INFINITE) == WAIT_FAILED)
{
    RpcRaiseException(APP_ERROR);
}
```



Les programmes clients qui utilisent un APC pour recevoir la notification d’une réponse asynchrone se placent généralement dans un État bloqué. Le fragment de code suivant illustre cela.


```C++
if (SleepEx(INFINITE, TRUE) != WAIT_IO_COMPLETION)
{
    RpcRaiseException(APP_ERROR);
}
```



Dans ce cas, le programme client passe en mode veille, en consommant aucun cycle de processeur, jusqu’à ce que la bibliothèque Runtime RPC appelle l’APC (non affiché).

L’exemple suivant illustre un client qui utilise un port de terminaison d’e/s pour attendre une réponse asynchrone.


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



Dans l’exemple précédent, l’appel à [**GetQueuedCompletionStatus**](/windows/desktop/api/ioapiset/nf-ioapiset-getqueuedcompletionstatus) attend indéfiniment jusqu’à ce que l’appel de procédure distante asynchrone se termine.

Un piège potentiel se produit lors de l’écriture d’applications multithread. Si un thread appelle un appel de procédure distante et se termine avant de recevoir une notification indiquant que l’envoi est terminé, l’appel de procédure distante peut échouer et le stub client peut fermer la connexion au serveur. Par conséquent, les threads qui appellent une procédure distante ne doivent pas se terminer avant que l’appel soit terminé ou annulé lorsque le comportement n’est pas souhaitable.

 

 