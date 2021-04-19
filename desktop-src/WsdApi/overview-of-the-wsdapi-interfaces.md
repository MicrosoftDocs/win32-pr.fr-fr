---
description: L’API WSDAPI (Web Services on Devices) est utilisée pour développer des applications clientes qui recherchent et accèdent à des appareils, ainsi que pour développer des hôtes d’appareils et des services associés qui s’exécutent sur Windows Vista et Windows Server 2008.
ms.assetid: 2b23d7d3-3b06-48c8-993e-49c72b139624
title: Vue d’ensemble des interfaces WSDAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3e728971741f97707c1dc72effdaf0ca17dbb2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517006"
---
# <a name="overview-of-the-wsdapi-interfaces"></a>Vue d’ensemble des interfaces WSDAPI

L’API WSDAPI (Web Services on Devices) est utilisée pour développer des applications clientes qui recherchent et accèdent à des appareils, ainsi que pour développer des hôtes d’appareils et des services associés qui s’exécutent sur Windows Vista et Windows Server 2008. L’API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) et l’outil [WsdCodeGen](web-services-for-devices-code-generator.md) sont des outils supplémentaires qui peuvent être utilisés pour le client, l’hôte d’appareil et le développement de services. Les interfaces WSDAPI peuvent être utilisées directement pour exposer des fonctionnalités avancées.

## <a name="major-wsdapi-interfaces"></a>Principales interfaces WSDAPI

Les quatre principales interfaces WSDAPI sont [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider), [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher), [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy)et [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost). Pour obtenir la liste de toutes les interfaces WSDAPI, consultez [services Web sur les interfaces des appareils](web-services-for-devices-interfaces.md).

## <a name="iwsdiscoveryprovider"></a>IWSDiscoveryProvider

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) est utilisé pour implémenter les fonctionnalités de WS-Discovery sur les clients.

[**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) émet des problèmes WS-Discovery [sonder](probe-message.md) et [résoudre](resolve-message.md) les messages, et reçoit les messages [Hello](hello-message.md), [Bye](bye-message.md), [messages ProbeMatches](probematches-message.md)et [ResolveMatches](resolvematches-message.md) . Utilisez les informations récupérées via l’interface **IWSDiscoveryProvider** lors de la création d’une interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) utilisée pour décrire et contrôler un appareil DPWS spécifique.

Une interface [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) n’est pas nécessaire lors de la résolution d’une adresse d’appareil DPWS particulière avant la création d’un proxy d’appareil. [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) résoudra automatiquement l’adresse de l’appareil, si nécessaire.

L’API de [détection de fonction](/previous-versions/windows/desktop/fundisc/fd-portal) peut être utilisée pour la découverte d’appareils et de services génériques, car l’API peut découvrir des appareils DPWS et également des appareils utilisant d’autres protocoles. Envisagez d’utiliser la découverte de fonction lors de l’écriture d’une application de découverte générique.

## <a name="iwsdiscoverypublisher"></a>IWSDiscoveryPublisher

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) est utilisé pour implémenter les fonctionnalités de WS-Discovery sur les services cibles, tels que les appareils.

[**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) permet à une application de publier sa présence à l’aide de messages WS-Discovery Hello et Bye. Cette interface permet à une application de recevoir des requêtes de sonde et de résolution, et de construire et d’envoyer des réponses messages ProbeMatches et ResolveMatches.

Une interface [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) n’est pas nécessaire lors de la publication simple de l’existence d’un objet [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) . **IWSDDeviceHost** gère sa propre présence WS-Discovery.

## <a name="iwsddeviceproxy"></a>IWSDDeviceProxy

[**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) est utilisé pour implémenter les fonctionnalités WS-Discovery, WS-MetadataExchange et de contrôle côté client. Cette fonctionnalité comprend un canal sécurisé facultatif, des fonctionnalités WS-Eventing et des pièces jointes.

L’interface [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) a les trois utilisations suivantes.

-   Résout les adresses d’appareils logiques, si nécessaire.
-   Initie les demandes de métadonnées aux appareils pour énumérer les types et les adresses des services.
-   Fournit une source pour les objets [**IWSDServiceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsdserviceproxy) , qui peuvent être utilisés pour émettre des messages de contrôle à des services spécifiques sur un appareil.

L’objet [**IWSDDeviceProxy**](/windows/desktop/api/WsdClient/nn-wsdclient-iwsddeviceproxy) est généralement créé et utilisé entièrement dans le code généré par [WsdCodeGen](web-services-for-devices-code-generator.md).

## <a name="iwsddevicehost"></a>IWSDDeviceHost

[**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) est utilisé pour implémenter la fonctionnalité WS-Discovery, WS-MetadataExchange et l’hébergement de service côté appareil. Les services hébergés peuvent répondre aux messages de contrôle et peuvent prendre en charge les fonctionnalités de canal sécurisé, WS-Eventing et pièce jointe.

L’interface [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) utilise les éléments suivants.

-   Héberge des objets de service.
-   Annonce la présence d’un hôte d’appareil sur le réseau à l’aide de WS-Discovery.
-   Répond aux demandes WS-MetadataExchange et décrit les types et les emplacements des services hébergés.
-   Distribue les demandes réseau en objets de service.

Les fonctionnalités de gestion des abonnements WS-Discovery, WS-MetadataExchange et WS-Eventing sont gérées entièrement au sein de l’objet hôte de l’appareil. Pour pouvoir héberger un service à l’intérieur d’un hôte d’appareil, les conditions suivantes doivent être respectées.

-   L’hôte doit être créé en appelant [**WSDCreateDeviceHost**](/windows/desktop/api/WsdHost/nf-wsdhost-wsdcreatedevicehost).
-   Les métadonnées associées au service doivent être inscrites.
-   Le service lui-même doit être inscrit.
-   L’hôte de l’appareil doit être démarré.

L’objet [**IWSDDeviceHost**](/windows/desktop/api/WsdHost/nn-wsdhost-iwsddevicehost) est généralement créé et utilisé dans le code généré par [WsdCodeGen](web-services-for-devices-code-generator.md).

 

 
