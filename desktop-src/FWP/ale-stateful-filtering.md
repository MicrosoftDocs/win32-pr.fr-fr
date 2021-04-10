---
title: Filtrage avec état ALE
description: Les filtres installés au niveau des couches d’application de la couche application (ALE) de la plateforme de filtrage Windows (WFP) effectuent un filtrage réseau avec état.
ms.assetid: d5a3fcad-d55e-4a07-af21-cb40e5e9a9ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30cc1b4a5830efd0fef6dc28c88db85cd9c88cca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104031237"
---
# <a name="ale-stateful-filtering"></a><span data-ttu-id="e1120-103">Filtrage avec état ALE</span><span class="sxs-lookup"><span data-stu-id="e1120-103">ALE Stateful Filtering</span></span>

<span data-ttu-id="e1120-104">Les filtres installés au niveau des couches d’application de la couche application (ALE) de la plateforme de filtrage Windows (WFP) effectuent un filtrage réseau avec état.</span><span class="sxs-lookup"><span data-stu-id="e1120-104">Filters installed at the Application Layer Enforcement (ALE) layers of the Windows Filtering Platform (WFP) perform stateful network filtering.</span></span> <span data-ttu-id="e1120-105">Un *fluide ALE* est utilisé comme base pour le filtrage avec état ALE.</span><span class="sxs-lookup"><span data-stu-id="e1120-105">An *ALE flow* is used as the basis for ALE stateful filtering.</span></span>

<span data-ttu-id="e1120-106">Un flux ALE est un moyen de classer le trafic réseau en le regroupant en fonction d’une adresse IP source, d’une adresse IP de destination, d’un port source, d’un port de destination et d’un protocole.</span><span class="sxs-lookup"><span data-stu-id="e1120-106">An ALE flow is a way of classifying network traffic by grouping it based on a Source IP Address, a Destination IP Address, a Source Port, a Destination Port, and a Protocol.</span></span> <span data-ttu-id="e1120-107">Un fluide ALE peut être générique, autrement dit un ou plusieurs des descripteurs peuvent correspondre à tout (ou caractère générique \* ).</span><span class="sxs-lookup"><span data-stu-id="e1120-107">An ALE flow could be generic, that is one or more of the descriptors could be matching everything (or wildcard \*).</span></span> <span data-ttu-id="e1120-108">Par exemple, un workflow générique UDP ALE est décrit en tant qu’adresse IP source = \* , adresse IP de destination = \* , port source = \* , port de destination = \* et protocole = UDP.</span><span class="sxs-lookup"><span data-stu-id="e1120-108">For example, a generic UDP ALE flow would be described as Source IP Address = \*, Destination IP Address = \*, Source Port = \*, Destination Port = \*, and Protocol = UDP.</span></span>

<span data-ttu-id="e1120-109">Une fois qu’une connexion est autorisée (les connexions entrantes sont autorisées au niveau de la couche FWPM d’authentification ALE de la couche et des connexions sortantes au niveau de la couche FWPM d’authentification ALE de la couche **\_ \_ ALE \_ \_ \_ v {4 \| 6}** ), un fluide ALE est créé de telle sorte que, en excluant une modification de stratégie, tous les paquets, entrants et sortants, qui appartiennent au même fluide ALE sont autorisés automatiquement. [**\_ \_ \_ \_ \_ \_ \|**](management-filtering-layer-identifiers-.md)</span><span class="sxs-lookup"><span data-stu-id="e1120-109">Once a connection is authorized (inbound connections are authorized at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer and outbound connections at the **FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}** layer), an ALE flow is created such that, barring a policy change, all packets, inbound and outbound, that belong to the same ALE flow are permitted automatically.</span></span> <span data-ttu-id="e1120-110">Étant donné qu’une modification de stratégie peut nécessiter le blocage des connexions précédemment autorisées, les flux ALE doivent être [réautorisés](ale-re-authorization.md) lorsqu’une modification de stratégie se produit.</span><span class="sxs-lookup"><span data-stu-id="e1120-110">Because a policy change might require blocking previously allowed connections, ALE flows need to be [reauthorized](ale-re-authorization.md) when a policy change occurs.</span></span>

<span data-ttu-id="e1120-111">Le filtrage avec état ALE réduit considérablement le nombre de classifications requises en classant uniquement le premier paquet qui appartient à un fluide ALE.</span><span class="sxs-lookup"><span data-stu-id="e1120-111">ALE stateful filtering reduces drastically the number of required classifications by classifying only the first packet that belongs to an ALE flow.</span></span> <span data-ttu-id="e1120-112">Par comparaison, le filtrage sans état requiert la classification de chaque paquet qui traverse le réseau.</span><span class="sxs-lookup"><span data-stu-id="e1120-112">By comparison, non-stateful filtering requires classification of every packet that traverse the network.</span></span>

<span data-ttu-id="e1120-113">Un fluide ALE est associé à une direction, qui est la direction du premier paquet du fluide.</span><span class="sxs-lookup"><span data-stu-id="e1120-113">An ALE flow has an associated direction, which is the direction of the first packet of the flow.</span></span> <span data-ttu-id="e1120-114">Cela permet d’obtenir des stratégies plus flexibles, en autorisant les connexions initiées entrantes à avoir des stratégies différentes des connexions sortantes initiées.</span><span class="sxs-lookup"><span data-stu-id="e1120-114">This allows for more flexible policies, by permitting inbound initiated connections to have different policies from outbound initiated connections.</span></span>

## <a name="tcp-ale-flow"></a><span data-ttu-id="e1120-115">Flow TCP ALE</span><span class="sxs-lookup"><span data-stu-id="e1120-115">TCP ALE Flow</span></span>

<span data-ttu-id="e1120-116">Un flux ALE pour le trafic TCP est identifié par cinq tuples de TCP/IP (adresse IP source, adresse IP de destination, port source, port de destination et protocole).</span><span class="sxs-lookup"><span data-stu-id="e1120-116">An ALE flow for TCP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="e1120-117">Un flot TCP ALE a la même durée de vie qu’un socket TCP connecté.</span><span class="sxs-lookup"><span data-stu-id="e1120-117">A TCP ALE flow has the same lifetime as a connected TCP socket.</span></span> <span data-ttu-id="e1120-118">Un socket TCP connecté peut être un socket créé à l’aide de [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) ou un socket créé à la suite d’un appel [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) .</span><span class="sxs-lookup"><span data-stu-id="e1120-118">A connected TCP socket could be either a socket created using [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) or a socket created as a result of an [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) call.</span></span>

<span data-ttu-id="e1120-119">ALE gère une relation un-à-un entre un fluide TCP ALE et un bloc de contrôle TCP (TCB).</span><span class="sxs-lookup"><span data-stu-id="e1120-119">ALE maintains a one-to-one relationship between a TCP ALE flow and a TCP Control Block (TCB).</span></span>

## <a name="udp-ale-flow"></a><span data-ttu-id="e1120-120">Flow PEA UDP</span><span class="sxs-lookup"><span data-stu-id="e1120-120">UDP ALE Flow</span></span>

> [!Note]  
> <span data-ttu-id="e1120-121">Les protocoles qui ne sont pas TCP ou ICMP sont traités comme UDP.</span><span class="sxs-lookup"><span data-stu-id="e1120-121">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="e1120-122">Un flux ALE pour le trafic UDP est identifié par cinq tuples de TCP/IP (adresse IP source, adresse IP de destination, port source, port de destination et protocole).</span><span class="sxs-lookup"><span data-stu-id="e1120-122">An ALE flow for UDP traffic is identified by the five-tuple of TCP/IP (Source IP Address, Destination IP Address, Source Port, Destination Port, and Protocol).</span></span>

<span data-ttu-id="e1120-123">Un workflow UDP ALE est créé sur la base d’un socket UDP et représente l’homologue distant avec lequel l’application communique.</span><span class="sxs-lookup"><span data-stu-id="e1120-123">A UDP ALE flow is created based on a UDP socket and it represents the remote peer that the application is communicating with.</span></span> <span data-ttu-id="e1120-124">Un homologue distant est identifié par un tuple (adresse IP de destination et port de destination).</span><span class="sxs-lookup"><span data-stu-id="e1120-124">A remote peer is identified by a (Destination IP Address and Destination Port) tuple.</span></span>

<span data-ttu-id="e1120-125">Il existe une relation un-à-plusieurs entre un socket UDP et les homologues distants avec lesquels il communique.</span><span class="sxs-lookup"><span data-stu-id="e1120-125">There is a one-to-many relationship between a UDP socket and the remote peers that it talks to.</span></span>

<span data-ttu-id="e1120-126">Lorsque le socket UDP local est fermé, tous les flux ALE qui lui sont associés sont supprimés.</span><span class="sxs-lookup"><span data-stu-id="e1120-126">When the local UDP socket is closed, all the ALE flows associated with it will be deleted.</span></span>

<span data-ttu-id="e1120-127">En l’absence de fermetures de sockets, les flux ALE de monodiffusion UDP ont un délai d’inactivité [configurable](ale-flow-customization.md) qui a pour valeur par défaut 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="e1120-127">In the absence of socket closures, UDP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="e1120-128">Si aucun paquet n’est envoyé ou reçu dans cette fenêtre, le Flow ALE sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="e1120-128">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="e1120-129">Ce délai d’attente par défaut est progressivement réduit lorsque le nombre de flux ALE atteint un certain seuil.</span><span class="sxs-lookup"><span data-stu-id="e1120-129">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

## <a name="icmp-ale-flow"></a><span data-ttu-id="e1120-130">Trafic de la ALE ALE</span><span class="sxs-lookup"><span data-stu-id="e1120-130">ICMP ALE Flow</span></span>

<span data-ttu-id="e1120-131">Un flux ALE pour le trafic ICMP est identifié par le code à six tuples (adresse IP source, adresse IP de destination, type ICMP, code ICMP, protocole et ID ICMP).</span><span class="sxs-lookup"><span data-stu-id="e1120-131">An ALE flow for ICMP traffic is identified by the six-tuple (Source IP Address, Destination IP Address, ICMP type, ICMP code, Protocol, and ICMP ID).</span></span> <span data-ttu-id="e1120-132">L’ID ICMP fait partie du flux ALE uniquement pour le trafic ICMP d’écho/réponse.</span><span class="sxs-lookup"><span data-stu-id="e1120-132">The ICMP ID is part of the ALE flow only for ICMP echo/reply traffic.</span></span>

<span data-ttu-id="e1120-133">En l’absence de fermetures de sockets, les flux ALE de monodiffusion ICMP ont un délai d’inactivité [configurable](ale-flow-customization.md) qui a pour valeur par défaut 60 secondes.</span><span class="sxs-lookup"><span data-stu-id="e1120-133">In the absence of socket closures, ICMP unicast ALE flows have a [configurable](ale-flow-customization.md) idle timeout that defaults to 60 seconds.</span></span> <span data-ttu-id="e1120-134">Si aucun paquet n’est envoyé ou reçu dans cette fenêtre, le Flow ALE sera supprimé.</span><span class="sxs-lookup"><span data-stu-id="e1120-134">If no packets are sent or received within this window, the ALE flow will be deleted.</span></span> <span data-ttu-id="e1120-135">Ce délai d’attente par défaut est progressivement réduit lorsque le nombre de flux ALE atteint un certain seuil.</span><span class="sxs-lookup"><span data-stu-id="e1120-135">This default timeout is progressively shortened when the number of ALE flows system-wide reaches a certain threshold.</span></span>

<span data-ttu-id="e1120-136">Seuls les messages ICMP sans erreur sont indiqués aux couches ALE.</span><span class="sxs-lookup"><span data-stu-id="e1120-136">Only ICMP non-error messages are indicated to ALE layers.</span></span> <span data-ttu-id="e1120-137">Les messages d’erreur ICMP peuvent être inspectés au niveau des \_ couches d’erreurs ICMP.</span><span class="sxs-lookup"><span data-stu-id="e1120-137">ICMP error messages can be inspected at ICMP\_ERROR layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e1120-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="e1120-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1120-139">Application de la couche application (ALE)</span><span class="sxs-lookup"><span data-stu-id="e1120-139">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="e1120-140">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="e1120-140">ALE Layers</span></span>](ale-layers.md)
</dt> <dt>

[<span data-ttu-id="e1120-141">Trafic de diffusion/multidiffusion ALE</span><span class="sxs-lookup"><span data-stu-id="e1120-141">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="e1120-142">Réautorisation ALE</span><span class="sxs-lookup"><span data-stu-id="e1120-142">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="e1120-143">Personnalisation du fluide ALE</span><span class="sxs-lookup"><span data-stu-id="e1120-143">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="e1120-144">Flux de paquets TCP</span><span class="sxs-lookup"><span data-stu-id="e1120-144">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="e1120-145">Flux de paquets UDP</span><span class="sxs-lookup"><span data-stu-id="e1120-145">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="e1120-146">Fonctions Winsock</span><span class="sxs-lookup"><span data-stu-id="e1120-146">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> </dl>

 

 