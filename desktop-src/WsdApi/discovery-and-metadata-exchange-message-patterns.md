---
description: Profil d’appareil pour les hôtes de services Web (DPWS) et les clients communiquent sur le réseau à l’aide d’une série de messages SOAP sur UDP et HTTP.
ms.assetid: 52282990-d993-4034-a791-2ee7c9c1663d
title: Modèles de message d’échange de métadonnées et de découverte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e9a08852c5f25572daf9932afd2ce4b7e03858a
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2021
ms.locfileid: "104211200"
---
# <a name="discovery-and-metadata-exchange-message-patterns"></a><span data-ttu-id="2c06e-103">Modèles de message d’échange de métadonnées et de découverte</span><span class="sxs-lookup"><span data-stu-id="2c06e-103">Discovery and Metadata Exchange Message Patterns</span></span>

<span data-ttu-id="2c06e-104">Profil d’appareil pour les hôtes de services Web (DPWS) et les clients communiquent sur le réseau à l’aide d’une série de messages SOAP sur UDP et HTTP.</span><span class="sxs-lookup"><span data-stu-id="2c06e-104">Device Profile for Web Services (DPWS) hosts and clients communicate over the network using a series of SOAP messages over UDP and HTTP.</span></span>

<span data-ttu-id="2c06e-105">Le diagramme suivant présente une vue d’ensemble du trafic UDP et HTTP attendu entre un hôte et un client DPWS.</span><span class="sxs-lookup"><span data-stu-id="2c06e-105">The following diagram shows an overview of the expected UDP and HTTP traffic between a DPWS host and client.</span></span>

![Diagramme montrant le trafic UDP et HTTP entre un hôte et un client DPWS.](images/ws-discovery-and-metadata-exchange-message-patterns.png)

<span data-ttu-id="2c06e-107">Les messages [Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md)et [obtient](get--metadata-exchange--http-request-and-message.md) sont tous générés sans sollicitation du réseau ; ces messages sont utilisés pour annoncer l’état de l’appareil ou pour émettre une demande de recherche.</span><span class="sxs-lookup"><span data-stu-id="2c06e-107">[Hello](hello-message.md), [Bye](bye-message.md), [Probe](probe-message.md), [Resolve](resolve-message.md), and [Get](get--metadata-exchange--http-request-and-message.md) messages are all generated without network solicitation; these messages are used to announce device state or to issue a search request.</span></span> <span data-ttu-id="2c06e-108">Les messages [messages ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md)et [GetResponse](getresponse--metadata-exchange--message.md) sont générés en réponse à des messages de sondage, de résolution et de récupération.</span><span class="sxs-lookup"><span data-stu-id="2c06e-108">[ProbeMatches](probematches-message.md), [ResolveMatches](resolvematches-message.md), and [GetResponse](getresponse--metadata-exchange--message.md) messages are generated in response to Probe, Resolve and Get messages.</span></span>

<span data-ttu-id="2c06e-109">Les messages [Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md)et [ResolveMatches](resolvematches-message.md) sont toujours exécutés sur UDP.</span><span class="sxs-lookup"><span data-stu-id="2c06e-109">[Hello](hello-message.md), [Bye](bye-message.md), [Resolve](resolve-message.md), and [ResolveMatches](resolvematches-message.md) messages will always occur over UDP.</span></span> <span data-ttu-id="2c06e-110">De même, les messages de métadonnées d' [extraction](get--metadata-exchange--http-request-and-message.md) et [GetResponse](getresponse--metadata-exchange--message.md) sont toujours exécutés sur http ou HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2c06e-110">Similarly, [Get](get--metadata-exchange--http-request-and-message.md) and [GetResponse](getresponse--metadata-exchange--message.md) metadata messages will always occur over HTTP or HTTPS.</span></span> <span data-ttu-id="2c06e-111">Les messages [Probe](probe-message.md) et [messages ProbeMatches](probematches-message.md) sont normalement transmis via UDP, mais ils ont lieu sur une connexion http ou https dans un scénario de découverte dirigée.</span><span class="sxs-lookup"><span data-stu-id="2c06e-111">[Probe](probe-message.md) and [ProbeMatches](probematches-message.md) messages are normally transmitted over UDP, but take place over an HTTP or HTTPS connection in a directed discovery scenario.</span></span> <span data-ttu-id="2c06e-112">Pour plus d’informations sur les modèles de message de découverte dirigée, consultez [Dépannage des applications à l’aide de la découverte dirigée](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="2c06e-112">For more information about directed discovery message patterns, see [Troubleshooting Applications Using Directed Discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>

<span data-ttu-id="2c06e-113">La liste suivante indique la séquence typique de messages sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="2c06e-113">The following list shows the typical sequence of messages on the wire.</span></span> <span data-ttu-id="2c06e-114">Tous les messages ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="2c06e-114">Not all messages are mandatory.</span></span>

1.  [<span data-ttu-id="2c06e-115">Bonjour</span><span class="sxs-lookup"><span data-stu-id="2c06e-115">Hello</span></span>](hello-message.md)
2.  [<span data-ttu-id="2c06e-116">Sonde</span><span class="sxs-lookup"><span data-stu-id="2c06e-116">Probe</span></span>](probe-message.md)
3.  [<span data-ttu-id="2c06e-117">Messages ProbeMatches</span><span class="sxs-lookup"><span data-stu-id="2c06e-117">ProbeMatches</span></span>](probematches-message.md)
4.  [<span data-ttu-id="2c06e-118">Résolution</span><span class="sxs-lookup"><span data-stu-id="2c06e-118">Resolve</span></span>](resolve-message.md)
5.  [<span data-ttu-id="2c06e-119">ResolveMatches</span><span class="sxs-lookup"><span data-stu-id="2c06e-119">ResolveMatches</span></span>](resolvematches-message.md)
6.  <span data-ttu-id="2c06e-120">[Obtenir](get--metadata-exchange--http-request-and-message.md) (demande d’échange de métadonnées)</span><span class="sxs-lookup"><span data-stu-id="2c06e-120">[Get](get--metadata-exchange--http-request-and-message.md) (metadata exchange request)</span></span>
7.  [<span data-ttu-id="2c06e-121">GetResponse</span><span class="sxs-lookup"><span data-stu-id="2c06e-121">GetResponse</span></span>](getresponse--metadata-exchange--message.md)
8.  [<span data-ttu-id="2c06e-122">Adieu</span><span class="sxs-lookup"><span data-stu-id="2c06e-122">Bye</span></span>](bye-message.md)

## <a name="related-topics"></a><span data-ttu-id="2c06e-123">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2c06e-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c06e-124">À propos des services Web sur les appareils</span><span class="sxs-lookup"><span data-stu-id="2c06e-124">About Web Services on Devices</span></span>](about-web-services-for-devices.md)
</dt> </dl>

 

 



