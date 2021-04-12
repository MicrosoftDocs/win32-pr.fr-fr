---
title: Opérations de service côté client
ms.assetid: 9d6e2441-91de-4108-b1c4-282fbca5fe7c
description: En savoir plus sur les opérations de service côté client
keywords:
- Service côté client services Web pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4cd00bfbd832db12a722363bf5b1af8f7298345
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203788"
---
# <a name="client-side-service-operations"></a><span data-ttu-id="5a1bd-106">Opérations de service côté client</span><span class="sxs-lookup"><span data-stu-id="5a1bd-106">Client-side Service Operations</span></span>

<span data-ttu-id="5a1bd-107">Voici la disposition d’une opération de service côté client :</span><span class="sxs-lookup"><span data-stu-id="5a1bd-107">The following is the layout of a client-side service operation:</span></span>

-   <span data-ttu-id="5a1bd-108">[WS \_ ServiceProxy \_ proxy de service](ws-service-proxy.md) \* : [service](service-proxy.md) proxy pour l’appel.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-108">[WS\_SERVICE\_PROXY](ws-service-proxy.md)\* serviceProxy: The [service proxy](service-proxy.md) for the call.</span></span>
-   <span data-ttu-id="5a1bd-109">[WS \_ ](ws-heap.md)Tas \* du tas : tas requis utilisé pour la sérialisation et la désérialisation du corps du [ \_ message WS](ws-message.md).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-109">[WS\_HEAP](ws-heap.md)\* heap: A required heap used for body serialization and deserialization of the [WS\_MESSAGE](ws-message.md).</span></span>
-   <span data-ttu-id="5a1bd-110">Paramètres des opérations de service : paramètres relatifs à l’opération de service.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-110">Service Operations Parameters: Parameters pertaining to the service operation.</span></span>
-   <span data-ttu-id="5a1bd-111">[**Appelez les propriétés et leur nombre**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): un tableau de propriétés d’appel.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-111">[**Call Properties and their count**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property): An array of call properties.</span></span>
-   <span data-ttu-id="5a1bd-112">Nombre de propriétés d' [**appel**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) : nombre de propriétés d’appel.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-112">[**Call**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property) property count: The count of call properties.</span></span>
-   <span data-ttu-id="5a1bd-113">[**WS \_ AsyncContext \_ Context**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asynchrone : contexte Async pour l’exécution de l’appel de manière asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-113">[**WS\_ASYNC\_CONTEXT**](/windows/desktop/api/WebServices/ns-webservices-ws_async_context) asyncContext: Async context for executing the call asynchronously.</span></span>
-   <span data-ttu-id="5a1bd-114">[WS \_ Erreur d’erreur :](ws-error.md) objet d’erreur enrichi.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-114">[WS\_ERROR](ws-error.md) error: Rich error object.</span></span>


### <a name="signature-for-client-side-service-operations"></a><span data-ttu-id="5a1bd-115">Signature pour les opérations de service côté client</span><span class="sxs-lookup"><span data-stu-id="5a1bd-115">Signature for Client-side Service Operations</span></span>

``` syntax
typedef HRESULT(CALLBACK *ICalculator_Add)(WS_SERVICE_PROXY* serviceProxy, 
                                           WS_HEAP* heap, 
                                           ULONG a, ULONG b, ULONG* result, 
                                           const WS_CALL_PROPERTY* callProperties, 
                                           const ULONG callPropertyCount, 
                                           const WS_ASYNC_CONTEXT* asyncContext, 
                                           WS_ERROR* error);
```

### <a name="memory-considerations-for-client-side-service-operations"></a><span data-ttu-id="5a1bd-116">Considérations relatives à la mémoire pour les opérations de service côté client</span><span class="sxs-lookup"><span data-stu-id="5a1bd-116">Memory Considerations for Client-side Service Operations</span></span>

<span data-ttu-id="5a1bd-117">L’appel à l’opération de service prend [un \_ segment WS](ws-heap.md) \* comme paramètre.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-117">The call to the service operation takes a [WS\_HEAP](ws-heap.md)\* as parameter.</span></span> <span data-ttu-id="5a1bd-118">Il s’agit d’un paramètre obligatoire utilisé pour la sérialisation/désérialisation des corps de message aux paramètres.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-118">This is a required parameter used for serialization/deserialization of message bodies to parameters.</span></span>

<span data-ttu-id="5a1bd-119">L’application doit appeler [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) , que l’appel ait réussi ou non.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-119">The application must call [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) whether the call succeeded or not.</span></span> <span data-ttu-id="5a1bd-120">Si l’appel a réussi et qu’il a des paramètres sortants, l’application doit appeler **WsResetHeap** immédiatement après avoir terminé avec les paramètres sortants.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-120">If the call succeeded and it has outgoing parameters, the application should call **WsResetHeap** immediately after it is finished with the outgoing parameters.</span></span>

<span data-ttu-id="5a1bd-121">L’application doit allouer de la mémoire pour les paramètres in et Out avec [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-121">The application should allocate memory for in and out parameters with [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc).</span></span> <span data-ttu-id="5a1bd-122">Le proxy de service peut être amené à les réallouer, de sorte que les pointeurs fournis seront remplacés.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-122">The service proxy may need to reallocate them so provided pointers will be overwritten.</span></span> <span data-ttu-id="5a1bd-123">Si vous tentez de libérer de la mémoire, cela entraînera l’arrêt de l’application.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-123">An attempt to free such memory will cause the application to crash.</span></span>

### <a name="client-side-service-operation-and-ws_heap"></a><span data-ttu-id="5a1bd-124">Opération de service côté client et \_ tas WS</span><span class="sxs-lookup"><span data-stu-id="5a1bd-124">Client-side Service Operation and WS\_HEAP</span></span>

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

### <a name="error-parameter"></a><span data-ttu-id="5a1bd-125">Paramètre d’erreur</span><span class="sxs-lookup"><span data-stu-id="5a1bd-125">Error parameter</span></span>

<span data-ttu-id="5a1bd-126">L’application doit toujours passer le paramètre d’erreur à :</span><span class="sxs-lookup"><span data-stu-id="5a1bd-126">The application should always pass in the error parameter to:</span></span>

-   <span data-ttu-id="5a1bd-127">Obtenir des informations détaillées sur l’erreur si une défaillance se produit pendant l’appel de l’opération de service.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-127">Get rich error information if a failure occurs during the service operation call.</span></span>
-   <span data-ttu-id="5a1bd-128">Obtient l’objet d’erreur si le service a retourné une erreur.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-128">Get the fault object if the service returned back a fault.</span></span> <span data-ttu-id="5a1bd-129">L’erreur se trouve dans l’objet Error.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-129">The fault is contained in the error object.</span></span> <span data-ttu-id="5a1bd-130">Dans ce cas, la valeur **HRESULT** retournée par l’opération de service est **erreur de point de terminaison WS \_ E \_ \_ \_ received** (voir les [valeurs de retour des services Web Windows](windows-web-services-return-values.md)).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-130">In this case, the **HRESULT** value returned from the service operation is **WS\_E\_ENDPOINT\_FAULT\_RECEIVED** (see [Windows Web Services Return Values](windows-web-services-return-values.md)).</span></span>

### <a name="call-properties-for-client-side-service-operations"></a><span data-ttu-id="5a1bd-131">Propriétés d’appel pour les opérations de service côté client</span><span class="sxs-lookup"><span data-stu-id="5a1bd-131">Call Properties for Client-side Service Operations</span></span>

<span data-ttu-id="5a1bd-132">Les propriétés d’appel permettent à une application de spécifier des paramètres personnalisés pour un appel donné.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-132">Call properties allow an application to specify custom settings for a given call.</span></span> <span data-ttu-id="5a1bd-133">Actuellement, une seule propriété d’appel est disponible avec le modèle de service, ID d’appel de la [**\_ \_ propriété \_ \_ WS Call**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-133">Currently, only one call property is available with the service model, [**WS\_CALL\_PROPERTY\_CALL\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id).</span></span>

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

### <a name="abandoning-a-call"></a><span data-ttu-id="5a1bd-134">Abandon d’un appel</span><span class="sxs-lookup"><span data-stu-id="5a1bd-134">Abandoning a Call</span></span>

<span data-ttu-id="5a1bd-135">Il est souvent souhaitable d’abandonner les résultats d’un appel afin de céder le contrôle à l’application, de sorte que l’exécution de l’appel réel soit gérée par l’infrastructure.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-135">It is often desirable to abandon the results of a call in order to relinquish the control back to the application, such that the actual call completion is handled by the infrastructure.</span></span> <span data-ttu-id="5a1bd-136">Le proxy de service fournit cette fonctionnalité par le biais de [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-136">Service proxy provides this facility through [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span>

<span data-ttu-id="5a1bd-137">Notez que le contrôle à l’appelant peut ne pas être remis immédiatement, mais la seule garantie que le runtime du proxy de service indique est qu’il n’attendait pas la fin d’une opération de liaison d’e/s avant de redonner le contrôle à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-137">Note that the control to the caller may not be given back immediately, the only guarantee that the service proxy runtime gives is that it would not wait for any I/O bound operation to complete before it gives control back to the caller.</span></span>

<span data-ttu-id="5a1bd-138">Les appels effectués sur une opération de service côté client peuvent être abandonnés au moyen d’un appel à [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-138">Calls on a client side service operation can be abandoned by means of a call to [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall).</span></span> <span data-ttu-id="5a1bd-139">Il prend un proxy de service et un ID d’appel. Un ID d’appel est fourni dans le cadre des propriétés d’appel d’une opération de service.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-139">It takes a service proxy and a call id. A call Id is given as part of a call properties on a service operation.</span></span>

<span data-ttu-id="5a1bd-140">Si l’ID d’appel est 0, le proxy de service abandonne tous les appels en attente sur cette instance.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-140">If the call Id is 0, then the service proxy will abandon all pending calls at that instance.</span></span>

### <a name="call-timeouts"></a><span data-ttu-id="5a1bd-141">Délais d’appel</span><span class="sxs-lookup"><span data-stu-id="5a1bd-141">Call Timeouts</span></span>

<span data-ttu-id="5a1bd-142">Par défaut, un proxy de service a un délai d’expiration de 30 secondes pour chaque appel.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-142">By default a service proxy has a 30 second timeout for every call.</span></span> <span data-ttu-id="5a1bd-143">Le délai d’attente d’un appel peut être modifié par la propriété du proxy du service de proxy d' [**\_ \_ \_ appel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) de la propriété WS proxy lors de la création d’un proxy de service via [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-143">The timeout on a call can be changed by [**WS\_PROXY\_PROPERTY\_CALL\_TIMEOUT**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) service proxy property when creating a service proxy through [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy).</span></span>

<span data-ttu-id="5a1bd-144">Une fois le délai d’attente atteint, l’appel est abandonné.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-144">After a timeout is reached, the call is abandoned.</span></span>

### <a name="return-values"></a><span data-ttu-id="5a1bd-145">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="5a1bd-145">Return Values</span></span>

<span data-ttu-id="5a1bd-146">Toutes les valeurs **HRESULT** de réussite doivent être traitées comme des succès, et toutes les valeurs d’échec doivent être traitées comme des échecs.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-146">All success **HRESULT** values must be treated as success, and all failure values must be treated as failures.</span></span> <span data-ttu-id="5a1bd-147">Voici quelques-unes des valeurs **HRESULT** qu’une application peut attendre :</span><span class="sxs-lookup"><span data-stu-id="5a1bd-147">The following are some of the **HRESULT** values that an application can expect:</span></span>

-   <span data-ttu-id="5a1bd-148">**WS \_ S \_ Async**: l’appel sera effectué de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-148">**WS\_S\_ASYNC**: Call will be completed asynchronously.</span></span>
-   <span data-ttu-id="5a1bd-149">ERREUR : l’appel a été effectué avec succès.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-149">NOERROR: Call completed successfully.</span></span>
-   <span data-ttu-id="5a1bd-150">**WS \_ E \_ opération \_ abandonnée**: l’appel a été abandonné.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-150">**WS\_E\_OPERATION\_ABANDONED**: The call has been abandoned.</span></span> <span data-ttu-id="5a1bd-151">L’objet Error contient la raison de l’abandon.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-151">The error object contains the reason for abandon.</span></span>
-   <span data-ttu-id="5a1bd-152">**WS \_ E \_ \_ opération non valide**: le proxy de service n’est pas dans un état approprié pour effectuer un appel, vérifiez l’état du proxy de service pour déterminer l’état du proxy de service.</span><span class="sxs-lookup"><span data-stu-id="5a1bd-152">**WS\_E\_INVALID\_OPERATION**: The service proxy is not in an appropriate state to make a call, check the service proxy state to figure out the state of the service proxy.</span></span>

<span data-ttu-id="5a1bd-153">Pour obtenir la liste complète des valeurs de retour, consultez [valeurs de retour des services Web Windows](windows-web-services-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="5a1bd-153">For a complete list of return values, see [Windows Web Services Return Values](windows-web-services-return-values.md).</span></span>

### <a name="code-examples"></a><span data-ttu-id="5a1bd-154">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="5a1bd-154">Code Examples</span></span>

<span data-ttu-id="5a1bd-155">Pour obtenir des exemples de code, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="5a1bd-155">For code examples, see the following:</span></span>

-   [<span data-ttu-id="5a1bd-156">CallAbandonExample</span><span class="sxs-lookup"><span data-stu-id="5a1bd-156">CallAbandonExample</span></span>](callabandonexample.md)
-   [<span data-ttu-id="5a1bd-157">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="5a1bd-157">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)

 

 




