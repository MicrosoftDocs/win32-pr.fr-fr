---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage des applications WSDAPI.
ms.assetid: befe4234-8d3a-4fc5-9a7d-faca94964af6
title: Résolution des problèmes liés aux autres applications WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a421f26237cc14d07a43e00faeb6d8bf49aa02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517571"
---
# <a name="troubleshooting-other-wsdapi-applications"></a>Résolution des problèmes liés aux autres applications WSDAPI

Les applications peuvent appeler directement des interfaces et des fonctions WSDAPI pour effectuer la découverte des appareils et l’échange de métadonnées. Les modèles de message utilisés par ces applications varient.

L’objectif de ce guide de résolution des problèmes est d’aider les développeurs d’applications WSDAPI à implémenter correctement un proxy d’appareil. Ce guide n’a pas pour but de vous aider à résoudre tous les aspects de WSDAPI. Si le proxy de l’appareil a été créé avec succès et que le client et l’hôte peuvent se voir sur le réseau, ce guide ne peut pas résoudre les problèmes de l’application. Pour résoudre les problèmes liés aux applications, suivez les instructions de la section [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft pour obtenir de l’aide.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxy"></a>Résolution des problèmes des clients appelant WSDCreateDeviceProxy

Les applications appellent [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) pour créer et initialiser une instance de l’interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . Cet objet proxy d’appareil peut être utilisé pour publier des services sur un appareil et pour échanger des métadonnées.

Une application qui appelle [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) utilise toujours les messages suivants.

-   [Get](get--metadata-exchange--http-request-and-message.md)
-   [GetResponse](getresponse--metadata-exchange--message.md)

Une application appelant [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) utilise parfois les messages suivants.

-   [Résolution](resolve-message.md)
-   [ResolveMatches](resolvematches-message.md)

Les messages [Resolve](resolve-message.md) et [ResolveMatches](resolvematches-message.md) sont générés lorsqu’une adresse d’appareil logique (autrement dit, une adresse de périphérique de la forme urn : UUID : {Guid}) est passée à *pszDeviceId*. Ces messages ne sont pas générés lorsqu’une adresse d’appareil physique est transmise à *pszDeviceId*. Lorsque les messages Resolve et ResolveMatches sont utilisés, ils sont envoyés avant les [messages d’extraction et de](getresponse--metadata-exchange--message.md) [récupération](get--metadata-exchange--http-request-and-message.md) .

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à une application appelant [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) à l’aide d’une adresse d’appareil physique.

1.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
2.  [Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à une application appelant [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) à l’aide d’une adresse d’appareil logique.

1.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
2.  [Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

Vérifiez que les messages [Resolve](resolve-message.md) et [ResolveMatches](resolvematches-message.md) sont générés et répondent aux exigences du trafic. Il n’est pas nécessaire de rechercher les messages [Probe](probe-message.md) ou [messages ProbeMatches](probematches-message.md) dans la sortie du client de débogage WSD ou dans les suivis réseau.

## <a name="troubleshooting-clients-calling-wsdcreatedeviceproxyadvanced"></a>Résolution des problèmes des clients appelant WSDCreateDeviceProxyAdvanced

Les applications appellent [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) pour créer et initialiser une instance de l’interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) . Contrairement à [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy), **WSDCreateDeviceProxyAdvanced** a un paramètre *pDeviceAddress* qui est utilisé pour définir l’adresse de transport de l’appareil. Si cette adresse de transport est spécifiée, la résolution des adresses logiques n’est pas [obligatoire et les](resolve-message.md) messages [ResolveMatches](resolvematches-message.md) ne sont pas générés.

Si *pDeviceAddress* a la valeur **null** et que *pszDeviceId* est une adresse logique, la résolution d’adresse est requise et les messages [de résolution et de](resolve-message.md) [ResolveMatches](resolvematches-message.md) sont générés.

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à une application appelant [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) avec un paramètre _pDeviceAddress_ non **null**. Ces procédures peuvent également être utilisées lorsque *pDeviceAddress* a la **valeur null** et que *pszDeviceId* est une adresse physique.

1.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
2.  [Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
3.  [Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).
4.  [Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à une application appelant [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) avec *PDeviceAddress* défini sur **null** et avec *pszDeviceId* défini sur une adresse logique.

1.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
2.  [Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).
5.  [Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).
6.  [Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).
7.  [Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).

Vérifiez que les messages [Resolve](resolve-message.md) et [ResolveMatches](resolvematches-message.md) sont générés et répondent aux exigences du trafic. Il n’est pas nécessaire de rechercher les messages [Probe](probe-message.md) ou [messages ProbeMatches](probematches-message.md) dans la sortie du client de débogage WSD ou dans les suivis réseau.

## <a name="troubleshooting-clients-using-the-iwsdiscoveryprovider-interface"></a>Résolution des problèmes des clients à l’aide de l’interface IWSDiscoveryProvider

Les applications qui appellent l’interface [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) n’effectuent pas d’échange de métadonnées. Cette interface est utilisée uniquement pour la découverte. Les modèles de message et les procédures de résolution des problèmes sont différents pour chaque méthode appelée sur l’interface **IWSDiscoveryProvider** .

Lorsqu’une application appelle [**IWSDiscoveryProvider :: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype), un message de [sondage](probe-message.md) est généré. Le message de sondage est envoyé par la multidiffusion UDP au port 3702. Un message [messages ProbeMatches](probematches-message.md) est généré en réponse. Le message messages ProbeMatches est envoyé par la monodiffusion UDP et provient du port 3702.

Quand une application appelle [**IWSDiscoveryProvider :: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid), un message de [résolution](resolve-message.md) est généré. Un message de résolution est envoyé par la multidiffusion UDP au port 3702. Un message [ResolveMatches](resolvematches-message.md) est généré en réponse. Le ResolveMatches est envoyé par la monodiffusion UDP et provient du port 3702.

Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à une application appelant [**IWSDiscoveryProvider :: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) ou [**IWSDiscoveryProvider :: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid). Vérifiez que les messages générés par l’API appelée répondent aux exigences de trafic.

1.  [Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).
2.  [Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).
3.  [Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).
4.  [Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).

Si une application appelle [**IWSDiscoveryProvider :: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress), il s’agit d’une application de découverte dirigée. Pour plus d’informations sur le dépannage, consultez [Dépannage des applications à l’aide de la découverte dirigée](troubleshooting-applications-using-directed-discovery.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de Prise en main avec WSDAPI](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



