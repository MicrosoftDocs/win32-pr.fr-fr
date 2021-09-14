---
description: Message WS-Discovery utilisé par un client pour rechercher des services sur le réseau par type de service.
ms.assetid: a0ede1d9-2e13-4d5e-8ccd-9e0c0217cac7
title: Message de sondage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f186de4f68faceca096ddaa231b57d1112bc1e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923259"
---
# <a name="probe-message"></a>Message de sondage

Un message de sondage est un message d' WS-Discovery utilisé par un client pour rechercher des services sur le réseau par type de service. Pour plus d’informations sur les messages de sondage, consultez la section 5,2 de la [spécification WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un message de sondage est envoyé par la multidiffusion UDP au port 3702. Les messages de sondage de monodiffusion ne sont pas pris en charge.

Les clients DPWS envoient des messages de sondage. La liste suivante répertorie les scénarios dans lesquels WSDAPI envoie un message de sondage.

-   Les clients de détection de fonction envoient des messages de sondage.
-   Les clients WSDAPI appelant [**IWSDiscoveryProvider :: SearchByAddress**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyaddress) envoient des messages de sonde.
-   Les clients WSDAPI appelant [**IWSDiscoveryProvider :: SearchByType**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbytype) envoient des messages de sonde.
-   Les applications utilisant la découverte dirigée envoient des messages de sondage via HTTP ou HTTPs.

> [!Note]  
> Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI. WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple. N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Le message SOAP suivant montre un exemple de message de sondage.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        urn:schemas-xmlsoap-org:ws:2005:04:discovery
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:MessageID>
</soap:Header>
<soap:Body>
    <wsd:Probe>
        <wsd:Types>wsdp:Device</wsd:Types>
    </wsd:Probe>
</soap:Body>
```

Un message de sondage a les points de focalisation suivants.



<table>
<colgroup>
<col  />
<col  />
<col  />
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
<td>Sonde</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Probe
&lt;/wsa:Action&gt;</code></pre></td>
<td>L’action SOAP de sondage identifie le message en tant que message de sondage.</td>
</tr>
<tr class="even">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:MessageID&gt;
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
&lt;/wsa:MessageID&gt;</code></pre></td>
<td>Contient l’identificateur de message, qui est référencé par l’élément latesto dans un message <a href="probematches-message.md">messages ProbeMatches</a> .</td>
</tr>
<tr class="odd">
<td>Types</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:Types&gt;wsdp:Device</wsd:Types></code></pre></td>
<td>Contient les types de WS-Discovery pour lesquels le client recherche. Cet élément ne doit pas être vide.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[détection et Messages de Exchange de métadonnées](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Message messages ProbeMatches](probematches-message.md)
</dt> </dl>

 

 



