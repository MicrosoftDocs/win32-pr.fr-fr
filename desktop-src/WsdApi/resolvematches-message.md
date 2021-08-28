---
description: Un message de WS-Discovery envoyé en réponse à un client résolve le message par un service correspondant.
ms.assetid: 0eaa4348-968e-4b45-9509-8b15476edaa1
title: Message ResolveMatches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 140d279a5e66835b7754e3f501732263dff430f2
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883634"
---
# <a name="resolvematches-message"></a>Message ResolveMatches

Un message ResolveMatches est un message WS-Discovery envoyé en réponse au message de [résolution](resolve-message.md) d’un client par un service correspondant. Pour plus d’informations sur les messages ResolveMatches, consultez la section 6,2 de la [spécification WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).

Un message ResolveMatches est envoyé par la monodiffusion UDP au port 3702 (le port à partir duquel le message de [résolution](resolve-message.md) du client a été envoyé). ResolveMatches doit être envoyé dans les 4 secondes du message de résolution ; dans le cas contraire, Windows pare-feu peut supprimer le paquet.

Toute application DPWS qui envoie des messages de [résolution](resolve-message.md) recevra des messages ResolveMatches.

> [!Note]  
> Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI. WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple. N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Le message SOAP suivant montre un exemple de message ResolveMatches.

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
        https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:64ddd01c-b0d6-4afd-aba6-6f1f161ce9d4
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
    </wsa:RelatesTo>
    <wsd:AppSequence InstanceId="1"
        SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
        MessageNumber="6">
    </wsd:AppSequence>
</soap:Header>
<soap:Body>
    <wsd:ResolveMatches>
        <wsd:ResolveMatch>
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
        </wsd:ResolveMatch>
    </wsd:ResolveMatches>
</soap:Body>
</soap:Envelope>
```

Un message ResolveMatches a les points de focalisation suivants.



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
<td>ResolveMatches</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Action&gt;
    https://schemas.xmlsoap.org/ws/2005/04/discovery/ResolveMatches
&lt;/wsa:Action&gt;</code></pre></td>
<td>L’action SOAP ResolveMatches identifie le message en tant que message ResolveMatches.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:RelatesTo&gt;
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
&lt;/wsa:RelatesTo&gt;</code></pre></td>
<td>Identificateur du message auquel le service répond. Cet en-tête correspond à MessageId dans le message de <a href="resolve-message.md">résolution</a> .</td>
</tr>
<tr class="odd">
<td>AppSequence</td>
<td><pre class="syntax" data-space="preserve"><code><wsd:AppSequence InstanceId=&quot;1&quot;
    SequenceId=&quot;urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772&quot;
    MessageNumber=&quot;6&quot;>
&lt;/wsd:AppSequence&gt;</code></pre></td>
<td>Contient des informations de séquencement d’application, qui permettent de maintenir la séquence de messages même si elles sont reçues dans le désordre. Le AppSequence est validé comme décrit dans <a href="appsequence-validation-rules.md">règles de validation AppSequence</a>.</td>
</tr>
<tr class="even">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code>&lt;wsa:Address&gt;
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
&lt;/wsa:Address&gt;</code></pre></td>
<td>Contient l’adresse du point de terminaison qui est résolu.</td>
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

[Résoudre le message](resolve-message.md)
</dt> </dl>

 

 



