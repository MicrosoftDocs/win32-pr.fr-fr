---
description: Message WS-Discovery envoyé par un service en réponse à un message de sondage de clients.
ms.assetid: 58d3d016-ae29-4090-9b88-e1125db59c95
title: Message messages ProbeMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 813549091edc6cbb1202d746c7a7f62ecf3e03b5
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882005"
---
# <a name="probematches-message"></a>Message messages ProbeMatches

Un message messages ProbeMatches est un message de WS-Discovery envoyé par un service en réponse au message de [sondage](probe-message.md) d’un client. Pour plus d’informations sur les messages messages ProbeMatches, consultez la section 5,3 de la [spécification WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un message messages ProbeMatches est envoyé par la monodiffusion UDP au port à partir duquel le message de [sondage](probe-message.md) du client a été envoyé. Messages ProbeMatches doit être envoyé dans les 4 secondes du message de sondage ; dans le cas contraire, Windows pare-feu peut supprimer le paquet.

Si aucun XAddrs n’est inclus dans le message messages ProbeMatches, le client peut envoyer un message de [résolution](resolve-message.md) par multidiffusion UDP au port 3702. Le client envoie un message de résolution lorsqu’un message HTTP (par exemple, une demande d’échange de métadonnées ou un [message de service](get--metadata-exchange--http-request-and-message.md) ) est envoyé.

Toute application DPWS qui envoie des messages de [sondage](probe-message.md) recevra des messages messages ProbeMatches.

> [!Note]  
> Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI. WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple. N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Le message SOAP suivant montre un exemple de message messages ProbeMatches.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsd="https://schemas.xmlsoap.org/ws/2005/04/discovery"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:967d0036-fe69-40ad-8191-dd1fc8ef64ab
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="9">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ProbeMatches>
        <wsd:ProbeMatch>
            <wsa:EndpointReference>
                <wsa:Address>
                    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                </wsa:Address>
            </wsa:EndpointReference>
            <wsd:Types>wsdp:Device</wsd:Types>
            <wsd:XAddrs>
                https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
            </wsd:XAddrs>
            <wsd:MetadataVersion>2</wsd:MetadataVersion>
        </wsd:ProbeMatch>
    </wsd:ProbeMatches>
</soap:Body>
</soap:Envelope>
```

Un message messages ProbeMatches a les points de focalisation suivants.



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
<td>Messages ProbeMatches</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ProbeMatches
&lt;/wsa:Action&gt;</code></pre></td>
<td>L’action SOAP messages ProbeMatches identifie le message en tant que message messages ProbeMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:RelatesTo&gt;
    urn:uuid:29cf10da-5c41-4d55-b184-5ee15e38ce23
&lt;/wsa:RelatesTo&gt;</code></pre></td>
<td>Identificateur du message auquel le service répond. Cet en-tête correspond à MessageId dans le message de <a href="probe-message.md">sondage</a> .</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;9&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Contient des informations de séquencement d’application, qui permettent de maintenir la séquence de messages même si elles sont reçues dans le désordre. Le AppSequence est validé comme décrit dans <a href="appsequence-validation-rules.md">règles de validation AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Contient l’adresse du point de terminaison. Ce adressé peut être référencé dans un message de <a href="resolve-message.md">résolution</a> .</td>
</tr>
<tr class="odd">
<td>XAddrs</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsd:XAddrs&gt;
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsd:XAddrs&gt;</code></pre></td>
<td>Les XAddrs sont des adresses de transport qui peuvent être utilisées pour la communication entre le client et le service. Les ADR sont validées comme décrit dans <a href="xaddr-validation-rules.md">règles de validation XAddr</a>.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[détection et Messages de Exchange de métadonnées](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Message de sondage](probe-message.md)
</dt> </dl>

 

 



