---
title: Opérations de service côté client
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: En savoir plus sur les opérations de service côté client
keywords:
- Services Web des opérations de service côté client pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73ccbb0c742d0be09570b0959c9c1a663d7f4d0f054cc88070d842ac6d954ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657299"
---
# <a name="client-side-service-operations"></a>Opérations de service côté client

Voici la disposition d’une opération de service côté client :

-   [WS \_ ServiceProxy \_ proxy de service](ws-service-proxy.md) \* : [service](service-proxy.md) proxy pour l’appel.
-   [WS \_ ](ws-heap.md)Tas \* du tas : tas requis utilisé pour la sérialisation et la désérialisation du corps du [ \_ message WS](ws-message.md).
-   Paramètres des opérations de service : paramètres relatifs à l’opération de service.
-   [**Appelez les propriétés et leur nombre**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): un tableau de propriétés d’appel.
-   Nombre de propriétés d' [**appel**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : nombre de propriétés d’appel.
-   [**WS \_ AsyncContext \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asynchrone : contexte Async pour l’exécution de l’appel de manière asynchrone.
-   [WS \_ Erreur d’erreur :](ws-error.md) objet d’erreur enrichi.


### <a name="signature-for-client-side-service-operations"></a>Signature pour les opérations de service côté client

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a>Considérations relatives à la mémoire pour les opérations de service côté client

L’appel à l’opération de service prend [un \_ segment WS](ws-heap.md) \* comme paramètre. Il s’agit d’un paramètre obligatoire utilisé pour la sérialisation/désérialisation des corps de message aux paramètres.

L’application doit appeler [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) , que l’appel ait réussi ou non. Si l’appel a réussi et qu’il a des paramètres sortants, l’application doit appeler **WsResetHeap** immédiatement après avoir terminé avec les paramètres sortants.

L’application doit allouer de la mémoire pour les paramètres in et Out avec [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc). Le proxy de service peut être amené à les réallouer, de sorte que les pointeurs fournis seront remplacés. Si vous tentez de libérer de la mémoire, cela entraînera l’arrêt de l’application.

### <a name="client-side-service-operation-and-ws_heap"></a>Opération de service côté client et \_ tas WS

``` syntax
HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessReceipt(orderReceipt);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderMemo, NULL, 0, NULL, error);
if(FAILED(hr))
    goto error;
hr = ProcessMemo(orderMemo);
WsResetHeap(heap);
if(FAILED(hr))
    goto error;
```

### <a name="error-parameter"></a>Paramètre d’erreur

L’application doit toujours passer le paramètre d’erreur à :

-   Obtenir des informations détaillées sur l’erreur si une défaillance se produit pendant l’appel de l’opération de service.
-   Obtient l’objet d’erreur si le service a retourné une erreur. L’erreur se trouve dans l’objet Error. dans ce cas, la valeur **HRESULT** retournée par l’opération de service est l' **erreur de point de terminaison WS \_ E \_ \_ \_ received** (voir [Windows les valeurs de retour des Services Web](windows-web-services-return-values.md)).

### <a name="call-properties-for-client-side-service-operations"></a>Propriétés d’appel pour les opérations de service côté client

Les propriétés d’appel permettent à une application de spécifier des paramètres personnalisés pour un appel donné. Actuellement, une seule propriété d’appel est disponible avec le modèle de service, ID d’appel de la [**\_ \_ propriété \_ \_ WS Call**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).

``` syntax
WS_CALL_PROPERTY callProperties[1] = {0};
callProperties[0].id = WS_CALL_PROPERTY_CALL_ID;
callProperties[0].value = 5;

HRESULT hr = IProcessOrder_ProcessOrder(serviceProxy, heap, orderNumber, &orderReceipt,  callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;
//:
//:
hr = IProcessOrder_CompleteOrder(serviceProxy, heap, orderNumber, &orderReceipt, callProperties, WsCountOf(callProperties), NULL, error);
if(FAILED(hr))
    goto error;

//:
//:
//:
// On a separate thread 
// In this case both the calls belong to call group 5, and will abandon as a result of the call to WsAbandonCall. 
hr = WsAbandonCall(serviceProxy, 5, error);
```

### <a name="abandoning-a-call"></a>Abandon d’un appel

Il est souvent souhaitable d’abandonner les résultats d’un appel afin de céder le contrôle à l’application, de sorte que l’exécution de l’appel réel soit gérée par l’infrastructure. Le proxy de service fournit cette fonctionnalité par le biais de [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).

Notez que le contrôle à l’appelant peut ne pas être remis immédiatement, mais la seule garantie que le runtime du proxy de service indique est qu’il n’attendait pas la fin d’une opération de liaison d’e/s avant de redonner le contrôle à l’appelant.

Les appels effectués sur une opération de service côté client peuvent être abandonnés au moyen d’un appel à [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall). Il prend un proxy de service et un ID d’appel. Un ID d’appel est fourni dans le cadre des propriétés d’appel d’une opération de service.

Si l’ID d’appel est 0, le proxy de service abandonne tous les appels en attente sur cette instance.

### <a name="call-timeouts"></a>Délais d’appel

Par défaut, un proxy de service a un délai d’expiration de 30 secondes pour chaque appel. Le délai d’attente d’un appel peut être modifié par la propriété du proxy du service de proxy d' [**\_ \_ \_ appel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) de la propriété WS proxy lors de la création d’un proxy de service via [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).

Une fois le délai d’attente atteint, l’appel est abandonné.

### <a name="return-values"></a>Valeurs de retour

Toutes les valeurs **HRESULT** de réussite doivent être traitées comme des succès, et toutes les valeurs d’échec doivent être traitées comme des échecs. Voici quelques-unes des valeurs **HRESULT** qu’une application peut attendre :

-   **WS \_ S \_ Async**: l’appel sera effectué de façon asynchrone.
-   ERREUR : l’appel a été effectué avec succès.
-   **WS \_ E \_ opération \_ abandonnée**: l’appel a été abandonné. L’objet Error contient la raison de l’abandon.
-   **WS \_ E \_ \_ opération non valide**: le proxy de service n’est pas dans un état approprié pour effectuer un appel, vérifiez l’état du proxy de service pour déterminer l’état du proxy de service.

pour obtenir la liste complète des valeurs de retour, consultez [Windows les valeurs renvoyées par les Services Web](windows-web-services-return-values.md).

### <a name="code-examples"></a>Exemples de code

Pour obtenir des exemples de code, consultez les rubriques suivantes :

-   [CallAbandonExample](callabandonexample.md)
-   [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




