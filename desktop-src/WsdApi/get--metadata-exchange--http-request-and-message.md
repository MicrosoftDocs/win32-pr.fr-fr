---
description: Message WS-Transfer utilisé pour demander des métadonnées.
ms.assetid: 18bf27aa-6ae5-4419-ae68-6df9eda10cd4
title: obtenir (métadonnées Exchange) la requête et le Message HTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9cf6241b38f7fa81cc5d9a7c21a0f5e1a406aa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518037"
---
# <a name="get-metadata-exchange-http-request-and-message"></a>obtenir (métadonnées Exchange) la requête et le Message HTTP

Un message d’extraction est un message WS-Transfer utilisé pour demander des métadonnées. Pour plus d’informations sur la récupération des messages, consultez la section 3,1 de la [spécification WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf). Étant donné que l’échange de métadonnées s’effectue via HTTP, un message d’extraction est la charge utile d’une requête HTTP.

Les clients DPWS envoient des messages d’extraction. Les clients de détection de fonction, les clients WSDAPI appelant [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy)et les clients wsdapi appelant [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) envoient ce message.

> [!Note]  
> Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI. WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple. N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

L’exemple suivant montre un exemple d’extraction de requête HTTP.

``` syntax
POST /37f86d35-e6ac-4241-964f-1d9ae46fb366
HTTP/1.1
Content-Type: application/soap+xml
User-Agent: WSDAPI
Host: 192.168.0.2:5357
Content-Length: 658
Connection: Keep-Alive
Cache-Control: no-cache
Pragma: no-cache
```

Une requête HTTP obtenir a les points de focus suivants.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Point de focus</th>
<th>Ligne d’en-tête</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Chemin d’URL</td>
<td><pre class="syntax" data-space="preserve"><code>POST /37f86d35-e6ac-4241-964f-1d9ae46fb366</code></pre></td>
<td>Chemin d’accès de l’URL où la requête obtenir HTTP a été publiée.</td>
</tr>
<tr class="even">
<td>Hôte et port</td>
<td><pre class="syntax" data-space="preserve"><code>Host: 192.168.0.2:5357</code></pre></td>
<td>Hôte et port où la requête HTTP obtenir a été dirigée.</td>
</tr>
</tbody>
</table>



 

Le message SOAP suivant montre un exemple d’extraction de message.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing">
<soap:Header>
    <wsa:To>
        urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:MessageID>
    <wsa:ReplyTo>
        <wsa:Address>
            https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
        </wsa:Address>
    </wsa:ReplyTo>
    <wsa:From>
        <wsa:Address>
            urn:uuid:49e131df-351a-4ece-9a6f-6a862d31cffa
        </wsa:Address>
    </wsa:From>
</soap:Header>
<soap:Body>
</soap:Body>
```

Un message d’extraction a les points de focalisation suivants.



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
<td>À</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:To&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:To&gt;</code></pre></td>
<td>Identificateur de l’appareil demandé pour les métadonnées.</td>
</tr>
<tr class="even">
<td>Obtenir</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2004/09/transfer/Get
</wsa:Action</code></pre></td>
<td>L’action obtenir un SOAP identifie le message en tant que message d’extraction.</td>
</tr>
<tr class="odd">
<td>MessageID</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:MessageID></code></pre></td>
<td>Contient l’identificateur de message, qui est référencé dans un message <a href="getresponse--metadata-exchange--message.md">GetResponse</a> .</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[détection et Messages de Exchange de métadonnées](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Message GetResponse](getresponse--metadata-exchange--message.md)
</dt> </dl>

 

 



