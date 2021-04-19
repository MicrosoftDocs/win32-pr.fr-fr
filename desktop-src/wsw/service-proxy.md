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
# <a name="service-proxy"></a>Proxy de service

Un proxy de service est le proxy côté client pour un service. Le proxy de service permet aux applications d’envoyer et de recevoir des [messages](message.md) sur un [canal](channel.md) en tant qu’appels de méthode.

Les proxys de service sont créés en fonction des besoins, ouverts, utilisés pour appeler un service et fermés quand vous n’en avez plus besoin. Une application peut également réutiliser un proxy de service pour se connecter à plusieurs reprises au même service sans les dépenses de temps et les ressources requises pour initialiser un proxy de service plusieurs fois. Le diagramme suivant illustre le déroulement des États possibles du proxy de service et des appels de fonction ou des événements qui mènent d’un État à un autre.

![Diagramme montrant les États du proxy de service et les appels de fonction ou les événements qui conduisent d’un État à un autre.](images/serviceproxystates.png)

Ces États du proxy de service sont énumérés dans l’énumération de l' [**\_ État du \_ proxy \_ WS service**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) .

Comme le montre le diagramme ci-dessus et le code suivant, un proxy de service est créé par un appel à la fonction [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) . En tant que paramètres pour cet appel, WWSAPI fournit les énumérations suivantes :

-   [**\_type de canal WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type)
-   [**\_liaison WS Channel \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)

Il accepte également les paramètres facultatifs à l’aide des types de données suivants :

-   [**\_ID de \_ propriété du proxy WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)
-   [**Description de la sécurité de WS \_ \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)

Lorsque le proxy de service a été créé, la fonction **WsCreateServiceProxy** retourne une référence au proxy de service, à [WS \_ service \_ proxy](ws-service-proxy.md), via un paramètre out.

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

Lorsque le proxy de service a été créé, l’application peut ouvrir le proxy de service pour la communication avec un service en appelant la fonction [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy) , en passant une structure d' [**adresse**](/windows/desktop/api/WebServices/ns-webservices-ws_endpoint_address) contenant l’adresse réseau du point de terminaison de service auquel se connecter.

``` syntax
WS_ENDPOINT_ADDRESS address = {0};
address.uri.chars = "net.tcp://localhost/example";
address.uri.length = wcslen("net.tcp://localhost/example";);
hr = WsOpenServiceProxy(serviceProxy, &address, NULL, error);
```

Lorsque le proxy de service a été ouvert, l’application peut l’utiliser pour effectuer des appels au service.

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

Lorsque l’application n’a plus besoin du proxy de service, elle ferme le proxy de service en appelant la fonction [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) . Elle libère également la mémoire associée en appelant [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy).

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

## <a name="reusing-the-service-proxy"></a>Réutilisation du proxy de service

Sinon, après avoir appelé [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy) , une application peut réutiliser le proxy de service en appelant la fonction [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy) .

``` syntax
hr = WsResetServiceProxy(
    serviceProxy, 
    error);
```

Pour plus d’informations sur l’utilisation des proxys de service dans différents contextes, consultez les rubriques suivantes :

-   [Proxy de service et sessions](service-proxy-and-sessions.md)
-   [Opération de service](service-operation.md)
-   [Opérations de service côté client](client-side-service-operations.md)
-   [HttpCalculatorClientExample](httpcalculatorclientexample.md)

### <a name="security"></a>Sécurité

Les considérations suivantes relatives à la conception des applications doivent être soigneusement notées quand vous utilisez l’API du proxy du service WWSAPI :

-   Le proxy de service n’effectue aucune validation des données au-delà de la validation de base du profil 2,0 et de la sérialisation XML. Il incombe à l’application de valider les données contenues dans les paramètres qu’elle reçoit dans le cadre de l’appel.
-   Configuration du nombre maximal d’appels en attente sur le proxy de service, à l’aide de la valeur d’énumération de l' [**\_ ID de \_ propriété \_ du proxy WS**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id) nombre **maximal d' \_ \_ \_ \_ \_ appels en attente**, offre une protection contre un serveur en cours d’exécution lent. La valeur maximale par défaut est 100. Les applications doivent être prudentes lors de la modification des valeurs par défaut.
-   Le proxy de service ne fournit aucune garantie de sécurité au-delà de celles spécifiées dans la structure de [**\_ \_ Description de sécurité WS**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description) utilisée pour communiquer avec le serveur.
-   Soyez vigilant lorsque vous modifiez les valeurs par défaut des [messages](message.md) et des [canaux](channel.md) sur le proxy de service. Lisez les considérations de sécurité associées aux messages et aux canaux avant de modifier les propriétés associées.
-   Le proxy de service chiffre toutes les informations d’identification qu’il conserve en mémoire.

Les éléments d’API suivants sont liés aux proxys de service.

| Rappel                                                          | Description                                                                                                                     |
|-------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [**\_rappel de \_ message de proxy WS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback) | Appelée lorsque les en-têtes du message d’entrée sont sur le ou lorsqu’un en-tête de message de sortie vient d’être reçu. |



 



| Énumération                                                 | Description                                                                               |
|-------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**ID de propriété de l' \_ appel WS \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_call_property_id)       | Énumère les paramètres facultatifs pour la configuration d’un appel sur une opération de service côté client. |
| [**\_ID de \_ propriété du proxy WS \_**](/windows/desktop/api/WebServices/ne-webservices-ws_proxy_property_id)     | Énumère les paramètres facultatifs pour la configuration du proxy de service.                         |
| [**\_État du \_ proxy WS service \_**](/windows/desktop/api/WebServices/ne-webservices-ws_service_proxy_state) | État du proxy de service.                                                           |



 



| Fonction                                                       | Description                                                                       |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------|
| [**WsAbandonCall**](/windows/desktop/api/WebServices/nf-webservices-wsabandoncall)                         | Abandonne un appel spécifié sur un proxy de service spécifié.                           |
| [**WsAbortServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsabortserviceproxy)             | Annule toutes les entrées et sorties en attente sur un proxy de service spécifié.                |
| [**WsCall**](/windows/desktop/api/WebServices/nf-webservices-wscall)                                       | Interne uniquement. Sérialise les arguments dans un message et les envoie sur le canal. |
| [**WsCloseServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscloseserviceproxy)             | Ferme un proxy de service pour la communication.                                         |
| [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy)           | Crée un proxy de service.                                                          |
| [**WsFreeServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsfreeserviceproxy)               | Libère la mémoire associée à un proxy de service.                              |
| [**WsGetServiceProxyProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetserviceproxyproperty) | Récupère une propriété de proxy de service spécifiée.                                     |
| [**WsOpenServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsopenserviceproxy)               | Ouvre un proxy de service à un point de terminaison de service.                                      |
| [**WsResetServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wsresetserviceproxy)             | Réinitialise le proxy de service.                                                             |



 



| Handle                                     | Description                                       |
|--------------------------------------------|---------------------------------------------------|
| [\_proxy WS service \_](ws-service-proxy.md) | Type opaque utilisé pour référencer un proxy de service. |



 



| Structure                                         | Description                 |
|---------------------------------------------------|-----------------------------|
| [**\_propriété d’appel WS \_**](/windows/desktop/api/WebServices/ns-webservices-ws_call_property)    | Spécifie une propriété d’appel.  |
| [**WS \_ \_propriété de proxy**](/windows/desktop/api/WebServices/ns-webservices-ws_proxy_property). | Spécifie une propriété de proxy. |



 

 

 




