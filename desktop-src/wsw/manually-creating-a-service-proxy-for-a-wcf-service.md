---
title: Création manuelle d’un proxy de service pour un service WCF
description: Le moyen le plus simple de créer un proxy de service client pour un service Windows Communication Foundation (WCF) se situe au niveau de la couche de modèle de service avec l’outil WsUtil, comme décrit dans la rubrique Création d’un client.
ms.assetid: ef545090-382b-44bd-b7ab-f5a285b6e202
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e061fda95298986ee6336dee0662d80c89a0a5a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106543608"
---
# <a name="manually-creating-a-service-proxy-for-a-wcf-service"></a>Création manuelle d’un proxy de service pour un service WCF

Le moyen le plus simple de créer un proxy de service client pour un service Windows Communication Foundation (WCF) se situe au niveau de la couche de [modèle de service](service-model-layer-overview.md) avec l’outil WsUtil, comme décrit dans la rubrique [création d’un client](creating-a-client.md) . Toutefois, si nécessaire, vous pouvez également créer un proxy de service manuellement. Cette API comprend une fonction [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) pour la création du proxy de service ainsi que des structures, des énumérations, etc. pour définir les propriétés nécessaires à l’interopérabilité avec WCF.

WCF fournit un certain nombre de liaisons standard, chacune ciblant un scénario d’utilisation spécifique. La liaison que le service auquel vous essayez de connecter utilise, à son tour, détermine les propriétés de canal que vous devez personnaliser pour que votre proxy de service communique avec le service.

## <a name="creating-a-service-proxy-for-wcfs-wshttpbinding"></a>Création d’un proxy de service pour WSHttpBinding de WCF

WSHttpBinding est destiné au scénario des services Web Internet de la principale. Il utilise la version la plus récente de SOAP 1,2 et WS-Addressing version 1,0, et active une large gamme de paramètres de sécurité sur les transports HTTP et HTTPs publics. WWSAPI n’a pas d’équivalent de WSHttpBinding (ou de l’une des liaisons standard WCF), mais comme sa version par défaut de SOAP, WS-Addressing version et le format d’encodage correspondent à ceux de WSHttpBinding, la création d’un proxy de service pour un service qui utilise WSHttpBinding est simple. Par exemple, pour créer un proxy de service pour communiquer avec un point de terminaison WSHttpBinding sans sécurité, vous pouvez simplement utiliser du code tel que l’extrait de code suivant (déclaration de variable, et le segment de mémoire et la création d’erreurs sont omis). Notez qu’aucune propriété de canal ou description de sécurité n’est spécifiée dans l’appel à la fonction [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) .


```C++
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        NULL, // channel properties
        0, // channel property count
        &proxy, 
        error);
```



La fonction crée le proxy de service et retourne un pointeur vers celui-ci dans le paramètre *serviceProxy* (&proxy dans l’appel de fonction ci-dessus).

## <a name="creating-a-service-proxy-for-wcfs-basichttpbinding"></a>Création d’un proxy de service pour BasicHttpBinding de WCF

Toutefois, lorsque vous créez manuellement un proxy de service pour un service WCF qui utilise une liaison BasicHttpBinding, il est nécessaire de définir la version SOAP et les propriétés de WS-Addressing du canal. Cela est dû au fait que WWSAPI est défini par défaut sur SOAP version 1,2 et WS-Addressing 1,0. Le BasicHttpBinding de WCF, en revanche, utilise la version SOAP 1,1 et aucun WS-Addressing.

Pour définir la version SOAP et les propriétés de WS-Addrssing du canal, déclarez un tableau de structures de [**\_ \_ Propriétés WS Channel**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property) qui contiendra les propriétés de canal et les informations associées.


```
WS_CHANNEL_PROPERTY channelProperties[4]; // Array to hold up to 4 channel properties

ULONG channelPropertyCount = 0; // Count of properties set
 
WS_ENVELOPE_VERSION soapVersion = WS_ENVELOPE_VERSION_SOAP_1_1; // Set required SOAP version
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ENVELOPE_VERSION; // Type of first channel property
channelProperties[channelPropertyCount].value = &soapVersion; // Address of the SOAP version value
channelProperties[channelPropertyCount].valueSize = sizeof(soapVersion); // Size of the value
channelPropertyCount++; // Increment property count
 
WS_ADDRESSING_VERSION addressingVersion = WS_ADDRESSING_VERSION_TRANSPORT; // Set required WS-Addressing value
channelProperties[channelPropertyCount].id = WS_CHANNEL_PROPERTY_ADDRESSING_VERSION; // Type of second channel property
channelProperties[channelPropertyCount].value = &addressingVersion ; // Address of the WS-Addressing value
channelProperties[channelPropertyCount].valueSize = sizeof(addressingVersion ); // Size of the value
channelPropertyCount++; // Increment property count
 
// add more channel properties here

```



Transmettez ensuite le tableau des propriétés de canal (channelProperties) et le nombre de propriétés (channelPropertyCount) au [**WsCreateServiceProxy**](/windows/desktop/api/WebServices/nf-webservices-wscreateserviceproxy) (ou [**WsCreateChannel**](/windows/desktop/api/WebServices/nf-webservices-wscreatechannel) si vous travaillez à la couche de canal).


```
// Create the proxy

hr = WsCreateServiceProxy(
        WS_CHANNEL_TYPE_REQUEST, 
        WS_HTTP_CHANNEL_BINDING, 
        NULL, // security description
        NULL, // proxy properties
        0, // proxy property count
        channelProperties, // channel properties
        channelPropertyCount, // channel property count
        &proxy, 
        error);
```



Le tableau que vous avez déclaré pour contenir les propriétés est copié dans **WsCreateServiceProxy** et, par conséquent, vous pouvez libérer la mémoire pour le tableau de propriétés immédiatement après avoir appelé la fonction. En outre, si vous allouez la mémoire à partir de la pile (comme l’extrait de code ci-dessus), vous pouvez également retourner à partir de la fonction immédiatement après l’appel.

## <a name="other-bindings"></a>Autres liaisons

En outre, WWSAPI fournit des mécanismes permettant de créer des proxys de service pour communiquer avec les services WCF à l’aide d’autres liaisons, telles que NetTcpBinding et WSFederationHttpBinding. La plupart de ces liaisons requièrent la définition de propriétés de canal supplémentaires, telles que les descripteurs de sécurité. Pour obtenir des exemples qui illustrent l’utilisation d’autres liaisons, consultez la section [exemples de services Web Windows](windows-web-services-examples.md), en particulier les [exemples de couche de canal TCP](tcp-channel-layer-examples.md), les exemples de couche de [canal http](http-channel-layer-examples.md)et les sous-sections [exemples de couche](security-channel-layer-examples.md) de canal de sécurité.

 

 




