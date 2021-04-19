---
title: Proxy de service
description: Un proxy de service est le proxy côté client pour un service.
ms.assetid: e1a5bf5e-dbc1-43e3-981b-7db4caa08bdc
keywords:
- Services Web proxy de service pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac82509fa155084cbb4ca3e6b9437728c6f853a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "106527032"
---
# <a name="service-proxy"></a><span data-ttu-id="cd82f-106">Proxy de service</span><span class="sxs-lookup"><span data-stu-id="cd82f-106">Service Proxy</span></span>

<span data-ttu-id="cd82f-107">Un proxy de service est le proxy côté client pour un service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-107">A service proxy is the client side proxy for a service.</span></span> <span data-ttu-id="cd82f-108">Le proxy de service permet aux applications d’envoyer et de recevoir des [messages](message.md) sur un [canal](channel.md) en tant qu’appels de méthode.</span><span class="sxs-lookup"><span data-stu-id="cd82f-108">The service proxy enables applications to send and receive [messages](message.md) over a [channel](channel.md) as method calls.</span></span>

<span data-ttu-id="cd82f-109">Les proxys de service sont créés en fonction des besoins, ouverts, utilisés pour appeler un service et fermés quand vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="cd82f-109">Service proxies are created as needed, opened, used to call a service, and closed when no longer needed.</span></span> <span data-ttu-id="cd82f-110">Une application peut également réutiliser un proxy de service pour se connecter à plusieurs reprises au même service sans les dépenses de temps et les ressources requises pour initialiser un proxy de service plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="cd82f-110">Alternatively, an application may reuse a service proxy to connect repeatedly to the same service without the expenditure of time and resources required for initialising a service proxy more than once.</span></span> <span data-ttu-id="cd82f-111">Le diagramme suivant illustre le déroulement des États possibles du proxy de service et des appels de fonction ou des événements qui mènent d’un État à un autre.</span><span class="sxs-lookup"><span data-stu-id="cd82f-111">The following diagram illustrates the flow of the possible states of the service proxy and the function calls or events that lead from one state to another.</span></span>

![Diagramme montrant les États du proxy de service et les appels de fonction ou les événements qui conduisent d’un État à un autre.](images/serviceproxystates.png)

<span data-ttu-id="cd82f-113">Ces États du proxy de service sont énumérés dans l’énumération de l' [**\_ État du \_ proxy \_ WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .</span><span class="sxs-lookup"><span data-stu-id="cd82f-113">These service proxy states are enumerated in the [**WS\_SERVICE\_PROXY\_STATE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) enumeration.</span></span>

<span data-ttu-id="cd82f-114">Comme le montre le diagramme ci-dessus et le code suivant, un proxy de service est créé par un appel à la fonction [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="cd82f-114">As the preceding diagram and the following code illustrate, a service proxy is created by a call to the [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) function.</span></span> <span data-ttu-id="cd82f-115">En tant que paramètres pour cet appel, WWSAPI fournit les énumérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd82f-115">As parameters for this call, WWSAPI provides the following enumerations:</span></span>

-   [<span data-ttu-id="cd82f-116">**\_type de canal WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-116">**WS\_CHANNEL\_TYPE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [<span data-ttu-id="cd82f-117">**\_liaison WS Channel \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-117">**WS\_CHANNEL\_BINDING**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

<span data-ttu-id="cd82f-118">Il accepte également les paramètres facultatifs à l’aide des types de données suivants :</span><span class="sxs-lookup"><span data-stu-id="cd82f-118">It also accepts optional parameters using the following data types:</span></span>

-   [<span data-ttu-id="cd82f-119">**\_ID de \_ propriété du proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-119">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [<span data-ttu-id="cd82f-120">**Description de la sécurité de WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-120">**WS\_SECURITY\_DESCRIPTION**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

<span data-ttu-id="cd82f-121">Lorsque le proxy de service a été créé, la fonction **WsCreateServiceProxy** retourne une référence au proxy de service, à [WS \_ service \_ proxy](ws-service-proxy.md), via un paramètre out.</span><span class="sxs-lookup"><span data-stu-id="cd82f-121">When the service proxy has been created, the **WsCreateServiceProxy** function returns a reference to the service proxy, [WS\_SERVICE\_PROXY](ws-service-proxy.md), through an out parameter.</span></span>

``` syntax
WS_SERVICE_PROXY* serviceProxy = NULL;
hr = WsCreateServiceProxy (
    WS_TCP_CHANNEL_BINDING, 
    WS_CHANNEL_TYPE_DUPLEX_SESSION, 
    NULL, 
    NULL, 
    0, 
    NULL,
    0,
    &serviceProxy, 
    error);
```

<span data-ttu-id="cd82f-122">Lorsque le proxy de service a été créé, l’application peut ouvrir le proxy de service pour la communication avec un service en appelant la fonction [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , en passant une structure d' [**adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contenant l’adresse réseau du point de terminaison de service auquel se connecter.</span><span class="sxs-lookup"><span data-stu-id="cd82f-122">When the service proxy has been created, the application can open the service proxy for communication to a service by calling the [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) function, passing an [**address**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) structure containing the network address of the service endpoint to connect to.</span></span>

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

<span data-ttu-id="cd82f-123">Lorsque le proxy de service a été ouvert, l’application peut l’utiliser pour effectuer des appels au service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-123">When the service proxy has been opened, the application can use it to make calls to the service.</span></span>

``` syntax
hr = Add(
    serviceProxy, 
    1, 
    2, 
    &result, 
    NULL, 
    0, 
    NULL, 
    error);
```

<span data-ttu-id="cd82f-124">Lorsque l’application n’a plus besoin du proxy de service, elle ferme le proxy de service en appelant la fonction [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="cd82f-124">When the application no longer needs the service proxy, it closes the service proxy by calling the [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) function.</span></span> <span data-ttu-id="cd82f-125">Elle libère également la mémoire associée en appelant [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span><span class="sxs-lookup"><span data-stu-id="cd82f-125">It also frees the associated memory by calling [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).</span></span>

``` syntax
hr = WsCloseServiceProxy(
    serviceProxy, 
    NULL, 
    error);
```

``` syntax
hr = WsFreeServiceProxy(
    serviceProxy, 
    error);
```

## <a name="reusing-the-service-proxy"></a><span data-ttu-id="cd82f-126">Réutilisation du proxy de service</span><span class="sxs-lookup"><span data-stu-id="cd82f-126">Reusing the Service Proxy</span></span>

<span data-ttu-id="cd82f-127">Sinon, après avoir appelé [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , une application peut réutiliser le proxy de service en appelant la fonction [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .</span><span class="sxs-lookup"><span data-stu-id="cd82f-127">Alternatively, after calling [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) an application can reuse the service proxy by calling the [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) function.</span></span>

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

<span data-ttu-id="cd82f-128">Pour plus d’informations sur l’utilisation des proxys de service dans différents contextes, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="cd82f-128">For more information on how service proxies are used in different contexts, see the following topics:</span></span>

-   [<span data-ttu-id="cd82f-129">Proxy de service et sessions</span><span class="sxs-lookup"><span data-stu-id="cd82f-129">Service Proxy and Sessions</span></span>](service-proxy-and-sessions.md)
-   [<span data-ttu-id="cd82f-130">Opération de service</span><span class="sxs-lookup"><span data-stu-id="cd82f-130">Service Operation</span></span>](service-operation.md)
-   [<span data-ttu-id="cd82f-131">Opérations de service côté client</span><span class="sxs-lookup"><span data-stu-id="cd82f-131">Client Side Service Operations</span></span>](client-side-service-operations.md)
-   [<span data-ttu-id="cd82f-132">HttpCalculatorClientExample</span><span class="sxs-lookup"><span data-stu-id="cd82f-132">HttpCalculatorClientExample</span></span>](httpcalculatorclientexample.md)

### <a name="security"></a><span data-ttu-id="cd82f-133">Sécurité</span><span class="sxs-lookup"><span data-stu-id="cd82f-133">Security</span></span>

<span data-ttu-id="cd82f-134">Les considérations suivantes relatives à la conception des applications doivent être soigneusement notées quand vous utilisez l’API du proxy du service WWSAPI :</span><span class="sxs-lookup"><span data-stu-id="cd82f-134">Following application design considerations should be carefully noted when you use the WWSAPI service proxy API:</span></span>

-   <span data-ttu-id="cd82f-135">Le proxy de service n’effectue aucune validation des données au-delà de la validation de base du profil 2,0 et de la sérialisation XML.</span><span class="sxs-lookup"><span data-stu-id="cd82f-135">The service proxy will not perform any validation of the data beyond Basic Profile 2.0 validation and XML serialization.</span></span> <span data-ttu-id="cd82f-136">Il incombe à l’application de valider les données contenues dans les paramètres qu’elle reçoit dans le cadre de l’appel.</span><span class="sxs-lookup"><span data-stu-id="cd82f-136">It is the responsibility of the application to validate the data contained in the parameters it receives back as part of the call.</span></span>
-   <span data-ttu-id="cd82f-137">Configuration du nombre maximal d’appels en attente sur le proxy de service, à l’aide de la valeur d’énumération de l' [**\_ ID de \_ propriété \_ du proxy WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) nombre **maximal d' \_ \_ \_ \_ \_ appels en attente**, offre une protection contre un serveur en cours d’exécution lent.</span><span class="sxs-lookup"><span data-stu-id="cd82f-137">Configuring the maximum number of pending calls on the service proxy, by using the [**WS\_PROXY\_PROPERTY\_ID**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) enumeration value **WS\_PROXY\_PROPERTY\_MAX\_PENDING\_CALLS**, provides protection against a slow running server.</span></span> <span data-ttu-id="cd82f-138">La valeur maximale par défaut est 100.</span><span class="sxs-lookup"><span data-stu-id="cd82f-138">The default maximum is 100.</span></span> <span data-ttu-id="cd82f-139">Les applications doivent être prudentes lors de la modification des valeurs par défaut.</span><span class="sxs-lookup"><span data-stu-id="cd82f-139">Applications must be careful in modifying the defaults.</span></span>
-   <span data-ttu-id="cd82f-140">Le proxy de service ne fournit aucune garantie de sécurité au-delà de celles spécifiées dans la structure de [**\_ \_ Description de sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) utilisée pour communiquer avec le serveur.</span><span class="sxs-lookup"><span data-stu-id="cd82f-140">The service proxy provides no security guarantees beyond those specified in the [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure used to communicate with the server.</span></span>
-   <span data-ttu-id="cd82f-141">Soyez vigilant lorsque vous modifiez les valeurs par défaut des [messages](message.md) et des [canaux](channel.md) sur le proxy de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-141">Take care when you modifying [message](message.md) and [channel](channel.md) defaults on the service proxy.</span></span> <span data-ttu-id="cd82f-142">Lisez les considérations de sécurité associées aux messages et aux canaux avant de modifier les propriétés associées.</span><span class="sxs-lookup"><span data-stu-id="cd82f-142">Read the security considerations associated with messages and channels before you modify any of the related properties.</span></span>
-   <span data-ttu-id="cd82f-143">Le proxy de service chiffre toutes les informations d’identification qu’il conserve en mémoire.</span><span class="sxs-lookup"><span data-stu-id="cd82f-143">Service proxy encrypts all credentials that it keeps in memory.</span></span>

<span data-ttu-id="cd82f-144">Les éléments d’API suivants sont liés aux proxys de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-144">The following API elements relate to service proxies.</span></span>

| <span data-ttu-id="cd82f-145">Rappel</span><span class="sxs-lookup"><span data-stu-id="cd82f-145">Callback</span></span>                                                          | <span data-ttu-id="cd82f-146">Description</span><span class="sxs-lookup"><span data-stu-id="cd82f-146">Description</span></span>                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd82f-147">**\_rappel de \_ message de proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-147">**WS\_PROXY\_MESSAGE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | <span data-ttu-id="cd82f-148">Appelée lorsque les en-têtes du message d’entrée sont sur le ou lorsqu’un en-tête de message de sortie vient d’être reçu.</span><span class="sxs-lookup"><span data-stu-id="cd82f-148">Invoked when the headers of the input message are about to be sent through or when an output message headers are just received.</span></span> |



 



| <span data-ttu-id="cd82f-149">Énumération</span><span class="sxs-lookup"><span data-stu-id="cd82f-149">Enumeration</span></span>                                                 | <span data-ttu-id="cd82f-150">Description</span><span class="sxs-lookup"><span data-stu-id="cd82f-150">Description</span></span>                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cd82f-151">**ID de propriété de l' \_ appel WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-151">**WS\_CALL\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | <span data-ttu-id="cd82f-152">Énumère les paramètres facultatifs pour la configuration d’un appel sur une opération de service côté client.</span><span class="sxs-lookup"><span data-stu-id="cd82f-152">Enumerates optional parameters for configuring a call on a client side service operation.</span></span> |
| [<span data-ttu-id="cd82f-153">**\_ID de \_ propriété du proxy WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-153">**WS\_PROXY\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | <span data-ttu-id="cd82f-154">Énumère les paramètres facultatifs pour la configuration du proxy de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-154">Enumerates optional parameters for configuring the service proxy.</span></span>                         |
| [<span data-ttu-id="cd82f-155">**\_État du \_ proxy WS service \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-155">**WS\_SERVICE\_PROXY\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | <span data-ttu-id="cd82f-156">État du proxy de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-156">The state of the service proxy.</span></span>                                                           |



 



| <span data-ttu-id="cd82f-157">Fonction</span><span class="sxs-lookup"><span data-stu-id="cd82f-157">Function</span></span>                                                       | <span data-ttu-id="cd82f-158">Description</span><span class="sxs-lookup"><span data-stu-id="cd82f-158">Description</span></span>                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [<span data-ttu-id="cd82f-159">**WsAbandonCall**</span><span class="sxs-lookup"><span data-stu-id="cd82f-159">**WsAbandonCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | <span data-ttu-id="cd82f-160">Abandonne un appel spécifié sur un proxy de service spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd82f-160">Abandons a specified call on a specified service proxy.</span></span>                           |
| [<span data-ttu-id="cd82f-161">**WsAbortServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="cd82f-161">**WsAbortServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | <span data-ttu-id="cd82f-162">Annule toutes les entrées et sorties en attente sur un proxy de service spécifié.</span><span class="sxs-lookup"><span data-stu-id="cd82f-162">Cancels all pending input and output on a specified service proxy.</span></span>                |
| [<span data-ttu-id="cd82f-163">**WsCall**</span><span class="sxs-lookup"><span data-stu-id="cd82f-163">**WsCall**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | <span data-ttu-id="cd82f-164">Interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="cd82f-164">Internal only.</span></span> <span data-ttu-id="cd82f-165">Sérialise les arguments dans un message et les envoie sur le canal.</span><span class="sxs-lookup"><span data-stu-id="cd82f-165">Serializes arguments into a message and sends it over the channel.</span></span> |
| [<span data-ttu-id="cd82f-166">**WsCloseServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="cd82f-166">**WsCloseServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | <span data-ttu-id="cd82f-167">Ferme un proxy de service pour la communication.</span><span class="sxs-lookup"><span data-stu-id="cd82f-167">Closes a service proxy for communication.</span></span>                                         |
| [<span data-ttu-id="cd82f-168">**WsCreateServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="cd82f-168">**WsCreateServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | <span data-ttu-id="cd82f-169">Crée un proxy de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-169">Creates a service proxy.</span></span>                                                          |
| [<span data-ttu-id="cd82f-170">**WsFreeServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="cd82f-170">**WsFreeServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | <span data-ttu-id="cd82f-171">Libère la mémoire associée à un proxy de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-171">Releases the memory associated with a service proxy.</span></span>                              |
| [<span data-ttu-id="cd82f-172">**WsGetServiceProxyProperty**</span><span class="sxs-lookup"><span data-stu-id="cd82f-172">**WsGetServiceProxyProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | <span data-ttu-id="cd82f-173">Récupère une propriété de proxy de service spécifiée.</span><span class="sxs-lookup"><span data-stu-id="cd82f-173">Retrieves a specified service proxy property.</span></span>                                     |
| [<span data-ttu-id="cd82f-174">**WsOpenServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="cd82f-174">**WsOpenServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | <span data-ttu-id="cd82f-175">Ouvre un proxy de service à un point de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-175">Opens a service proxy to a service endpoint.</span></span>                                      |
| [<span data-ttu-id="cd82f-176">**WsResetServiceProxy**</span><span class="sxs-lookup"><span data-stu-id="cd82f-176">**WsResetServiceProxy**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | <span data-ttu-id="cd82f-177">Réinitialise le proxy de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-177">Resets service proxy.</span></span>                                                             |



 



| <span data-ttu-id="cd82f-178">Handle</span><span class="sxs-lookup"><span data-stu-id="cd82f-178">Handle</span></span>                                     | <span data-ttu-id="cd82f-179">Description</span><span class="sxs-lookup"><span data-stu-id="cd82f-179">Description</span></span>                                       |
|--------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="cd82f-180">\_proxy WS service \_</span><span class="sxs-lookup"><span data-stu-id="cd82f-180">WS\_SERVICE\_PROXY</span></span>](ws-service-proxy.md) | <span data-ttu-id="cd82f-181">Type opaque utilisé pour référencer un proxy de service.</span><span class="sxs-lookup"><span data-stu-id="cd82f-181">An opaque type used to reference a service proxy.</span></span> |



 



| <span data-ttu-id="cd82f-182">Structure</span><span class="sxs-lookup"><span data-stu-id="cd82f-182">Structure</span></span>                                         | <span data-ttu-id="cd82f-183">Description</span><span class="sxs-lookup"><span data-stu-id="cd82f-183">Description</span></span>                 |
|---------------------------------------------------|-----------------------------|
| [<span data-ttu-id="cd82f-184">**\_propriété d’appel WS \_**</span><span class="sxs-lookup"><span data-stu-id="cd82f-184">**WS\_CALL\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | <span data-ttu-id="cd82f-185">Spécifie une propriété d’appel.</span><span class="sxs-lookup"><span data-stu-id="cd82f-185">Specifies a call property.</span></span>  |
| <span data-ttu-id="cd82f-186">[**WS \_ \_propriété de proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span><span class="sxs-lookup"><span data-stu-id="cd82f-186">[**WS\_PROXY\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property).</span></span> | <span data-ttu-id="cd82f-187">Spécifie une propriété de proxy.</span><span class="sxs-lookup"><span data-stu-id="cd82f-187">Specifies a proxy property.</span></span> |



 

 

 




