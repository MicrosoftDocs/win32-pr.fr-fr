---
title: Flux de paquets UDP
description: Ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues au cours d’une session UDP classique.
ms.assetid: ab618c1f-3e7c-4f4b-b4ff-9e396d3258d9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 790de49e971d5506c1732b9c4d30b88643c7af0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310694"
---
# <a name="udp-packet-flows"></a><span data-ttu-id="5fbd7-103">Flux de paquets UDP</span><span class="sxs-lookup"><span data-stu-id="5fbd7-103">UDP Packet Flows</span></span>

<span data-ttu-id="5fbd7-104">Cette section décrit l’ordre dans lequel les couches du moteur de filtre de la plateforme de filtrage Windows (WFP) sont parcourues au cours d’une session UDP classique.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-104">This section describes the order in which the layers of the Windows Filtering Platform (WFP) filter engine are traversed during a typical UDP session.</span></span>

> [!Note]  
> <span data-ttu-id="5fbd7-105">Les flux de paquets UDP pour IPv6 suivent le même modèle que pour IPv4.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-105">UDP packet flows for IPv6 follow the same pattern as for IPv4.</span></span>

 

> [!Note]  
> <span data-ttu-id="5fbd7-106">Tous les flux de paquets non-TCP suivent le même modèle que les flux de paquets UDP.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-106">All non-TCP packet flows follow the same pattern as UDP packet flows.</span></span>

 

## <a name="udp-connection-establishment"></a><span data-ttu-id="5fbd7-107">Établissement de la connexion UDP</span><span class="sxs-lookup"><span data-stu-id="5fbd7-107">UDP Connection Establishment</span></span>

<dl> <span data-ttu-id="5fbd7-108">Le serveur (récepteur) effectue une ouverture passive</span><span class="sxs-lookup"><span data-stu-id="5fbd7-108">Server (receiver) performs Passive Open</span></span>

-   <span data-ttu-id="5fbd7-109">liaison : FWPM \_ \_ \_ \_ v4 de redirection de liaison ALE \_ de couche (windows 7/Windows Server 2008 R2 uniquement)</span><span class="sxs-lookup"><span data-stu-id="5fbd7-109">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="5fbd7-110">liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-110">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>

  
<span data-ttu-id="5fbd7-111">Le client (expéditeur) effectue une ouverture active</span><span class="sxs-lookup"><span data-stu-id="5fbd7-111">Client (sender) performs Active Open</span></span>

-   <span data-ttu-id="5fbd7-112">liaison : FWPM \_ \_ \_ \_ v4 de redirection de liaison ALE \_ de couche (windows 7/Windows Server 2008 R2 uniquement)</span><span class="sxs-lookup"><span data-stu-id="5fbd7-112">bind: FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="5fbd7-113">liaison : FWPM de l' \_ \_ \_ attribution de ressources ALE de couche ALE \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-113">bind: FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V4</span></span>
-   <span data-ttu-id="5fbd7-114">SendTo : FWPM \_ \_ \_ \_ de redirection de connexion ALE de couche \_ (windows 7/Windows Server 2008 R2 uniquement)</span><span class="sxs-lookup"><span data-stu-id="5fbd7-114">sendto: FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V4 (Windows 7 / Windows Server 2008 R2 only)</span></span>
-   <span data-ttu-id="5fbd7-115">SendTo : FWPM \_ de \_ \_ connexion d’authentification ALE de couche ALE \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-115">sendto: FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V4</span></span>
-   <span data-ttu-id="5fbd7-116">FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-116">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="5fbd7-117">données : données de datagramme de la \_ couche FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-117">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>
-   <span data-ttu-id="5fbd7-118">Message UDP : FWPM \_ couche de \_ \_ transport sortant \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-118">UDP message: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="5fbd7-119">Datagrammes IP : \_ couche FWPM \_ sortie \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-119">IP datagrams: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

  
<span data-ttu-id="5fbd7-120">Serveur</span><span class="sxs-lookup"><span data-stu-id="5fbd7-120">Server</span></span>

-   <span data-ttu-id="5fbd7-121">Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-121">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="5fbd7-122">Message UDP : \_ couche FWPM \_ \_ v4 transport entrant \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-122">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="5fbd7-123">Message UDP : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-123">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="5fbd7-124">FWPM \_ v4 de la couche \_ ALE \_ \_ établie \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-124">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V4</span></span>
-   <span data-ttu-id="5fbd7-125">données : données de datagramme de la \_ couche FWPM \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-125">data: FWPM\_LAYER\_DATAGRAM\_DATA\_V4</span></span>

  
</dl>

## <a name="udp-message-received-with-no-one-listening-on-the-port-or-protocol"></a><span data-ttu-id="5fbd7-126">Message UDP reçu sans écoute sur le port ou le protocole</span><span class="sxs-lookup"><span data-stu-id="5fbd7-126">UDP Message Received with No One Listening on the Port or Protocol</span></span>

<span data-ttu-id="5fbd7-127">Serveur (récepteur)</span><span class="sxs-lookup"><span data-stu-id="5fbd7-127">Server (receiver)</span></span>

-   <span data-ttu-id="5fbd7-128">Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-128">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="5fbd7-129">Datagrammes IP : FWPM \_ couche de \_ sortie \_ IPPACKET \_ v4 \_ ignorée</span><span class="sxs-lookup"><span data-stu-id="5fbd7-129">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4\_DISCARD</span></span>
-   <span data-ttu-id="5fbd7-130">Dest ICMP inaccessible : \_ erreur ICMP de sortie de la couche FWPM \_ \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-130">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V4</span></span>
-   <span data-ttu-id="5fbd7-131">Transfert ICMP impossible : \_ \_ \_ v4 de transport sortant \_ de la couche FWPM</span><span class="sxs-lookup"><span data-stu-id="5fbd7-131">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="5fbd7-132">Dest ICMP inaccessible : FWPM \_ couche \_ sortante \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-132">ICMP Dest Unreachable: FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V4</span></span>

> [!Note]  
> <span data-ttu-id="5fbd7-133">UDP sans point de terminaison est indiqué dans IPPACKET ignorée avec une condition d’erreur spécifique.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-133">UDP with no endpoint is indicated at IPPACKET discard with a specific error condition.</span></span> <span data-ttu-id="5fbd7-134">Bloquer ce paquet sur IPPACKET ignore pour empêcher la pile d’envoyer l’événement correspondant (erreur ICMP).</span><span class="sxs-lookup"><span data-stu-id="5fbd7-134">Block this packet at IPPACKET discard to cause the stack not to send the corresponding event (ICMP error).</span></span>

 

## <a name="successful-reauthorization-of-a-udp-packet"></a><span data-ttu-id="5fbd7-135">Réautorisation réussie d’un paquet UDP</span><span class="sxs-lookup"><span data-stu-id="5fbd7-135">Successful Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="5fbd7-136">Serveur (récepteur)</span><span class="sxs-lookup"><span data-stu-id="5fbd7-136">Server (receiver)</span></span>

-   <span data-ttu-id="5fbd7-137">Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-137">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="5fbd7-138">Message UDP : \_ couche FWPM \_ \_ v4 transport entrant \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-138">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="5fbd7-139">Message UDP : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-139">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="5fbd7-140">Message UDP : \_ \_ données de datagramme de la couche FWPM \_ \_ V4 (entrant)</span><span class="sxs-lookup"><span data-stu-id="5fbd7-140">UDP message: FWPM\_LAYER\_DATAGRAM\_DATA\_V4(INBOUND)</span></span>

## <a name="failed-reauthorization-of-a-udp-packet"></a><span data-ttu-id="5fbd7-141">Échec de la réautorisation d’un paquet UDP</span><span class="sxs-lookup"><span data-stu-id="5fbd7-141">Failed Reauthorization of a UDP Packet</span></span>

<span data-ttu-id="5fbd7-142">Serveur (récepteur)</span><span class="sxs-lookup"><span data-stu-id="5fbd7-142">Server (receiver)</span></span>

-   <span data-ttu-id="5fbd7-143">Datagrammes IP : \_ couche FWPM \_ entrée \_ IPPACKET \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-143">IP datagrams: FWPM\_LAYER\_INBOUND\_IPPACKET\_V4</span></span>
-   <span data-ttu-id="5fbd7-144">Message UDP : \_ couche FWPM \_ \_ v4 transport entrant \_</span><span class="sxs-lookup"><span data-stu-id="5fbd7-144">UDP message: FWPM\_LAYER\_INBOUND\_TRANSPORT\_V4</span></span>
-   <span data-ttu-id="5fbd7-145">Message UDP : FWPM \_ d' \_ authentification ALE de la couche ALE- \_ accepter la \_ \_ \_ v4</span><span class="sxs-lookup"><span data-stu-id="5fbd7-145">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4</span></span>
-   <span data-ttu-id="5fbd7-146">Message UDP : FWPM de l' \_ authentification ALE de la couche \_ ALE \_ \_ reçues \_ accepter la \_ v4 \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="5fbd7-146">UDP message: FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V4\_DISCARD</span></span>

## <a name="udp-connection-termination"></a><span data-ttu-id="5fbd7-147">Arrêt de la connexion UDP</span><span class="sxs-lookup"><span data-stu-id="5fbd7-147">UDP Connection Termination</span></span>

<span data-ttu-id="5fbd7-148">L’arrêt de la connexion UDP n’est pas indiqué dans une couche WFP.</span><span class="sxs-lookup"><span data-stu-id="5fbd7-148">UDP connection termination is not indicated at any WFP layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fbd7-149">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="5fbd7-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fbd7-150">Réautorisation ALE</span><span class="sxs-lookup"><span data-stu-id="5fbd7-150">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="5fbd7-151">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="5fbd7-151">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

 




