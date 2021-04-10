---
title: Flux de paquets TCP
description: Ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues pendant une session TCP classique.
ms.assetid: 75319c91-f77b-4dec-b94f-36772f1f1d53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2203ccb4b2793983bd5b1052d53c2700d3033a4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940135"
---
# <a name="tcp-packet-flows"></a><span data-ttu-id="2686e-103">Flux de paquets TCP</span><span class="sxs-lookup"><span data-stu-id="2686e-103">TCP Packet Flows</span></span>

<span data-ttu-id="2686e-104">Cette section décrit l’ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues pendant une session TCP classique.</span><span class="sxs-lookup"><span data-stu-id="2686e-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical TCP session.</span></span>

> [!Note]  
> <span data-ttu-id="2686e-105">Les flux de paquets TCP pour IPv6 suivent le même modèle que pour IPv4.</span><span class="sxs-lookup"><span data-stu-id="2686e-105">TCP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="2686e-106">Les flux de paquets non TCP suivent le même modèle que les [flux de paquets UDP](udp-packet-flows.md).</span><span class="sxs-lookup"><span data-stu-id="2686e-106">Non-TCP packet flows follow the same pattern as [UDP packet flows](udp-packet-flows.md).</span></span>

 

## <a name="tcp-connection-establishment"></a><span data-ttu-id="2686e-107">Établissement de la connexion TCP</span><span class="sxs-lookup"><span data-stu-id="2686e-107">TCP Connection Establishment</span></span>

<dl> <span data-ttu-id="2686e-108">Le serveur (récepteur) effectue une ouverture passive</span><span class="sxs-lookup"><span data-stu-id="2686e-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="2686e-109">liaison : FWPM \_ \_ \_ \_ v4 de redirection de liaison ALE \_ de couche (windows 7/Windows Server 2008 R2 uniquement)</span><span class="sxs-lookup"><span data-stu-id="2686e-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="2686e-110">liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_</span><span class="sxs-lookup"><span data-stu-id="2686e-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="2686e-111">écouter : FWPM \_ \_ V4 d' \_ écoute d’authentification ALE \_ de couche \_</span><span class="sxs-lookup"><span data-stu-id="2686e-111">listen: FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V4</span></span>

  
<span data-ttu-id="2686e-112">Le client (expéditeur) effectue une ouverture active</span><span class="sxs-lookup"><span data-stu-id="2686e-112">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="2686e-113">liaison : FWPM \_ \_ \_ \_ v4 de redirection de liaison ALE \_ de couche (windows 7/Windows Server 2008 R2 uniquement)</span><span class="sxs-lookup"><span data-stu-id="2686e-113">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="2686e-114">liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_</span><span class="sxs-lookup"><span data-stu-id="2686e-114">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="2686e-115">connexion : FWPM \_ \_ \_ \_ de redirection de connexion ALE de couche \_ (windows 7/Windows Server 2008 R2 uniquement)</span><span class="sxs-lookup"><span data-stu-id="2686e-115">connect: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="2686e-116">connexion : FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="2686e-116">connect: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="2686e-117">SYN : \_ couche FWPM \_ v4 de \_ transport \_ sortant</span><span class="sxs-lookup"><span data-stu-id="2686e-117">SYN: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-118">SYN : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-118">SYN: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2686e-119">Serveur</span><span class="sxs-lookup"><span data-stu-id="2686e-119">Server</span></span>

-   <span data-ttu-id="2686e-120">SYN : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-120">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2686e-121">SYN : \_ couche FWPM \_ \_ v4 transport entrant \_</span><span class="sxs-lookup"><span data-stu-id="2686e-121">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-122">SYN : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-122">SYN: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="2686e-123">SYN-ACK : \_ couche FWPM \_ v4 de \_ transport \_ sortant</span><span class="sxs-lookup"><span data-stu-id="2686e-123">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-124">SYN-ACK : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-124">SYN-ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2686e-125">Client</span><span class="sxs-lookup"><span data-stu-id="2686e-125">Client</span></span>

-   <span data-ttu-id="2686e-126">SYN-ACK : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-126">SYN-ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2686e-127">SYN-ACK : \_ transport entrant de couche FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-127">SYN-ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-128">FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_</span><span class="sxs-lookup"><span data-stu-id="2686e-128">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="2686e-129">ACK : \_ couche FWPM \_ v4 de \_ transport \_ sortant</span><span class="sxs-lookup"><span data-stu-id="2686e-129">ACK: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-130">ACK : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-130">ACK: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2686e-131">Serveur</span><span class="sxs-lookup"><span data-stu-id="2686e-131">Server</span></span>

-   <span data-ttu-id="2686e-132">ACK : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-132">ACK: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2686e-133">ACK : \_ couche FWPM \_ \_ v4 transport entrant \_</span><span class="sxs-lookup"><span data-stu-id="2686e-133">ACK: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-134">FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_</span><span class="sxs-lookup"><span data-stu-id="2686e-134">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="2686e-135">Listen est terminé.</span><span class="sxs-lookup"><span data-stu-id="2686e-135">Listen completes.</span></span> <span data-ttu-id="2686e-136">Le serveur peut effectuer une acceptation.</span><span class="sxs-lookup"><span data-stu-id="2686e-136">Server can perform an accept.</span></span>

  
</dl>

## <a name="tcp-syn-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="2686e-137">TCP SYN reçu sans écoute sur le port ou le protocole</span><span class="sxs-lookup"><span data-stu-id="2686e-137">TCP SYN Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="2686e-138">Serveur (récepteur)</span><span class="sxs-lookup"><span data-stu-id="2686e-138">Server (receiver)</span></span>

-   <span data-ttu-id="2686e-139">SYN : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-139">SYN: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2686e-140">SYN : \_ couche FWPM \_ \_ v4 transport entrant \_ \_ rejeté</span><span class="sxs-lookup"><span data-stu-id="2686e-140">SYN: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4\_DISCARD</span></span>
-   <span data-ttu-id="2686e-141">RST : \_ transport sortant de couche FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-141">RST: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-142">RST : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-142">RST: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="2686e-143">TCP SYN sans point de terminaison est indiqué dans TRANSPORT ignore avec une condition d’erreur spécifique.</span><span class="sxs-lookup"><span data-stu-id="2686e-143">TCP SYN with no endpoint is indicated at TRANSPORT discard with a specific error condition.</span></span> <span data-ttu-id="2686e-144">Bloquer ce paquet au niveau du TRANSPORT rejeté pour empêcher la pile d’envoyer l’événement correspondant (RST).</span><span class="sxs-lookup"><span data-stu-id="2686e-144">Block this packet at TRANSPORT discard to cause the stack not to send the corresponding event (RST).</span></span> <span data-ttu-id="2686e-145">Pour obtenir un exemple de filtrage en mode furtif, consultez [prévention de l’analyse des ports](preventing-port-scanning.md).</span><span class="sxs-lookup"><span data-stu-id="2686e-145">For an example of stealth-mode filtering, see [Preventing Port Scanning](preventing-port-scanning.md).</span></span>

 

## <a name="data-transmitted-over-a-tcp-connection"></a><span data-ttu-id="2686e-146">Données transmises via une connexion TCP</span><span class="sxs-lookup"><span data-stu-id="2686e-146">Data Transmitted Over a TCP Connection</span></span>

<dl> <span data-ttu-id="2686e-147">Client (expéditeur)</span><span class="sxs-lookup"><span data-stu-id="2686e-147">Client (sender)</span></span>

-   <span data-ttu-id="2686e-148">Envoyer</span><span class="sxs-lookup"><span data-stu-id="2686e-148">send</span></span>
-   <span data-ttu-id="2686e-149">données : FWPM \_ de \_ flux de couche \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-149">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="2686e-150">Segments TCP : FWPM \_ couche de \_ \_ transport sortant \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-150">TCP segments: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-151">Datagrammes IP : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-151">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="2686e-152">Serveur (récepteur)</span><span class="sxs-lookup"><span data-stu-id="2686e-152">Server (receiver)</span></span>

-   <span data-ttu-id="2686e-153">Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-153">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2686e-154">Segments TCP : FWPM \_ couche de \_ \_ transport entrant \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-154">TCP segments: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-155">données : FWPM \_ de \_ flux de couche \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-155">data: FWPM\_LAYER\_STREAM\_V4</span></span>
-   <span data-ttu-id="2686e-156">Les données sont disponibles pour la lecture.</span><span class="sxs-lookup"><span data-stu-id="2686e-156">Data is available to read.</span></span>

  
</dl>

## <a name="successful-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="2686e-157">Réautorisation réussie d’un paquet TCP</span><span class="sxs-lookup"><span data-stu-id="2686e-157">Successful Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="2686e-158">Serveur (récepteur)</span><span class="sxs-lookup"><span data-stu-id="2686e-158">Server (receiver)</span></span>

-   <span data-ttu-id="2686e-159">Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-159">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2686e-160">Segment TCP : \_ couche FWPM \_ \_ v4 transport entrant \_</span><span class="sxs-lookup"><span data-stu-id="2686e-160">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-161">Segment TCP : FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues accepter la \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-161">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="2686e-162">données : FWPM \_ \_ de flux \_ de couche V4 (entrant)</span><span class="sxs-lookup"><span data-stu-id="2686e-162">data: FWPM\_LAYER\_STREAM\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-tcp-packet"></a><span data-ttu-id="2686e-163">Échec de la réautorisation d’un paquet TCP</span><span class="sxs-lookup"><span data-stu-id="2686e-163">Failed Reauthorization of a TCP Packet</span></span>

<span data-ttu-id="2686e-164">Serveur (récepteur)</span><span class="sxs-lookup"><span data-stu-id="2686e-164">Server (receiver)</span></span>

-   <span data-ttu-id="2686e-165">Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-165">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="2686e-166">Segment TCP : \_ couche FWPM \_ \_ v4 transport entrant \_</span><span class="sxs-lookup"><span data-stu-id="2686e-166">TCP segment: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="2686e-167">Segment TCP : FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues accepter la \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="2686e-167">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="2686e-168">Segment TCP : FWPM \_ V4 d’authentification ALE de la couche \_ ALE \_ \_ \_ \_ \_ ignorée</span><span class="sxs-lookup"><span data-stu-id="2686e-168">TCP segment: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="tcp-connection-termination"></a><span data-ttu-id="2686e-169">Arrêt de la connexion TCP</span><span class="sxs-lookup"><span data-stu-id="2686e-169">TCP Connection Termination</span></span>

<span data-ttu-id="2686e-170">L’arrêt de la connexion TCP n’est pas indiqué dans une couche WFP.</span><span class="sxs-lookup"><span data-stu-id="2686e-170">TCP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2686e-171">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="2686e-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2686e-172">Réautorisation ALE</span><span class="sxs-lookup"><span data-stu-id="2686e-172">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="2686e-173">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="2686e-173">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




