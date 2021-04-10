---
title: Conditions de filtrage disponibles pour chaque couche de filtrage (Fwpmu. h)
description: Le moteur de filtre de la plateforme de filtrage Windows (WFP) prend en charge un ensemble différent de conditions de filtrage à chacune de ses couches de filtrage.
ms.assetid: 6faace21-44ec-49dd-8e77-e403c258c14a
topic_type:
- apiref
api_name:
- FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD
- FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD
- FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD
- FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD
- FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD
- FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6
- FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD
- FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6
- FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD
- FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6
- FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6
- FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD
- FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD
- FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6
- FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD
- FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD
- FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6
- FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6
- FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6
- FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6
- FWPM_LAYER_RPC_UM
- FWPM_LAYER_RPC_EPMAP
- FWPM_LAYER_RPC_EP_ADD
- FWPM_LAYER_RPC_PROXY_CONN
- FWPM_LAYER_RPC_PROXY_IF
- FWPM_LAYER_KM_AUTHORIZATION
- FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET
- FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE
- FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET
- FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0c3806c7c3c7a5fa7f10af0e5e11c212bd93e3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941655"
---
# <a name="filtering-conditions-available-at-each-filtering-layer"></a><span data-ttu-id="a8478-103">Conditions de filtrage disponibles pour chaque couche de filtrage</span><span class="sxs-lookup"><span data-stu-id="a8478-103">Filtering Conditions Available at Each Filtering Layer</span></span>

<span data-ttu-id="a8478-104">Le moteur de filtre de la plateforme de filtrage Windows (WFP) prend en charge un ensemble différent de conditions de filtrage à chacune de ses couches de filtrage.</span><span class="sxs-lookup"><span data-stu-id="a8478-104">The Windows Filtering Platform (WFP) filter engine supports a different set of filtering conditions at each of its filtering layers.</span></span>

<span data-ttu-id="a8478-105">La liste des conditions de filtrage disponibles à chaque couche est la suivante.</span><span class="sxs-lookup"><span data-stu-id="a8478-105">The list of filtering conditions that are available at each layer are as follows.</span></span>

## <a name="fwpm_layer_inbound_ippacket_v4--fwpm_layer_inbound_ippacket_v4_discard--fwpm_layer_inbound_ippacket_v6--fwpm_layer_inbound_ippacket_v6_discard"></a><span data-ttu-id="a8478-106">FWPM_LAYER_INBOUND_IPPACKET_V4/FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_INBOUND_IPPACKET_V6/FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-106">FWPM_LAYER_INBOUND_IPPACKET_V4 / FWPM_LAYER_INBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_INBOUND_IPPACKET_V6 / FWPM_LAYER_INBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-107">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-107">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-108">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-108">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-109">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-109">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-110">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-111">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-112">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-113">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-114">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-115">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-115">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_outbound_ippacket_v4--fwpm_layer_outbound_ippacket_v4_discard--fwpm_layer_outbound_ippacket_v6--fwpm_layer_outbound_ippacket_v6_discard"></a><span data-ttu-id="a8478-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4/FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD/FWPM_LAYER_OUTBOUND_IPPACKET_V6/FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-116">FWPM_LAYER_OUTBOUND_IPPACKET_V4 / FWPM_LAYER_OUTBOUND_IPPACKET_V4_DISCARD / FWPM_LAYER_OUTBOUND_IPPACKET_V6 / FWPM_LAYER_OUTBOUND_IPPACKET_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-117">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-117">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-118">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-118">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-119">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-119">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-120">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-121">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-122">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-123">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-124">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-125">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-125">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_ipforward_v4--fwpm_layer_ipforward_v4_discard--fwpm_layer_ipforward_v6--fwpm_layer_ipforward_v6_discard"></a><span data-ttu-id="a8478-126">FWPM_LAYER_IPFORWARD_V4/FWPM_LAYER_IPFORWARD_V4_DISCARD/FWPM_LAYER_IPFORWARD_V6/FWPM_LAYER_IPFORWARD_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-126">FWPM_LAYER_IPFORWARD_V4 / FWPM_LAYER_IPFORWARD_V4_DISCARD / FWPM_LAYER_IPFORWARD_V6 / FWPM_LAYER_IPFORWARD_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-127">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-127">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-128">FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-129">FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-130">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="a8478-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-131">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-132">FWPM_CONDITION_IP_FORWARD_INTERFACE</span></span>
- <span data-ttu-id="a8478-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-133">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-134">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="a8478-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-135">FWPM_CONDITION_SOURCE_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-136">FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-137">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-137">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-138">FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE</span></span> 
- <span data-ttu-id="a8478-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-139">FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="a8478-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-140">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="a8478-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-141">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_inbound_transport_v4--fwpm_layer_inbound_transport_v4_discard--fwpm_layer_inbound_transport_v6--fwpm_layer_inbound_transport_v6_discard"></a><span data-ttu-id="a8478-142">FWPM_LAYER_INBOUND_TRANSPORT_V4/FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_INBOUND_TRANSPORT_V6/FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-142">FWPM_LAYER_INBOUND_TRANSPORT_V4 / FWPM_LAYER_INBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_INBOUND_TRANSPORT_V6 / FWPM_LAYER_INBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-143">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-143">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-144">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-144">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-145">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-145">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-146">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-147">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-148">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-149">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-149">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-150">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-150">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-151">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-152">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-152">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-153">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-154">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-154">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-155">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-155">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-156">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_transport_v4--fwpm_layer_outbound_transport_v4_discard--fwpm_layer_outbound_transport_v6--fwpm_layer_outbound_transport_v6_discard"></a><span data-ttu-id="a8478-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4/FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD/FWPM_LAYER_OUTBOUND_TRANSPORT_V6/FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-157">FWPM_LAYER_OUTBOUND_TRANSPORT_V4 / FWPM_LAYER_OUTBOUND_TRANSPORT_V4_DISCARD / FWPM_LAYER_OUTBOUND_TRANSPORT_V6 / FWPM_LAYER_OUTBOUND_TRANSPORT_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-158">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-158">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-159">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-159">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-160">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-160">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-161">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-162">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-163">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-164">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-165">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-165">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-166">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-166">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-167">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-168">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-168">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-169">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-170">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-170">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-171">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-171">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-172">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_stream_v4--fwpm_layer_stream_v4_discard--fwpm_layer_stream_v6--fwpm_layer_stream_v6_discard"></a><span data-ttu-id="a8478-173">FWPM_LAYER_STREAM_V4/FWPM_LAYER_STREAM_V4_DISCARD/FWPM_LAYER_STREAM_V6/FWPM_LAYER_STREAM_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-173">FWPM_LAYER_STREAM_V4 / FWPM_LAYER_STREAM_V4_DISCARD / FWPM_LAYER_STREAM_V6 / FWPM_LAYER_STREAM_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-174">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="a8478-174">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="a8478-175">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-175">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-176">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-177">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-178">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-178">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-179">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-180">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-180">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
## <a name="fwpm_layer_datagram_data_v4--fwpm_layer_datagram_data_v4_discard--fwpm_layer_datagram_data_v6--fwpm_layer_datagram_data_v6_discard"></a><span data-ttu-id="a8478-181">FWPM_LAYER_DATAGRAM_DATA_V4/FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD/FWPM_LAYER_DATAGRAM_DATA_V6/FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-181">FWPM_LAYER_DATAGRAM_DATA_V4 / FWPM_LAYER_DATAGRAM_DATA_V4_DISCARD / FWPM_LAYER_DATAGRAM_DATA_V6 / FWPM_LAYER_DATAGRAM_DATA_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-182">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="a8478-182">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="a8478-183">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-183">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-184">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-184">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-185">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-185">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-186">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-187">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-188">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-189">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-189">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-190">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-190">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-191">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-192">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-192">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-193">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-194">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-194">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_stream_packet-v4--fwpm_layer_stream_packet-v6"></a><span data-ttu-id="a8478-195">FWPM_LAYER_STREAM_PACKET V4/FWPM_LAYER_STREAM_PACKET V6</span><span class="sxs-lookup"><span data-stu-id="a8478-195">FWPM_LAYER_STREAM_PACKET V4 / FWPM_LAYER_STREAM_PACKET V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-196">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-196">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-197">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="a8478-197">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="a8478-198">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-198">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-199">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-199">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-200">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-200">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-201">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-202">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-203">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-203">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-204">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-205">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-205">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-206">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-207">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-207">FWPM_CONDITION_TUNNEL_TYPE</span></span>
## <a name="fwpm_layer_inbound_icmp_error_v4--fwpm_layer_inbound_icmp_error_v4_discard--fwpm_layer_inbound_icmp_error_v6--fwpm_layer_inbound_icmp_error_v6_discard"></a><span data-ttu-id="a8478-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4/FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_INBOUND_ICMP_ERROR_V6/FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-208">FWPM_LAYER_INBOUND_ICMP_ERROR_V4 / FWPM_LAYER_INBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_INBOUND_ICMP_ERROR_V6 / FWPM_LAYER_INBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-209">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-210">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7 :** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-211">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-212">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="a8478-213">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-213">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-214">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="a8478-214">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="a8478-215">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-215">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="a8478-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-216">FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-217">FWPM_CONDITION_EMBEDDED_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-218">FWPM_CONDITION_EMBEDDED_PROTOCOL</span></span>
- <span data-ttu-id="a8478-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-219">FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-220">FWPM_CONDITION_EMBEDDED_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-221">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-222">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-223">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-224">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7 :** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-225">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7 :** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-226">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7 :** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-227">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-228">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-228">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-229">FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_outbound_icmp_error_v4--fwpm_layer_outbound_icmp_error_v4_discard--fwpm_layer_outbound_icmp_error_v6--fwpm_layer_outbound_icmp_error_v6_discard"></a><span data-ttu-id="a8478-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6/FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-230">FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V4_DISCARD / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6 / FWPM_LAYER_OUTBOUND_ICMP_ERROR_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-231">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-231">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-232">FWPM_CONDITION_ICMP_CODE</span><span class="sxs-lookup"><span data-stu-id="a8478-232">FWPM_CONDITION_ICMP_CODE</span></span>
- <span data-ttu-id="a8478-233">FWPM_CONDITION_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-233">FWPM_CONDITION_ICMP_TYPE</span></span>

- <span data-ttu-id="a8478-234">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-234">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-235">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-235">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-236">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-237">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-238">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-239">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-240">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-241">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-241">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-242">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-242">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-243">FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID</span></span>
## <a name="fwpm_layer_ale_bind_redirect_v4--fwpm_layer_ale_bind_redirect-v6"></a><span data-ttu-id="a8478-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4/FWPM_LAYER_ALE_BIND_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="a8478-244">FWPM_LAYER_ALE_BIND_REDIRECT_V4 / FWPM_LAYER_ALE_BIND_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-245">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-245">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-246">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-246">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-247">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-247">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-248">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-248">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-249">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-250">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-251">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-251">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-252">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-252">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-253">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-253">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-254">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-254">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_assignment_v4--fwpm_layer_ale_resource_assignment_v4_discard--fwpm_layer_ale_resource_assignment_v6--fwpm_layer_ale_resource_assignment_v6_discard"></a><span data-ttu-id="a8478-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6/FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-255">FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V4_DISCARD / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6 / FWPM_LAYER_ALE_RESOURCE_ASSIGNMENT_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-256">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-256">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span><span class="sxs-lookup"><span data-stu-id="a8478-257">FWPM_CONDITION_ALE_PROMISCUOUS_MODE</span></span>
- <span data-ttu-id="a8478-258">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-258">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-259">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-259">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-260">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-260">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-261">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-262">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-263">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-264">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-264">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-265">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-265">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-266">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-266">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-267">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-267">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-268">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="a8478-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-269">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-270">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-270">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-271">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-271">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_resource_release_v4--fwpm_layer_ale_resource_release_v6"></a><span data-ttu-id="a8478-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4/FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-272">FWPM_LAYER_ALE_RESOURCE_RELEASE_V4 / FWPM_LAYER_ALE_RESOURCE_RELEASE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-273">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-273">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-274">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-274">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-275">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-275">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-276">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-276">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-277">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-278">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-279">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-280">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-280">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-281">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-281">FWPM_CONDITION_IP_PROTOCOL</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-282">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-282">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-283">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-283">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_endpoint_closure_v4--fwpm_layer_ale_endpoint_closure_v6"></a><span data-ttu-id="a8478-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4/FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-284">FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V4 / FWPM_LAYER_ALE_ENDPOINT_CLOSURE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-285">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-285">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-286">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-286">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-287">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-287">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-288">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-288">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-289">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-290">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-291">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-292">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-292">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-293">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-293">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-294">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-295">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-295">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-296">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-296">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-297">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-297">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_listen_v4--fwpm_layer_ale_auth_listen_v4_discard--fwpm_layer_ale_auth_listen_v6--fwpm_layer_ale_auth_listen_v6_discard"></a><span data-ttu-id="a8478-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4/FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD/FWPM_LAYER_ALE_AUTH_LISTEN_V6/FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-298">FWPM_LAYER_ALE_AUTH_LISTEN_V4 / FWPM_LAYER_ALE_AUTH_LISTEN_V4_DISCARD / FWPM_LAYER_ALE_AUTH_LISTEN_V6 / FWPM_LAYER_ALE_AUTH_LISTEN_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-299">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-299">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-300">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-300">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-301">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-301">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-302">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-302">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-303">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-304">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-305">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-306">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-306">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-307">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-307">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-308">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-308">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-309">FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID</span></span>
- <span data-ttu-id="a8478-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-310">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-311">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-311">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-312">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-312">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_recv_accept_v4--fwpm_layer_ale_auth_recv_accept_v4_discard--fwpm_layer_ale_auth_recv_accept_v6--fwpm_layer_ale_auth_recv_accept_v6_discard"></a><span data-ttu-id="a8478-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6/FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-313">FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6 / FWPM_LAYER_ALE_AUTH_RECV_ACCEPT_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-314">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-314">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="a8478-315">FWPM_CONDITION_ALE_NAP_CONTEXT</span></span>
- <span data-ttu-id="a8478-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-316">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="a8478-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-317">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="a8478-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-318">FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</span></span>
- <span data-ttu-id="a8478-319">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-319">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-320">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-321">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista/Windows 7 :** FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-322">FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-323">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="a8478-324">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-324">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-325">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-326">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-327">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-328">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-329">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-329">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-330">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-330">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-331">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-332">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-332">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista/Windows 7 :** FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-333">FWPM_CONDITION_LOCAL_INTERFACE_INDEX **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista/Windows 7 :** FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-334">FWPM_CONDITION_LOCAL_INTERFACE_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista/Windows 7 :** FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-335">FWPM_CONDITION_LOCAL_TUNNEL_TYPE **Windows Vista / Windows 7:** FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-336">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-336">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-337">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-338">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="a8478-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-339">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-340">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="a8478-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-341">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-342">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="a8478-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-343">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="a8478-344">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="a8478-344">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="a8478-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-345">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-346">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-346">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-347">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-347">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_connect_redirect_v4--fwpm_layer_ale_connect_redirect-v6"></a><span data-ttu-id="a8478-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4/FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span><span class="sxs-lookup"><span data-stu-id="a8478-348">FWPM_LAYER_ALE_CONNECT_REDIRECT_V4 / FWPM_LAYER_ALE_CONNECT_REDIRECT V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-349">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-349">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-350">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-350">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-351">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-351">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-352">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-352">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-353">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-354">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-355">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-355">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-356">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-356">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-357">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-357">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-358">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-359">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-360">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-360">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-361">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-361">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_auth_connect_v4--fwpm_layer_ale_auth_connect_v4_discard--fwpm_layer_ale_auth_connect_v6--fwpm_layer_ale_auth_connect_v6_discard"></a><span data-ttu-id="a8478-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4/FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD/FWPM_LAYER_ALE_AUTH_CONNECT_V6/FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-362">FWPM_LAYER_ALE_AUTH_CONNECT_V4 / FWPM_LAYER_ALE_AUTH_CONNECT_V4_DISCARD / FWPM_LAYER_ALE_AUTH_CONNECT_V6 / FWPM_LAYER_ALE_AUTH_CONNECT_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-363">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-363">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-364">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="a8478-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-365">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="a8478-366">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-366">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-367">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-367">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-368">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-368">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-369">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-370">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-371">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-372">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-373">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-373">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-374">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-374">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-375">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-376">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-376">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-377">FWPM_CONDITION_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-378">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-378">FWPM_CONDITION_TUNNEL_TYPE</span></span>
- <span data-ttu-id="a8478-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-379">FWPM_CONDITION_IP_ARRIVAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-380">FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-381">FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE</span></span>
- <span data-ttu-id="a8478-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 et laterFWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-382">FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX Windows Vista _sp1 and laterFWPM_CONDITION_INTERFACE_INDEX</span></span> 
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-383">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-383">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-384">FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-385">FWPM_CONDITION_IP_NEXTHOP_INTERFACE</span></span>
- <span data-ttu-id="a8478-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-386">FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-387">FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE</span></span>
- <span data-ttu-id="a8478-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-388">FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-389">FWPM_CONDITION_ORIGINAL_PROFILE_ID</span></span>
- <span data-ttu-id="a8478-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-390">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
- <span data-ttu-id="a8478-391">FWPM_CONDITION_REAUTHORIZE_REASON</span><span class="sxs-lookup"><span data-stu-id="a8478-391">FWPM_CONDITION_REAUTHORIZE_REASON</span></span>
- <span data-ttu-id="a8478-392">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="a8478-392">FWPM_CONDITION_PEER_NAME</span></span>
- <span data-ttu-id="a8478-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-393">FWPM_CONDITION_ORIGINAL_ICMP_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-394">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-394">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-395">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-395">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_ale_flow_established_v4--fwpm_layer_ale_flow_established_v4_discard--fwpm_layer_ale_flow_established_v6--fwpm_layer_ale_flow_established_v6_discard"></a><span data-ttu-id="a8478-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6/FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span><span class="sxs-lookup"><span data-stu-id="a8478-396">FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V4_DISCARD / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6 / FWPM_LAYER_ALE_FLOW_ESTABLISHED_V6_DISCARD</span></span>
- <span data-ttu-id="a8478-397">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-397">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-398">FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</span></span>
- <span data-ttu-id="a8478-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-399">FWPM_CONDITION_ALE_REMOTE_USER_ID</span></span>
- <span data-ttu-id="a8478-400">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-400">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-401">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="a8478-401">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="a8478-402">FWPM_CONDITION_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-402">FWPM_CONDITION_FLAGS</span></span>
- <span data-ttu-id="a8478-403">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-403">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-404">FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-405">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-406">FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-407">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-408">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-408">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-409">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-409">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-410">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-411">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-411">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
- <span data-ttu-id="a8478-412">FWPM_CONDITION_TUNNEL_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-412">FWPM_CONDITION_TUNNEL_TYPE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-413">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-413">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-414">FWPM_CONDITION_ALE_PACKAGE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-414">FWPM_CONDITION_ALE_PACKAGE_ID</span></span>
## <a name="fwpm_layer_name_resolution_cache_v4--fwpm_layer_name_resolution_cache_v6"></a><span data-ttu-id="a8478-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4/FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-415">FWPM_LAYER_NAME_RESOLUTION_CACHE_V4 / FWPM_LAYER_NAME_RESOLUTION_CACHE_V6</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-416">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-416">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-417">FWPM_CONDITION_ALE_USER_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-417">FWPM_CONDITION_ALE_USER_ID</span></span>
- <span data-ttu-id="a8478-418">FWPM_CONDITION_ALE_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-418">FWPM_CONDITION_ALE_APP_ID</span></span>
- <span data-ttu-id="a8478-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-419">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-420">FWPM_CONDITION_PEER_NAME</span><span class="sxs-lookup"><span data-stu-id="a8478-420">FWPM_CONDITION_PEER_NAME</span></span>
## <a name="fwpm_layer_ipsec_km_demux_v4--fwpm_layer_ipsec_km_demux_v6"></a><span data-ttu-id="a8478-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4/FWPM_LAYER_IPSEC_KM_DEMUX_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-421">FWPM_LAYER_IPSEC_KM_DEMUX_V4 / FWPM_LAYER_IPSEC_KM_DEMUX_V6</span></span>
- <span data-ttu-id="a8478-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-422">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-423">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
## <a name="fwpm_layer_ipsec_v4--fwpm_layer_ipsec_v6"></a><span data-ttu-id="a8478-424">FWPM_LAYER_IPSEC_V4/FWPM_LAYER_IPSEC_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-424">FWPM_LAYER_IPSEC_V4 / FWPM_LAYER_IPSEC_V6</span></span>
- <span data-ttu-id="a8478-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-425">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-426">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-426">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-427">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-427">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-428">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-429">FWPM_CONDITION_IP_REMOTE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-429">FWPM_CONDITION_IP_REMOTE_PORT</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-430">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-430">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-431">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-432">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_ikeext_v4--fwpm_layer_ikeext_v6"></a><span data-ttu-id="a8478-433">FWPM_LAYER_IKEEXT_V4/FWPM_LAYER_IKEEXT_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-433">FWPM_LAYER_IKEEXT_V4 / FWPM_LAYER_IKEEXT_V6</span></span>
- <span data-ttu-id="a8478-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-434">FWPM_CONDITION_IP_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-435">FWPM_CONDITION_IP_REMOTE_ADDRESS</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-436">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-436">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-437">FWPM_CONDITION_IP_LOCAL_INTERFACE</span></span>
- <span data-ttu-id="a8478-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-438">FWPM_CONDITION_CURRENT_PROFILE_ID</span></span>
## <a name="fwpm_layer_rpc_um"></a><span data-ttu-id="a8478-439">FWPM_LAYER_RPC_UM</span><span class="sxs-lookup"><span data-stu-id="a8478-439">FWPM_LAYER_RPC_UM</span></span>
- <span data-ttu-id="a8478-440">FWPM_CONDITION_DCOM_APP_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-440">FWPM_CONDITION_DCOM_APP_ID</span></span>
- <span data-ttu-id="a8478-441">FWPM_CONDITION_IMAGE_NAME</span><span class="sxs-lookup"><span data-stu-id="a8478-441">FWPM_CONDITION_IMAGE_NAME</span></span>
- <span data-ttu-id="a8478-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="a8478-442">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="a8478-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-443">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="a8478-444">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-444">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="a8478-445">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="a8478-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-446">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>
- <span data-ttu-id="a8478-447">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="a8478-447">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="a8478-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="a8478-448">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="a8478-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="a8478-449">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="a8478-450">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-450">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="a8478-451">FWPM_CONDITION_RPC_IF_FLAG</span><span class="sxs-lookup"><span data-stu-id="a8478-451">FWPM_CONDITION_RPC_IF_FLAG</span></span>
- <span data-ttu-id="a8478-452">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="a8478-452">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="a8478-453">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="a8478-453">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="a8478-454">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-454">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="a8478-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="a8478-455">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="a8478-456">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="a8478-456">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_epmap"></a><span data-ttu-id="a8478-457">FWPM_LAYER_RPC_EPMAP</span><span class="sxs-lookup"><span data-stu-id="a8478-457">FWPM_LAYER_RPC_EPMAP</span></span>
- <span data-ttu-id="a8478-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="a8478-458">FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</span></span>
- <span data-ttu-id="a8478-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-459">FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</span></span>
- <span data-ttu-id="a8478-460">FWPM_CONDITION_IP_LOCAL_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-460">FWPM_CONDITION_IP_LOCAL_PORT</span></span>
- <span data-ttu-id="a8478-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span><span class="sxs-lookup"><span data-stu-id="a8478-461">FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</span></span>
- <span data-ttu-id="a8478-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-462">FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</span></span>

- <span data-ttu-id="a8478-463">FWPM_CONDITION_PIPE</span><span class="sxs-lookup"><span data-stu-id="a8478-463">FWPM_CONDITION_PIPE</span></span>
- <span data-ttu-id="a8478-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span><span class="sxs-lookup"><span data-stu-id="a8478-464">FWPM_CONDITION_REMOTE_USER_TOKEN</span></span>
- <span data-ttu-id="a8478-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span><span class="sxs-lookup"><span data-stu-id="a8478-465">FWPM_CONDITION_RPC_AUTH_LEVEL</span></span>
- <span data-ttu-id="a8478-466">FWPM_CONDITION_RPC_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-466">FWPM_CONDITION_RPC_AUTH_TYPE</span></span>
- <span data-ttu-id="a8478-467">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="a8478-467">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="a8478-468">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="a8478-468">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="a8478-469">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-469">FWPM_CONDITION_RPC_PROTOCOL</span></span>
- <span data-ttu-id="a8478-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span><span class="sxs-lookup"><span data-stu-id="a8478-470">FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</span></span>
- <span data-ttu-id="a8478-471">FWPM_CONDITION_SEC_KEY_SIZE</span><span class="sxs-lookup"><span data-stu-id="a8478-471">FWPM_CONDITION_SEC_KEY_SIZE</span></span>
## <a name="fwpm_layer_rpc_ep_add"></a><span data-ttu-id="a8478-472">FWPM_LAYER_RPC_EP_ADD</span><span class="sxs-lookup"><span data-stu-id="a8478-472">FWPM_LAYER_RPC_EP_ADD</span></span>
- <span data-ttu-id="a8478-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="a8478-473">FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</span></span>
- <span data-ttu-id="a8478-474">FWPM_CONDITION_RPC_EP_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-474">FWPM_CONDITION_RPC_EP_FLAGS</span></span>
- <span data-ttu-id="a8478-475">FWPM_CONDITION_RPC_EP_VALUE</span><span class="sxs-lookup"><span data-stu-id="a8478-475">FWPM_CONDITION_RPC_EP_VALUE</span></span>
- <span data-ttu-id="a8478-476">FWPM_CONDITION_RPC_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-476">FWPM_CONDITION_RPC_PROTOCOL</span></span>
## <a name="fwpm_layer_rpc_proxy_conn"></a><span data-ttu-id="a8478-477">FWPM_LAYER_RPC_PROXY_CONN</span><span class="sxs-lookup"><span data-stu-id="a8478-477">FWPM_LAYER_RPC_PROXY_CONN</span></span>
- <span data-ttu-id="a8478-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="a8478-478">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="a8478-479">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="a8478-479">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="a8478-480">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="a8478-480">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="a8478-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-481">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="a8478-482">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="a8478-482">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="a8478-483">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-483">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_rpc_proxy_if"></a><span data-ttu-id="a8478-484">FWPM_LAYER_RPC_PROXY_IF</span><span class="sxs-lookup"><span data-stu-id="a8478-484">FWPM_LAYER_RPC_PROXY_IF</span></span>
- <span data-ttu-id="a8478-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span><span class="sxs-lookup"><span data-stu-id="a8478-485">FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</span></span>
- <span data-ttu-id="a8478-486">FWPM_CONDITION_CLIENT_CERT_OID</span><span class="sxs-lookup"><span data-stu-id="a8478-486">FWPM_CONDITION_CLIENT_CERT_OID</span></span>
- <span data-ttu-id="a8478-487">FWPM_CONDITION_CLIENT_TOKEN</span><span class="sxs-lookup"><span data-stu-id="a8478-487">FWPM_CONDITION_CLIENT_TOKEN</span></span>
- <span data-ttu-id="a8478-488">FWPM_CONDITION_RPC_IF_UUID</span><span class="sxs-lookup"><span data-stu-id="a8478-488">FWPM_CONDITION_RPC_IF_UUID</span></span>
- <span data-ttu-id="a8478-489">FWPM_CONDITION_RPC_IF_VERSION</span><span class="sxs-lookup"><span data-stu-id="a8478-489">FWPM_CONDITION_RPC_IF_VERSION</span></span>
- <span data-ttu-id="a8478-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-490">FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</span></span>
- <span data-ttu-id="a8478-491">FWPM_CONDITION_RPC_SERVER_NAME</span><span class="sxs-lookup"><span data-stu-id="a8478-491">FWPM_CONDITION_RPC_SERVER_NAME</span></span>
- <span data-ttu-id="a8478-492">FWPM_CONDITION_RPC_SERVER_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-492">FWPM_CONDITION_RPC_SERVER_PORT</span></span>
## <a name="fwpm_layer_km_authorization"></a><span data-ttu-id="a8478-493">FWPM_LAYER_KM_AUTHORIZATION</span><span class="sxs-lookup"><span data-stu-id="a8478-493">FWPM_LAYER_KM_AUTHORIZATION</span></span>
###  <a name="windows-7--and-later"></a><span data-ttu-id="a8478-494">Windows 7 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-494">Windows 7  and later</span></span>
- <span data-ttu-id="a8478-495">FWPM_CONDITION_REMOTE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-495">FWPM_CONDITION_REMOTE_ID</span></span>
- <span data-ttu-id="a8478-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-496">FWPM_CONDITION_AUTHENTICATION_TYPE</span></span>
- <span data-ttu-id="a8478-497">FWPM_CONDITION_KM_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-497">FWPM_CONDITION_KM_TYPE</span></span>
- <span data-ttu-id="a8478-498">FWPM_CONDITION_KM_MODE</span><span class="sxs-lookup"><span data-stu-id="a8478-498">FWPM_CONDITION_KM_MODE</span></span>
- <span data-ttu-id="a8478-499">FWPM_CONDITION_DIRECTION</span><span class="sxs-lookup"><span data-stu-id="a8478-499">FWPM_CONDITION_DIRECTION</span></span>
- <span data-ttu-id="a8478-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span><span class="sxs-lookup"><span data-stu-id="a8478-500">FWPM_CONDITION_IPSEC_POLICY_KEY</span></span>
## <a name="fwpm_layer_inbound_mac_frame_ethernet--fwpm_layer_outbound_mac_frame_ethernet"></a><span data-ttu-id="a8478-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET/FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="a8478-501">FWPM_LAYER_INBOUND_MAC_FRAME_ETHERNET / FWPM_LAYER_OUTBOUND_MAC_FRAME_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-502">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-502">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-503">FWPM_CONDITION_INTERFACE_MAC_ADDRESS</span></span>
- <span data-ttu-id="a8478-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-504">FWPM_CONDITION_MAC_LOCAL_ADDRESS</span></span>
- <span data-ttu-id="a8478-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-505">FWPM_CONDITION_MAC_REMOTE_ADDRESS</span></span>
- <span data-ttu-id="a8478-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-506">FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-507">FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-508">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-508">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="a8478-509">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-509">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="a8478-510">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-510">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="a8478-511">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-511">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-512">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-512">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="a8478-513">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-513">FWPM_CONDITION_L2_FLAGS</span></span>
##  <a name="fwpm_layer_inbound_mac_frame_native--fwpm_layer_outbound_mac_frame_native"></a><span data-ttu-id="a8478-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE/FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span><span class="sxs-lookup"><span data-stu-id="a8478-514">FWPM_LAYER_INBOUND_MAC_FRAME_NATIVE / FWPM_LAYER_OUTBOUND_MAC_FRAME_NATIVE</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-515">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-515">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-516">FWPM_CONDITION_NDIS_MEDIA_TYPE</span></span>
- <span data-ttu-id="a8478-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-517">FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</span></span>
- <span data-ttu-id="a8478-518">FWPM_CONDITION_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="a8478-518">FWPM_CONDITION_INTERFACE</span></span>
- <span data-ttu-id="a8478-519">FWPM_CONDITION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-519">FWPM_CONDITION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-520">FWPM_CONDITION_INTERFACE_INDEX</span><span class="sxs-lookup"><span data-stu-id="a8478-520">FWPM_CONDITION_INTERFACE_INDEX</span></span>
- <span data-ttu-id="a8478-521">FWPM_CONDITION_NDIS_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-521">FWPM_CONDITION_NDIS_PORT</span></span>
- <span data-ttu-id="a8478-522">FWPM_CONDITION_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-522">FWPM_CONDITION_L2_FLAGS</span></span>
## <a name="fwpm_layer_egress_vswitch_ethernet--fwpm_layer_ingress_vswitch_ethernet"></a><span data-ttu-id="a8478-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET/FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="a8478-523">FWPM_LAYER_EGRESS_VSWITCH_ETHERNET / FWPM_LAYER_INGRESS_VSWITCH_ETHERNET</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-524">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-524">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-525">FWPM_CONDITION_MAC_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="a8478-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-526">FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-527">FWPM_CONDITION_MAC_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="a8478-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-528">FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</span></span>
- <span data-ttu-id="a8478-529">FWPM_CONDITION_ETHER_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-529">FWPM_CONDITION_ETHER_TYPE</span></span>
- <span data-ttu-id="a8478-530">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-530">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="a8478-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-531">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="a8478-532">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-532">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="a8478-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-533">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="a8478-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-534">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="a8478-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-535">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-536">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="a8478-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-537">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>
##  <a name="fwpm_layer_egress_vswitch_transport_v4--fwpm_layer_ingress_vswitch_transport_v4--fwpm_layer_egressvswitch_transport_v6--fwpm_layer_ingress_vswitch_transport_v6"></a><span data-ttu-id="a8478-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4/FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6/FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span><span class="sxs-lookup"><span data-stu-id="a8478-538">FWPM_LAYER_EGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V4 / FWPM_LAYER_EGRESSVSWITCH_TRANSPORT_V6 / FWPM_LAYER_INGRESS_VSWITCH_TRANSPORT_V6</span></span>
###  <a name="windows-8--and-later"></a><span data-ttu-id="a8478-539">Windows 8 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="a8478-539">Windows 8  and later</span></span>
- <span data-ttu-id="a8478-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-540">FWPM_CONDITION_IP_SOURCE_ADDRESS</span></span>
- <span data-ttu-id="a8478-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span><span class="sxs-lookup"><span data-stu-id="a8478-541">FWPM_CONDITION_IP_DESTINATION_ADDRESS</span></span>
- <span data-ttu-id="a8478-542">FWPM_CONDITION_IP_PROTOCOL</span><span class="sxs-lookup"><span data-stu-id="a8478-542">FWPM_CONDITION_IP_PROTOCOL</span></span>
- <span data-ttu-id="a8478-543">FWPM_CONDITION_IP_SOURCE_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-543">FWPM_CONDITION_IP_SOURCE_PORT</span></span>
- <span data-ttu-id="a8478-544">FWPM_CONDITION_IP_DESTINATION_PORT</span><span class="sxs-lookup"><span data-stu-id="a8478-544">FWPM_CONDITION_IP_DESTINATION_PORT</span></span>
- <span data-ttu-id="a8478-545">FWPM_CONDITION_VLAN_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-545">FWPM_CONDITION_VLAN_ID</span></span>
- <span data-ttu-id="a8478-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-546">FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</span></span>
- <span data-ttu-id="a8478-547">FWPM_CONDITION_VSWITCH_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-547">FWPM_CONDITION_VSWITCH_ID</span></span>
- <span data-ttu-id="a8478-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-548">FWPM_CONDITION_VSWITCH_NETWORK_TYPE</span></span>
- <span data-ttu-id="a8478-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-549">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</span></span>
- <span data-ttu-id="a8478-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-550">FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-551">FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</span></span>
- <span data-ttu-id="a8478-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span><span class="sxs-lookup"><span data-stu-id="a8478-552">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</span></span>
- <span data-ttu-id="a8478-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span><span class="sxs-lookup"><span data-stu-id="a8478-553">FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</span></span>
- <span data-ttu-id="a8478-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span><span class="sxs-lookup"><span data-stu-id="a8478-554">FWPM_CONDITION_VSWITCH_L2_FLAGS</span></span>



## <a name="remarks"></a><span data-ttu-id="a8478-555">Notes</span><span class="sxs-lookup"><span data-stu-id="a8478-555">Remarks</span></span>

<span data-ttu-id="a8478-556">Les suffixes V4 et V6 à la fin des identificateurs de couche indiquent si la couche se trouve dans la pile réseau IPv4 ou dans la pile réseau IPv6.</span><span class="sxs-lookup"><span data-stu-id="a8478-556">The V4 and V6 suffixes at the end of the layer identifiers indicate whether the layer is located in the IPv4 network stack or in the IPv6 network stack.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8478-557">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a8478-557">Requirements</span></span>



| <span data-ttu-id="a8478-558">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a8478-558">Requirement</span></span> | <span data-ttu-id="a8478-559">Valeur</span><span class="sxs-lookup"><span data-stu-id="a8478-559">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a8478-560">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8478-560">Minimum supported client</span></span><br/> | <span data-ttu-id="a8478-561">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8478-561">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a8478-562">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a8478-562">Minimum supported server</span></span><br/> | <span data-ttu-id="a8478-563">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a8478-563">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a8478-564">En-tête</span><span class="sxs-lookup"><span data-stu-id="a8478-564">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8478-565"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="a8478-565"><dt>Fwpmu.h</dt></span></span> </dl> |



 

 





