---
description: Message WS-Discovery utilisé pour annoncer le départ d’un appareil ou d’un service à partir du réseau.
ms.assetid: 7b9abfcc-28ab-4f29-af69-6dc68e3f51b6
title: Message Bye
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8276c05314b31782442bfdf6de998dd41241391de9dc94947409041c8f4aa420
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738651"
---
# <a name="bye-message"></a>Message Bye

Un message Bye est un message d' WS-Discovery utilisé pour annoncer le départ d’un appareil ou d’un service à partir du réseau. Pour plus d’informations sur les messages Bye, consultez la section 4,2 de la [spécification WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Les messages Bye ne sont pas sollicités. Les messages sont facultatifs.

> [!Note]  
> Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI. WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple. N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Le message SOAP suivant montre un exemple de message bye.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:193ccfa0-347d-41a1-9285-f500b6b96a15
    </wsa:MessageID>
    <wsd:AppSequence InstanceId="2"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="21">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:Bye>
        <wsa:EndpointReference>
            <wsa:Address>
                urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsa:Address>
        </wsa:EndpointReference>
    </wsd:Bye>
</soap:Body>
```

Un message Bye a les points de focalisation suivants.



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
<td>Adieu</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Bye
</wsa:Action></code></pre></td>
<td>L’action SOAP Bye identifie le message en tant que message bye.</td>
</tr>
<tr class="even">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;2&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;21&quot;>
</wsd:AppSequence></code></pre></td>
<td>Contient des informations de séquencement d’application, qui permettent de maintenir la séquence de messages même si elles sont reçues dans le désordre. Le AppSequence est validé comme décrit dans <a href="appsequence-validation-rules.md">règles de validation AppSequence</a>.</td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contient l’adresse du point de terminaison en cours de mise hors connexion.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[détection et Messages de Exchange de métadonnées](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Message de salutation](hello-message.md)
</dt> </dl>

 

 



