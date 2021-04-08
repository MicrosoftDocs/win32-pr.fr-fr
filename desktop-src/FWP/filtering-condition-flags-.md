---
title: Indicateurs de condition de filtrage (Fwptypes. h)
description: Les indicateurs de condition de filtrage de la plateforme de filtrage Windows (WFP) sont tous représentés par un champ de champ.
ms.assetid: fe879479-331d-42ef-ac2f-634f0c13c21d
topic_type:
- apiref
api_name:
- FWP_CONDITION_FLAG_IS_LOOPBACK
- FWP_CONDITION_FLAG_IS_IPSEC_SECURED
- FWP_CONDITION_FLAG_IS_REAUTHORIZE
- FWP_CONDITION_FLAG_IS_WILDCARD_BIND
- FWP_CONDITION_FLAG_IS_RAW_ENDPOINT
- FWP_CONDITION_FLAG_IS_FRAGMENT
- FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP
- FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY
- FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY
- FWP_CONDITION_FLAG_IS_IMPLICIT_BIND
- FWP_CONDITION_FLAG_IS_REASSEMBLED
- FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED
- FWP_CONDITION_FLAG_IS_PROMISCUOUS
- FWP_CONDITION_FLAG_IS_AUTH_FW
- FWP_CONDITION_FLAG_IS_RECLASSIFY
- FWP_CONDITION_FLAG_IS_PROXY_CONNECTION
- FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK
- FWP_CONDITION_FLAG_IS_RESERVED
- FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE
- FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE
- FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING
- FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION
- FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION
- FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED
- FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC
- FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC
- FWP_CONDITION_L2_IS_NATIVE_ETHERNET
- FWP_CONDITION_L2_IS_WIFI
- FWP_CONDITION_L2_IS_MOBILE_BROADBAND
- FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA
- FWP_CONDITION_L2_IS_VM2VM
- FWP_CONDITION_L2_IS_MALFORMED_PACKET
- FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP
- FWP_CONDITION_L2_IF_CONNECTOR_PRESENT
api_location:
- fwptypes.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c88fa56f37332d52ed31f5ef042c5064a82ac4d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743149"
---
# <a name="filtering-condition-flags"></a><span data-ttu-id="74557-103">Indicateurs de condition de filtrage</span><span class="sxs-lookup"><span data-stu-id="74557-103">Filtering Condition Flags</span></span>

<span data-ttu-id="74557-104">Les indicateurs de condition de filtrage de la plateforme de filtrage Windows (WFP) sont tous représentés par un champ de champ.</span><span class="sxs-lookup"><span data-stu-id="74557-104">The Windows Filtering Platform (WFP) filtering condition flags are each represented by a bitfield.</span></span>

<span data-ttu-id="74557-105">Ces indicateurs et les couches de filtrage dans lesquelles ils peuvent être utilisés sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="74557-105">These flags and the filtering layers where they can be used are defined as follows.</span></span>

<dl> <dt>

<span data-ttu-id="74557-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ loopback**</span><span class="sxs-lookup"><span data-stu-id="74557-106"><span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-107">Teste si le trafic réseau est en boucle.</span><span class="sxs-lookup"><span data-stu-id="74557-107">Tests if the network traffic is loopback traffic.</span></span>

<span data-ttu-id="74557-108">Filtrage des couches :</span><span class="sxs-lookup"><span data-stu-id="74557-108">Filtering layers:</span></span>

-   <span data-ttu-id="74557-109">\_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-109">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-110">\_Couche FWPM \_ sortante \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-110">FWPM\_LAYER\_OUTBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-111">\_Transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-111">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-112">\_Transport sortant de la couche FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-112">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-113">\_Flux de couche FWPM \_ \_ {v4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-113">FWPM\_LAYER\_STREAM\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-114">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-114">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="74557-115">\_Couche FWPM \_ \_ erreur ICMP entrante \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-115">FWPM\_LAYER\_INBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-116">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-116">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="74557-117">\_Erreur ICMP sortie de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-117">FWPM\_LAYER\_OUTBOUND\_ICMP\_ERROR\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-118">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-118">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="74557-119">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-119">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-120">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-120">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-121">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-121">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="74557-122">FWPM \_ de \_ couche \_ ALE \_ établi \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-122">FWPM\_LAYER\_ALE\_FLOW\_ESTABLISHED\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-123">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-123">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ sécurisé par IPSec \_**</span><span class="sxs-lookup"><span data-stu-id="74557-124"><span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_SECURED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-125">Teste si le trafic réseau est protégé par IPsec.</span><span class="sxs-lookup"><span data-stu-id="74557-125">Tests if the network traffic is protected by IPsec.</span></span>

<span data-ttu-id="74557-126">Filtrage des couches :</span><span class="sxs-lookup"><span data-stu-id="74557-126">Filtering layers:</span></span>

-   <span data-ttu-id="74557-127">\_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-127">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-128">\_Transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-128">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-129">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-129">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-130">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-130">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ Reauthorize**</span><span class="sxs-lookup"><span data-stu-id="74557-131"><span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**FWP\_CONDITION\_FLAG\_IS\_REAUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-132">Teste une modification de stratégie au lieu d’une nouvelle connexion.</span><span class="sxs-lookup"><span data-stu-id="74557-132">Tests for a policy change as opposed to a new connection.</span></span>

<span data-ttu-id="74557-133">Filtrage des couches :</span><span class="sxs-lookup"><span data-stu-id="74557-133">Filtering layers:</span></span>

-   <span data-ttu-id="74557-134">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-134">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-135">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-135">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**l' \_ indicateur de condition fwp \_ est une liaison de \_ \_ caractères génériques \_**</span><span class="sxs-lookup"><span data-stu-id="74557-136"><span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_WILDCARD\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-137">Teste si l’application a spécifié une adresse générique lors de la liaison à une adresse de réseau local.</span><span class="sxs-lookup"><span data-stu-id="74557-137">Tests if the application specified a wildcard address when binding to a local network address.</span></span>

<span data-ttu-id="74557-138">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-138">Filtering layer:</span></span>

-   <span data-ttu-id="74557-139">\_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-139">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**l' \_ indicateur de condition fwp \_ est un point de \_ \_ \_ terminaison brut**</span><span class="sxs-lookup"><span data-stu-id="74557-140"><span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**FWP\_CONDITION\_FLAG\_IS\_RAW\_ENDPOINT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-141">Teste si le point de terminaison local qui envoie et reçoit le trafic est un point de terminaison brut.</span><span class="sxs-lookup"><span data-stu-id="74557-141">Tests if the local endpoint that is sending and receiving traffic is a raw endpoint.</span></span>

<span data-ttu-id="74557-142">Filtrage des couches :</span><span class="sxs-lookup"><span data-stu-id="74557-142">Filtering layers:</span></span>

-   <span data-ttu-id="74557-143">\_Transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-143">FWPM\_LAYER\_INBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-144">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-144">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="74557-145">\_Transport sortant de la couche FWPM \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-145">FWPM\_LAYER\_OUTBOUND\_TRANSPORT\_V{4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-146">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-146">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="74557-147">Données de datagramme de la \_ couche FWPM \_ \_ \_ {v4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-147">FWPM\_LAYER\_DATAGRAM\_DATA\_{V4\|6}</span></span>
    > [!Note]  
    > <span data-ttu-id="74557-148">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-148">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

     

-   <span data-ttu-id="74557-149">\_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-149">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-150">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-150">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-151">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-151">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ fragment**</span><span class="sxs-lookup"><span data-stu-id="74557-152"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-153">Teste si la \_ structure de liste de mémoires tampons nette \_ transmise à un pilote de légende est un fragment de paquet IP.</span><span class="sxs-lookup"><span data-stu-id="74557-153">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver is an IP packet fragment.</span></span>

<span data-ttu-id="74557-154">Filtrage des couches :</span><span class="sxs-lookup"><span data-stu-id="74557-154">Filtering layers:</span></span>

-   <span data-ttu-id="74557-155">\_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-155">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-156">FWPM \_ couche \_ entrante \_ IPPACKET \_ V {4 \| 6} \_ Ignorer</span><span class="sxs-lookup"><span data-stu-id="74557-156">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}\_DISCARD</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**l' \_ indicateur de condition fwp \_ est un groupe de \_ \_ fragments \_**</span><span class="sxs-lookup"><span data-stu-id="74557-157"><span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**FWP\_CONDITION\_FLAG\_IS\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-158">Teste si la \_ \_ structure de liste de mémoires TAMPONs nette transmise à un pilote de légende décrit une liste liée de fragments de paquets.</span><span class="sxs-lookup"><span data-stu-id="74557-158">Tests if the NET\_BUFFER\_LIST structure passed to a callout driver describes a linked list of packet fragments.</span></span>

<span data-ttu-id="74557-159">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-159">Filtering layer:</span></span>

-   <span data-ttu-id="74557-160">FWPM \_ couche \_ IPFORWARD \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-160">FWPM\_LAYER\_IPFORWARD\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ \_ \_ reclassifier IPSec Natt**</span><span class="sxs-lookup"><span data-stu-id="74557-161"><span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_IPSEC\_NATT\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-162">Indique que le même paquet est reclassifié au niveau de la couche de transport, lorsque le shim NAT IPsec traduit la valeur du port distant.</span><span class="sxs-lookup"><span data-stu-id="74557-162">Indicates that the same packet is being re-classified at the transport layer, when the IPsec NAT shim translates the remote port value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**l' \_ indicateur de condition fwp \_ requiert une \_ \_ \_ classification ALE**</span><span class="sxs-lookup"><span data-stu-id="74557-163"><span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**FWP\_CONDITION\_FLAG\_REQUIRES\_ALE\_CLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-164">Indique que le paquet sera reclassé au niveau de la couche de réception/acceptation ALE.</span><span class="sxs-lookup"><span data-stu-id="74557-164">Indicates that the packet will be reclassified at the ALE receive/accept layer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**l' \_ indicateur de condition fwp \_ est une \_ \_ liaison implicite \_**</span><span class="sxs-lookup"><span data-stu-id="74557-165"><span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**FWP\_CONDITION\_FLAG\_IS\_IMPLICIT\_BIND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-166">Teste si Windows Sockets effectue une liaison implicite.</span><span class="sxs-lookup"><span data-stu-id="74557-166">Tests if Windows Sockets is performing an implicit bind.</span></span>

<span data-ttu-id="74557-167">Disponible uniquement sur Windows Vista et Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="74557-167">Available only on Windows Vista and Windows Server 2008.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ réassemblé**</span><span class="sxs-lookup"><span data-stu-id="74557-168"><span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**FWP\_CONDITION\_FLAG\_IS\_REASSEMBLED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-169">Teste si le paquet a été réassemblé.</span><span class="sxs-lookup"><span data-stu-id="74557-169">Tests if the packet has been reassembled.</span></span>

> [!Note]  
> <span data-ttu-id="74557-170">Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-170">Available only on Windows Server 2008, Windows Vista with SP1, and later.</span></span>

 

<span data-ttu-id="74557-171">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-171">Filtering layer:</span></span>

-   <span data-ttu-id="74557-172">\_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-172">FWPM\_LAYER\_INBOUND\_IPPACKET\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**l' \_ indicateur de condition fwp \_ est l’application de \_ \_ nom \_ \_ spécifiée**</span><span class="sxs-lookup"><span data-stu-id="74557-173"><span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**FWP\_CONDITION\_FLAG\_IS\_NAME\_APP\_SPECIFIED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-174">Teste si le nom de l’ordinateur homologue auquel l’application s’attend à se connecter a été reçu via une API telle que [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) et n’est pas obtenue via les heuristiques de mise en cache.</span><span class="sxs-lookup"><span data-stu-id="74557-174">Tests if the name of the peer machine that the application is expecting to connect to has been received via an API such as [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) and not obtained via the caching heuristics.</span></span>

> [!Note]  
> <span data-ttu-id="74557-175">Disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-175">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="74557-176">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-176">Filtering layer:</span></span>

-   <span data-ttu-id="74557-177">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-177">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ promiscuité**</span><span class="sxs-lookup"><span data-stu-id="74557-178"><span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**FWP\_CONDITION\_FLAG\_IS\_PROMISCUOUS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-179">Réservé.</span><span class="sxs-lookup"><span data-stu-id="74557-179">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**l' \_ indicateur de condition fwp \_ est le \_ \_ \_ FW auth**</span><span class="sxs-lookup"><span data-stu-id="74557-180"><span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**FWP\_CONDITION\_FLAG\_IS\_AUTH\_FW**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-181">Teste si la connexion est authentifiée de bout en bout, même si les paquets individuels n’ont pas été vérifiés.</span><span class="sxs-lookup"><span data-stu-id="74557-181">Tests if the connection is end-to-end authenticated, even if the individual packets have not been verified.</span></span>

> [!Note]  
> <span data-ttu-id="74557-182">Disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-182">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="74557-183">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-183">Filtering layer:</span></span>

-   <span data-ttu-id="74557-184">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-184">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-185">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-185">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ reclassifier**</span><span class="sxs-lookup"><span data-stu-id="74557-186"><span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**FWP\_CONDITION\_FLAG\_IS\_RECLASSIFY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-187">Teste si le moteur de filtrage reclasse une demande de liaison ou d’écoute précédente.</span><span class="sxs-lookup"><span data-stu-id="74557-187">Tests if the filtering engine is reclassifying a previous bind or listen request.</span></span>

> [!Note]  
> <span data-ttu-id="74557-188">Disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-188">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<span data-ttu-id="74557-189">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-189">Filtering layer:</span></span>

-   <span data-ttu-id="74557-190">Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-190">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-191">\_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-191">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**l' \_ indicateur de condition fwp \_ est une \_ \_ \_ connexion proxy**</span><span class="sxs-lookup"><span data-stu-id="74557-192"><span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**FWP\_CONDITION\_FLAG\_IS\_PROXY\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-193">Teste si la connexion utilise un proxy.</span><span class="sxs-lookup"><span data-stu-id="74557-193">Tests if the connection uses a proxy.</span></span>

> [!Note]  
> <span data-ttu-id="74557-194">Disponible uniquement sur Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="74557-194">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**l' \_ indicateur de condition fwp \_ est un \_ \_ \_ bouclage APPCONTAINER**</span><span class="sxs-lookup"><span data-stu-id="74557-195"><span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-196">Teste si le trafic réseau est un trafic de bouclage de conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="74557-196">Tests if the network traffic is app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="74557-197">Disponible uniquement sur Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="74557-197">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**l' \_ indicateur de condition fwp \_ est un \_ \_ \_ bouclage non APPCONTAINER \_**</span><span class="sxs-lookup"><span data-stu-id="74557-198"><span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**FWP\_CONDITION\_FLAG\_IS\_NON\_APPCONTAINER\_LOOPBACK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-199">Teste si le trafic réseau est un trafic de bouclage de conteneur non-App.</span><span class="sxs-lookup"><span data-stu-id="74557-199">Tests if the network traffic is non-app container loopback traffic.</span></span>

> [!Note]  
> <span data-ttu-id="74557-200">Disponible uniquement sur Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="74557-200">Available only on Windows 8 and Windows Server 2012.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ réservé**</span><span class="sxs-lookup"><span data-stu-id="74557-201"><span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**FWP\_CONDITION\_FLAG\_IS\_RESERVED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-202">Réservé.</span><span class="sxs-lookup"><span data-stu-id="74557-202">Reserved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**l’indicateur de condition FWP respecte l' \_ \_ \_ autorisation de \_ \_ stratégie \_**</span><span class="sxs-lookup"><span data-stu-id="74557-203"><span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**FWP\_CONDITION\_FLAG\_IS\_HONORING\_POLICY\_AUTHORIZE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-204">Indique que la classification en cours est en cours d’exécution pour honorer l’intention d’une application du Windows Store redirigée pour se connecter à un ordinateur hôte spécifié.</span><span class="sxs-lookup"><span data-stu-id="74557-204">Indicates that the current classification is being performed to honor the intention of a redirected Windows Store app to connect to a specified host.</span></span> <span data-ttu-id="74557-205">Une telle classification contient les mêmes valeurs de champ de classement que si l’application n’a jamais été redirigée.</span><span class="sxs-lookup"><span data-stu-id="74557-205">Such a classification will contain the same classifiable field values as if the app were never redirected.</span></span> <span data-ttu-id="74557-206">L’indicateur indique également qu’une classification future sera appelée pour correspondre à la destination redirigée effective.</span><span class="sxs-lookup"><span data-stu-id="74557-206">The flag also indicates that a future classification will be invoked to match the effective redirected destination.</span></span> <span data-ttu-id="74557-207">Si l’application est redirigée vers un service proxy pour inspection, cela signifie également qu’une classification future sera appelée sur la connexion proxy.</span><span class="sxs-lookup"><span data-stu-id="74557-207">If the app is redirected to a proxy service for inspection, it also means a future classification will be invoked on the proxy connection.</span></span> <span data-ttu-id="74557-208">Les pilotes de légende doivent généralement autoriser cette classification.</span><span class="sxs-lookup"><span data-stu-id="74557-208">Callout drivers should generally allow this classification.</span></span>

> [!Note]  
> <span data-ttu-id="74557-209">Disponible uniquement sur Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="74557-209">Available only on Windows 8 and Windows Server 2012.</span></span>

 

<span data-ttu-id="74557-210">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-210">Filtering layer:</span></span>

-   <span data-ttu-id="74557-211">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-211">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="74557-212">Les indicateurs suivants spécifient la raison de la réautorisation d’une connexion précédemment autorisée.</span><span class="sxs-lookup"><span data-stu-id="74557-212">The following flags specify the reason for reauthorizing a previously authorized connection.</span></span> <span data-ttu-id="74557-213">Ces indicateurs et les couches de filtrage dans lesquelles ils peuvent être utilisés sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="74557-213">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="74557-214">Ces conditions de filtrage sont uniquement disponibles sur Windows Server 2008 R2, Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-214">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="74557-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**CONDITION FWP-autoriser la modification de la \_ \_ \_ stratégie de motif \_ \_**</span><span class="sxs-lookup"><span data-stu-id="74557-215"><span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-216">Indique que la connexion a été réautorisée en raison de l’ajout ou de la suppression de filtres.</span><span class="sxs-lookup"><span data-stu-id="74557-216">Indicates that the connection was reauthorized due to filters being added or removed.</span></span>

<span data-ttu-id="74557-217">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-217">Filtering layer:</span></span>

-   <span data-ttu-id="74557-218">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-218">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-219">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-219">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**\_condition fwp \_ réautoriser la \_ raison \_ de la nouvelle \_ interface d’arrivée \_**</span><span class="sxs-lookup"><span data-stu-id="74557-220"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_ARRIVAL\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-221">Indique que le paquet est arrivé à partir d’une interface inconnue.</span><span class="sxs-lookup"><span data-stu-id="74557-221">Indicates that the packet has arrived from an unknown interface.</span></span>

<span data-ttu-id="74557-222">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-222">Filtering layer:</span></span>

-   <span data-ttu-id="74557-223">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-223">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-224">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-224">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**\_condition fwp \_ réautoriser la \_ raison \_ de la nouvelle \_ \_ interface NEXTHOP**</span><span class="sxs-lookup"><span data-stu-id="74557-225"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_NEXTHOP\_INTERFACE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-226">Indique que le paquet sera en cours de départiment d’une interface inconnue.</span><span class="sxs-lookup"><span data-stu-id="74557-226">Indicates that the packet will be departing from an unknown interface.</span></span>

<span data-ttu-id="74557-227">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-227">Filtering layer:</span></span>

-   <span data-ttu-id="74557-228">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-228">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-229">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-229">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**\_condition fwp \_ réautoriser le \_ \_ franchissement du profil \_**</span><span class="sxs-lookup"><span data-stu-id="74557-230"><span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_PROFILE\_CROSSING**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-231">Indique que le paquet est passé par les interfaces de plusieurs catégories réseau.</span><span class="sxs-lookup"><span data-stu-id="74557-231">Indicates that the packet has passed through interfaces of more than one network category.</span></span>

<span data-ttu-id="74557-232">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-232">Filtering layer:</span></span>

-   <span data-ttu-id="74557-233">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-233">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-234">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-234">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**\_condition fwp \_ réautoriser le \_ motif de la \_ \_ fin de la classification**</span><span class="sxs-lookup"><span data-stu-id="74557-235"><span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_CLASSIFY\_COMPLETION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-236">Indique qu’une connexion précédemment maintenue est maintenant autorisée à se terminer.</span><span class="sxs-lookup"><span data-stu-id="74557-236">Indicates that a previously held connection is now being allowed to complete.</span></span>

<span data-ttu-id="74557-237">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-237">Filtering layer:</span></span>

-   <span data-ttu-id="74557-238">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-238">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-239">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-239">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**\_condition fwp \_ réautoriser la \_ raison pour laquelle les \_ \_ Propriétés IPSec \_ ont changé**</span><span class="sxs-lookup"><span data-stu-id="74557-240"><span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_IPSEC\_PROPERTIES\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-241">Indique que les propriétés IPsec ont changé, ou que la connexion est passée d’un texte en clair à une connexion sécurisée.</span><span class="sxs-lookup"><span data-stu-id="74557-241">Indicates that IPsec properties have changed, or that the connection has changed from clear text to a secure connection.</span></span>

<span data-ttu-id="74557-242">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-242">Filtering layer:</span></span>

-   <span data-ttu-id="74557-243">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-243">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-244">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-244">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**\_condition fwp \_ réautoriser raison de l' \_ inspection du \_ \_ flux moyen \_**</span><span class="sxs-lookup"><span data-stu-id="74557-245"><span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_MID\_STREAM\_INSPECTION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-246">Indique qu’une connexion TCP précédemment établie est actuellement en cours d’inspection.</span><span class="sxs-lookup"><span data-stu-id="74557-246">Indicates that a previously established TCP connection is now being inspected.</span></span>

<span data-ttu-id="74557-247">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-247">Filtering layer:</span></span>

-   <span data-ttu-id="74557-248">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-248">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-249">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-249">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_condition fwp \_ réautoriser la \_ raison pour laquelle la \_ propriété de socket \_ \_ a changé**</span><span class="sxs-lookup"><span data-stu-id="74557-250"><span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_SOCKET\_PROPERTY\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-251">Indique que les propriétés de socket ont été définies après l’autorisation et l’établissement d’une connexion.</span><span class="sxs-lookup"><span data-stu-id="74557-251">Indicates that socket properties have been set after a connection was authorized and established.</span></span>

<span data-ttu-id="74557-252">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-252">Filtering layer:</span></span>

-   <span data-ttu-id="74557-253">FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-253">FWPM\_LAYER\_ALE\_AUTH\_CONNECT\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-254">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-254">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**\_condition fwp \_ réautoriser la \_ raison du \_ nouveau \_ \_ \_ \_ paquet Bcast de trafic entrant**</span><span class="sxs-lookup"><span data-stu-id="74557-255"><span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**FWP\_CONDITION\_REAUTHORIZE\_REASON\_NEW\_INBOUND\_MCAST\_BCAST\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-256">Indique que les nouveaux paquets de multidiffusion ou de diffusion entrants sont à nouveau autorisés au niveau des \_ appels de réception ALE \_ .</span><span class="sxs-lookup"><span data-stu-id="74557-256">Indicates that new inbound multicast or broadcast packets are being re-authorized at ALE\_RECV\_ACCEPT callouts.</span></span>

<span data-ttu-id="74557-257">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-257">Filtering layer:</span></span>

-   <span data-ttu-id="74557-258">FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-258">FWPM\_LAYER\_ALE\_AUTH\_RECV\_ACCEPT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="74557-259">Les indicateurs suivants spécifient les propriétés de socket qui sont liées au fait qu’une application souhaite recevoir le trafic de traversée latérale.</span><span class="sxs-lookup"><span data-stu-id="74557-259">The following flags specify socket properties which are related to whether an application wants to receive Edge Traversal traffic.</span></span> <span data-ttu-id="74557-260">Ces indicateurs et les couches de filtrage dans lesquelles ils peuvent être utilisés sont définis comme suit.</span><span class="sxs-lookup"><span data-stu-id="74557-260">These flags and the filtering layers where they can be used are defined as follows.</span></span>

> [!Note]  
> <span data-ttu-id="74557-261">Ces conditions de filtrage sont uniquement disponibles sur Windows Server 2008 R2, Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="74557-261">These filtering conditions are available only on Windows Server 2008 R2, Windows 7, and later.</span></span>

 

<dl> <dt>

<span data-ttu-id="74557-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**l' \_ indicateur de propriété de socket de condition fwp \_ est le \_ \_ \_ \_ \_ port système \_ RPC**</span><span class="sxs-lookup"><span data-stu-id="74557-262"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_IS\_SYSTEM\_PORT\_RPC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-263">Indique que l’application communique avec un port RPC dynamique.</span><span class="sxs-lookup"><span data-stu-id="74557-263">Indicates that the application is communicating with a dynamic RPC port.</span></span>

<span data-ttu-id="74557-264">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-264">Filtering layer:</span></span>

-   <span data-ttu-id="74557-265">Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-265">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-266">\_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-266">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_indicateur de propriété de socket de condition fwp \_ \_ \_ \_ autoriser \_ \_ le trafic Edge**</span><span class="sxs-lookup"><span data-stu-id="74557-267"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_ALLOW\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-268">Indique que l’application souhaite recevoir le trafic spécifique à la traversée latérale.</span><span class="sxs-lookup"><span data-stu-id="74557-268">Indicates that the application wants to receive edge traversal-specific traffic.</span></span>

<span data-ttu-id="74557-269">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-269">Filtering layer:</span></span>

-   <span data-ttu-id="74557-270">Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-270">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-271">\_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-271">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_indicateur de propriété de socket de condition fwp \_ \_ \_ \_ refuser \_ \_ le trafic de périphérie**</span><span class="sxs-lookup"><span data-stu-id="74557-272"><span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**FWP\_CONDITION\_SOCKET\_PROPERTY\_FLAG\_DENY\_EDGE\_TRAFFIC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-273">Indique que l’application ne souhaite pas recevoir ou traiter le trafic spécifique à travers la périphérie.</span><span class="sxs-lookup"><span data-stu-id="74557-273">Indicates that the application does not want to receive or process edge traversal-specific traffic.</span></span>

<span data-ttu-id="74557-274">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-274">Filtering layer:</span></span>

-   <span data-ttu-id="74557-275">Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-275">FWPM\_LAYER\_ALE\_AUTH\_LISTEN\_V{4\|6}</span></span>
-   <span data-ttu-id="74557-276">\_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}</span><span class="sxs-lookup"><span data-stu-id="74557-276">FWPM\_LAYER\_ALE\_RESOURCE\_ASSIGNMENT\_V{4\|6}</span></span>


</dt> </dl> </dd> </dl>

<span data-ttu-id="74557-277">Les indicateurs suivants spécifient les détails de connexion relatifs au filtrage L2.</span><span class="sxs-lookup"><span data-stu-id="74557-277">The following flags specify connection details related to L2 filtering.</span></span>

> [!Note]  
> <span data-ttu-id="74557-278">Ces conditions de filtrage sont uniquement disponibles sur Windows 8 et Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="74557-278">These filtering conditions are available only on Windows 8 and Windows Server 2012.</span></span>

 

<dl> <dt>

<span data-ttu-id="74557-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**La \_ condition fwp \_ L2 \_ est \_ native \_ Ethernet**</span><span class="sxs-lookup"><span data-stu-id="74557-279"><span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**FWP\_CONDITION\_L2\_IS\_NATIVE\_ETHERNET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-280">Indique que la connexion est native Ethernet.</span><span class="sxs-lookup"><span data-stu-id="74557-280">Indicates that the connection is native Ethernet.</span></span>

<span data-ttu-id="74557-281">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-281">Filtering layer:</span></span>

-   <span data-ttu-id="74557-282">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-282">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-283">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-283">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-284">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-284">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-285">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-285">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**La \_ condition fwp \_ L2 \_ est \_ WiFi**</span><span class="sxs-lookup"><span data-stu-id="74557-286"><span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**FWP\_CONDITION\_L2\_IS\_WIFI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-287">Indique que la connexion est Wi-Fi.</span><span class="sxs-lookup"><span data-stu-id="74557-287">Indicates that the connection is Wi-Fi.</span></span>

<span data-ttu-id="74557-288">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-288">Filtering layer:</span></span>

-   <span data-ttu-id="74557-289">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-289">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-290">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-290">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-291">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-291">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-292">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-292">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**La \_ condition fwp \_ L2 \_ est \_ Mobile \_ Broadband**</span><span class="sxs-lookup"><span data-stu-id="74557-293"><span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**FWP\_CONDITION\_L2\_IS\_MOBILE\_BROADBAND**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-294">Indique que la connexion est de haut débit mobile.</span><span class="sxs-lookup"><span data-stu-id="74557-294">Indicates that the connection is mobile broadband.</span></span>

<span data-ttu-id="74557-295">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-295">Filtering layer:</span></span>

-   <span data-ttu-id="74557-296">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-296">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-297">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-297">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-298">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-298">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-299">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-299">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**\_La condition fwp \_ L2 \_ est \_ WiFi \_ direct \_ Data**</span><span class="sxs-lookup"><span data-stu-id="74557-300"><span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**FWP\_CONDITION\_L2\_IS\_WIFI\_DIRECT\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-301">Indique que la connexion est Wi-Fi directe.</span><span class="sxs-lookup"><span data-stu-id="74557-301">Indicates that the connection is Wi-Fi Direct.</span></span>

<span data-ttu-id="74557-302">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-302">Filtering layer:</span></span>

-   <span data-ttu-id="74557-303">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-303">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-304">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-304">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-305">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-305">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-306">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-306">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**La \_ condition fwp \_ L2 \_ est \_ VM2VM**</span><span class="sxs-lookup"><span data-stu-id="74557-307"><span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**FWP\_CONDITION\_L2\_IS\_VM2VM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-308">Indique que la connexion se fait entre des machines virtuelles.</span><span class="sxs-lookup"><span data-stu-id="74557-308">Indicates that the connection is between virtual machines.</span></span>

<span data-ttu-id="74557-309">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-309">Filtering layer:</span></span>

-   <span data-ttu-id="74557-310">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-310">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-311">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-311">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-312">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-312">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-313">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-313">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**La \_ condition fwp \_ L2 \_ est un \_ paquet mal formé \_**</span><span class="sxs-lookup"><span data-stu-id="74557-314"><span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**FWP\_CONDITION\_L2\_IS\_MALFORMED\_PACKET**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-315">Indique qu’un paquet semble incorrect.</span><span class="sxs-lookup"><span data-stu-id="74557-315">Indicates that a packet appears to be malformed.</span></span>

<span data-ttu-id="74557-316">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-316">Filtering layer:</span></span>

-   <span data-ttu-id="74557-317">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-317">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-318">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-318">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-319">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-319">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-320">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-320">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**La \_ condition fwp \_ L2 \_ est un \_ \_ groupe de fragments IP \_**</span><span class="sxs-lookup"><span data-stu-id="74557-321"><span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**FWP\_CONDITION\_L2\_IS\_IP\_FRAGMENT\_GROUP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-322">Indique un groupe de fragments de paquets IP.</span><span class="sxs-lookup"><span data-stu-id="74557-322">Indicates an IP packet fragment group.</span></span>

<span data-ttu-id="74557-323">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-323">Filtering layer:</span></span>

-   <span data-ttu-id="74557-324">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-324">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-325">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-325">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-326">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-326">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-327">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-327">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="74557-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_Condition fwp \_ L2 \_ si le \_ connecteur est \_ présent**</span><span class="sxs-lookup"><span data-stu-id="74557-328"><span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**FWP\_CONDITION\_L2\_IF\_CONNECTOR\_PRESENT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="74557-329">Indique qu’un connecteur est présent.</span><span class="sxs-lookup"><span data-stu-id="74557-329">Indicates that a connector is present.</span></span>

<span data-ttu-id="74557-330">Couche de filtrage :</span><span class="sxs-lookup"><span data-stu-id="74557-330">Filtering layer:</span></span>

-   <span data-ttu-id="74557-331">couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="74557-331">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-332">couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif</span><span class="sxs-lookup"><span data-stu-id="74557-332">FWPM\_LAYER\_INBOUND\_MAC\_FRAME\_NATIVE</span></span>
-   <span data-ttu-id="74557-333">couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_</span><span class="sxs-lookup"><span data-stu-id="74557-333">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_ETHERNET</span></span>
-   <span data-ttu-id="74557-334">\_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native</span><span class="sxs-lookup"><span data-stu-id="74557-334">FWPM\_LAYER\_OUTBOUND\_MAC\_FRAME\_NATIVE</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="74557-335">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="74557-335">Requirements</span></span>



| <span data-ttu-id="74557-336">Condition requise</span><span class="sxs-lookup"><span data-stu-id="74557-336">Requirement</span></span> | <span data-ttu-id="74557-337">Valeur</span><span class="sxs-lookup"><span data-stu-id="74557-337">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74557-338">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74557-338">Minimum supported client</span></span><br/> | <span data-ttu-id="74557-339">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74557-339">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="74557-340">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="74557-340">Minimum supported server</span></span><br/> | <span data-ttu-id="74557-341">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="74557-341">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74557-342">En-tête</span><span class="sxs-lookup"><span data-stu-id="74557-342">Header</span></span><br/>                   | <dl> <span data-ttu-id="74557-343"><dt>Fwptypes. h</dt></span><span class="sxs-lookup"><span data-stu-id="74557-343"><dt>Fwptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74557-344">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="74557-344">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74557-345">**Filtrage des identificateurs de couche**</span><span class="sxs-lookup"><span data-stu-id="74557-345">**Filtering Layer Identifiers**</span></span>](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

