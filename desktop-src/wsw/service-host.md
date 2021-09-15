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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127411133"
---
# <a name="service-host"></a>Hôte de service

L’hôte de service est l’environnement d’exécution pour l’hébergement d’un service au sein d’un processus.


Un service peut configurer un ou plusieurs points de terminaison à l’intérieur d’un hôte de service.

![Diagramme montrant la structure d’un hôte de service contenant un point de terminaison de service.](images/servicehost.png)

## <a name="creating-a-service-host"></a>Création d’un hôte de service

Avant de créer un hôte de service, un service doit définir ses points de terminaison. Un point de terminaison dans l’hôte de service est spécifié dans la structure de [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) et il est défini par les informations suivantes :

-   Adresse, qui est l’URI physique sur lequel le service sera hébergé.
-   Structure [**de \_ \_ type WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) qui spécifie le type du canal sous-jacent pour le point de terminaison.
-   Structure [**de \_ \_ liaison WS Channel**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) qui spécifie la liaison du canal.
-   Une structure de [**\_ \_ Description de sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) qui contient la description de sécurité pour le point de terminaison.
-   Structure [**de \_ \_ contrat de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_contract) qui représente le [contrat de service](contract.md) pour le point de terminaison.
-   Structure [**de \_ \_ \_ rappel de sécurité WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) qui spécifie une fonction de rappel d’autorisation pour le point de terminaison.
-   Structure [**de \_ propriété de point de \_ terminaison \_ de service Web**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property) qui contient un tableau de propriétés de point de terminaison de service.

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

Seuls les contrats unidirectionnels sont pris en charge pour SOAP sur UDP, représentés par la [**\_ liaison de \_ canal \_ WS UDP**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding) dans l’énumération de **\_ \_ liaison WS Channel** .

Une fois qu’un point de terminaison est défini, il peut être passé à la fonction [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) , qui prend un tableau de pointeurs vers des structures de [**point de \_ \_ terminaison WS service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) .

``` syntax
HRESULT hr = WsCreateServiceHost (serviceEndpoints, 1, NULL, 0, &host, error);
```

Une application peut éventuellement fournir un tableau de [**Propriétés de service**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property) à [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) pour configurer des paramètres personnalisés sur l’hôte de service.

Une application ouvre l’hôte de service pour commencer à accepter les demandes des clients.

``` syntax
WsOpenServiceHost(serviceHost, NULL, NULL);
```

Après l’ouverture de l’hôte de service, l’application peut la fermer s’il n’y a plus d’opérations qui l’exigent. Notez que cela ne libère pas ses ressources, et qu’elle peut être rouverte avec un appel ultérieur à [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost).

``` syntax
WsCloseServiceHost(serviceHost, NULL, NULL);
```

Après la fermeture de l’hôte de service, une application peut réinitialiser l’hôte de service en vue de sa réutilisation.

``` syntax
WsResetServiceHost(serviceHost, NULL);
```

Lorsque l’application est exécutée avec l’hôte de service, elle peut libérer les ressources associées à l’hôte de service en appelant la fonction [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost) . Notez que [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost) doit être appelé avant d’appeler cette fonction.

``` syntax
WsFreeServiceHost(serviceHost, NULL);
```

Pour plus d’informations sur l’attachement d’un état personnalisé à l’hôte de service, consultez état de l’hôte de l' [utilisateur](user-host-state.md) .

Pour plus d’informations sur l’autorisation dans un hôte de service pour un point de terminaison donné, consultez [autorisation de service](service-authorization.md).

Pour Iinformation sur l’implémentation d’opérations de service et de contrats de service pour un service, consultez les rubriques [opérations de service](server-side-service-operations.md) et [contrat de service](contract.md).

## <a name="security"></a>Sécurité

Une application peut utiliser les propriétés suivantes pour contrôler la quantité de ressources allouées par l’hôte de service pour le compte de l’application :

-   [**WS \_ propriété de point de terminaison de SERVICE \_ \_ \_ Max \_ accepting \_ Channels**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ accès concurrentiel maximal**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)à la propriété du point de terminaison de service,
-   [**WS \_ propriété de point de terminaison de SERVICE \_ \_ \_ Max \_ Channels**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id),
-   [**WS \_ \_ \_ \_ \_ \_ \_ taille maximale du tas du corps**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)de la propriété de point de terminaison de service,
-   [**WS \_ propriété de point de terminaison de SERVICE \_ \_ \_ \_ \_ \_ taille max**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id). du pool d’appels,
-   [**WS \_ \_ \_ \_ taille maximale du \_ pool de \_ canaux \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id)de la propriété du point de terminaison de service.

Les valeurs par défaut sécurisées sont choisies pour chacune de ces propriétés, une application doit être prudente si elle souhaite modifier ces propriétés. Au-delà des propriétés mentionnées ci-dessus, les propriétés de [canal](channel.md), d' [écouteur](listener.md) et de [message](message.md) spécifiques peuvent également être modifiées par l’application. Reportez-vous aux considérations sur la sécurité de ces composants avant de modifier ces paramètres.

En outre, les considérations suivantes relatives à la conception des applications doivent être évaluées avec soin lors de l’utilisation de l’API hôte du service WWSAPI :

-   Quand vous utilisez MEX, les applications doivent veiller à ne pas divulguer de données sensibles. En guise d’atténuation, si la nature des données exposées via MEX est sensible, les applications peuvent choisir de configurer le point de terminaison MEX avec une liaison sécurisée nécessitant l’authentification au minimum et d’implémenter l’autorisation dans le cadre du point de terminaison à l’aide du [**\_ rappel de \_ sécurité \_ WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Par défaut, les informations d’erreur enrichies par défaut sont désactivées sur l’hôte de service par la propriété de [**\_ Divulgation d’erreur de \_ propriété \_ \_ WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id) . Il est à la discrétion de l’application d’envoyer des informations d’erreur riches dans le cadre de l’erreur. Toutefois, cela peut entraîner la divulgation d’informations et, par conséquent, il est recommandé de modifier ce paramètre uniquement pour les scénarios de débogage.
-   Au-delà de la validation effectuée pour le profil de base 2,0 et la sérialisation XML, l’hôte de service n’effectue aucune validation sur le contenu des données reçues dans le cadre des paramètres d’opération de service. Il est de la responsabilité de l’application d’effectuer toutes les validations de paramètres.
-   L’autorisation n’est pas implémentée dans le cadre de l’hôte de service. Toutefois, les applications peuvent implémenter leur propre schéma d’autorisation à l’aide de la [**\_ \_ Description**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) de sécurité WS et du [**\_ rappel de \_ sécurité \_ WS service**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback).
-   Il incombe à l’application d’utiliser des liaisons sécurisées sur son point de terminaison. L’hôte de service ne fournit pas de sécurité au-delà de ce qui est configuré sur le point de terminaison.

Les éléments d’API suivants sont utilisés avec l’hôte de service.

| Rappel                                                                             | Description                                                                     |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**\_rappel de \_ canal d’acceptation de service Web \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback) | Appelée lorsqu’un canal est accepté sur un écouteur de point de terminaison par l’hôte de service. |
| [**\_rappel de \_ canal de fermeture du service WS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)   | Appelée lorsqu’un canal est fermé ou abandonné sur un point de terminaison.                     |



 



| Énumération                                                                    | Description                                                                                 |
|--------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [**ID de propriété du point de terminaison de \_ service WS \_ \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_endpoint_property_id) | Paramètres facultatifs pour la configuration d’un [**\_ point de \_ terminaison de service WS**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint). |
| [**État de l' \_ hôte WS service \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_host_state)                      | États dans lesquels un hôte de service peut se trouver.                                                   |
| [**\_ID de \_ propriété de service Web \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_property_id)                    | Paramètres facultatifs pour la configuration de l’hôte de service.                                       |



 



| Fonction                                                     | Description                                                                                  |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| [**WsAbortServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsabortservicehost)             | Interrompt et interrompt les opérations en cours sur l’hôte de service.                          |
| [**WsCloseServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscloseservicehost)             | Ferme tous les écouteurs afin qu’aucun nouveau canal ne soit accepté par le client.                   |
| [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost)           | Crée un hôte de service.                                                                      |
| [**WsFreeServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsfreeservicehost)               | Libère la mémoire associée à un objet hôte de service.                                   |
| [**WsGetServiceHostProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetservicehostproperty) | Récupère une propriété de l’hôte de service spécifiée.                                                 |
| [**WsOpenServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsopenservicehost)               | Ouvre un hôte de service pour la communication et démarre les écouteurs sur tous les points de terminaison.        |
| [**WsResetServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wsresetservicehost)             | Réinitialise l’hôte de service pour la réutilisation et réinitialise le canal et les écouteurs sous-jacents en vue de les réutiliser. |



 



| Handle                                       | Description                                      |
|----------------------------------------------|--------------------------------------------------|
| [**\_hôte de service WS \_**](ws-service-host.md) | Type opaque utilisé pour référencer un hôte de service. |



 



| Structure                                                                              | Description                                                                     |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [**point de terminaison de \_ service WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint)                                   | Représente un point de terminaison individuel sur un hôte de service.                            |
| [**\_propriété de \_ point de terminaison de service WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint_property)                | Spécifie un paramètre propre au service.                                           |
| [**\_propriété de service Web \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property)                                   | Spécifie un paramètre propre au service.                                           |
| [**rappel d’acceptation de la \_ propriété de service Web \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_accept_callback) | Spécifie le rappel qui est appelé lorsqu’un canal est accepté avec succès. |
| [**rappel de fermeture de la \_ propriété WS service \_ \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_property_close_callback)   | Spécifie le rappel qui est appelé lorsqu’un canal va être fermé.    |



 

 

 




