---
title: Modèle asynchrone
description: la plupart des opérations dans Windows API de Services Web peuvent être effectuées de façon synchrone ou asynchrone.
ms.assetid: d0b3f154-2219-4085-a652-e9aeb126598c
keywords:
- Services Web de modèle asynchrone pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0c5e38dfbc0bc2ed397949da86f9a572a5b1ed5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127295163"
---
# <a name="asynchronous-model"></a>Modèle asynchrone

la plupart des opérations dans Windows API de Services Web peuvent être effectuées de façon synchrone ou asynchrone. Pour appeler une fonction de façon synchrone, transmettez une valeur null pour la structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Pour spécifier qu’une fonction peut être exécutée de façon asynchrone, transmettez un **\_ \_ contexte WS Async** non null à la fonction.

Lorsqu’elle est appelée de façon asynchrone, une fonction peut néanmoins se terminer de façon synchrone ou asynchrone. si la fonction se termine de façon synchrone, elle retourne une valeur qui indique le succès ou l’erreur final, et cette valeur est toujours autre chose que **WS \_ S \_ ASYNC** (consultez [Windows les valeurs de retour des Services Web](windows-web-services-return-values.md)). Une valeur de retour de **WS \_ S \_ Async**, toutefois, indique que la fonction se termine de façon asynchrone. Lorsque la fonction se termine de façon asynchrone, un rappel est appelé pour signaler la fin de l’opération. Ce rappel indique la valeur finale de réussite ou d’erreur. Le rappel n’est pas appelé si l’opération se termine de façon synchrone.

Pour créer un contexte asynchrone, initialisez les champs **callback** et **callbackState** de la structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) . Le champ **callbackState** est utilisé pour spécifier un pointeur vers les données définies par l’utilisateur qui sont passées à la fonction de [**\_ \_ rappel WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) .

L’exemple suivant illustre l’appel d’une fonction de manière asynchrone en passant un pointeur vers une structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) qui contient le rappel et un pointeur vers les données d’État.

``` syntax
HRESULT ExampleAsyncFunction(WS_ASYNC_CONTEXT* asyncContext);
void ExampleAsyncFunction()
{
    // Set up the WS_ASYNC_CONTEXT structure.
    MyState* myState = ...;  \\ Declare a pointer to user-defined data.
    WS_ASYNC_CONTEXT asyncContext;
    asyncContext.callback = MyCallback;  \\ Set the callback.
    asyncContext.callbackState = myState; \\ Set the pointer to the user-defined data.

    // Start the asynchronous operation
    HRESULT hr = SomeFunction(&asyncContext);

    if (hr == WS_S_ASYNC)
    {
        // The operation is completing asynchronously.  The callback is called 
        // when the operation is complete.
    }
    else
    {
        // The operation completed synchronously.  The callback is not called.
    }
}
void CALLBACK MyCallback(HRESULT hr, WS_CALLBACK_MODEL callbackModel, void* callbackState)
{
    MyState* myState = (MyState*)callbackState;

    // The operation completed asynchronously.
}
```

La structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) est utilisée par la fonction asynchrone uniquement pendant la durée de l’appel de fonction (pas pendant la durée de l’opération asynchrone), afin que vous puissiez la déclarer en toute sécurité sur la pile.

Si d’autres paramètres, en plus de la structure de [**\_ \_ contexte WS Async**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) , sont passés à une fonction asynchrone en tant que pointeurs et que la fonction se termine de façon asynchrone, il incombe à l’appelant de conserver les valeurs vers lesquelles ces paramètres sont actifs (non libérés) jusqu’à ce que le rappel asynchrone soit appelé.

Il existe des limitations sur les opérations qu’un rappel peut effectuer. Pour plus d’informations sur les opérations possibles, consultez le [**\_ \_ modèle de rappel WS**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model).

Quand vous implémentez une fonction asynchrone, n’appelez pas le rappel sur le thread qui a appelé la fonction asynchrone avant que la fonction asynchrone soit retournée à l’appelant, ce qui interrompt le modèle asynchrone.

Lors de l’implémentation d’une fonction qui doit exécuter une série d’opérations asynchrones, envisagez d’utiliser la fonction d’assistance [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) .

L' [exemple de fonction asynchrone](asyncmodelexample.md) montre comment implémenter et utiliser des fonctions qui suivent le modèle asynchrone.

Le démarrage d’une opération d’e/s asynchrone consomme des ressources système. Si un nombre suffisant d’opérations d’e/s est démarré, le système peut cesser de répondre. Pour éviter cela, une application doit limiter le nombre d’opérations asynchrones qu’elle démarre.

Le modèle asynchrone utilise les éléments d’API suivants.

| Rappel                                         | Description                                                                                                                           |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_rappel WS asynchrone \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback) | Paramètre de fonction de rappel utilisé avec le modèle asynchrone.                                                                     |
| [**WS \_ Async, \_ fonction**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function) | Utilisé avec [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) pour spécifier la fonction suivante à appeler dans une série d’opérations asynchrones. |



 



| Énumération                                      | Description                                                                                                       |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [**\_modèle de rappel WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model) | Spécifie le comportement de thread d’un rappel (par exemple, [**un \_ \_ rappel WS Async**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)). |



 



| Fonction                                 | Description                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) | Appelle un rappel défini par l’utilisateur qui peut lancer une opération asynchrone et indiquer une fonction qui doit être appelée lorsque l’opération asynchrone est terminée. |



 



| Structure                                          | Description                                                                                                                           |
|----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**\_contexte WS Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)     | Spécifie le rappel asynchrone et un pointeur vers les données définies par l’utilisateur, qui seront passées au rappel asynchrone.            |
| [**fonctionnement de WS \_ Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_operation) | Utilisé avec [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) pour spécifier la fonction suivante à appeler dans une série d’opérations asynchrones. |
| [**\_État WS Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_state)         | Utilisé par [**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute) pour gérer l’état d’une opération asynchrone.                                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemple de fonction asynchrone](asyncmodelexample.md)
</dt> <dt>

[**\_rappel WS asynchrone \_**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
</dt> <dt>

[**\_contexte WS Async \_**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)
</dt> <dt>

[**\_modèle de rappel WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_callback_model)
</dt> <dt>

[**WsAsyncExecute**](/windows/desktop/api/WebServices/nf-webservices-wsasyncexecute)
</dt> </dl>

 

 




