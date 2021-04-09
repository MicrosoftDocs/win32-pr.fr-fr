---
title: Identificateurs de légende intégrés (Fwpmu. h)
description: Les identificateurs des fonctions de légende intégrées à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID. Ces identificateurs sont définis comme suit.
ms.assetid: b283cb2e-7f82-4d44-982a-38499504e3bc
topic_type:
- apiref
api_name:
- FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4 / FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6
- FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4 / FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6
- FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4 / FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6
- FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4 / FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6
- FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4 / FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6
- FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP / FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP
- FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4 / FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6
- FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4 / FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6 / FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4
- FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4
- FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6
- FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4 / FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c21d0428953d8b3e27590b186d931a7d902db377
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942798"
---
# <a name="built-in-callout-identifiers"></a><span data-ttu-id="6d464-104">Identificateurs de légende intégrés</span><span class="sxs-lookup"><span data-stu-id="6d464-104">Built-in Callout Identifiers</span></span>

<span data-ttu-id="6d464-105">Les identificateurs des fonctions de légende intégrées à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID.</span><span class="sxs-lookup"><span data-stu-id="6d464-105">The identifiers for the callout functions that are built in to the Windows Filtering Platform (WFP) are each represented by a GUID.</span></span> <span data-ttu-id="6d464-106">Ces identificateurs sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="6d464-106">These identifiers are defined as follows.</span></span>

<span data-ttu-id="6d464-107">Les suffixes V4 et V6 à la fin des identificateurs de légende indiquent si la légende est pour la pile réseau IPv4 ou pour la pile réseau IPv6.</span><span class="sxs-lookup"><span data-stu-id="6d464-107">The V4 and V6 suffixes at the end of the callout identifiers indicate whether the callout is for the IPv4 network stack or for the IPv6 network stack.</span></span>

<dl> <dt>

<span data-ttu-id="6d464-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ de \_ transport entrant IPSec \_ \_ \_ v4/FWPM \_ \_ \_ \_ \_ , appel de transport entrant IPSec V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-108"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-109">Vérifie que chaque paquet reçu supposé arriver sur une association de sécurité en mode de transport arrive en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="6d464-109">Verifies that each received packet that is supposed to arrive over a transport mode security association arrives securely.</span></span>

<span data-ttu-id="6d464-110">Cette légende est applicable au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="6d464-110">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ de \_ \_ transport sortant IPSec \_ \_ v4/FWPM, \_ appel \_ \_ \_ \_ de transport sortant IPSec V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-111"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TRANSPORT\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-112">Indique à IPsec le trafic sortant qui doit être sécurisé via des associations de sécurité en mode de transport.</span><span class="sxs-lookup"><span data-stu-id="6d464-112">Indicates to IPsec the outbound traffic that must be secured over transport mode security associations.</span></span>

<span data-ttu-id="6d464-113">Cette légende est applicable au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="6d464-113">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ \_ tunnel entrant IPSec \_ \_ \_ v4/FWPM appel tunnel \_ \_ entrant IPSec \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-114"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-115">Vérifie que chaque paquet reçu supposé arriver sur une association de sécurité en mode de tunnel arrive en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="6d464-115">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="6d464-116">Cette légende est applicable au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="6d464-116">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**\_Appel FWPM \_ \_ tunnel sortant IPSec \_ \_ v4/FWPM appel tunnel \_ \_ \_ sortant IPSec \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-117"><span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_OUTBOUND\_TUNNEL\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-118">Indique à IPsec le trafic sortant qui doit être sécurisé par rapport aux associations de sécurité en mode tunnel.</span><span class="sxs-lookup"><span data-stu-id="6d464-118">Indicates to IPsec the outbound traffic that must be secured over tunnel mode security associations.</span></span>

<span data-ttu-id="6d464-119">Cette légende est applicable au niveau de la couche de transport.</span><span class="sxs-lookup"><span data-stu-id="6d464-119">This callout is applicable at the transport layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ appel \_ IPSec \_ Forward \_ entrant \_ tunnel \_ v4/FWPM \_ appel du \_ \_ tunnel entrant de transfert IPSec \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-120"><span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_INBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-121">Vérifie que chaque paquet reçu supposé arriver sur une association de sécurité en mode de tunnel arrive en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="6d464-121">Verifies that each received packet that is supposed to arrive over a tunnel mode security association arrives securely.</span></span>

<span data-ttu-id="6d464-122">Cette légende est applicable au niveau de la couche de transfert.</span><span class="sxs-lookup"><span data-stu-id="6d464-122">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**\_Appel du \_ tunnel sortant IPSec de \_ \_ tunnel sortant FWPM \_ \_ v4/FWPM, \_ appel de \_ \_ tunnel sortant en aval IPSec \_ \_ \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-123"><span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V4 / FWPM\_CALLOUT\_IPSEC\_FORWARD\_OUTBOUND\_TUNNEL\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-124">Indique à IPsec le trafic sortant qui doit être sécurisé via une association de sécurité en mode tunnel.</span><span class="sxs-lookup"><span data-stu-id="6d464-124">Indicates to IPsec the outbound traffic that must be secured over a tunnel mode security association.</span></span>

<span data-ttu-id="6d464-125">Cette légende est applicable au niveau de la couche de transfert.</span><span class="sxs-lookup"><span data-stu-id="6d464-125">This callout is applicable at the forwarding layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM d' \_ appel \_ IPSec \_ entrant \_ initiate \_ Secure \_ v4/FWPM, \_ appel de \_ \_ \_ \_ Secure \_ V6 sécurisé**</span><span class="sxs-lookup"><span data-stu-id="6d464-126"><span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_INITIATE\_SECURE\_V6**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-127">Vérifie que chaque connexion entrante censée arriver en sécurité arrive en toute sécurité.</span><span class="sxs-lookup"><span data-stu-id="6d464-127">Verifies that each incoming connection that is supposed to arrive secure arrives securely.</span></span>

<span data-ttu-id="6d464-128">Cette légende s’applique à la couche d’acceptation ALE.</span><span class="sxs-lookup"><span data-stu-id="6d464-128">This callout is applicable at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ appel \_ IPSec de \_ \_ tunnel entrant \_ ALE \_ accepter \_ v4/FWPM \_ appel \_ du \_ tunnel entrant \_ ALE \_ - \_ accepter \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-129"><span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V4 / FWPM\_CALLOUT\_IPSEC\_INBOUND\_TUNNEL\_ALE\_ACCEPT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-130">Autorise les paquets IP en mode de tunnel IPsec lorsqu’ils sont classés au niveau de la couche d’acceptation ALE.</span><span class="sxs-lookup"><span data-stu-id="6d464-130">Permits the IPsec tunnel mode IP-in-IP packets when they get classified at the ALE accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM d' \_ appel \_ IPSec \_ ALE \_ Connect \_ v4/FWPM, \_ appel \_ \_ \_ \_ V6 de connexion ALE IPSec**</span><span class="sxs-lookup"><span data-stu-id="6d464-131"><span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V4 / FWPM\_CALLOUT\_IPSEC\_ALE\_CONNECT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-132">Applique les modificateurs de stratégie IPsec aux applications clientes.</span><span class="sxs-lookup"><span data-stu-id="6d464-132">Applies IPsec policy modifiers to client applications.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**Appel \_ FWPM \_ \_ DOSP \_ \_ v4/FWPM \_ \_ \_ \_ \_ de l’appel de la sortie de la sortie d’IPSec DOSP de la sortie V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-133"><span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V4 / FWPM\_CALLOUT\_IPSEC\_DOSP\_FORWARD\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-134">Signale à la protection DoS IPsec que le trafic doit être vérifié pour les attaques potentielles et peut nécessiter un débit limité.</span><span class="sxs-lookup"><span data-stu-id="6d464-134">Signals to IPsec DoS Protection that traffic needs to be verified for potential DoS and may need to be rate limited.</span></span>

> [!Note]  
> <span data-ttu-id="6d464-135">Disponible uniquement dans Windows 7 et Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="6d464-135">Available only in Windows 7 and Windows Server 2008 R2.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ légende de la \_ couche de \_ transport WFP \_ \_ \_ \_ -suppression silencieuse/FWPM \_ légende mode \_ \_ \_ \_ \_ silencieux \_ de la couche de transport**</span><span class="sxs-lookup"><span data-stu-id="6d464-136"><span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V4\_SILENT\_DROP / FWPM\_CALLOUT\_WFP\_TRANSPORT\_LAYER\_V6\_SILENT\_DROP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-137">Implémente le filtrage en mode furtif en supprimant silencieusement tous les paquets entrants pour lesquels TCP n’a pas de point de terminaison d’écoute.</span><span class="sxs-lookup"><span data-stu-id="6d464-137">Implements stealth-mode filtering by silently dropping all incoming packets for which TCP does not have a listening endpoint.</span></span>

<span data-ttu-id="6d464-138">Cette légende s’applique à la couche rejet de transport entrant.</span><span class="sxs-lookup"><span data-stu-id="6d464-138">This callout is applicable at the inbound transport discard layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM de connexion \_ \_ TCP \_ Chimney de \_ \_ couche \_ v4/FWPM, appel de couche \_ \_ V6 de connexion TCP \_ Chimney \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d464-139"><span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-140">Active ou désactive le déchargement TCP Chimney pour chaque connexion sortante.</span><span class="sxs-lookup"><span data-stu-id="6d464-140">Enables or disables TCP chimney offload for each outgoing connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ de \_ protocole TCP \_ Chimney \_ Accept \_ couche \_ v4/FWPM avec appel de \_ \_ \_ \_ couche accepter la \_ couche \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-141"><span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_CHIMNEY\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-142">Active ou désactive le déchargement TCP Chimney pour chaque connexion entrante.</span><span class="sxs-lookup"><span data-stu-id="6d464-142">Enables or disables TCP chimney offload for each incoming connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ Callout \_ Set \_ options \_ Set \_ Connect \_ couche \_ v4/FWPM \_ appel \_ Set \_ options \_ Set \_ Connect \_ couche \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-143"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-144">Définit les options de classification sur les flux sortants.</span><span class="sxs-lookup"><span data-stu-id="6d464-144">Sets classify options on outbound flows.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ Callout \_ Set \_ options \_ d' \_ authentification \_ recevoir accepter \_ couche \_ v4/FWPM \_ appel des \_ options SET \_ \_ autorisation \_ recv \_ accepter \_ couche \_ V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-145"><span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_SET\_OPTIONS\_AUTH\_RECV\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-146">Définit les options de classification sur les flux entrants.</span><span class="sxs-lookup"><span data-stu-id="6d464-146">Sets classify options on inbound flows.</span></span>

> [!Note]  
> <span data-ttu-id="6d464-147">Disponible uniquement dans Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6d464-147">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM de la couche connexion \_ \_ auth Connect réservée \_ \_ \_ v4/FWPM, appel de la couche d’authentification \_ \_ \_ réservée \_ auth \_ Connect \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d464-148"><span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_RESERVED\_AUTH\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-149">Cet identificateur est réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="6d464-149">This identifier is reserved for internal use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM de l' \_ \_ \_ écoute ALE Traversal d' \_ écoute ALE de l' \_ écoute ALE/FWPM, légende de l' \_ \_ \_ \_ écoute ALE de TEREDO ALE \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6d464-150"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_LISTEN\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-151">Signale au service Teredo qu’une application requiert une adresse Teredo.</span><span class="sxs-lookup"><span data-stu-id="6d464-151">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="6d464-152">Pour Windows 7 et les versions ultérieures, utilisez la **FWPM d' \_ \_ \_ \_ \_ écoute \_ ALE Traversal de traversée** de la légende.</span><span class="sxs-lookup"><span data-stu-id="6d464-152">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**\_Assignation de \_ \_ ressource ALE Traversal de l' \_ \_ affectation de ressources ALE \_ \_ \_ \_ \_ \_ \_ \_ FWPM**</span><span class="sxs-lookup"><span data-stu-id="6d464-153"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6 / FWPM\_CALLOUT\_TEREDO\_ALE\_RESOURCE\_ASSIGNMENT\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-154">Signale au service Teredo qu’une application requiert une adresse Teredo.</span><span class="sxs-lookup"><span data-stu-id="6d464-154">Signals to the Teredo service that an application requires a Teredo address.</span></span>

> [!Note]  
> <span data-ttu-id="6d464-155">Pour Windows 7 et les versions ultérieures, utilisez la version d' **\_ affectation de \_ \_ \_ ressources ALE Traversal \_ \_ \_ de l’appel Edge FWPM V6**.</span><span class="sxs-lookup"><span data-stu-id="6d464-155">For Windows 7 and later, use **FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V6**.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM de l' \_ \_ \_ affectation de \_ ressources ALE Traversal \_ de \_ l' \_ appel Edge**</span><span class="sxs-lookup"><span data-stu-id="6d464-156"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_RESOURCE\_ASSIGNMENT\_V4**</span></span> 
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-157">Cet identificateur est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6d464-157">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**\_V4 d' \_ \_ \_ écoute ALE TRAVERSée \_ de l’FWPM de la \_ légende**</span><span class="sxs-lookup"><span data-stu-id="6d464-158"><span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**FWPM\_CALLOUT\_EDGE\_TRAVERSAL\_ALE\_LISTEN\_V4**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-159">Cet identificateur est réservé à une utilisation ultérieure.</span><span class="sxs-lookup"><span data-stu-id="6d464-159">This identifier is reserved for future use.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ appels \_ TCP \_ modèles \_ TCP \_ \_ v4 couche v4/FWPM appel de la \_ \_ \_ \_ \_ couche \_ V6 de connexion**</span><span class="sxs-lookup"><span data-stu-id="6d464-160"><span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_CONNECT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-161">Applique les paramètres de modèle TCP pour les connexions sortantes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="6d464-161">Applies TCP template settings for matching outgoing connections.</span></span>

> [!Note]  
> <span data-ttu-id="6d464-162">Disponible uniquement dans Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6d464-162">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="6d464-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM \_ de \_ modèles TCP Accept de la \_ \_ \_ couche \_ v4/FWPM appel \_ \_ \_ \_ \_ \_ de la couche accepter la couche V6**</span><span class="sxs-lookup"><span data-stu-id="6d464-163"><span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V4 / FWPM\_CALLOUT\_TCP\_TEMPLATES\_ACCEPT\_LAYER\_V6**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="6d464-164">Applique les paramètres de modèle TCP pour les connexions entrantes correspondantes.</span><span class="sxs-lookup"><span data-stu-id="6d464-164">Applies TCP template settings for matching incoming connections.</span></span>

> [!Note]  
> <span data-ttu-id="6d464-165">Disponible uniquement dans Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="6d464-165">Available only in Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6d464-166">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d464-166">Requirements</span></span>



| <span data-ttu-id="6d464-167">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d464-167">Requirement</span></span> | <span data-ttu-id="6d464-168">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d464-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6d464-169">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d464-169">Minimum supported client</span></span><br/> | <span data-ttu-id="6d464-170">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d464-170">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d464-171">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d464-171">Minimum supported server</span></span><br/> | <span data-ttu-id="6d464-172">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d464-172">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6d464-173">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d464-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d464-174"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d464-174"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





