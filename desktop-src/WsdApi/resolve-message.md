---
description: Message WS-Discovery utilisé par un client pour rechercher des services sur le réseau par nom.
ms.assetid: b963bd2a-47cb-4f8d-8272-a586e6d6a047
title: Résoudre le message
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3390d97aad972f001b98587c6b5e7cd7ac708b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524990"
---
# <a name="resolve-message"></a><span data-ttu-id="7752c-103">Résoudre le message</span><span class="sxs-lookup"><span data-stu-id="7752c-103">Resolve Message</span></span>

<span data-ttu-id="7752c-104">Un message de résolution est un message d' WS-Discovery utilisé par un client pour rechercher des services sur le réseau par nom.</span><span class="sxs-lookup"><span data-stu-id="7752c-104">A Resolve message is a WS-Discovery message used by a client to search for services on the network by name.</span></span> <span data-ttu-id="7752c-105">Un client envoie un message de résolution uniquement lorsqu’un message HTTP (par exemple, une demande d’échange de métadonnées ou un [message de service](get--metadata-exchange--http-request-and-message.md) ) est envoyé.</span><span class="sxs-lookup"><span data-stu-id="7752c-105">A client will only send a Resolve message when an HTTP message (such as a [Get](get--metadata-exchange--http-request-and-message.md) metadata exchange request or a service message) will be sent.</span></span> <span data-ttu-id="7752c-106">Pour plus d’informations sur la résolution des messages, consultez la section 6,1 de la [spécification WS-Discovery](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span><span class="sxs-lookup"><span data-stu-id="7752c-106">For more information about Resolve messages, see section 6.1 of the [WS-Discovery Specification](https://specs.xmlsoap.org/ws/2005/04/discovery/ws-discovery.pdf).</span></span>

<span data-ttu-id="7752c-107">Un message de résolution est envoyé par la multidiffusion UDP au port 3702.</span><span class="sxs-lookup"><span data-stu-id="7752c-107">A Resolve message is sent by UDP multicast to port 3702.</span></span> <span data-ttu-id="7752c-108">Les messages de résolution de monodiffusion ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="7752c-108">Unicast Resolve messages are not supported.</span></span>

<span data-ttu-id="7752c-109">Les clients DPWS envoient des messages de résolution.</span><span class="sxs-lookup"><span data-stu-id="7752c-109">DPWS clients send Resolve messages.</span></span> <span data-ttu-id="7752c-110">La liste suivante répertorie les scénarios dans lesquels WSDAPI envoie un message de résolution.</span><span class="sxs-lookup"><span data-stu-id="7752c-110">The following list shows scenarios in which WSDAPI will send a Resolve message.</span></span>

-   <span data-ttu-id="7752c-111">Un client de découverte de fonction envoie un message de résolution si aucun XAddrs n’est inclus dans un message [messages ProbeMatches](probematches-message.md) .</span><span class="sxs-lookup"><span data-stu-id="7752c-111">A Function Discovery client sends a Resolve message if no XAddrs are included in a [ProbeMatches](probematches-message.md) message.</span></span>
-   <span data-ttu-id="7752c-112">Un client qui appelle les méthodes [**IWSDiscoveryProvider :: SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) envoie un message de résolution.</span><span class="sxs-lookup"><span data-stu-id="7752c-112">A client calling the [**IWSDiscoveryProvider::SearchById**](/windows/desktop/api/WsdDisco/nf-wsddisco-iwsdiscoveryprovider-searchbyid) methods will send a Resolve message.</span></span>
-   <span data-ttu-id="7752c-113">Un client appelant [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) peut envoyer un message de résolution si une adresse d’appareil logique est passée à *pszDeviceId*.</span><span class="sxs-lookup"><span data-stu-id="7752c-113">A client calling [**WSDCreateDeviceProxy**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxy) may send a Resolve message if a logical device address is passed to *pszDeviceId*.</span></span>
-   <span data-ttu-id="7752c-114">Un client qui appelle [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) envoie un message de résolution si la fonction est appelée avec le paramètre pDeviceAddress défini sur **null**.</span><span class="sxs-lookup"><span data-stu-id="7752c-114">A client calling [**WSDCreateDeviceProxyAdvanced**](/windows/desktop/api/WsdClient/nf-wsdclient-wsdcreatedeviceproxyadvanced) will send a Resolve message if the function is called with the pDeviceAddress parameter set to **NULL**.</span></span>

> [!Note]  
> <span data-ttu-id="7752c-115">Cette rubrique montre un exemple de message DPWS généré par les hôtes et les clients WSDAPI.</span><span class="sxs-lookup"><span data-stu-id="7752c-115">This topic shows a sample DPWS message generated by WSDAPI clients and hosts.</span></span> <span data-ttu-id="7752c-116">WSDAPI analyse et accepte d’autres messages conformes à DPWS qui ne sont pas conformes à cet exemple.</span><span class="sxs-lookup"><span data-stu-id="7752c-116">WSDAPI will parse and accept other DPWS-compliant messages that do not conform to this sample.</span></span> <span data-ttu-id="7752c-117">N’utilisez pas cet exemple pour vérifier l’interopérabilité DPWS. Utilisez à la place l' [outil wsdapi Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) .</span><span class="sxs-lookup"><span data-stu-id="7752c-117">Do not use this sample to verify DPWS interoperability; use the [WSDAPI Basic Interoperability Tool (WSDBIT)](https://msdn.microsoft.com/library/cc264250.aspx) instead.</span></span>

 

<span data-ttu-id="7752c-118">Le message SOAP suivant montre un exemple de message de résolution.</span><span class="sxs-lookup"><span data-stu-id="7752c-118">The following SOAP message shows a sample Resolve message.</span></span>

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

<span data-ttu-id="7752c-119">Un message de résolution a les points de focalisation suivants.</span><span class="sxs-lookup"><span data-stu-id="7752c-119">A Resolve message has the following focus points.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7752c-120">Point de focus</span><span class="sxs-lookup"><span data-stu-id="7752c-120">Focus point</span></span></th>
<th><span data-ttu-id="7752c-121">XML</span><span class="sxs-lookup"><span data-stu-id="7752c-121">XML</span></span></th>
<th><span data-ttu-id="7752c-122">Description</span><span class="sxs-lookup"><span data-stu-id="7752c-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7752c-123">Résoudre</span><span class="sxs-lookup"><span data-stu-id="7752c-123">Resolve</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Action>
    https://schemas.xmlsoap.org/ws/2005/04/discovery/Resolve
</wsa:Action></code></pre></td>
<td><span data-ttu-id="7752c-124">L’action Resolve SOAP identifie le message en tant que message de résolution.</span><span class="sxs-lookup"><span data-stu-id="7752c-124">The Resolve SOAP action identifies the message as a Resolve message.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7752c-125">MessageID</span><span class="sxs-lookup"><span data-stu-id="7752c-125">MessageID</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:MessageID>
    urn:uuid:38d1c3d9-8d73-4424-8861-6b7ee2af24d3
</wsa:MessageID></code></pre></td>
<td><span data-ttu-id="7752c-126">Contient l’identificateur de message, qui est référencé dans un message <a href="resolvematches-message.md">ResolveMatches</a> .</span><span class="sxs-lookup"><span data-stu-id="7752c-126">Contains the message identifier, which is referenced in a <a href="resolvematches-message.md">ResolveMatches</a> message.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7752c-127">Adresse</span><span class="sxs-lookup"><span data-stu-id="7752c-127">Address</span></span></td>
<td><pre class="syntax" data-space="preserve"><code><wsa:Address>
    urn:uuid:37f86d35-e6ac-4241-964f-1d9ae46fb366
</wsa:Address></code></pre></td>
<td><span data-ttu-id="7752c-128">Contient l’adresse du point de terminaison qui est résolu.</span><span class="sxs-lookup"><span data-stu-id="7752c-128">Contains the address of the endpoint being resolved.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7752c-129">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7752c-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7752c-130">Détection et messages d’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="7752c-130">Discovery and Metadata Exchange Messages</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> <dt>

[<span data-ttu-id="7752c-131">Message ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="7752c-131">ResolveMatches Message</span></span>](resolvematches-message.md)
</dt> </dl>

 

 



