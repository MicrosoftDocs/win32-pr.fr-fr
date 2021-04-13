---
title: Couches ALE
description: L’application de la couche application (ALE) est constituée de plusieurs couches de filtrage et de nombreuses couches de rejet correspondantes.
ms.assetid: 3ac71787-2350-4a60-b0bf-b00b52d30b83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a96e3b2ae5092bf8cca014eb3603eea5efe8f71
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314723"
---
# <a name="ale-layers"></a><span data-ttu-id="58d3c-103">Couches ALE</span><span class="sxs-lookup"><span data-stu-id="58d3c-103">ALE Layers</span></span>

<span data-ttu-id="58d3c-104">L’application de la couche application (ALE) est constituée de plusieurs couches de filtrage et de nombreuses couches de rejet correspondantes.</span><span class="sxs-lookup"><span data-stu-id="58d3c-104">The Application Layer Enforcement (ALE) consists of several filtering layers and many matching discard layers.</span></span> <span data-ttu-id="58d3c-105">Toutes les couches du moteur de filtrage de la plateforme de filtrage Windows (WFP), y compris ALE, sont décrites dans [**filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md).</span><span class="sxs-lookup"><span data-stu-id="58d3c-105">All the Windows Filtering Platform (WFP) filtering engine layers, including ALE, are described in [**Filtering Layer Identifiers**](management-filtering-layer-identifiers-.md).</span></span> <span data-ttu-id="58d3c-106">Cette rubrique contient une description plus détaillée des couches de filtrage qui font partie de ALE.</span><span class="sxs-lookup"><span data-stu-id="58d3c-106">This topic contains a more detailed description of the filtering layers that are part of ALE.</span></span>

## <a name="resource_assignment"></a><span data-ttu-id="58d3c-107">attribution de ressources \_</span><span class="sxs-lookup"><span data-stu-id="58d3c-107">RESOURCE\_ASSIGNMENT</span></span>

<span data-ttu-id="58d3c-108">Un filtre a été mis en correspondance pour les opérations de liaison réseau, explicites ou implicites, au niveau de la couche [**FWPM \_ allocation de ressources ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) .</span><span class="sxs-lookup"><span data-stu-id="58d3c-108">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for network bind operations, explicit or implicit.</span></span>

<span data-ttu-id="58d3c-109">Si un filtre à cette couche est mis en correspondance pour autoriser la création de sockets bruts, l’indicateur de condition fwp est défini sur indicateur de [**\_ point de \_ \_ \_ \_ terminaison brut**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="58d3c-109">If a filter at this layer is matched to authorize raw socket creation, the [**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**](filtering-condition-flags-.md) flag will be set.</span></span>

<span data-ttu-id="58d3c-110">Si un filtre de cette couche est mis en correspondance pour autoriser la réception du mode de proximité, le champ du [**\_ \_ \_ \_ mode de proximité ALE de condition fwp**](filtering-condition-identifiers-.md) est défini sur SIO \_ RCVALL.</span><span class="sxs-lookup"><span data-stu-id="58d3c-110">If a filter at this layer is matched to authorize promiscuous mode receiving, the [**FWP\_CONDITION\_ALE\_PROMISCUOUS\_MODE**](filtering-condition-identifiers-.md) field will be set to SIO\_RCVALL.</span></span> <span data-ttu-id="58d3c-111">Pour obtenir une description de SIO \_ RCVALL, consultez [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span><span class="sxs-lookup"><span data-stu-id="58d3c-111">For a description of SIO\_RCVALL, see [**WSAIoctl**](/windows/desktop/api/winsock2/nf-winsock2-wsaioctl).</span></span>

> [!Note]  
> <span data-ttu-id="58d3c-112">Il s’agit de la seule couche dans laquelle le mode de proximité peut être filtré.</span><span class="sxs-lookup"><span data-stu-id="58d3c-112">This is the only layer where promiscuous mode can be filtered.</span></span>

 

<span data-ttu-id="58d3c-113">Si aucun port n’est spécifié lors de la **liaison ()**, autrement dit, si le port est défini sur 0 (zéro), la pile TCP/IP sélectionne un port de la plage de ports dynamiques (19152 – 65535).</span><span class="sxs-lookup"><span data-stu-id="58d3c-113">If no port is specified during **bind()**, that is, port is set to 0 (zero), then the TCP/IP stack will select a port from the dynamic port range (19152–65535).</span></span> <span data-ttu-id="58d3c-114">Le port sélectionné sera classé à cette couche avec l’indicateur de [**condition fwp est un indicateur de \_ \_ \_ \_ \_ liaison de caractères génériques**](filtering-condition-flags-.md) .</span><span class="sxs-lookup"><span data-stu-id="58d3c-114">The selected port will be classified at this layer along with the [**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**](filtering-condition-flags-.md) flag.</span></span>

<span data-ttu-id="58d3c-115">Si l’adresse locale n’est pas spécifiée dans l’appel [**Bind ()**](/windows/desktop/api/winsock/nf-winsock-bind) , le champ adresse locale a la [**valeur \_ fwp vide**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="58d3c-115">If the local address is not specified in the [**bind()**](/windows/desktop/api/winsock/nf-winsock-bind) call, the local address field is set to [**FWP\_EMPTY**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span>

## <a name="auth_listen"></a><span data-ttu-id="58d3c-116">écoute d’authentification \_</span><span class="sxs-lookup"><span data-stu-id="58d3c-116">AUTH\_LISTEN</span></span>

<span data-ttu-id="58d3c-117">Un filtre au niveau de la couche FWPM d’écoute de l' [**\_ \_ écouteur d’authentification ALE de la couche \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance pour les appels d' [**écoute TCP ()**](/windows/desktop/api/winsock2/nf-winsock2-listen) .</span><span class="sxs-lookup"><span data-stu-id="58d3c-117">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**listen()**](/windows/desktop/api/winsock2/nf-winsock2-listen) calls.</span></span>

## <a name="auth_recv_accept"></a><span data-ttu-id="58d3c-118">acceptation de l’autorisation \_ recv \_</span><span class="sxs-lookup"><span data-stu-id="58d3c-118">AUTH\_RECV\_ACCEPT</span></span>

<span data-ttu-id="58d3c-119">Un filtre au niveau de la couche [**FWPM d' \_ authentification ALE de la couche ALE est \_ \_ \_ \_ accepté \_ \|**](management-filtering-layer-identifiers-.md) pour les appels TCP [**Accept ()**](/windows/desktop/api/winsock2/nf-winsock2-accept) , pour les premiers paquets UDP (monodiffusion) à partir d’une adresse distante unique/d’un tuple de port, et pour les premiers messages ICMP non-erreur entrante (monodiffusion) avec un type, un code et un ID ICMP uniques.</span><span class="sxs-lookup"><span data-stu-id="58d3c-119">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**accept()**](/windows/desktop/api/winsock2/nf-winsock2-accept) calls, for first UDP packets (unicast) from a unique remote address/port tuple, and for first inbound non-error ICMP messages (unicast) with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="58d3c-120">Les protocoles qui ne sont pas TCP ou ICMP sont traités comme UDP.</span><span class="sxs-lookup"><span data-stu-id="58d3c-120">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="58d3c-121">Les paquets TCP reçus par les sockets bruts sont gérés de la même façon que le trafic UDP.</span><span class="sxs-lookup"><span data-stu-id="58d3c-121">TCP packets received by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="58d3c-122">Autrement dit, seul le premier TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) et le premier TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sur des sockets bruts seront filtrés.</span><span class="sxs-lookup"><span data-stu-id="58d3c-122">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="auth_connect"></a><span data-ttu-id="58d3c-123">connexion d’authentification \_</span><span class="sxs-lookup"><span data-stu-id="58d3c-123">AUTH\_CONNECT</span></span>

<span data-ttu-id="58d3c-124">Un filtre au niveau de la couche [**FWPM d' \_ \_ authentification ALE de couche ALE \_ \_ \_ \|**](management-filtering-layer-identifiers-.md) est mis en correspondance pour les appels TCP [**Connect ()**](/windows/desktop/api/winsock2/nf-winsock2-connect) , pour les premiers paquets UDP envoyés à une adresse distante et un TUPLE de port uniques, et pour les premiers messages ICMP non-erreur sortants avec un type, un code et un ID ICMP uniques.</span><span class="sxs-lookup"><span data-stu-id="58d3c-124">A filter at the [**FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched for TCP [**connect()**](/windows/desktop/api/winsock2/nf-winsock2-connect) calls, for first UDP packets sent to a unique remote address and port tuple, and for first outbound non-error ICMP messages with a unique ICMP type, code, and ID.</span></span>

> [!Note]  
> <span data-ttu-id="58d3c-125">Les protocoles qui ne sont pas TCP ou ICMP sont traités comme UDP.</span><span class="sxs-lookup"><span data-stu-id="58d3c-125">Protocols that are not TCP or ICMP are treated like UDP.</span></span>

 

<span data-ttu-id="58d3c-126">Les paquets TCP envoyés par les sockets bruts sont gérés de la même façon que le trafic UDP.</span><span class="sxs-lookup"><span data-stu-id="58d3c-126">TCP packets sent by raw sockets are handled similarly to UDP traffic.</span></span> <span data-ttu-id="58d3c-127">Autrement dit, seul le premier TCP [**Send ()**](/windows/desktop/api/winsock2/nf-winsock2-send) et le premier TCP [**recv ()**](/windows/desktop/api/winsock/nf-winsock-recv) sur des sockets bruts seront filtrés.</span><span class="sxs-lookup"><span data-stu-id="58d3c-127">That is, only the first TCP [**send()**](/windows/desktop/api/winsock2/nf-winsock2-send) and the first TCP [**recv()**](/windows/desktop/api/winsock/nf-winsock-recv) over raw sockets will be filtered.</span></span>

## <a name="flow_established"></a><span data-ttu-id="58d3c-128">FLOW \_ établi</span><span class="sxs-lookup"><span data-stu-id="58d3c-128">FLOW\_ESTABLISHED</span></span>

<span data-ttu-id="58d3c-129">Un filtre au niveau de la couche FWPM de la couche [**\_ \_ ALE \_ \_ établie \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance après la réussite d’une négociation TCP triple.</span><span class="sxs-lookup"><span data-stu-id="58d3c-129">A filter at the [**FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after a TCP three-way handshake has successfully completed.</span></span> <span data-ttu-id="58d3c-130">Pour le trafic non-TCP, le filtre est mis en correspondance immédiatement après la mise en correspondance des filtres des couches d’authentification/d' **authentification \_** des **autorisations de \_ réception \_ d’authentification** .</span><span class="sxs-lookup"><span data-stu-id="58d3c-130">For non-TCP traffic, the filter is matched immediately after filters from **AUTH\_RECV\_ACCEPT** or **AUTH\_CONNECT** layers are matched.</span></span>

<span data-ttu-id="58d3c-131">Un filtre au niveau de cette couche ne doit pas retourner de bloc ou d’autorisation.</span><span class="sxs-lookup"><span data-stu-id="58d3c-131">A filter at this layer should not return Block or Permit.</span></span>

<span data-ttu-id="58d3c-132">Cette couche est utilisée par les pilotes de légende pour suivre l’état de la connexion, décrite en détail dans la documentation du [Kit de pilotes Windows](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) .</span><span class="sxs-lookup"><span data-stu-id="58d3c-132">This layer is used by callout drivers to track connection state, described in detail in the [Windows Driver Kit](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) documentation.</span></span>

## <a name="resource_release"></a><span data-ttu-id="58d3c-133">version de la ressource \_</span><span class="sxs-lookup"><span data-stu-id="58d3c-133">RESOURCE\_RELEASE</span></span>

<span data-ttu-id="58d3c-134">Un filtre au niveau de la couche FWPM de la mise à jour de la [**\_ ressource ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance après la libération des ressources allouées via l' **\_ attribution de ressources** .</span><span class="sxs-lookup"><span data-stu-id="58d3c-134">A filter at the [**FWPM\_LAYER\_ALE\_RESOURCE\_RELEASE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched after resources that were allocated via **RESOURCE\_ASSIGNMENT** have been freed.</span></span>

## <a name="endpoint_closure"></a><span data-ttu-id="58d3c-135">fermeture du point de terminaison \_</span><span class="sxs-lookup"><span data-stu-id="58d3c-135">ENDPOINT\_CLOSURE</span></span>

<span data-ttu-id="58d3c-136">Un filtre au niveau de la couche [**FWPM de clôture du point de terminaison ALE de la \_ couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) est mis en correspondance lorsqu’un protocole TCP connecté ou un point de terminaison de sockets UDP est fermé.</span><span class="sxs-lookup"><span data-stu-id="58d3c-136">A filter at the [**FWPM\_LAYER\_ALE\_ENDPOINT\_CLOSURE\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer is matched when a connected TCP flow or UDP sockets endpoint is closed.</span></span>

## <a name="connect_redirect"></a><span data-ttu-id="58d3c-137">\_rediriger la connexion</span><span class="sxs-lookup"><span data-stu-id="58d3c-137">CONNECT\_REDIRECT</span></span>

<span data-ttu-id="58d3c-138">Un filtre au niveau de la couche [**FWPM \_ redirection de la connexion ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) permet la modification des adresses et des ports distants.</span><span class="sxs-lookup"><span data-stu-id="58d3c-138">A filter at the [**FWPM\_LAYER\_ALE\_CONNECT\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of remote addresses and ports.</span></span> <span data-ttu-id="58d3c-139">La connexion sortante est redirigée pour la durée de cette connexion.</span><span class="sxs-lookup"><span data-stu-id="58d3c-139">The outbound connection will be redirected for the duration of that connection.</span></span>

## <a name="bind_redirect"></a><span data-ttu-id="58d3c-140">redirection de liaison \_</span><span class="sxs-lookup"><span data-stu-id="58d3c-140">BIND\_REDIRECT</span></span>

<span data-ttu-id="58d3c-141">Un filtre au niveau de la couche [**FWPM de \_ redirection de liaison ALE de la couche \_ \_ \_ \_ V {4 \| 6}**](management-filtering-layer-identifiers-.md) permet de modifier l’adresse locale et les ports du Socket sous-jacent.</span><span class="sxs-lookup"><span data-stu-id="58d3c-141">A filter at the [**FWPM\_LAYER\_ALE\_BIND\_REDIRECT\_V{4\|6}**](management-filtering-layer-identifiers-.md) layer allows for modification of the underlying socket's local address and ports.</span></span> <span data-ttu-id="58d3c-142">Le socket local sera redirigé pendant la durée de vie du socket</span><span class="sxs-lookup"><span data-stu-id="58d3c-142">The local socket will be redirected for the lifetime of the socket</span></span>

## <a name="ale-discard-layers"></a><span data-ttu-id="58d3c-143">Couches de rejet ALE</span><span class="sxs-lookup"><span data-stu-id="58d3c-143">ALE DISCARD Layers</span></span>

<span data-ttu-id="58d3c-144">Pour chaque couche ALE décrite ci-dessus, le moteur de filtrage contient une couche correspondante à ignorer.</span><span class="sxs-lookup"><span data-stu-id="58d3c-144">For each of the ALE layers described above the filtering engine contains a matching discard layer.</span></span> <span data-ttu-id="58d3c-145">Les couches de rejet ALE sont utilisées par les légendes à des fins de journalisation.</span><span class="sxs-lookup"><span data-stu-id="58d3c-145">The ALE discard layers are used by callouts for logging purposes.</span></span> <span data-ttu-id="58d3c-146">Les paquets et les indications qui ont été ignorés dans l’une des couches de filtrage ALE sont indiqués dans la couche de suppression ALE correspondante.</span><span class="sxs-lookup"><span data-stu-id="58d3c-146">Packets and indications that have been discarded at one of the ALE filtering layers are indicated to the matching ALE discard layer.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58d3c-147">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="58d3c-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58d3c-148">Application de la couche application (ALE)</span><span class="sxs-lookup"><span data-stu-id="58d3c-148">Application Layer Enforcement (ALE)</span></span>](application-layer-enforcement--ale-.md)
</dt> <dt>

[<span data-ttu-id="58d3c-149">Filtrage avec état ALE</span><span class="sxs-lookup"><span data-stu-id="58d3c-149">ALE Stateful Filtering</span></span>](ale-stateful-filtering.md)
</dt> <dt>

[<span data-ttu-id="58d3c-150">Trafic de diffusion/multidiffusion ALE</span><span class="sxs-lookup"><span data-stu-id="58d3c-150">ALE Multicast/Broadcast Traffic</span></span>](ale-multicast-broadcast-traffic.md)
</dt> <dt>

[<span data-ttu-id="58d3c-151">Réautorisation ALE</span><span class="sxs-lookup"><span data-stu-id="58d3c-151">ALE Reauthorization</span></span>](ale-re-authorization.md)
</dt> <dt>

[<span data-ttu-id="58d3c-152">Personnalisation du fluide ALE</span><span class="sxs-lookup"><span data-stu-id="58d3c-152">ALE Flow Customization</span></span>](ale-flow-customization.md)
</dt> <dt>

[<span data-ttu-id="58d3c-153">Flux de paquets TCP</span><span class="sxs-lookup"><span data-stu-id="58d3c-153">TCP Packet Flows</span></span>](tcp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="58d3c-154">Flux de paquets UDP</span><span class="sxs-lookup"><span data-stu-id="58d3c-154">UDP Packet Flows</span></span>](udp-packet-flows.md)
</dt> <dt>

[<span data-ttu-id="58d3c-155">Fonctions Winsock</span><span class="sxs-lookup"><span data-stu-id="58d3c-155">Winsock Functions</span></span>](/windows/desktop/WinSock/winsock-functions)
</dt> <dt>

[<span data-ttu-id="58d3c-156">**Indicateurs de condition de filtrage**</span><span class="sxs-lookup"><span data-stu-id="58d3c-156">**Filtering Condition Flags**</span></span>](filtering-condition-flags-.md)
</dt> <dt>

[<span data-ttu-id="58d3c-157">**Conditions de filtrage disponibles pour chaque couche de filtrage**</span><span class="sxs-lookup"><span data-stu-id="58d3c-157">**Filtering Conditions Available At Each Filtering Layer**</span></span>](filtering-conditions-available-at-each-filtering-layer.md)
</dt> </dl>

 

 