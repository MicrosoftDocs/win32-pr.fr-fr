---
title: Hôte de service
description: L’hôte de service est l’environnement d’exécution pour l’hébergement d’un service au sein d’un processus.
ms.assetid: 42e4d24d-5611-4561-b874-6dc3f3f88c73
keywords:
- Services Web de l’hôte de service pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0170f7dc0dfda99887b7d11d68d073517e0eb85f
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "106539144"
---
# <a name="service-host"></a><span data-ttu-id="f0eb9-106">Hôte de service</span><span class="sxs-lookup"><span data-stu-id="f0eb9-106">Service Host</span></span>

<span data-ttu-id="f0eb9-107">L’hôte de service est l’environnement d’exécution pour l’hébergement d’un service au sein d’un processus.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-107">The service host is the runtime environment for hosting a service within a process.</span></span>


<span data-ttu-id="f0eb9-108">Un service peut configurer un ou plusieurs points de terminaison à l’intérieur d’un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-108">A service can configure one or more endpoints inside a service host.</span></span>

![Diagramme montrant la structure d’un hôte de service contenant un point de terminaison de service.](images/servicehost.png)

## <a name="creating-a-service-host"></a><span data-ttu-id="f0eb9-110">Création d’un hôte de service</span><span class="sxs-lookup"><span data-stu-id="f0eb9-110">Creating a service host</span></span>

<span data-ttu-id="f0eb9-111">Avant de créer un hôte de service, un service doit définir ses points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-111">Before creating a service host, a service needs to define its endpoints.</span></span> <span data-ttu-id="f0eb9-112">Un point de terminaison dans l’hôte de service est spécifié dans la structure de [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) et il est défini par les informations suivantes :</span><span class="sxs-lookup"><span data-stu-id="f0eb9-112">An endpoint in service host is specified in the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structure and it is defined by the following information:</span></span>

-   <span data-ttu-id="f0eb9-113">Adresse, qui est l’URI physique sur lequel le service sera hébergé.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-113">An address, which is the physical URI on which the service will be hosted.</span></span>
-   <span data-ttu-id="f0eb9-114">Structure [**de \_ \_ type WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) qui spécifie le type du canal sous-jacent pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-114">A [**WS\_CHANNEL\_TYPE**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) structure that specifies the type of the underlying channel for the endpoint.</span></span>
-   <span data-ttu-id="f0eb9-115">Structure [**de \_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) qui spécifie la liaison du canal.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-115">A [**WS\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) structure that specifies the binding of the channel.</span></span>
-   <span data-ttu-id="f0eb9-116">Une structure de [**\_ \_ Description de sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) qui contient la description de sécurité pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-116">A [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) structure that contains the security description for the endpoint.</span></span>
-   <span data-ttu-id="f0eb9-117">Structure [**de \_ \_ contrat de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) qui représente le [contrat de service](contract.md) pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-117">A [**WS\_SERVICE\_CONTRACT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) structure that represents the [service contract](contract.md) for the endpoint.</span></span>
-   <span data-ttu-id="f0eb9-118">Structure [**de \_ \_ \_ rappel de sécurité WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) qui spécifie une fonction de rappel d’autorisation pour le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-118">A [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) structure that specifies an authorization callback function for the endpoint.</span></span>
-   <span data-ttu-id="f0eb9-119">Structure [**de \_ propriété de point de \_ terminaison \_ de service Web**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) qui contient un tableau de propriétés de point de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-119">A [**WS\_SERVICE\_ENDPOINT\_PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) structure that contains an array of service endpoint properties.</span></span>

``` syntax
WS_SERVICE_ENDPOINT serviceEndpoint = {0};
const WS_SERVICE_ENDPOINT* serviceEndpoints[1];
serviceEndpoints[0] = &serviceEndpoint;
WS_STRING url = WS_STRING_VALUE(L"net.tcp://+/Example");

// Method based service contract for the service
static WS_SERVICE_CONTRACT calculatorContract = 
{
    &calculatorContractDescription, // comes from a generated header.
    NULL,
    &calculatorFunctions, // specified by the application
};

serviceEndpoint.address.url = &url;
serviceEndpoint.binding.channelBinding =  WS_TCP_CHANNEL_BINDING; 
serviceEndpoint.contract = &calculatorContract;  
serviceEndpoint.channelType = WS_CHANNEL_TYPE_DUPLEX_SESSION; 
serviceEndpoint.authorizationCallback = AuthorizationCallback; // Authorization callback.
```

<span data-ttu-id="f0eb9-120">Seuls les contrats unidirectionnels sont pris en charge pour SOAP sur UDP, représentés par la [**\_ liaison de \_ canal \_ WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dans l’énumération de **\_ \_ liaison WS Channel** .</span><span class="sxs-lookup"><span data-stu-id="f0eb9-120">Only one-way contracts are supported for SOAP over UDP, represented by [**WS\_UDP\_CHANNEL\_BINDING**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) in the **WS\_CHANNEL\_BINDING** enumeration.</span></span>

<span data-ttu-id="f0eb9-121">Une fois qu’un point de terminaison est défini, il peut être passé à la fonction [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , qui prend un tableau de pointeurs vers des structures de [**point de \_ \_ terminaison WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .</span><span class="sxs-lookup"><span data-stu-id="f0eb9-121">After an endpoint is defined, it can be passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function, which takes an array of pointers to [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) structures.</span></span>

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

<span data-ttu-id="f0eb9-122">Une application peut éventuellement fournir un tableau de [**Propriétés de service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) à [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) pour configurer des paramètres personnalisés sur l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-122">An application can optionally provide an array of [**service properties**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) to [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) to configure custom settings on the service host.</span></span>

<span data-ttu-id="f0eb9-123">Une application ouvre l’hôte de service pour commencer à accepter les demandes des clients.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-123">An application opens the service host to start accepting client requests.</span></span>

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="f0eb9-124">Après l’ouverture de l’hôte de service, l’application peut la fermer s’il n’y a plus d’opérations qui l’exigent.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-124">After opening the service host, the application can close it if there are no more operations that require it.</span></span> <span data-ttu-id="f0eb9-125">Notez que cela ne libère pas ses ressources, et qu’elle peut être rouverte avec un appel ultérieur à [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span><span class="sxs-lookup"><span data-stu-id="f0eb9-125">Note that this does not release its resources, and that it can be reopened with a subsequent call to [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).</span></span>

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

<span data-ttu-id="f0eb9-126">Après la fermeture de l’hôte de service, une application peut réinitialiser l’hôte de service en vue de sa réutilisation.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-126">After closing the service host, an application may reset the service host for reuse.</span></span>

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

<span data-ttu-id="f0eb9-127">Lorsque l’application est exécutée avec l’hôte de service, elle peut libérer les ressources associées à l’hôte de service en appelant la fonction [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) .</span><span class="sxs-lookup"><span data-stu-id="f0eb9-127">When the application is done with the service host it can free the resources associated with the service host by calling the [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) function.</span></span> <span data-ttu-id="f0eb9-128">Notez que [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) doit être appelé avant d’appeler cette fonction.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-128">Note that [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) must be called before calling this function.</span></span>

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

<span data-ttu-id="f0eb9-129">Pour plus d’informations sur l’attachement d’un état personnalisé à l’hôte de service, consultez état de l’hôte de l' [utilisateur](user-host-state.md) .</span><span class="sxs-lookup"><span data-stu-id="f0eb9-129">For information on attaching a custom state to the service host, see [User Host State](user-host-state.md)</span></span>

<span data-ttu-id="f0eb9-130">Pour plus d’informations sur l’autorisation dans un hôte de service pour un point de terminaison donné, consultez [autorisation de service](service-authorization.md).</span><span class="sxs-lookup"><span data-stu-id="f0eb9-130">For information on authorization in a service host for a given endpoint, see [Service Authorization](service-authorization.md).</span></span>

<span data-ttu-id="f0eb9-131">Pour Iinformation sur l’implémentation d’opérations de service et de contrats de service pour un service, consultez les rubriques [opérations de service](server-side-service-operations.md) et [contrat de service](contract.md).</span><span class="sxs-lookup"><span data-stu-id="f0eb9-131">For iinformation on implementing service operations and service contracts for a service, see the [service operations](server-side-service-operations.md) and [service contract](contract.md)topics.</span></span>

## <a name="security"></a><span data-ttu-id="f0eb9-132">Sécurité</span><span class="sxs-lookup"><span data-stu-id="f0eb9-132">Security</span></span>

<span data-ttu-id="f0eb9-133">Une application peut utiliser les propriétés suivantes pour contrôler la quantité de ressources allouées par l’hôte de service pour le compte de l’application :</span><span class="sxs-lookup"><span data-stu-id="f0eb9-133">An application can use the followin properties to control the amount of resources the service host allocates on behalf of the application:</span></span>

-   <span data-ttu-id="f0eb9-134">[**WS \_ propriété de point de terminaison de SERVICE \_ \_ \_ Max \_ accepting \_ Channels**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="f0eb9-134">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_ACCEPTING\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="f0eb9-135">[**WS \_ \_ \_ \_ \_ accès concurrentiel maximal**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)à la propriété du point de terminaison de service,</span><span class="sxs-lookup"><span data-stu-id="f0eb9-135">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CONCURRENCY**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="f0eb9-136">[**WS \_ propriété de point de terminaison de SERVICE \_ \_ \_ Max \_ Channels**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span><span class="sxs-lookup"><span data-stu-id="f0eb9-136">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNELS**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="f0eb9-137">[**WS \_ \_ \_ \_ \_ \_ \_ taille maximale du tas du corps**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)de la propriété de point de terminaison de service,</span><span class="sxs-lookup"><span data-stu-id="f0eb9-137">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_BODY\_HEAP\_MAX\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="f0eb9-138">[**WS \_ propriété de point de terminaison de SERVICE \_ \_ \_ \_ \_ \_ taille max**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id). du pool d’appels,</span><span class="sxs-lookup"><span data-stu-id="f0eb9-138">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CALL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),</span></span>
-   <span data-ttu-id="f0eb9-139">[**WS \_ \_ \_ \_ taille maximale du \_ pool de \_ canaux \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)de la propriété du point de terminaison de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-139">[**WS\_SERVICE\_ENDPOINT\_PROPERTY\_MAX\_CHANNEL\_POOL\_SIZE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id).</span></span>

<span data-ttu-id="f0eb9-140">Les valeurs par défaut sécurisées sont choisies pour chacune de ces propriétés, une application doit être prudente si elle souhaite modifier ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-140">Secure defaults are chosen for each of these properties, an application must be careful if it wishes to modify these properties.</span></span> <span data-ttu-id="f0eb9-141">Au-delà des propriétés mentionnées ci-dessus, les propriétés de [canal](channel.md), d' [écouteur](listener.md) et de [message](message.md) spécifiques peuvent également être modifiées par l’application.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-141">Beyond the above-mentioned properties, [channel](channel.md), [listener](listener.md) and [message](message.md) specific properties can also be modified by the application.</span></span> <span data-ttu-id="f0eb9-142">Reportez-vous aux considérations sur la sécurité de ces composants avant de modifier ces paramètres.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-142">Refer to the security considerations of these components before modifying any of these settings.</span></span>

<span data-ttu-id="f0eb9-143">En outre, les considérations suivantes relatives à la conception des applications doivent être évaluées avec soin lors de l’utilisation de l’API hôte du service WWSAPI :</span><span class="sxs-lookup"><span data-stu-id="f0eb9-143">In addition, the following application design considerations should be carefully evaluated when using WWSAPI service host API:</span></span>

-   <span data-ttu-id="f0eb9-144">Quand vous utilisez MEX, les applications doivent veiller à ne pas divulguer de données sensibles.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-144">When using MEX, applications should be careful not to disclose any sensitive data.</span></span> <span data-ttu-id="f0eb9-145">En guise d’atténuation, si la nature des données exposées via MEX est sensible, les applications peuvent choisir de configurer le point de terminaison MEX avec une liaison sécurisée nécessitant l’authentification au minimum et d’implémenter l’autorisation dans le cadre du point de terminaison à l’aide du [**\_ rappel de \_ sécurité \_ WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="f0eb9-145">As a mitigation, if the nature of the data being exposed through MEX is sensitive, applications may choose to configure the MEX endpoint with a secure binding requiring authentication at the very least and implement authorization as part of the endpoint using the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="f0eb9-146">Par défaut, les informations d’erreur enrichies par défaut sont désactivées sur l’hôte de service par la propriété de [**\_ Divulgation d’erreur de \_ propriété \_ \_ WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) .</span><span class="sxs-lookup"><span data-stu-id="f0eb9-146">By default rich error information through faults is disabled on service host by [**WS\_SERVICE\_PROPERTY\_FAULT\_DISCLOSURE**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) property.</span></span> <span data-ttu-id="f0eb9-147">Il est à la discrétion de l’application d’envoyer des informations d’erreur riches dans le cadre de l’erreur.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-147">It is upon the discretion of the application to send rich error information as part of the fault.</span></span> <span data-ttu-id="f0eb9-148">Toutefois, cela peut entraîner la divulgation d’informations et, par conséquent, il est recommandé de modifier ce paramètre uniquement pour les scénarios de débogage.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-148">However, this can result in information disclosure and thus it is recommended that this setting is only changed for debugging scenarios.</span></span>
-   <span data-ttu-id="f0eb9-149">Au-delà de la validation effectuée pour le profil de base 2,0 et la sérialisation XML, l’hôte de service n’effectue aucune validation sur le contenu des données reçues dans le cadre des paramètres d’opération de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-149">Beyond validation performed for Basic Profile 2.0 and XML serialization, service host performs no validation on the data content received as part of service operation parameters.</span></span> <span data-ttu-id="f0eb9-150">Il est de la responsabilité de l’application d’effectuer toutes les validations de paramètres.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-150">It is the responsibility of the application to perform all parameter validations on its own.</span></span>
-   <span data-ttu-id="f0eb9-151">L’autorisation n’est pas implémentée dans le cadre de l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-151">Authorization is not implemented as part of service host.</span></span> <span data-ttu-id="f0eb9-152">Toutefois, les applications peuvent implémenter leur propre schéma d’autorisation à l’aide de la [**\_ \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) de sécurité WS et du [**\_ rappel de \_ sécurité \_ WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span><span class="sxs-lookup"><span data-stu-id="f0eb9-152">However, applications can implement their own authorization scheme using [**WS\_SECURITY\_DESCRIPTION**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) and the [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).</span></span>
-   <span data-ttu-id="f0eb9-153">Il incombe à l’application d’utiliser des liaisons sécurisées sur son point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-153">It is the responsibility of the application to use secure bindings on its endpoint.</span></span> <span data-ttu-id="f0eb9-154">L’hôte de service ne fournit pas de sécurité au-delà de ce qui est configuré sur le point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-154">Service host does not provide any security beyond what is configured on the endpoint.</span></span>

<span data-ttu-id="f0eb9-155">Les éléments d’API suivants sont utilisés avec l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-155">The following API elements are used with the service host.</span></span>

| <span data-ttu-id="f0eb9-156">Rappel</span><span class="sxs-lookup"><span data-stu-id="f0eb9-156">Callback</span></span>                                                                             | <span data-ttu-id="f0eb9-157">Description</span><span class="sxs-lookup"><span data-stu-id="f0eb9-157">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f0eb9-158">**\_rappel de \_ canal d’acceptation de service Web \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-158">**WS\_SERVICE\_ACCEPT\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | <span data-ttu-id="f0eb9-159">Appelée lorsqu’un canal est accepté sur un écouteur de point de terminaison par l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-159">Invoked when a channel is accepted on an endpoint listener by the service host.</span></span> |
| [<span data-ttu-id="f0eb9-160">**\_rappel de \_ canal de fermeture du service WS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-160">**WS\_SERVICE\_CLOSE\_CHANNEL\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | <span data-ttu-id="f0eb9-161">Appelée lorsqu’un canal est fermé ou abandonné sur un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-161">Invoked when a channel is closed or aborted on an endpoint.</span></span>                     |



 



| <span data-ttu-id="f0eb9-162">Énumération</span><span class="sxs-lookup"><span data-stu-id="f0eb9-162">Enumeration</span></span>                                                                    | <span data-ttu-id="f0eb9-163">Description</span><span class="sxs-lookup"><span data-stu-id="f0eb9-163">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0eb9-164">**ID de propriété du point de terminaison de \_ service WS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-164">**WS\_SERVICE\_ENDPOINT\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | <span data-ttu-id="f0eb9-165">Paramètres facultatifs pour la configuration d’un [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span><span class="sxs-lookup"><span data-stu-id="f0eb9-165">Optional parameters for configuring a [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint).</span></span> |
| [<span data-ttu-id="f0eb9-166">**État de l' \_ hôte WS service \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-166">**WS\_SERVICE\_HOST\_STATE**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | <span data-ttu-id="f0eb9-167">États dans lesquels un hôte de service peut se trouver.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-167">The states that a service host can be in.</span></span>                                                   |
| [<span data-ttu-id="f0eb9-168">**\_ID de \_ propriété de service Web \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-168">**WS\_SERVICE\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | <span data-ttu-id="f0eb9-169">Paramètres facultatifs pour la configuration de l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-169">Optional parameters for configuring the service host.</span></span>                                       |



 



| <span data-ttu-id="f0eb9-170">Fonction</span><span class="sxs-lookup"><span data-stu-id="f0eb9-170">Function</span></span>                                                     | <span data-ttu-id="f0eb9-171">Description</span><span class="sxs-lookup"><span data-stu-id="f0eb9-171">Description</span></span>                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0eb9-172">**WsAbortServiceHost**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-172">**WsAbortServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | <span data-ttu-id="f0eb9-173">Interrompt et interrompt les opérations en cours sur l’hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-173">Interrupts and discontinues current operations on the service host.</span></span>                          |
| [<span data-ttu-id="f0eb9-174">**WsCloseServiceHost**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-174">**WsCloseServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | <span data-ttu-id="f0eb9-175">Ferme tous les écouteurs afin qu’aucun nouveau canal ne soit accepté par le client.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-175">Closes all listeners so that no new channels are accepted from the client.</span></span>                   |
| [<span data-ttu-id="f0eb9-176">**WsCreateServiceHost**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-176">**WsCreateServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | <span data-ttu-id="f0eb9-177">Crée un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-177">Creates a service host.</span></span>                                                                      |
| [<span data-ttu-id="f0eb9-178">**WsFreeServiceHost**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-178">**WsFreeServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | <span data-ttu-id="f0eb9-179">Libère la mémoire associée à un objet hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-179">Releases the memory associated with a service host object.</span></span>                                   |
| [<span data-ttu-id="f0eb9-180">**WsGetServiceHostProperty**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-180">**WsGetServiceHostProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | <span data-ttu-id="f0eb9-181">Récupère une propriété de l’hôte de service spécifiée.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-181">Retrieves a specified Service Host property.</span></span>                                                 |
| [<span data-ttu-id="f0eb9-182">**WsOpenServiceHost**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-182">**WsOpenServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | <span data-ttu-id="f0eb9-183">Ouvre un hôte de service pour la communication et démarre les écouteurs sur tous les points de terminaison.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-183">Opens a service host for communication and starts the listeners on all the endpoints.</span></span>        |
| [<span data-ttu-id="f0eb9-184">**WsResetServiceHost**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-184">**WsResetServiceHost**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | <span data-ttu-id="f0eb9-185">Réinitialise l’hôte de service pour la réutilisation et réinitialise le canal et les écouteurs sous-jacents en vue de les réutiliser.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-185">Resets the service host for reuse and resets the underlying channel and listeners for reuse.</span></span> |



 



| <span data-ttu-id="f0eb9-186">Handle</span><span class="sxs-lookup"><span data-stu-id="f0eb9-186">Handle</span></span>                                       | <span data-ttu-id="f0eb9-187">Description</span><span class="sxs-lookup"><span data-stu-id="f0eb9-187">Description</span></span>                                      |
|----------------------------------------------|--------------------------------------------------|
| [<span data-ttu-id="f0eb9-188">**\_hôte de service WS \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-188">**WS\_SERVICE\_HOST**</span></span>](ws-service-host.md) | <span data-ttu-id="f0eb9-189">Type opaque utilisé pour référencer un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-189">An opaque type used to reference a service host.</span></span> |



 



| <span data-ttu-id="f0eb9-190">Structure</span><span class="sxs-lookup"><span data-stu-id="f0eb9-190">Structure</span></span>                                                                              | <span data-ttu-id="f0eb9-191">Description</span><span class="sxs-lookup"><span data-stu-id="f0eb9-191">Description</span></span>                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="f0eb9-192">**point de terminaison de \_ service WS \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-192">**WS\_SERVICE\_ENDPOINT**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | <span data-ttu-id="f0eb9-193">Représente un point de terminaison individuel sur un hôte de service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-193">Represents an individual endpoint on a service host.</span></span>                            |
| [<span data-ttu-id="f0eb9-194">**\_propriété de \_ point de terminaison de service WS \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-194">**WS\_SERVICE\_ENDPOINT\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | <span data-ttu-id="f0eb9-195">Spécifie un paramètre propre au service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-195">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="f0eb9-196">**\_propriété de service Web \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-196">**WS\_SERVICE\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | <span data-ttu-id="f0eb9-197">Spécifie un paramètre propre au service.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-197">Specifies a service-specific setting.</span></span>                                           |
| [<span data-ttu-id="f0eb9-198">**rappel d’acceptation de la \_ propriété de service Web \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-198">**WS\_SERVICE\_PROPERTY\_ACCEPT\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | <span data-ttu-id="f0eb9-199">Spécifie le rappel qui est appelé lorsqu’un canal est accepté avec succès.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-199">Specifies the callback which is called when a channel is successfully accepted.</span></span> |
| [<span data-ttu-id="f0eb9-200">**rappel de fermeture de la \_ propriété WS service \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f0eb9-200">**WS\_SERVICE\_PROPERTY\_CLOSE\_CALLBACK**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | <span data-ttu-id="f0eb9-201">Spécifie le rappel qui est appelé lorsqu’un canal va être fermé.</span><span class="sxs-lookup"><span data-stu-id="f0eb9-201">Specifies the callback which is called when a channel is about to be closed.</span></span>    |



 

 

 




