---
description: AppSequence les informations contenues dans WS-Discovery annonce et les messages de réponse (Hello, messages ProbeMatches et ResolveMatches).
ms.assetid: f54eaa09-7ce8-4948-a0c5-edf2d054f6d5
title: Règles de validation AppSequence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ea44c1ee2d157608ddd1756e71d7183f310df87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528593"
---
# <a name="appsequence-validation-rules"></a><span data-ttu-id="200b7-103">Règles de validation AppSequence</span><span class="sxs-lookup"><span data-stu-id="200b7-103">AppSequence Validation Rules</span></span>

<span data-ttu-id="200b7-104">AppSequence les informations contenues dans WS-Discovery annonce et les messages de réponse ([Hello](hello-message.md), [messages ProbeMatches](probematches-message.md)et [ResolveMatches](resolvematches-message.md)).</span><span class="sxs-lookup"><span data-stu-id="200b7-104">AppSequence information contained in WS-Discovery announcement and response messages ([Hello](hello-message.md), [ProbeMatches](probematches-message.md), and [ResolveMatches](resolvematches-message.md)).</span></span> <span data-ttu-id="200b7-105">Ces informations sont traitées et validées par WSDAPI avant que ces messages ne soient transmis aux composants situés au-dessus de la pile (tels que l’Explorateur réseau ou une application qui appelle WSDAPI).</span><span class="sxs-lookup"><span data-stu-id="200b7-105">This information is processed and validated by WSDAPI before these messages are passed on to components above the stack (such as Network Explorer or an application calling into WSDAPI).</span></span>

<span data-ttu-id="200b7-106">Le code XML suivant montre un exemple d’élément AppSequence.</span><span class="sxs-lookup"><span data-stu-id="200b7-106">The following XML shows a sample AppSequence element.</span></span> <span data-ttu-id="200b7-107">Le préfixe WSD fait référence à l’espace de noms `https://schemas.xmlsoap.org/ws/2005/04/discovery` .</span><span class="sxs-lookup"><span data-stu-id="200b7-107">The wsd prefix refers to the namespace `https://schemas.xmlsoap.org/ws/2005/04/discovery`.</span></span>

``` syntax
<wsd:AppSequence InstanceId="2"
    SequenceId="urn:uuid:369a7d7b-5f87-48a4-aa9a-189edf2a8772"
    MessageNumber="21">
</wsd:AppSequence>
```

<span data-ttu-id="200b7-108">WSDAPI ignore les messages périmés.</span><span class="sxs-lookup"><span data-stu-id="200b7-108">WSDAPI ignores stale messages.</span></span> <span data-ttu-id="200b7-109">Pour chaque périphérique (identifié de façon unique par l’adresse du point de terminaison dans le corps SOAP), WSDAPI ignore les messages avec un MessageNumber AppSequence inférieur au dernier message vu.</span><span class="sxs-lookup"><span data-stu-id="200b7-109">For each device (uniquely identified by the Endpoint Address in the SOAP Body), WSDAPI ignores any messages with an AppSequence MessageNumber lower than the last message seen.</span></span>

<span data-ttu-id="200b7-110">WSDAPI ignore les annonces XAddr obsolètes.</span><span class="sxs-lookup"><span data-stu-id="200b7-110">WSDAPI ignores stale XAddr announcements.</span></span> <span data-ttu-id="200b7-111">Si l’ID d’instance de AppSequence est inférieur au dernier InstanceId vu, WSDAPI ignore le XAddrs publié dans le corps SOAP.</span><span class="sxs-lookup"><span data-stu-id="200b7-111">If the AppSequence InstanceId is lower than the last InstanceId seen, WSDAPI ignores the XAddrs advertised in the SOAP body.</span></span> <span data-ttu-id="200b7-112">En outre, si l’InstanceId est le même que le précédent, mais que MetadataVersion est inférieur au dernier MetadataVersion, WSDAPI ignore le XAddrs.</span><span class="sxs-lookup"><span data-stu-id="200b7-112">Also, if the InstanceId is the same as previous but the MetadataVersion is lower than the last MetadataVersion, WSDAPI ignores the XAddrs.</span></span>

<span data-ttu-id="200b7-113">WSDAPI ignore les messages de WS-Discovery dupliqués.</span><span class="sxs-lookup"><span data-stu-id="200b7-113">WSDAPI ignores duplicate WS-Discovery messages.</span></span> <span data-ttu-id="200b7-114">Si deux messages WS-Discovery identiques sont envoyés au WSDAPI, seule la première reçue sera traitée.</span><span class="sxs-lookup"><span data-stu-id="200b7-114">If two identical WS-Discovery messages are sent to WSDAPI, only the first received will be processed.</span></span> <span data-ttu-id="200b7-115">Cela s’applique en général uniquement aux applications qui appellent directement dans les interfaces [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) ou [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) .</span><span class="sxs-lookup"><span data-stu-id="200b7-115">This is typically only relevant for applications that call directly into the [**IWSDiscoveryPublisher**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoverypublisher) or [**IWSDiscoveryProvider**](/windows/desktop/api/WsdDisco/nn-wsddisco-iwsdiscoveryprovider) interfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="200b7-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="200b7-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="200b7-117">Modèles de message d’échange de métadonnées et de découverte</span><span class="sxs-lookup"><span data-stu-id="200b7-117">Discovery and Metadata Exchange Message Patterns</span></span>](discovery-and-metadata-exchange-message-patterns.md)
</dt> </dl>

 

 



