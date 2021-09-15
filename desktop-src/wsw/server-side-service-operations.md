---
title: Opérations de service côté serveur
description: Cette section décrit les opérations de service côté service.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Services Web des opérations de service côté serveur pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525069"
---
# <a name="server-side-service-operations"></a>Opérations de service côté serveur

Cette section décrit les opérations de service côté service.


Voici la disposition d’une opération de service côté serveur

-   contexte de [ \_ \_ contexte](ws-operation-context.md) de l’opération const WS \* : [contexte](context.md)de l’opération.
-   Paramètres des opérations de service : paramètres relatifs à l’opération de service.
-   const [**WS \_ Async \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext : contexte Async pour exécuter les opérations de service de façon asynchrone.
-   [WS \_ Erreur d’erreur](ws-error.md) \* : objet d’erreur enrichi.

``` syntax
HRESULT CALLBACK Add(const WS_OPERATION_CONTEXT* context, 
                     ULONG a, ULONG b, ULONG* result, 
                     const WS_ASYNC_CONTEXT* asyncContext, 
                     WS_ERROR* error)
{
    *result = a +b;
    return NOERROR;
}
```

## <a name="fault-and-error-handling"></a>Gestion des erreurs et des erreurs

Le côté serveur doit utiliser des erreurs pour envoyer des conditions d’erreur au client. Il peut le faire en retournant un HRESULT ayant échoué et en incorporant l’erreur dans l’objet d’erreur.

Si l’erreur n’est pas définie sur l’objet d’erreur et qu’un échec de HRESULT est retourné, l’infrastructure tente à nouveau de remettre une erreur au client. Le niveau de détail divulgué au client dans ce cas est contrôlé par la propriété de service [**de \_ \_ Divulgation d' \_ Erreurs \_ de la propriété WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) sur l' [hôte de service](service-host.md).

## <a name="call-completion"></a>Fin de l’appel

Un appel sur une opération de service côté serveur synchrone est considéré comme terminé lorsqu’il a renvoyé le contrôle à l’hôte de service. Pour une opération de service asynchrone, un appel est considéré comme terminé une fois que la notification de rappel est émise par l’implémentation de l’opération de service.

## <a name="call-lifetime"></a>Durée de vie de l’appel

Une attention particulière doit être prise lors de l’implémentation d’une opération de service côté serveur sur sa durée de vie. La durée de vie d’un appel peut avoir un impact considérable sur le temps nécessaire à l’arrêt de l’hôte de service.

Si une opération de service côté serveur est supposée se bloquer en raison d’une opération de liaison d’e/s, il est recommandé d’inscrire un rappel d’annulation de sorte qu’il soit notifié lorsque l’hôte de service est abandonné ou lorsque la connexion sous-jacente est fermée par le client.

## <a name="server-side-service-operations-and-memory-consideration"></a>Considérations sur la mémoire et les opérations de service côté serveur

Si une opération de service doit allouer de la mémoire pour ses paramètres sortants, elle doit utiliser l’objet de [ \_ tas WS](ws-heap.md) disponible dans le contexte de l' [ \_ \_ opération WS](ws-operation-context.md).

Exemple : opération de service et \_ tas WS

``` syntax
HRESULT CALLBACK ProcessOrder (const WS_OPERATION_CONTEXT* context, const ULONG orderNumber, OrderReceipt** orderReceipt, const WS_ASYNC_CONTEXT* asyncContext, WS_ERROR* error)
{
    WS_HEAP* heap;
    HRESULT hr = WsGetOperationContextProperty (context, WS_OPERATION_CONTEXT_PROPERTY_HEAP, &heap, sizeof(heap), NULL, error);
    if (FAILED(hr))
        return hr;
    hr = WsAlloc(heap, sizeof (OrderReceipt), orderReceipt, error);
    if (FAILED(hr))
        return hr;
    hr = FillInReceipt(*orderReceipt);
    if (FAILED(hr))
        return hr;
    return NOERROR;
} 
```

## <a name="return-values"></a>Valeurs de retour

-   WS \_ S \_ Async : l’appel sera terminé Async.
-   Fin de WS \_ S \_ : l’appel s’est terminé avec succès, le serveur n’attend pas de [ \_ message WS](ws-message.md) du client au-delà de cet appel. Si un autre \_ message WS est présent dans, le serveur doit abandonner le canal.
-   NOERROR/tous les autres HRESULT de réussite : appel terminé avec succès. Notez qu’il est recommandé que l’application ne retourne pas HRESULT, autre que la réussite de l’opération de service.
-   Tout avec un échec HRESULT : une erreur est renvoyée au client si l’une d’elles est disponible dans WS \_ Error. Dans le cas contraire, une erreur générique est renvoyée au client. Consultez la discussion d’erreur ci-dessus.

Consultez la section annulation de l' [appel](call-cancellation.md).

 

 




