---
description: Message WS-Discovery utilisé par un client pour rechercher des services sur le réseau par nom.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Résoudre le message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54887db566ee428e6bfe9ec2de9016a637884b092611a85e607c55aaa4176abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118991609"
---
# <a name="resolve-message"></a>Résoudre le message

Un message de résolution est un message d' WS-Discovery utilisé par un client pour rechercher des services sur le réseau par nom. Un client envoie un message de résolution uniquement lorsqu’un message HTTP (par exemple, une demande d’échange de métadonnées ou un [message de service](get--metadata-exchange--http-request-and-message.md) ) est envoyé. Pour plus d’informations sur la résolution des messages, consultez la section 6,1 de la [spécification WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un message de résolution est envoyé par la multidiffusion UDP au port 3702. Les messages de résolution de monodiffusion ne sont pas pris en charge.

Les clients DPWS envoient des messages de résolution. La liste suivante répertorie les scénarios dans lesquels WSDAPI envoie un message de résolution.

-   Un client de découverte de fonction envoie un message de résolution si aucun XAddrs n’est inclus dans un message [messages ProbeMatches](probematches-message.md) .
-   Un client qui appelle les méthodes [**IWSDiscoveryProvider :: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) envoie un message de résolution.
-   Un client appelant [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) peut envoyer un message de résolution si une adresse d’appareil logique est passée à *pszDeviceId*.
-   Un client qui appelle [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) envoie un message de résolution si la fonction est appelée avec le paramètre pDeviceAddress défini sur **null**.

> [!Note]  
> Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI. WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple. N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Le message SOAP suivant montre un exemple de message de résolution.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery">
<soap:Header>
    <wsa:To>
urn:schemas-xmlsoap-org:ws:2005:04:discovery
</wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Resolve>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Resolve>
</soap:Body>
</soap:Envelope>
```

Un message de résolution a les points de focalisation suivants.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Point de focus</th>
<th>XML</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Résoudre</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td>L’action Resolve SOAP identifie le message en tant que message de résolution.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td>Contient l’identificateur de message, qui est référencé dans un message <a href="resolvematches-message.md">ResolveMatches</a> .</td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contient l’adresse du point de terminaison qui est résolu.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[détection et Messages de Exchange de métadonnées](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Message ResolveMatches](resolvematches-message.md)
</dt> </dl>

 

 



