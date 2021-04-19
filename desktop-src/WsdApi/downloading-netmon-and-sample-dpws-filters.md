---
description: Moniteur réseau Microsoft 3 (NetMon) est un analyseur de paquets utilisé pour inspecter le trafic réseau.
ms.assetid: 015a6a6d-9e07-4f22-b931-dcce77051bef
title: Téléchargement de Netmon et des exemples de filtres DPWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47790b26164ec0ed2792d1d1e1f2ad4ba5d77d38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531870"
---
# <a name="downloading-netmon-and-sample-dpws-filters"></a><span data-ttu-id="64e75-103">Téléchargement de Netmon et des exemples de filtres DPWS</span><span class="sxs-lookup"><span data-stu-id="64e75-103">Downloading Netmon and Sample DPWS Filters</span></span>

<span data-ttu-id="64e75-104">Moniteur réseau Microsoft 3 (NetMon) est un analyseur de paquets utilisé pour inspecter le trafic réseau.</span><span class="sxs-lookup"><span data-stu-id="64e75-104">Microsoft Network Monitor 3 (Netmon) is a packet analyzer used to inspect network traffic.</span></span> <span data-ttu-id="64e75-105">Vous devez télécharger Netmon avant de suivre les étapes de dépannage indiquées dans [inspection des suivis réseau pour UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) et [inspecter les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md) .</span><span class="sxs-lookup"><span data-stu-id="64e75-105">Netmon must be downloaded before the troubleshooting steps given in [Inspecting Network Traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md) and [Inspecting Network Traces for HTTP Metadata Exchange](inspecting-network-traces-for-http-metadata-exchange.md) can be followed.</span></span> <span data-ttu-id="64e75-106">Une fois Netmon téléchargé, vous pouvez utiliser des filtres DPWS pour isoler le trafic concerné.</span><span class="sxs-lookup"><span data-stu-id="64e75-106">After Netmon has been downloaded, DPWS filters can be used to help isolate traffic of interest.</span></span>

## <a name="downloading-netmon"></a><span data-ttu-id="64e75-107">Téléchargement de NetMon</span><span class="sxs-lookup"><span data-stu-id="64e75-107">Downloading Netmon</span></span>

<span data-ttu-id="64e75-108">Pour télécharger NetMon, accédez à [Moniteur réseau Microsoft](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) et suivez les instructions.</span><span class="sxs-lookup"><span data-stu-id="64e75-108">To download Netmon, go to [Microsoft Network Monitor](https://www.microsoft.com/downloads/details.aspx?displaylang=en&FamilyID=983b941d-06cb-4658-b7f6-3088333d062f) and follow the instructions.</span></span> <span data-ttu-id="64e75-109">Pour plus d’informations sur NetMon, consultez « informations sur Moniteur réseau 3,0 » dans la base de connaissances de l’aide et du support à l’adresse [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="64e75-109">For more information about Netmon, see "Information about Network Monitor 3.0" in the Help and Support Knowledge Base at [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

## <a name="sample-dpws-filters"></a><span data-ttu-id="64e75-110">Exemples de filtres DPWS</span><span class="sxs-lookup"><span data-stu-id="64e75-110">Sample DPWS Filters</span></span>

<span data-ttu-id="64e75-111">Parfois, la résolution des problèmes d’échange de WS-Discovery et de métadonnées doit avoir lieu sur un réseau occupé.</span><span class="sxs-lookup"><span data-stu-id="64e75-111">Sometimes, WS-Discovery and metadata exchange troubleshooting must take place on a busy network.</span></span> <span data-ttu-id="64e75-112">Les exemples de filtres peuvent être utilisés pour limiter la sortie Netmon au trafic qui vous intéresse.</span><span class="sxs-lookup"><span data-stu-id="64e75-112">The sample filters can be used to help limit the Netmon output to traffic of interest.</span></span> <span data-ttu-id="64e75-113">Pour plus d’informations sur l’utilisation des filtres NetMon, consultez [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741) .</span><span class="sxs-lookup"><span data-stu-id="64e75-113">For more information about using Netmon filters, see [https://support.microsoft.com/kb/933741](https://support.microsoft.com/kb/933741).</span></span>

<span data-ttu-id="64e75-114">L’exemple suivant montre un filtre qui limite la sortie à tout le trafic de diffusion WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="64e75-114">The following example shows a filter that limits output to all broadcast WS-Discovery traffic.</span></span>

> [!Note]  
> <span data-ttu-id="64e75-115">Ce filtre ne capture pas le trafic des piles qui ne répondent pas aux messages de multidiffusion WS-Discovery qui proviennent du port 3702.</span><span class="sxs-lookup"><span data-stu-id="64e75-115">This filter does not capture traffic from stacks that do not respond to multicast WS-Discovery messages that originate at port 3702.</span></span> <span data-ttu-id="64e75-116">Si une telle pile est utilisée, vous devez modifier cet exemple de filtre avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="64e75-116">If such a stack is being used, then this sample filter must be modified before use.</span></span>

 

``` syntax
// All broadcast WS-Discovery traffic
UDP.Port == 3702
```

<span data-ttu-id="64e75-117">L’exemple suivant illustre un filtre qui limite la sortie aux messages HTTP envoyés aux piles WSDAPI sur le port par défaut.</span><span class="sxs-lookup"><span data-stu-id="64e75-117">The following example shows a filter that limits output to HTTP messages sent to WSDAPI stacks on the default port.</span></span>

> [!Note]  
> <span data-ttu-id="64e75-118">Les services peuvent envoyer des messages HTTP pertinents à partir de ports autres que 5357.</span><span class="sxs-lookup"><span data-stu-id="64e75-118">Services may send relevant HTTP messages from ports other than 5357.</span></span> <span data-ttu-id="64e75-119">Si le trafic provenant d’autres ports présente un intérêt, vous devez modifier cet exemple de filtre avant de l’utiliser.</span><span class="sxs-lookup"><span data-stu-id="64e75-119">If traffic from other ports is of interest, then this sample filter must be modified before use.</span></span>

 

``` syntax
// HTTP messages sent to WSDAPI stacks on default port
TCP.Port == 5357
```

<span data-ttu-id="64e75-120">L’exemple suivant illustre un filtre qui limite la sortie au trafic de multidiffusion IPv4.</span><span class="sxs-lookup"><span data-stu-id="64e75-120">The following example shows a filter that limits output to IPv4 multicast traffic.</span></span>

``` syntax
// All IPv4 multicast traffic
IPv4.DestinationAddress == 239.255.255.250
```

<span data-ttu-id="64e75-121">L’exemple suivant illustre un filtre qui limite la sortie au trafic de multidiffusion IPv6.</span><span class="sxs-lookup"><span data-stu-id="64e75-121">The following example shows a filter that limits output to IPv6 multicast traffic.</span></span>

``` syntax
// All IPv6 multicast traffic
IPv6.DestinationAddress == FF02::C
```

<span data-ttu-id="64e75-122">Certains filtres peuvent être combinés pour limiter davantage les résultats.</span><span class="sxs-lookup"><span data-stu-id="64e75-122">Some filters can be combined to further limit results.</span></span> <span data-ttu-id="64e75-123">L’exemple suivant illustre un filtre qui limite la sortie au trafic de multidiffusion IPv4 WS-Discovery.</span><span class="sxs-lookup"><span data-stu-id="64e75-123">The following example shows a filter that limits output to IPv4 multicast WS-Discovery traffic.</span></span>

``` syntax
// All IPv4 multicast WS-Discovery traffic
UDP.Port==3702 && IPv4.DestinationAddress=239.255.255.250
```

<span data-ttu-id="64e75-124">Lorsque ces filtres sont utilisés, le trafic pertinent peut être exclu des résultats Netmon.</span><span class="sxs-lookup"><span data-stu-id="64e75-124">When these filters are used, relevant traffic may be excluded from the Netmon results.</span></span> <span data-ttu-id="64e75-125">Une exclusion peut se produire lorsque les services résident sur des ports autres que les ports par défaut (5357/5358) et lorsqu’une pile DPWS ne répond pas aux messages à l’aide du port par défaut.</span><span class="sxs-lookup"><span data-stu-id="64e75-125">Exclusion can occur when services reside at ports other than the default ports (5357/5358) and when a DPWS stack does not respond to messages using the default port.</span></span> <span data-ttu-id="64e75-126">Dans ce cas, les filtres doivent être modifiés avant d’être utilisés.</span><span class="sxs-lookup"><span data-stu-id="64e75-126">In these cases, the filters must be modified before use.</span></span>

## <a name="related-topics"></a><span data-ttu-id="64e75-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="64e75-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="64e75-128">Procédures de diagnostic WSDAPI</span><span class="sxs-lookup"><span data-stu-id="64e75-128">WSDAPI Diagnostic Procedures</span></span>](wsdapi-diagnostic-procedures.md)
</dt> <dt>

[<span data-ttu-id="64e75-129">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="64e75-129">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



