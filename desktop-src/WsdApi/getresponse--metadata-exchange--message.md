---
description: Message WS-Transfer utilisé pour répondre à une demande de métadonnées.
ms.assetid: aff05317-35db-4ea6-9692-1e09e4682fe7
title: Message GetResponse (échange de métadonnées)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b91546076698f17a25b8a87444ae3eca71d65a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104203005"
---
# <a name="getresponse-metadata-exchange-message"></a>Message GetResponse (échange de métadonnées)

Un message GetResponse est un message WS-Transfer utilisé pour répondre à une demande de métadonnées. Pour plus d’informations sur les messages GetResponse, consultez la section 3,1 de la [spécification WS-Transfer](https://specs.xmlsoap.org/ws/2004/09/transfer/WS-Transfer.pdf).

Toute application DPWS qui envoie des messages d' [extraction](get--metadata-exchange--http-request-and-message.md) recevra des messages GetResponse.

> [!Note]  
> Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI. WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple. N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .

 

Le message SOAP suivant montre un exemple de message GetResponse.

``` syntax
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope
    xmlns:soap="https://www.w3.org/2003/05/soap-envelope"
    xmlns:wsa="https://schemas.xmlsoap.org/ws/2004/08/addressing"
    xmlns:wsx="https://schemas.xmlsoap.org/ws/2004/09/mex"
    xmlns:wsdp="https://schemas.xmlsoap.org/ws/2006/02/devprof"
    xmlns:sim="https://schemas.example.org/SimpleService"
    xmlns:att="https://schemas.example.org/AttachmentService"
    xmlns:eve="https://schemas.example.org/EventingService">
<soap:Header>
    <wsa:To>
        https://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous
    </wsa:To>
    <wsa:Action>
        https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
    </wsa:Action>
    <wsa:MessageID>
        urn:uuid:119dcdf5-fc0d-4d40-bf1f-de52dc292744
    </wsa:MessageID>
    <wsa:RelatesTo>
        urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
    </wsa:RelatesTo>
</soap:Header>
<soap:Body>
    <wsx:Metadata>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisDevice">
            <wsdp:ThisDevice>
                <wsdp:FriendlyName>
                    WSDAPI Basic Interop Server
                </wsdp:FriendlyName>
                <wsdp:FirmwareVersion>alpha</wsdp:FirmwareVersion>
                <wsdp:SerialNumber>1</wsdp:SerialNumber>
            </wsdp:ThisDevice>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/ThisModel">
            <wsdp:ThisModel>
                <wsdp:Manufacturer>
                    Microsoft
                </wsdp:Manufacturer>
                <wsdp:ManufacturerUrl>
                    https://www.microsoft.com/
                </wsdp:ManufacturerUrl>
                <wsdp:ModelName>
                    WSDAPI Interop device
                </wsdp:ModelName>
                <wsdp:ModelNumber>0.1</wsdp:ModelNumber>
                <wsdp:ModelUrl>
                    https://www.microsoft.com/
                </wsdp:ModelUrl>
                <wsdp:PresentationUrl>
                    https://www.microsoft.com/
                </wsdp:PresentationUrl>
            </wsdp:ThisModel>
        </wsx:MetadataSection>
        <wsx:MetadataSection Dialect="https://schemas.xmlsoap.org/ws/2006/02/devprof/Relationship">
            <wsdp:Relationship Type="https://schemas.xmlsoap.org/ws/2006/02/devprof/host">
                <wsdp:Host>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleDeviceType</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleDevice
                    </wsdp:ServiceId>
                </wsdp:Host>
                <wsdp:Hosted>
                    <wsa:EndpointReference>
                        <wsa:Address>
                            https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
                        </wsa:Address>
                    </wsa:EndpointReference>
                    <wsdp:Types>sim:SimpleService</wsdp:Types>
                    <wsdp:ServiceId>
                        https://testdevice.interop/SimpleService1
                    </wsdp:ServiceId>
                </wsdp:Hosted>
            </wsdp:Relationship>
        </wsx:MetadataSection>
    </wsx:Metadata>
</soap:Body>
</soap:Envelope>
```

Un message GetResponse a les points de focus suivants.



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
<td>GetResponse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2004/09/transfer/GetResponse
</wsa:Action></code></pre></td>
<td>L’action GetResponse SOAP identifie le message en tant que message GetResponse.</td>
</tr>
<tr class="even">
<td>RelatesTo</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:RelatesTo>
    urn:uuid:027bec45-c37c-466c-936c-68f648abe2bb
</wsa:RelatesTo></code></pre></td>
<td>Identificateur du message auquel l’appareil répond. Cet en-tête correspond à MessageID dans le message d' <a href="get--metadata-exchange--http-request-and-message.md">extraction</a> .</td>
</tr>
<tr class="odd">
<td>Adresse</td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    https://192.168.0.2:5357/37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td>Contient l’adresse du point de terminaison des services hébergés sur cet appareil.</td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Détection et messages d’échange de métadonnées](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[Obtenir le message.](get--metadata-exchange--http-request-and-message.md)
</dt> </dl>

 

 



