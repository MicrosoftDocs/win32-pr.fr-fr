---
title: Opérations de service côté serveur
description: Cette section décrit les opérations de service côté service.
ms.assetid: d209cf2f-47f5-4025-8af4-1626c867a66a
keywords:
- Services d’exploitation côté serveur, services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c7ad5a327c1cb79278aa562bfaa1753f008a542
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104383299"
---
# <a name="server-side-service-operations"></a><span data-ttu-id="7154a-106">Opérations de service côté serveur</span><span class="sxs-lookup"><span data-stu-id="7154a-106">Server Side Service Operations</span></span>

<span data-ttu-id="7154a-107">Cette section décrit les opérations de service côté service.</span><span class="sxs-lookup"><span data-stu-id="7154a-107">This section describes service side service operations.</span></span>


<span data-ttu-id="7154a-108">Voici la disposition d’une opération de service côté serveur</span><span class="sxs-lookup"><span data-stu-id="7154a-108">The following is the layout of a server side service operation</span></span>

-   <span data-ttu-id="7154a-109">contexte de [ \_ \_ contexte](ws-operation-context.md) de l’opération const WS \* : [contexte](context.md)de l’opération.</span><span class="sxs-lookup"><span data-stu-id="7154a-109">const [WS\_OPERATION\_CONTEXT](ws-operation-context.md)\* context: The operation [context](context.md).</span></span>
-   <span data-ttu-id="7154a-110">Paramètres des opérations de service : paramètres relatifs à l’opération de service.</span><span class="sxs-lookup"><span data-stu-id="7154a-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="7154a-111">const [**WS \_ Async \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) \* asyncContext : contexte Async pour exécuter les opérations de service de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7154a-111">const [**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context)\* asyncContext: Async context for executing the service operations asynchronously.</span></span>
-   <span data-ttu-id="7154a-112">[WS \_ Erreur d’erreur](ws-error.md) \* : objet d’erreur enrichi.</span><span class="sxs-lookup"><span data-stu-id="7154a-112">[WS\_ERROR](ws-error.md)\* error: Rich error object.</span></span>

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

## <a name="fault-and-error-handling"></a><span data-ttu-id="7154a-113">Gestion des erreurs et des erreurs</span><span class="sxs-lookup"><span data-stu-id="7154a-113">Fault And Error Handling</span></span>

<span data-ttu-id="7154a-114">Le côté serveur doit utiliser des erreurs pour envoyer des conditions d’erreur au client.</span><span class="sxs-lookup"><span data-stu-id="7154a-114">The server side should use faults to deliver error conditions to the client.</span></span> <span data-ttu-id="7154a-115">Il peut le faire en retournant un HRESULT ayant échoué et en incorporant l’erreur dans l’objet d’erreur.</span><span class="sxs-lookup"><span data-stu-id="7154a-115">It can do so by returning a failing HRESULT and embedding the fault in the error object.</span></span>

<span data-ttu-id="7154a-116">Si l’erreur n’est pas définie sur l’objet d’erreur et qu’un échec de HRESULT est retourné, l’infrastructure tente à nouveau de remettre une erreur au client.</span><span class="sxs-lookup"><span data-stu-id="7154a-116">If the fault is not set on the error object and a failure HRESULT is returned, the infrastructure will attempt deliver a fault back to client.</span></span> <span data-ttu-id="7154a-117">Le niveau de détail divulgué au client dans ce cas est contrôlé par la propriété de service [**de \_ \_ Divulgation d' \_ Erreurs \_ de la propriété WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) sur l' [hôte de service](service-host.md).</span><span class="sxs-lookup"><span data-stu-id="7154a-117">The level of details disclosed to the client in such a case is controlled by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) service property on the [Service Host](service-host.md).</span></span>

## <a name="call-completion"></a><span data-ttu-id="7154a-118">Fin de l’appel</span><span class="sxs-lookup"><span data-stu-id="7154a-118">Call Completion</span></span>

<span data-ttu-id="7154a-119">Un appel sur une opération de service côté serveur synchrone est considéré comme terminé lorsqu’il a renvoyé le contrôle à l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="7154a-119">A call on a synchronous server side service operation is said to be complete when either it has returned control back to the service host.</span></span> <span data-ttu-id="7154a-120">Pour une opération de service asynchrone, un appel est considéré comme terminé une fois que la notification de rappel est émise par l’implémentation de l’opération de service.</span><span class="sxs-lookup"><span data-stu-id="7154a-120">For an asynchronous service operation a call is considered complete once the callback notification is issued by the service operation implementation.</span></span>

## <a name="call-lifetime"></a><span data-ttu-id="7154a-121">Durée de vie de l’appel</span><span class="sxs-lookup"><span data-stu-id="7154a-121">Call Lifetime</span></span>

<span data-ttu-id="7154a-122">Une attention particulière doit être prise lors de l’implémentation d’une opération de service côté serveur sur sa durée de vie.</span><span class="sxs-lookup"><span data-stu-id="7154a-122">Special care should be taken when implementing a server side service operation about its lifetime.</span></span> <span data-ttu-id="7154a-123">La durée de vie d’un appel peut avoir un impact considérable sur le temps nécessaire à l’arrêt de l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="7154a-123">The lifetime of a call can greatly affect how long the service host takes to shutdown.</span></span>

<span data-ttu-id="7154a-124">Si une opération de service côté serveur est supposée se bloquer en raison d’une opération de liaison d’e/s, il est recommandé d’inscrire un rappel d’annulation de sorte qu’il soit notifié lorsque l’hôte de service est abandonné ou lorsque la connexion sous-jacente est fermée par le client.</span><span class="sxs-lookup"><span data-stu-id="7154a-124">If a server side service operation is expected to block because of some IO bound operation, it is recommended that it registers a cancellation callback such that it is notified if when service host is being aborted, or when the underlying connection is closed by the client.</span></span>

## <a name="server-side-service-operations-and-memory-consideration"></a><span data-ttu-id="7154a-125">Considérations sur la mémoire et les opérations de service côté serveur</span><span class="sxs-lookup"><span data-stu-id="7154a-125">Server side service operations and memory consideration</span></span>

<span data-ttu-id="7154a-126">Si une opération de service doit allouer de la mémoire pour ses paramètres sortants, elle doit utiliser l’objet de [ \_ tas WS](ws-heap.md) disponible dans le contexte de l' [ \_ \_ opération WS](ws-operation-context.md).</span><span class="sxs-lookup"><span data-stu-id="7154a-126">If a service operation needs to allocate memory for its outgoing parameters, it should use [WS\_HEAP](ws-heap.md) object available to it through the [WS\_OPERATION\_CONTEXT](ws-operation-context.md).</span></span>

<span data-ttu-id="7154a-127">Exemple : opération de service et \_ tas WS</span><span class="sxs-lookup"><span data-stu-id="7154a-127">Example: Service Operation and WS\_HEAP</span></span>

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

## <a name="return-values"></a><span data-ttu-id="7154a-128">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7154a-128">Return Values</span></span>

-   <span data-ttu-id="7154a-129">WS \_ S \_ Async : l’appel sera terminé Async.</span><span class="sxs-lookup"><span data-stu-id="7154a-129">WS\_S\_ASYNC: Call will be completed async.</span></span>
-   <span data-ttu-id="7154a-130">Fin de WS \_ S \_ : l’appel s’est terminé avec succès, le serveur n’attend pas de [ \_ message WS](ws-message.md) du client au-delà de cet appel.</span><span class="sxs-lookup"><span data-stu-id="7154a-130">WS\_S\_END: Call completed successfully, the server is not expecting any [WS\_MESSAGE](ws-message.md) from the client beyond this call.</span></span> <span data-ttu-id="7154a-131">Si un autre \_ message WS est présent dans, le serveur doit abandonner le canal.</span><span class="sxs-lookup"><span data-stu-id="7154a-131">If another WS\_MESSAGE comes in then the server should abort the channel.</span></span>
-   <span data-ttu-id="7154a-132">NOERROR/tous les autres HRESULT de réussite : appel terminé avec succès.</span><span class="sxs-lookup"><span data-stu-id="7154a-132">NOERROR/All other success HRESULTS: Call completed successfully.</span></span> <span data-ttu-id="7154a-133">Notez qu’il est recommandé que l’application ne retourne pas HRESULT, autre que la réussite de l’opération de service.</span><span class="sxs-lookup"><span data-stu-id="7154a-133">Note that it is recommended that the application should not return HRESULT other then NOERROR for successful completion of service operation.</span></span>
-   <span data-ttu-id="7154a-134">Tout avec un échec HRESULT : une erreur est renvoyée au client si l’une d’elles est disponible dans WS \_ Error.</span><span class="sxs-lookup"><span data-stu-id="7154a-134">Everything with a failure HRESULT: A fault is send back to the client if one is available in WS\_ERROR.</span></span> <span data-ttu-id="7154a-135">Dans le cas contraire, une erreur générique est renvoyée au client.</span><span class="sxs-lookup"><span data-stu-id="7154a-135">Otherwise a generic fault is send back to the client.</span></span> <span data-ttu-id="7154a-136">Consultez la discussion d’erreur ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="7154a-136">See fault discussion above.</span></span>

<span data-ttu-id="7154a-137">Consultez la section annulation de l' [appel](call-cancellation.md).</span><span class="sxs-lookup"><span data-stu-id="7154a-137">See, [Call cancellation](call-cancellation.md).</span></span>

 

 




