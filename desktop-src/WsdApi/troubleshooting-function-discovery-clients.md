---
description: Répertorie les procédures de diagnostic à utiliser lors du dépannage des clients de découverte de fonctions.
ms.assetid: e488882a-fadd-4150-89ef-b958c3df34c6
title: Résolution des problèmes des clients de découverte des fonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a44c17b269a604efa1f5f999dff22211cee24f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753668"
---
# <a name="troubleshooting-function-discovery-clients"></a><span data-ttu-id="a94b3-103">Résolution des problèmes des clients de découverte des fonctions</span><span class="sxs-lookup"><span data-stu-id="a94b3-103">Troubleshooting Function Discovery Clients</span></span>

<span data-ttu-id="a94b3-104">Clients de découverte de fonction :</span><span class="sxs-lookup"><span data-stu-id="a94b3-104">Function Discovery clients:</span></span>

-   <span data-ttu-id="a94b3-105">Toujours utiliser les WS-Discovery UDP pour la découverte des appareils</span><span class="sxs-lookup"><span data-stu-id="a94b3-105">Always use UDP WS-Discovery for device discovery</span></span>
-   <span data-ttu-id="a94b3-106">Toujours initier des connexions HTTP ou HTTPs pour l’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="a94b3-106">Always initiate HTTP or HTTPS connections for metadata exchange</span></span>
-   <span data-ttu-id="a94b3-107">Utilisez parfois la découverte dirigée</span><span class="sxs-lookup"><span data-stu-id="a94b3-107">Sometimes use directed discovery</span></span>
-   <span data-ttu-id="a94b3-108">Utilisez parfois un canal sécurisé (HTTPs) pour l’échange de métadonnées</span><span class="sxs-lookup"><span data-stu-id="a94b3-108">Sometimes use a secure channel (HTTPS) for metadata exchange</span></span>

<span data-ttu-id="a94b3-109">La liste suivante présente la séquence classique des messages envoyés et reçus par les clients de détection de fonction.</span><span class="sxs-lookup"><span data-stu-id="a94b3-109">The following list shows the typical sequence of messages sent and received by Function Discovery clients.</span></span> <span data-ttu-id="a94b3-110">Tous les messages ne sont pas obligatoires.</span><span class="sxs-lookup"><span data-stu-id="a94b3-110">Not all messages are mandatory.</span></span>

1.  <span data-ttu-id="a94b3-111">Le client envoie un message de [sondage](probe-message.md) pour détecter les appareils et les services.</span><span class="sxs-lookup"><span data-stu-id="a94b3-111">The client sends a [Probe](probe-message.md) message to discover devices and services.</span></span> <span data-ttu-id="a94b3-112">Si le client utilise la découverte dirigée, ce message est envoyé via HTTP ou HTTPs ; dans le cas contraire, le message est envoyé par la multidiffusion UDP au port 3702.</span><span class="sxs-lookup"><span data-stu-id="a94b3-112">If the client is using directed discovery then this message is sent over HTTP or HTTPS; otherwise, the message is sent by UDP multicast to port 3702.</span></span>
2.  <span data-ttu-id="a94b3-113">Le client reçoit des messages [messages ProbeMatches](probematches-message.md) à partir des appareils ou services correspondants.</span><span class="sxs-lookup"><span data-stu-id="a94b3-113">The client receives [ProbeMatches](probematches-message.md) messages from matching devices or services.</span></span> <span data-ttu-id="a94b3-114">Les messages de découverte dirigée sont envoyés via HTTP ou HTTPs. dans le cas contraire, ces messages sont envoyés par la monodiffusion UDP et proviennent du port 3702.</span><span class="sxs-lookup"><span data-stu-id="a94b3-114">Directed discovery messages are sent over HTTP or HTTPS; otherwise, these messages are sent by UDP unicast and originate from port 3702.</span></span>
3.  <span data-ttu-id="a94b3-115">Si aucun XAddrs n’a été inclus dans le message messages ProbeMatches, le client enverra un message de [résolution](resolve-message.md) par multidiffusion UDP au port 3702.</span><span class="sxs-lookup"><span data-stu-id="a94b3-115">If no XAddrs were included in the ProbeMatches message, then the client will send a [Resolve](resolve-message.md) message by UDP multicast to port 3702.</span></span>
4.  <span data-ttu-id="a94b3-116">Si un message de [résolution](resolve-message.md) a été envoyé, le client reçoit un message [ResolveMatches](resolvematches-message.md) à partir de services correspondants.</span><span class="sxs-lookup"><span data-stu-id="a94b3-116">If a [Resolve](resolve-message.md) message was sent, then the client receives a [ResolveMatches](resolvematches-message.md) message from matching services.</span></span> <span data-ttu-id="a94b3-117">Ce message est envoyé par la monodiffusion UDP du port 3702 vers le port d’origine du message de résolution.</span><span class="sxs-lookup"><span data-stu-id="a94b3-117">This message is sent by UDP unicast from port 3702 to the port where the Resolve message originated.</span></span>
5.  <span data-ttu-id="a94b3-118">Le client envoie un message d' [extraction](get--metadata-exchange--http-request-and-message.md) pour demander des métadonnées à partir de l’appareil ou du service.</span><span class="sxs-lookup"><span data-stu-id="a94b3-118">The client sends a [Get](get--metadata-exchange--http-request-and-message.md) message to request metadata from the device or service.</span></span> <span data-ttu-id="a94b3-119">Ce message est envoyé par HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="a94b3-119">This message is sent by HTTP or HTTPS.</span></span>
6.  <span data-ttu-id="a94b3-120">Le client reçoit un message [GetResponse](getresponse--metadata-exchange--message.md) avec les métadonnées du périphérique ou du service.</span><span class="sxs-lookup"><span data-stu-id="a94b3-120">The client receives a [GetResponse](getresponse--metadata-exchange--message.md) message with the device or service metadata.</span></span> <span data-ttu-id="a94b3-121">Ce message est envoyé par HTTP ou HTTPs.</span><span class="sxs-lookup"><span data-stu-id="a94b3-121">This message is sent by HTTP or HTTPS.</span></span>

<span data-ttu-id="a94b3-122">Les procédures de diagnostic suivantes doivent être utilisées (dans l’ordre) pour aider à identifier les problèmes liés à un client de découverte de fonctions.</span><span class="sxs-lookup"><span data-stu-id="a94b3-122">The following diagnostic procedures should be used (in order) to help identify problems with a Function Discovery client.</span></span>

<span data-ttu-id="a94b3-123">**Pour dépanner un client de découverte de fonctions**</span><span class="sxs-lookup"><span data-stu-id="a94b3-123">**To troubleshoot a Function Discovery client**</span></span>

1.  <span data-ttu-id="a94b3-124">Si la découverte dirigée est utilisée, [résolvez les problèmes de détection dirigée](troubleshooting-applications-using-directed-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-124">If directed discovery is used, [troubleshoot directed discovery](troubleshooting-applications-using-directed-discovery.md).</span></span>
2.  <span data-ttu-id="a94b3-125">[Inspectez les paramètres de l’adaptateur et du pare-feu](inspecting-adapter-and-firewall-settings.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-125">[Inspect adapter and firewall settings](inspecting-adapter-and-firewall-settings.md).</span></span>
3.  <span data-ttu-id="a94b3-126">[Utilisez un hôte et un client génériques pour UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-126">[Use a generic host and client for UDP WS-Discovery](using-a-generic-host-and-client-for-udp-ws-discovery.md).</span></span>
4.  <span data-ttu-id="a94b3-127">[Utilisez le client de débogage WSD pour vérifier le trafic de multidiffusion](using-wsddebug-client-to-verify-multicast-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-127">[Use WSD Debug Client to verify multicast traffic](using-wsddebug-client-to-verify-multicast-traffic.md).</span></span>
5.  <span data-ttu-id="a94b3-128">[Inspectez les suivis réseau pour le service WS-Discovery UDP](inspecting-network-traces-for-udp-ws-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-128">[Inspect network traces for UDP WS-Discovery](inspecting-network-traces-for-udp-ws-discovery.md).</span></span>
6.  <span data-ttu-id="a94b3-129">[Utilisez un hôte et un client génériques pour l’échange de métadonnées http](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-129">[Use a generic host and client for HTTP metadata exchange](using-a-generic-host-and-client-for-http-metadata-exchange.md).</span></span>
7.  <span data-ttu-id="a94b3-130">[Utilisez la journalisation WinHTTP pour vérifier le trafic d’extraction](using-winhttp-logging-to-verify-get-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-130">[Use WinHTTP logging to verify Get traffic](using-winhttp-logging-to-verify-get-traffic.md).</span></span>
8.  <span data-ttu-id="a94b3-131">[Inspectez les traces réseau pour l’échange de métadonnées http](inspecting-network-traces-for-http-metadata-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="a94b3-131">[Inspect network traces for HTTP metadata exchange](inspecting-network-traces-for-http-metadata-exchange.md).</span></span>

<span data-ttu-id="a94b3-132">Si la source du problème ne peut pas être identifiée à l’aide des procédures de diagnostic ci-dessus, suivez les instructions de la procédure d' [activation du suivi wsdapi](enabling-wsdapi-tracing.md) et contactez le support Microsoft.</span><span class="sxs-lookup"><span data-stu-id="a94b3-132">If the source of the problem cannot be identified using the above diagnostic procedures, follow the directions in [Enabling WSDAPI Tracing](enabling-wsdapi-tracing.md) and contact Microsoft support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a94b3-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a94b3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a94b3-134">Résolution des problèmes de Prise en main avec WSDAPI</span><span class="sxs-lookup"><span data-stu-id="a94b3-134">Getting Started with WSDAPI Troubleshooting</span></span>](getting-started-with-wsdapi-troubleshooting.md)
</dt> </dl>

 

 



