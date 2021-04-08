---
title: Filtrage des identificateurs de condition (Fwpmu. h)
description: Les identificateurs de condition de filtrage de la plateforme de filtrage Windows (WFP) sont représentés par un GUID.
ms.assetid: 4f0b970a-e511-4107-8023-22a8775905b9
topic_type:
- apiref
api_name:
- FWPM_CONDITION_INTERFACE_MAC_ADDRESS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS
- FWPM_CONDITION_MAC_REMOTE_ADDRESS
- FWPM_CONDITION_ETHER_TYPE
- FWPM_CONDITION_VLAN_ID
- FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID
- FWPM_CONDITION_NDIS_PORT
- FWPM_CONDITION_NDIS_MEDIA_TYPE
- FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE
- FWPM_CONDITION_L2_FLAGS
- FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_SOURCE_ADDRESS
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS
- FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE
- FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_SOURCE_PORT
- FWPM_CONDITION_VSWITCH_ICMP_TYPE
- FWPM_CONDITION_IP_DESTINATION_PORT
- FWPM_CONDITION_VSWITCH_ICMP_CODE
- FWPM_CONDITION_VSWITCH_ID
- FWPM_CONDITION_VSWITCH_NETWORK_TYPE
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID
- FWPM_CONDITION_VSWITCH_SOURCE_VM_ID
- FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID
- FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE
- FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE
- FWPM_CONDITION_INTERFACE
- FWPM_CONDITION_ALE_PACKAGE_ID
- FWPM_CONDITION_ALE_ORIGINAL_APP_ID
- FWPM_CONDITION_IP_NEXTHOP_ADDRESS
- FWPM_CONDITION_IP_NEXTHOP_INTERFACE
- FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE
- FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE
- FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX
- FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ORIGINAL_PROFILE_ID
- FWPM_CONDITION_CURRENT_PROFILE_ID
- FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID
- FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID
- FWPM_CONDITION_REAUTHORIZE_REASON
- FWPM_CONDITION_ALE_REAUTH_REASON
- FWPM_CONDITION_ORIGINAL_ICMP_TYPE
- FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE
- FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE
- FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH
- FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY
- FWPM_CONDITION_IP_ARRIVAL_INTERFACE
- FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE
- FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE
- FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX
- FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_INDEX
- FWPM_CONDITION_LOCAL_INTERFACE_TYPE
- FWPM_CONDITION_LOCAL_TUNNEL_TYPE
- FWPM_CONDITION_IP_LOCAL_ADDRESS
- FWPM_CONDITION_IP_REMOTE_ADDRESS
- FWPM_CONDITION_IP_SOURCE_ADDRESS
- FWPM_CONDITION_IP_DESTINATION_ADDRESS
- FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE
- FWPM_CONDITION_IP_LOCAL_INTERFACE
- FWPM_CONDITION_INTERFACE_TYPE
- FWPM_CONDITION_TUNNEL_TYPE
- FWPM_CONDITION_IP_FORWARD_INTERFACE
- FWPM_CONDITION_IP_PROTOCOL
- FWPM_CONDITION_IP_LOCAL_PORT
- FWPM_CONDITION_ICMP_TYPE
- FWPM_CONDITION_IP_REMOTE_PORT
- FWPM_CONDITION_ICMP_CODE
- FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE
- FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS
- FWPM_CONDITION_EMBEDDED_PROTOCOL
- FWPM_CONDITION_EMBEDDED_LOCAL_PORT
- FWPM_CONDITION_EMBEDDED_REMOTE_PORT
- FWPM_CONDITION_FLAGS
- FWPM_CONDITION_DIRECTION
- FWPM_CONDITION_INTERFACE_INDEX
- FWPM_CONDITION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_INTERFACE_INDEX
- FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_INTERFACE_INDEX
- FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX
- FWPM_CONDITION_ALE_APP_ID
- FWPM_CONDITION_ALE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_USER_ID
- FWPM_CONDITION_ALE_REMOTE_MACHINE_ID
- FWPM_CONDITION_ALE_PROMISCUOUS_MODE
- FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT
- FWPM_CONDITION_ALE_NAP_CONTEXT
- FWPM_CONDITION_QM_MODE
- FWPM_CONDITION_KM_AUTH_NAP_CONTEXT
- FWPM_CONDITION_PEER_NAME
- FWPM_CONDITION_REMOTE_ID
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_KM_TYPE
- FWPM_CONDITION_KM_MODE
- FWPM_CONDITION_IPSEC_POLICY_KEY
- FWPM_CONDITION_AUTHENTICATION_TYPE
- FWPM_CONDITION_REMOTE_USER_TOKEN
- FWPM_CONDITION_RPC_IF_UUID
- FWPM_CONDITION_RPC_IF_VERSION
- FWPM_CONDITION_RPC_IF_FLAG
- FWPM_CONDITION_DCOM_APP_ID
- FWPM_CONDITION_IMAGE_NAME
- FWPM_CONDITION_RPC_PROTOCOL
- FWPM_CONDITION_RPC_AUTH_TYPE
- FWPM_CONDITION_RPC_AUTH_LEVEL
- FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM
- FWPM_CONDITION_SEC_KEY_SIZE
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V4
- FWPM_CONDITION_IP_LOCAL_ADDRESS_V6
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V4
- FWPM_CONDITION_IP_REMOTE_ADDRESS_V6
- FWPM_CONDITION_PIPE
- FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID
- FWPM_CONDITION_RPC_EP_VALUE
- FWPM_CONDITION_RPC_EP_FLAGS
- FWPM_CONDITION_CLIENT_TOKEN
- FWPM_CONDITION_RPC_SERVER_NAME
- FWPM_CONDITION_RPC_SERVER_PORT
- FWPM_CONDITION_RPC_PROXY_AUTH_TYPE
- FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH
- FWPM_CONDITION_CLIENT_CERT_OID
- FWPM_CONDITION_NET_EVENT_TYPE
api_location:
- Fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 617946e5708bb982f96edcad155bcbf2509596dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739845"
---
# <a name="filtering-condition-identifiers"></a><span data-ttu-id="14573-103">Filtrage des identificateurs de condition</span><span class="sxs-lookup"><span data-stu-id="14573-103">Filtering Condition Identifiers</span></span>

<span data-ttu-id="14573-104">Les identificateurs de condition de filtrage de la plateforme de filtrage Windows (WFP) sont représentés par un **GUID**.</span><span class="sxs-lookup"><span data-stu-id="14573-104">The Windows Filtering Platform (WFP) filtering condition identifiers are each represented by a **GUID**.</span></span> <span data-ttu-id="14573-105">Le type de données de la valeur de condition pour chaque condition de filtrage est spécifié sous la forme d’un [**\_ \_ type de données fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span><span class="sxs-lookup"><span data-stu-id="14573-105">The data type for the condition value for each filtering condition is specified as an [**FWP\_DATA\_TYPE**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type).</span></span> <span data-ttu-id="14573-106">Ces identificateurs et leurs types de données sont définis ici.</span><span class="sxs-lookup"><span data-stu-id="14573-106">These identifiers and their data types are defined here.</span></span>

<span data-ttu-id="14573-107">Les conditions standard sont répertoriées en premier, suivies des conditions spécifiques du mode utilisateur.</span><span class="sxs-lookup"><span data-stu-id="14573-107">The standard conditions are listed first, followed by the conditions specific to user mode.</span></span> <span data-ttu-id="14573-108">Les conditions sont regroupées par système d’exploitation pris en charge, afin que vous puissiez identifier facilement les conditions prises en charge pour un système d’exploitation donné.</span><span class="sxs-lookup"><span data-stu-id="14573-108">Conditions are grouped by supported operating system, so that you can easily tell which conditions are supported for a given OS.</span></span>

> [!Note]  
> <span data-ttu-id="14573-109">Chacune des conditions de filtrage suivantes est disponible uniquement dans un sous-ensemble des couches de filtrage WFP.</span><span class="sxs-lookup"><span data-stu-id="14573-109">Each of the following filtering conditions is available only at a subset of the WFP filtering layers.</span></span> <span data-ttu-id="14573-110">Pour plus d’informations sur la disponibilité de chaque condition dans une couche donnée, consultez [**conditions de filtrage disponibles à chaque couche de filtrage**](filtering-conditions-available-at-each-filtering-layer.md).</span><span class="sxs-lookup"><span data-stu-id="14573-110">For more information on each condition's availability at any given layer, see [**Filtering Conditions Available at Each Filtering Layer**](filtering-conditions-available-at-each-filtering-layer.md).</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="14573-111">Conditions disponibles pour Windows 8 et Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14573-111">Conditions available for Windows 8 and Windows Server 2012</span></span></th>
<th style="text-align: left;"><span data-ttu-id="14573-112">Description</span><span class="sxs-lookup"><span data-stu-id="14573-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl> <span data-ttu-id="14573-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-113"><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-114">Adresse MAC d’une interface locale particulière.</span><span class="sxs-lookup"><span data-stu-id="14573-114">The MAC address of a particular local interface.</span></span><br/> <span data-ttu-id="14573-115"><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-115"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl> <span data-ttu-id="14573-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-116"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-117">Adresse de destination d’un frame entrant, ou adresse source d’un frame sortant.</span><span class="sxs-lookup"><span data-stu-id="14573-117">Destination address of an inbound frame, or source address of an outbound frame.</span></span><br/> <span data-ttu-id="14573-118"><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-118"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl> <span data-ttu-id="14573-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-119"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-120">Adresse source d’un frame entrant ou adresse de destination d’un frame sortant.</span><span class="sxs-lookup"><span data-stu-id="14573-120">Source address of an inbound frame, or destination address of an outbound frame.</span></span><br/> <span data-ttu-id="14573-121"><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-121"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl> <span data-ttu-id="14573-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-122"><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-123">Type de données de la charge utile du réseau Ethernet v2.</span><span class="sxs-lookup"><span data-stu-id="14573-123">The Ethernet V2 network payload data type.</span></span> <span data-ttu-id="14573-124">(Voir ETHERNET_TYPE_IPV4, etc. dans netiodef. h.)</span><span class="sxs-lookup"><span data-stu-id="14573-124">(See ETHERNET_TYPE_IPV4, etc. in netiodef.h.)</span></span><br/> <span data-ttu-id="14573-125"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-125"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl> <span data-ttu-id="14573-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-126"><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-127">Les 16 bits d’en-tête VLAN, y compris les champs VID, CFI et Priority, conformément à la norme 802.1 q (voir VLAN_TAG dans netiodef. h pour les positions des champs de bits).</span><span class="sxs-lookup"><span data-stu-id="14573-127">The 16-bits of VLAN header including the VID, CFI, and Priority fields as per the 802.1q standard (see VLAN_TAG in netiodef.h for the positions of the bitfields).</span></span><br/> <span data-ttu-id="14573-128"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-128"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl> <span data-ttu-id="14573-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-129"><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-130">Identificateur unique du réseau vSwitch.</span><span class="sxs-lookup"><span data-stu-id="14573-130">Unique identifier for the vSwitch network.</span></span> <span data-ttu-id="14573-131">Ne peut pas être utilisé conjointement avec VLAN_IDs.</span><span class="sxs-lookup"><span data-stu-id="14573-131">Cannot be used in conjunction with VLAN_IDs.</span></span><br/> <span data-ttu-id="14573-132"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-132"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl> <span data-ttu-id="14573-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-133"><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-134">Numéro de port du port NDIS.</span><span class="sxs-lookup"><span data-stu-id="14573-134">The port number of the NDIS port.</span></span><br/> <span data-ttu-id="14573-135"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-135"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl> <span data-ttu-id="14573-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-136"><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-137">Type de média du port NDIS.</span><span class="sxs-lookup"><span data-stu-id="14573-137">The media type of the NDIS port.</span></span><br/> <span data-ttu-id="14573-138"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-138"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="14573-139"><strong>Valeurs possibles :</strong> L’une des <strong>NDIS_MEDIUM</strong> valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="14573-139"><strong>Possible values:</strong> Any of the <strong>NDIS_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="14573-140">(Voir ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="14573-140">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl> <span data-ttu-id="14573-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-141"><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-142">Type de média physique du port NDIS.</span><span class="sxs-lookup"><span data-stu-id="14573-142">The physical media type of the NDIS port.</span></span><br/> <span data-ttu-id="14573-143"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-143"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="14573-144"><strong>Valeurs possibles :</strong> L’une des <strong>NDIS_PHYSICAL_MEDIUM</strong> valeurs d’énumération.</span><span class="sxs-lookup"><span data-stu-id="14573-144"><strong>Possible values:</strong> Any of the <strong>NDIS_PHYSICAL_MEDIUM</strong> enumeration values.</span></span> <span data-ttu-id="14573-145">(Voir ntddndis. h.)</span><span class="sxs-lookup"><span data-stu-id="14573-145">(See ntddndis.h.)</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl> <span data-ttu-id="14573-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-146"><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-147">Or au niveau du bit d’une combinaison d’indicateurs de condition de filtrage.</span><span class="sxs-lookup"><span data-stu-id="14573-147">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="14573-148"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-148"><strong>Data type:</strong> FWP_UINT32</span></span><br/> <span data-ttu-id="14573-149"><strong>Valeurs possibles :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-149"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span><span class="sxs-lookup"><span data-stu-id="14573-150">FWP_CONDITION_L2_IS_MOBILE_BROADBAND</span></span></li>
<li><span data-ttu-id="14573-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span><span class="sxs-lookup"><span data-stu-id="14573-151">FWP_CONDITION_L2_IS_NATIVE_ETHERNET</span></span></li>
<li><span data-ttu-id="14573-152">FWP_CONDITION_L2_IS_WIFI</span><span class="sxs-lookup"><span data-stu-id="14573-152">FWP_CONDITION_L2_IS_WIFI</span></span></li>
<li><span data-ttu-id="14573-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span><span class="sxs-lookup"><span data-stu-id="14573-153">FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl> <span data-ttu-id="14573-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-154"><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-155">Type d’adresse de l’adresse locale physique.</span><span class="sxs-lookup"><span data-stu-id="14573-155">The address type of the physical local address.</span></span><br/> <span data-ttu-id="14573-156"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-156"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="14573-157"><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.</span><span class="sxs-lookup"><span data-stu-id="14573-157"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="14573-158">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="14573-158">DlUnicast</span></span></li>
<li><span data-ttu-id="14573-159">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="14573-159">DlMulticast</span></span></li>
<li><span data-ttu-id="14573-160">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="14573-160">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl> <span data-ttu-id="14573-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-161"><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-162">Type d’adresse de l’adresse distante physique.</span><span class="sxs-lookup"><span data-stu-id="14573-162">The address type of the physical remote address.</span></span><br/> <span data-ttu-id="14573-163"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-163"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="14573-164"><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.</span><span class="sxs-lookup"><span data-stu-id="14573-164"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="14573-165">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="14573-165">DlUnicast</span></span></li>
<li><span data-ttu-id="14573-166">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="14573-166">DlMulticast</span></span></li>
<li><span data-ttu-id="14573-167">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="14573-167">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl> <span data-ttu-id="14573-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-168"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-169">Adresse source physique d’un frame.</span><span class="sxs-lookup"><span data-stu-id="14573-169">The physical source address of a frame.</span></span><br/> <span data-ttu-id="14573-170"><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-170"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl> <span data-ttu-id="14573-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-171"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-172">Adresse physique de destination d’une trame.</span><span class="sxs-lookup"><span data-stu-id="14573-172">The physical destination address of a frame.</span></span><br/> <span data-ttu-id="14573-173"><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-173"><strong>Data type:</strong> FWP_BYTE_ARRAY6_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl> <span data-ttu-id="14573-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-174"><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-175">Type d’adresse de l’adresse de destination physique.</span><span class="sxs-lookup"><span data-stu-id="14573-175">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="14573-176"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-176"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="14573-177"><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.</span><span class="sxs-lookup"><span data-stu-id="14573-177"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="14573-178">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="14573-178">DlUnicast</span></span></li>
<li><span data-ttu-id="14573-179">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="14573-179">DlMulticast</span></span></li>
<li><span data-ttu-id="14573-180">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="14573-180">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl> <span data-ttu-id="14573-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-181"><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-182">Type d’adresse de l’adresse de destination physique.</span><span class="sxs-lookup"><span data-stu-id="14573-182">The address type of the physical destination address.</span></span><br/> <span data-ttu-id="14573-183"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-183"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="14573-184"><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.</span><span class="sxs-lookup"><span data-stu-id="14573-184"><strong>Possible values:</strong> Any of the following <strong>DL_ADDRESS_TYPE</strong> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="14573-185">DlUnicast</span><span class="sxs-lookup"><span data-stu-id="14573-185">DlUnicast</span></span></li>
<li><span data-ttu-id="14573-186">DlMulticast</span><span class="sxs-lookup"><span data-stu-id="14573-186">DlMulticast</span></span></li>
<li><span data-ttu-id="14573-187">DlBroadcast</span><span class="sxs-lookup"><span data-stu-id="14573-187">DlBroadcast</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl> <span data-ttu-id="14573-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-188"><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-189">Port source du transport du paquet.</span><span class="sxs-lookup"><span data-stu-id="14573-189">The source port of the packet's transport.</span></span><br/> <span data-ttu-id="14573-190"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-190"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl> <span data-ttu-id="14573-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-191"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-192">Champ de type ICMP, tel que spécifié dans le document RFC 792.</span><span class="sxs-lookup"><span data-stu-id="14573-192">The ICMP type field, as specified in RFC 792.</span></span><br/> <span data-ttu-id="14573-193"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-193"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl> <span data-ttu-id="14573-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-194"><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-195">Port de destination du transport du paquet.</span><span class="sxs-lookup"><span data-stu-id="14573-195">The destination port of the packet's transport.</span></span><br/> <span data-ttu-id="14573-196"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-196"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl> <span data-ttu-id="14573-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-197"><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-198">Champ de code ICMP, tel que spécifié dans le document RFC 792.</span><span class="sxs-lookup"><span data-stu-id="14573-198">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="14573-199"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-199"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl> <span data-ttu-id="14573-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-200"><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-201">Identificateur unique d’une instance de vSwitch.</span><span class="sxs-lookup"><span data-stu-id="14573-201">Unique identifier of an vSwitch instance.</span></span><br/> <span data-ttu-id="14573-202"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-202"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl> <span data-ttu-id="14573-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-203"><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-204">Spécifie si l’instance vSwitch fait partie d’un réseau virtuel externe, interne ou privé.</span><span class="sxs-lookup"><span data-stu-id="14573-204">Specifies whether the vSwitch instance is part of an external, internal, or private virtual network.</span></span><br/> <span data-ttu-id="14573-205"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-205"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl> <span data-ttu-id="14573-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-206"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-207">Identificateur unique de la source du paquet en cours.</span><span class="sxs-lookup"><span data-stu-id="14573-207">Unique identifier of the source of the current packet.</span></span> <span data-ttu-id="14573-208">(Nom d’une machine virtuelle-NIC, P-NIC ou V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="14573-208">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="14573-209"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-209"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl> <span data-ttu-id="14573-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-210"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-211">Identificateur unique de la destination du paquet actuel.</span><span class="sxs-lookup"><span data-stu-id="14573-211">Unique identifier of the destination of the current packet.</span></span> <span data-ttu-id="14573-212">(Nom d’une machine virtuelle-NIC, P-NIC ou V-NIC.)</span><span class="sxs-lookup"><span data-stu-id="14573-212">(The name of a VM-NIC, P-NIC, or V-NIC.)</span></span><br/> <span data-ttu-id="14573-213"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-213"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl> <span data-ttu-id="14573-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-214"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-215">Identificateur unique de la machine virtuelle source vSwitch.</span><span class="sxs-lookup"><span data-stu-id="14573-215">Unique identifier of the vSwitch source virtual machine.</span></span><br/> <span data-ttu-id="14573-216"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-216"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl> <span data-ttu-id="14573-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-217"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-218">Identificateur unique de la machine virtuelle de destination vSwitch.</span><span class="sxs-lookup"><span data-stu-id="14573-218">Unique identifier of the vSwitch destination virtual machine.</span></span><br/> <span data-ttu-id="14573-219"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-219"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl> <span data-ttu-id="14573-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-220"><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-221">Type d’interface de la source du paquet en cours.</span><span class="sxs-lookup"><span data-stu-id="14573-221">Interface type of the source of the current packet.</span></span><br/> <span data-ttu-id="14573-222"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-222"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="14573-223"><strong>Valeurs possibles :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-223"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-224">SwitchNicSyntheticNic (lorsque le type d’interface est VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="14573-224">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="14573-225">SwitchNicEmulatedNic (lorsque le type d’interface est VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="14573-225">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="14573-226">SwitchNicPhysicalNic (lorsque le type d’interface est P-NIC)</span><span class="sxs-lookup"><span data-stu-id="14573-226">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="14573-227">SwitchNicVNic (lorsque le type d’interface est V-NIC, connecté à la partition hôte)</span><span class="sxs-lookup"><span data-stu-id="14573-227">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl> <span data-ttu-id="14573-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-228"><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-229">Type d’interface de la destination du paquet actuel.</span><span class="sxs-lookup"><span data-stu-id="14573-229">Interface type of the destination of the current packet.</span></span><br/> <span data-ttu-id="14573-230"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-230"><strong>Data type:</strong> FWP_UINT8</span></span><br/> <span data-ttu-id="14573-231"><strong>Valeurs possibles :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-231"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-232">SwitchNicSyntheticNic (lorsque le type d’interface est VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="14573-232">SwitchNicSyntheticNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="14573-233">SwitchNicEmulatedNic (lorsque le type d’interface est VM-NIC)</span><span class="sxs-lookup"><span data-stu-id="14573-233">SwitchNicEmulatedNic (when interface type is VM-NIC)</span></span></li>
<li><span data-ttu-id="14573-234">SwitchNicPhysicalNic (lorsque le type d’interface est P-NIC)</span><span class="sxs-lookup"><span data-stu-id="14573-234">SwitchNicPhysicalNic (when interface type is P-NIC)</span></span></li>
<li><span data-ttu-id="14573-235">SwitchNicVNic (lorsque le type d’interface est V-NIC, connecté à la partition hôte)</span><span class="sxs-lookup"><span data-stu-id="14573-235">SwitchNicVNic (when interface type is V-NIC, connected to the host partition)</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl> <span data-ttu-id="14573-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-236"><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-237">LUID de l’interface réseau associée à l’adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="14573-237">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="14573-238"><strong>Type de données :</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-238"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl> <span data-ttu-id="14573-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-239"><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-240">Identificateur de sécurité (SID) d’un conteneur d’application.</span><span class="sxs-lookup"><span data-stu-id="14573-240">The security identifier (SID) of an app container.</span></span><br/> <span data-ttu-id="14573-241"><strong>Type de données :</strong> FWP_SID</span><span class="sxs-lookup"><span data-stu-id="14573-241"><strong>Data type:</strong> FWP_SID</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl> <span data-ttu-id="14573-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-242"><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-243">Le chemin d’accès complet de l’appareil de l’application, par exemple &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .</span><span class="sxs-lookup"><span data-stu-id="14573-243">The fully qualified device path of the application, such as &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.</span></span> <span data-ttu-id="14573-244">Lorsqu’une connexion a été redirigée, il s’agit de l’identificateur de l’application d’origine. dans le cas contraire, ce sera le même que <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span><span class="sxs-lookup"><span data-stu-id="14573-244">When a connection has been redirected, this will be the identifier of the originating app; otherwise this will be the same as <strong>FWPM_CONDITION_ALE_APP_ID</strong>.</span></span><br/> <span data-ttu-id="14573-245"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-245"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
</tbody>
</table>





| <span data-ttu-id="14573-246">Conditions disponibles pour Windows 7, Windows Server 2008 R2 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="14573-246">Conditions available for Windows 7, Windows Server 2008 R2, and later</span></span>                                                                                                                                                                                                    | <span data-ttu-id="14573-247">Description</span><span class="sxs-lookup"><span data-stu-id="14573-247">Description</span></span>                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <span data-ttu-id="14573-248"><dt>**\_ \_ \_ adresse IP NEXTHOP \_ de la condition FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-248"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_ADDRESS**</dt></span></span> </dl>                                             | <span data-ttu-id="14573-249">Adresse IP de l’interface de saut suivant.</span><span class="sxs-lookup"><span data-stu-id="14573-249">The IP address of the next-hop interface.</span></span><br/> <span data-ttu-id="14573-250">**Type de données :** \_Masque d' \_ ADR v4 v4 \_</span><span class="sxs-lookup"><span data-stu-id="14573-250">**Data type:** FWP\_V4\_ADDR\_MASK</span></span><br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <span data-ttu-id="14573-251"><dt>**\_interface d' \_ IP \_ NEXTHOP \_ d’une condition FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-251"><dt>**FWPM\_CONDITION\_IP\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>                                       | <span data-ttu-id="14573-252">Interface de saut suivant à partir de laquelle le paquet sera en cours de déconditionnement.</span><span class="sxs-lookup"><span data-stu-id="14573-252">The next-hop interface from which the packet will be departing.</span></span> <br/> <span data-ttu-id="14573-253">**Type de données :** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-253">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <span data-ttu-id="14573-254"><dt>**\_condition FWPM \_ \_ type d’interface NEXTHOP \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-254"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_TYPE**</dt></span></span> </dl>                                 | <span data-ttu-id="14573-255">Type d’interface de l’interface de saut suivant.</span><span class="sxs-lookup"><span data-stu-id="14573-255">The interface type of the next-hop interface.</span></span><br/> <span data-ttu-id="14573-256">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-256">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <span data-ttu-id="14573-257"><dt>**\_type de \_ tunnel de tronçons de la condition FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-257"><dt>**FWPM\_CONDITION\_NEXTHOP\_TUNNEL\_TYPE**</dt></span></span> </dl>                                          | <span data-ttu-id="14573-258">Type de tunnel de l’interface de saut suivant.</span><span class="sxs-lookup"><span data-stu-id="14573-258">The tunnel type of the next-hop interface.</span></span><br/> <span data-ttu-id="14573-259">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-259">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <span data-ttu-id="14573-260"><dt>**FWPM \_ état \_ d' \_ interface NEXTHOP de la condition \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-260"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_INDEX**</dt></span></span> </dl>                              | <span data-ttu-id="14573-261">Index d’interface de l’interface de saut suivant.</span><span class="sxs-lookup"><span data-stu-id="14573-261">The interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="14573-262">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-262">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <span data-ttu-id="14573-263"><dt>**FWPM \_ condition de la \_ sous- \_ \_ interface de tronçons \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-263"><dt>**FWPM\_CONDITION\_NEXTHOP\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl>                 | <span data-ttu-id="14573-264">Index de sous-interface de l’interface de saut suivant.</span><span class="sxs-lookup"><span data-stu-id="14573-264">The sub-interface index of the next-hop interface.</span></span><br/> <span data-ttu-id="14573-265">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-265">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <span data-ttu-id="14573-266"><dt>**\_ID de \_ profil d’origine de la condition FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-266"><dt>**FWPM\_CONDITION\_ORIGINAL\_PROFILE\_ID**</dt></span></span> </dl>                                          | <span data-ttu-id="14573-267">Catégorie réseau de l’interface d’arrivée ou de saut suivant par le biais de laquelle le Flow ALE (entrant ou sortant) est créé.</span><span class="sxs-lookup"><span data-stu-id="14573-267">The network category of the arrival or next-hop interface through which the ALE flow (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="14573-268">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-268">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <span data-ttu-id="14573-269"><dt>**\_ID de \_ \_ profil actuel de condition \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-269"><dt>**FWPM\_CONDITION\_CURRENT\_PROFILE\_ID**</dt></span></span> </dl>                                             | <span data-ttu-id="14573-270">Catégorie réseau de l’interface d’arrivée ou de saut suivant par le biais de laquelle le paquet en cours (entrant ou sortant) est créé.</span><span class="sxs-lookup"><span data-stu-id="14573-270">The network category of the arrival or next-hop interface through which the current packet (inbound or outbound) is created.</span></span> <br/> <span data-ttu-id="14573-271">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-271">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <span data-ttu-id="14573-272"><dt>**ID de profil de l' \_ \_ interface locale de condition FWPM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-272"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>                    | <span data-ttu-id="14573-273">Catégorie de réseau de l’interface de remise.</span><span class="sxs-lookup"><span data-stu-id="14573-273">The network category of the delivery interface.</span></span><br/> <span data-ttu-id="14573-274">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-274">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <span data-ttu-id="14573-275"><dt>**ID de profil de l’interface d’arrivée de la \_ condition FWPM \_ \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-275"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="14573-276">Catégorie réseau de l’interface d’arrivée.</span><span class="sxs-lookup"><span data-stu-id="14573-276">The network category of the arrival interface.</span></span><br/> <span data-ttu-id="14573-277">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-277">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <span data-ttu-id="14573-278"><dt>**ID de profil de l' \_ \_ \_ interface NEXTHOP \_ \_ de la condition FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-278"><dt>**FWPM\_CONDITION\_NEXTHOP\_INTERFACE\_PROFILE\_ID**</dt></span></span> </dl>              | <span data-ttu-id="14573-279">Catégorie réseau de l’interface de saut suivant.</span><span class="sxs-lookup"><span data-stu-id="14573-279">The network category of the next-hop interface.</span></span><br/> <span data-ttu-id="14573-280">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-280">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <span data-ttu-id="14573-281"><dt>**raison de l’autorisation de la \_ condition FWPM \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-281"><dt>**FWPM\_CONDITION\_REAUTHORIZE\_REASON**</dt></span></span> </dl>                                              | <span data-ttu-id="14573-282">Raison de la réautorisation d’une connexion précédemment autorisée.</span><span class="sxs-lookup"><span data-stu-id="14573-282">The reason for reauthorizing a previously authorized connection.</span></span><br/> <span data-ttu-id="14573-283">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-283">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <span data-ttu-id="14573-284"><dt>**\_raison de \_ la \_ réauthentification ALE de condition FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-284"><dt>**FWPM\_CONDITION\_ALE\_REAUTH\_REASON**</dt></span></span> </dl>                                                | <span data-ttu-id="14573-285">La raison pour laquelle vous autorisez une connexion précédemment autorisée, telle que la **condition fwp, \_ \_ réautorisez la \_ \_ \_ modification** de la stratégie de motif (ou l’une des autres valeurs indiquées dans [**indicateurs de condition de filtrage**](filtering-condition-flags-.md)).</span><span class="sxs-lookup"><span data-stu-id="14573-285">The reason for reauthorizing a previously authorized connection, such as **FWP\_CONDITION\_REAUTHORIZE\_REASON\_POLICY\_CHANGE** (or one of the other values listed in [**Filtering Condition Flags**](filtering-condition-flags-.md)).</span></span><br/> <span data-ttu-id="14573-286">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-286">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <span data-ttu-id="14573-287"><dt>**\_ \_ \_ type ICMP d’origine \_ de la condition FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-287"><dt>**FWPM\_CONDITION\_ORIGINAL\_ICMP\_TYPE**</dt></span></span> </dl>                                             | <span data-ttu-id="14573-288">Type ICMP avec lequel le Flow a été créé.</span><span class="sxs-lookup"><span data-stu-id="14573-288">The ICMP type with which the flow was created.</span></span><br/> <span data-ttu-id="14573-289">**Type de données :** FWP \_ UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-289">**Data type:** FWP\_UINT16</span></span><br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <span data-ttu-id="14573-290"><dt>**\_interface d' \_ \_ arrivée physique \_ IP \_ de condition FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-290"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="14573-291">LUID de l’interface physique associée à l’adresse IP d’arrivée.</span><span class="sxs-lookup"><span data-stu-id="14573-291">The LUID of the physical interface associated with the arrival IP address.</span></span><br/> <span data-ttu-id="14573-292">**Type de données :** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-292">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <span data-ttu-id="14573-293"><dt>**\_ \_ \_ \_ interface physique NEXTHOP IP \_ de la condition FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-293"><dt>**FWPM\_CONDITION\_IP\_PHYSICAL\_NEXTHOP\_INTERFACE**</dt></span></span> </dl>           | <span data-ttu-id="14573-294">LUID de l’interface physique du tronçon suivant.</span><span class="sxs-lookup"><span data-stu-id="14573-294">The LUID of the physical interface of the next hop.</span></span><br/> <span data-ttu-id="14573-295">**Type de données :** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-295">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <span data-ttu-id="14573-296"><dt>**époque de quarantaine de l' \_ interface de condition FWPM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-296"><dt>**FWPM\_CONDITION\_INTERFACE\_QUARANTINE\_EPOCH**</dt></span></span> </dl>                     | <span data-ttu-id="14573-297">Nombre de époques associé à une interface.</span><span class="sxs-lookup"><span data-stu-id="14573-297">The epoch count associated with an interface.</span></span> <span data-ttu-id="14573-298">Réservé.</span><span class="sxs-lookup"><span data-stu-id="14573-298">Reserved.</span></span><br/> <span data-ttu-id="14573-299">**Type de données :** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-299">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <span data-ttu-id="14573-300"><dt>**\_propriété de \_ \_ Socket de \_ pare-feu SIO \_ de condition FWPM ALE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-300"><dt>**FWPM\_CONDITION\_ALE\_SIO\_FIREWALL\_SOCKET\_PROPERTY**</dt></span></span> </dl> | <span data-ttu-id="14573-301">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="14573-301">Reserved for internal use.</span></span> <br/> <span data-ttu-id="14573-302">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-302">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                              |





| <span data-ttu-id="14573-303">Constantes disponibles pour Windows Vista avec SP1, Windows Server 2008 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="14573-303">Constants available for Windows Vista with SP1, Windows Server 2008, and later</span></span>                                                                                                                                                                           | <span data-ttu-id="14573-304">Description</span><span class="sxs-lookup"><span data-stu-id="14573-304">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <span data-ttu-id="14573-305"><dt>**\_interface d' \_ \_ arrivée IP de condition \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-305"><dt>**FWPM\_CONDITION\_IP\_ARRIVAL\_INTERFACE**</dt></span></span> </dl>                       | <span data-ttu-id="14573-306">LUID de l’interface réseau associée à l’adresse IP d’arrivée.</span><span class="sxs-lookup"><span data-stu-id="14573-306">The LUID for the network interface associated with the arrival IP address.</span></span> <br/> <span data-ttu-id="14573-307">**Type de données :** FWP \_ UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-307">**Data type:** FWP\_UINT64</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <span data-ttu-id="14573-308"><dt>**\_type d' \_ interface d’arrivée \_ \_ de la condition FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-308"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                 | <span data-ttu-id="14573-309">Type de l’interface réseau d’arrivée telle que définie par l’IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="14573-309">The type of the arrival network interface as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="14573-310">Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="14573-310">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="14573-311">**Valeurs possibles :** Valeurs de type d’interface listées dans le fichier d’en-tête Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="14573-311">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="14573-312">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-312">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <span data-ttu-id="14573-313"><dt>**FWPM \_ \_type de \_ tunnel \_ d’arrivée des conditions**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-313"><dt> **FWPM\_CONDITION\_ARRIVAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="14573-314">Méthode d’encapsulation utilisée par un tunnel associé à l’interface réseau d’arrivée si le membre de type est un \_ tunnel de type \_ .</span><span class="sxs-lookup"><span data-stu-id="14573-314">The encapsulation method used by a tunnel associated with the arrival network interface if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="14573-315">Le type de tunnel est défini par l’IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="14573-315">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="14573-316">Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="14573-316">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="14573-317">**Valeurs possibles :** \_Valeurs de type d’énumération de type de tunnel listées dans le fichier d’en-tête ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="14573-317">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="14573-318">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-318">**Data type:** FWP\_UINT32</span></span><br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <span data-ttu-id="14573-319"><dt>**INDEX de l’interface d’arrivée de la \_ condition FWPM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-319"><dt>**FWPM\_CONDITION\_ARRIVAL\_INTERFACE\_INDEX**</dt></span></span> </dl>              | <span data-ttu-id="14573-320">Index de l’interface réseau d’arrivée, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-320">The index of the arrival network interface, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="14573-321">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-321">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <span data-ttu-id="14573-322"><dt>**\_index d' \_ interface de sous-interface d’arrivée de condition FWPM \_ \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-322"><dt>**FWPM\_CONDITION\_ARRIVAL\_SUB\_INTERFACE\_INDEX**</dt></span></span> </dl> | <span data-ttu-id="14573-323">Index de l’interface réseau d’arrivée, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-323">The index of the arrival network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="14573-324">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-324">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <span data-ttu-id="14573-325"><dt>**\_index d' \_ \_ interface locale de condition \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-325"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_INDEX**</dt></span></span> </dl>                    | <span data-ttu-id="14573-326">Index de l’interface réseau, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-326">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="14573-327">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-327">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <span data-ttu-id="14573-328"><dt>**\_type d' \_ \_ interface locale de condition \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-328"><dt>**FWPM\_CONDITION\_LOCAL\_INTERFACE\_TYPE**</dt></span></span> </dl>                       | <span data-ttu-id="14573-329">Type d’interface défini par l’IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="14573-329">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="14573-330">Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="14573-330">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="14573-331">**Valeurs possibles :** Valeurs de type d’interface listées dans le fichier d’en-tête Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="14573-331">**Possible values:** The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="14573-332">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-332">**Data type:** FWP\_UINT32</span></span><br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <span data-ttu-id="14573-333"><dt>**\_type de \_ \_ tunnel local de condition \_ FWPM**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-333"><dt>**FWPM\_CONDITION\_LOCAL\_TUNNEL\_TYPE**</dt></span></span> </dl>                                | <span data-ttu-id="14573-334">Méthode d’encapsulation utilisée par un tunnel si le type du membre est \_ un \_ tunnel de type.</span><span class="sxs-lookup"><span data-stu-id="14573-334">The encapsulation method used by a tunnel if the Type member is IF\_TYPE\_TUNNEL.</span></span> <span data-ttu-id="14573-335">Le type de tunnel est défini par l’IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="14573-335">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="14573-336">Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="14573-336">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="14573-337">**Valeurs possibles :** \_Valeurs de type d’énumération de type de tunnel listées dans le fichier d’en-tête ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="14573-337">**Possible values:** The TUNNEL\_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="14573-338">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-338">**Data type:** FWP\_UINT32</span></span> <br/>                                              |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="14573-339">Constantes disponibles pour Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="14573-339">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="14573-340">Description</span><span class="sxs-lookup"><span data-stu-id="14573-340">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl> <span data-ttu-id="14573-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-341"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-342">Adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="14573-342">The local IP address.</span></span> <br/> <span data-ttu-id="14573-343"><strong>Type de données :</strong> Pour une adresse IPv4</span><span class="sxs-lookup"><span data-stu-id="14573-343"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="14573-344">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-344">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-345">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-345">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-346"><strong>Type de données :</strong> Pour une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="14573-346"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="14573-347">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-347">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-348">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-348">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl> <span data-ttu-id="14573-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-349"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-350">Adresse IP distante.</span><span class="sxs-lookup"><span data-stu-id="14573-350">The remote IP address.</span></span> <br/> <span data-ttu-id="14573-351"><strong>Type de données :</strong> Pour une adresse IPv4</span><span class="sxs-lookup"><span data-stu-id="14573-351"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="14573-352">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-352">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-353">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-353">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-354"><strong>Type de données :</strong> Pour une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="14573-354"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="14573-355">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-355">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-356">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-356">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl> <span data-ttu-id="14573-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-357"><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-358">Adresse IP source pour les paquets transférés.</span><span class="sxs-lookup"><span data-stu-id="14573-358">The source IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="14573-359"><strong>Type de données :</strong> Pour une adresse IPv4</span><span class="sxs-lookup"><span data-stu-id="14573-359"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="14573-360">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-360">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-361">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-361">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-362"><strong>Type de données :</strong> Pour une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="14573-362"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="14573-363">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-363">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-364">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-364">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl> <span data-ttu-id="14573-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-365"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-366">Adresse IP de destination pour les paquets transférés.</span><span class="sxs-lookup"><span data-stu-id="14573-366">The destination IP address for forwarded packets.</span></span> <br/> <span data-ttu-id="14573-367"><strong>Type de données :</strong> Pour une adresse IPv4</span><span class="sxs-lookup"><span data-stu-id="14573-367"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="14573-368">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-368">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-369">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-369">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-370"><strong>Type de données :</strong> Pour une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="14573-370"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="14573-371">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-371">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-372">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-372">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl> <span data-ttu-id="14573-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-373"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-374">Type d’adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="14573-374">The local IP address type.</span></span> <br/> <span data-ttu-id="14573-375"><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> suivantes.</span><span class="sxs-lookup"><span data-stu-id="14573-375"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="14573-376">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="14573-376">NlatUnspecified</span></span></li>
<li><span data-ttu-id="14573-377">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="14573-377">NlatUnicast</span></span></li>
<li><span data-ttu-id="14573-378">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="14573-378">NlatAnycast</span></span></li>
<li><span data-ttu-id="14573-379">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="14573-379">NlatMulticast</span></span></li>
<li><span data-ttu-id="14573-380">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="14573-380">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-381"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-381"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl> <span data-ttu-id="14573-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-382"><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-383">Type d’adresse IP de destination pour les paquets transférés.</span><span class="sxs-lookup"><span data-stu-id="14573-383">The destination IP address type for forwarded packets.</span></span> <br/> <span data-ttu-id="14573-384"><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> suivantes.</span><span class="sxs-lookup"><span data-stu-id="14573-384"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="14573-385">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="14573-385">NlatUnspecified</span></span></li>
<li><span data-ttu-id="14573-386">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="14573-386">NlatUnicast</span></span></li>
<li><span data-ttu-id="14573-387">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="14573-387">NlatAnycast</span></span></li>
<li><span data-ttu-id="14573-388">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="14573-388">NlatMulticast</span></span></li>
<li><span data-ttu-id="14573-389">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="14573-389">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-390"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-390"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl> <span data-ttu-id="14573-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-391"><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-392">LUID de l’interface réseau associée à l’adresse IP locale.</span><span class="sxs-lookup"><span data-stu-id="14573-392">The LUID for the network interface associated with the local IP address.</span></span> <br/> <span data-ttu-id="14573-393"><strong>Type de données :</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-393"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl> <span data-ttu-id="14573-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-394"><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-395">Type d’interface défini par l’IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="14573-395">The interface type as defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="14573-396">Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span><span class="sxs-lookup"><span data-stu-id="14573-396">For more information, see [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib).</span></span> <br/> <span data-ttu-id="14573-397"><strong>Valeurs possibles :</strong> Valeurs de type d’interface listées dans le fichier d’en-tête Ipifcons. h.</span><span class="sxs-lookup"><span data-stu-id="14573-397"><strong>Possible values:</strong> The interface type values listed in the Ipifcons.h header file.</span></span><br/> <span data-ttu-id="14573-398"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-398"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl> <span data-ttu-id="14573-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-399"><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-400">Méthode d’encapsulation utilisée par un tunnel si le membre de type est IF_TYPE_TUNNEL.</span><span class="sxs-lookup"><span data-stu-id="14573-400">The encapsulation method used by a tunnel if the Type member is IF_TYPE_TUNNEL.</span></span> <span data-ttu-id="14573-401">Le type de tunnel est défini par l’IANA (Internet Assigned Names Authority).</span><span class="sxs-lookup"><span data-stu-id="14573-401">The tunnel type is defined by the Internet Assigned Names Authority (IANA).</span></span> <span data-ttu-id="14573-402">Pour plus d’informations, consultez <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span><span class="sxs-lookup"><span data-stu-id="14573-402">For more information, see <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>.</span></span> <br/> <span data-ttu-id="14573-403"><strong>Valeurs possibles :</strong> TUNNEL_TYPE valeurs de type énumération figurant dans le fichier d’en-tête ifdef. h.</span><span class="sxs-lookup"><span data-stu-id="14573-403"><strong>Possible values:</strong> The TUNNEL_TYPE enumeration type values listed in the Ifdef.h header file.</span></span><br/> <span data-ttu-id="14573-404"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-404"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl> <span data-ttu-id="14573-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-405"><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-406">LUID de l’interface réseau sur laquelle le paquet transféré doit être envoyé.</span><span class="sxs-lookup"><span data-stu-id="14573-406">The LUID for the network interface on which the packet being forwarded is to be sent out.</span></span> <br/> <span data-ttu-id="14573-407"><strong>Type de données :</strong> FWP_UINT64</span><span class="sxs-lookup"><span data-stu-id="14573-407"><strong>Data type:</strong> FWP_UINT64</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl> <span data-ttu-id="14573-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-408"><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-409">Numéro de protocole IP, tel que spécifié dans le document RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="14573-409">The IP protocol number, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="14573-410"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-410"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl> <span data-ttu-id="14573-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-411"><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-412">Numéro de port du protocole de transport local.</span><span class="sxs-lookup"><span data-stu-id="14573-412">The local transport protocol port number.</span></span><br/> <span data-ttu-id="14573-413"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-413"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl> <span data-ttu-id="14573-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-414"><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-415">Champ de type ICMP, tel que spécifié dans le document RFC 792.</span><span class="sxs-lookup"><span data-stu-id="14573-415">The ICMP type field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="14573-416"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-416"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl> <span data-ttu-id="14573-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-417"><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-418">Numéro de port du protocole de transport distant.</span><span class="sxs-lookup"><span data-stu-id="14573-418">The remote transport protocol port number.</span></span> <br/> <span data-ttu-id="14573-419"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-419"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl> <span data-ttu-id="14573-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-420"><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-421">Champ de code ICMP, tel que spécifié dans le document RFC 792.</span><span class="sxs-lookup"><span data-stu-id="14573-421">The ICMP code field, as specified in RFC 792.</span></span> <br/> <span data-ttu-id="14573-422"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-422"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl> <span data-ttu-id="14573-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-423"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-424">Le type d’adresse IP locale qui est incorporé dans le paquet ICMP.</span><span class="sxs-lookup"><span data-stu-id="14573-424">The local IP address type that is embedded in the ICMP packet.</span></span><br/> <span data-ttu-id="14573-425"><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> suivantes.</span><span class="sxs-lookup"><span data-stu-id="14573-425"><strong>Possible values:</strong> Any of the following <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> enumeration values.</span></span>
<ul>
<li><span data-ttu-id="14573-426">NlatUnspecified</span><span class="sxs-lookup"><span data-stu-id="14573-426">NlatUnspecified</span></span></li>
<li><span data-ttu-id="14573-427">NlatUnicast</span><span class="sxs-lookup"><span data-stu-id="14573-427">NlatUnicast</span></span></li>
<li><span data-ttu-id="14573-428">NlatAnycast</span><span class="sxs-lookup"><span data-stu-id="14573-428">NlatAnycast</span></span></li>
<li><span data-ttu-id="14573-429">NlatMulticast</span><span class="sxs-lookup"><span data-stu-id="14573-429">NlatMulticast</span></span></li>
<li><span data-ttu-id="14573-430">NlatBroadcast</span><span class="sxs-lookup"><span data-stu-id="14573-430">NlatBroadcast</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-431"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-431"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl> <span data-ttu-id="14573-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-432"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-433">L’adresse IP distante qui est incorporée dans le paquet ICMP.</span><span class="sxs-lookup"><span data-stu-id="14573-433">The remote IP address that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="14573-434"><strong>Type de données :</strong> Pour une adresse IPv4</span><span class="sxs-lookup"><span data-stu-id="14573-434"><strong>Data type:</strong> For an IPv4 address</span></span>
<ul>
<li><span data-ttu-id="14573-435">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-435">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-436">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-436">FWP_UINT32</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-437"><strong>Type de données :</strong> Pour une adresse IPv6</span><span class="sxs-lookup"><span data-stu-id="14573-437"><strong>Data type:</strong> For an IPv6 address</span></span>
<ul>
<li><span data-ttu-id="14573-438">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-438">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-439">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-439">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl> <span data-ttu-id="14573-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-440"><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-441">Numéro de protocole IP incorporé dans le paquet ICMP, tel que spécifié dans le document RFC 1700.</span><span class="sxs-lookup"><span data-stu-id="14573-441">The IP protocol number that is embedded in the ICMP packet, as specified in RFC 1700.</span></span> <br/> <span data-ttu-id="14573-442"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-442"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl> <span data-ttu-id="14573-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-443"><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-444">Numéro de port du protocole de transport local qui est incorporé dans le paquet ICMP.</span><span class="sxs-lookup"><span data-stu-id="14573-444">The local transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="14573-445"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-445"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl> <span data-ttu-id="14573-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-446"><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-447">Numéro de port du protocole de transport distant qui est incorporé dans le paquet ICMP.</span><span class="sxs-lookup"><span data-stu-id="14573-447">The remote transport protocol port number that is embedded in the ICMP packet.</span></span> <br/> <span data-ttu-id="14573-448"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-448"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl> <span data-ttu-id="14573-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-449"><dt><strong>FWPM_CONDITION_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-450">Or au niveau du bit d’une combinaison d’indicateurs de condition de filtrage.</span><span class="sxs-lookup"><span data-stu-id="14573-450">A bitwise OR of a combination of filtering condition flags.</span></span> <br/> <span data-ttu-id="14573-451"><strong>Valeurs possibles :</strong> Voir <a href="filtering-condition-flags-.md"> <strong>indicateurs de condition de filtrage</strong></a></span><span class="sxs-lookup"><span data-stu-id="14573-451"><strong>Possible values:</strong> See <a href="filtering-condition-flags-.md"><strong>Filtering Condition Flags</strong></a></span></span><br/> <span data-ttu-id="14573-452"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-452"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl> <span data-ttu-id="14573-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-453"><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-454">Direction du trafic ou du flux de données.</span><span class="sxs-lookup"><span data-stu-id="14573-454">The direction of the traffic or data flow.</span></span> <br/> <span data-ttu-id="14573-455"><strong>Valeurs possibles :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-455"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-456">FWP_DIRECTION_INBOUND</span><span class="sxs-lookup"><span data-stu-id="14573-456">FWP_DIRECTION_INBOUND</span></span></li>
<li><span data-ttu-id="14573-457">FWP_DIRECTION_OUTBOUND</span><span class="sxs-lookup"><span data-stu-id="14573-457">FWP_DIRECTION_OUTBOUND</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-458">Pour les couches de datagrammes (FWPM_LAYER_DATAGRAM_DATA_ *) et les couches de paquets de flux (FWPM_LAYER_STREAM_PACKET_*), la valeur sera la même que la direction du paquet.</span><span class="sxs-lookup"><span data-stu-id="14573-458">For datagram layers (FWPM_LAYER_DATAGRAM_DATA_ *) and stream packet layers (FWPM_LAYER_STREAM_PACKET_*), the value will be the same as the direction of the packet.</span></span> <br/> <span data-ttu-id="14573-459">Pour les couches de flux (FWPM_LAYER_STREAM_ *) et les couches établies par flux (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), la valeur sera la même que la direction de la connexion.</span><span class="sxs-lookup"><span data-stu-id="14573-459">For stream layers (FWPM_LAYER_STREAM_ *) and flow established layers (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), the value will be the same as direction of the connection.</span></span> <span data-ttu-id="14573-460">(Par exemple, lorsqu’une application locale initie la connexion, un paquet entrant a <strong>FWPM_CONDITION_DIRECTION</strong> défini sur <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span><span class="sxs-lookup"><span data-stu-id="14573-460">(For example, when a local application initiates the connection, an inbound packet has <strong>FWPM_CONDITION_DIRECTION</strong> set to <strong>FWP_DIRECTION_OUTBOUND</strong>.)</span></span> <br/> <span data-ttu-id="14573-461"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-461"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl> <span data-ttu-id="14573-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-462"><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-463">Index de l’interface réseau, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-463">The index of the network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="14573-464"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-464"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl> <span data-ttu-id="14573-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-465"><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-466">Index de l’interface réseau logique, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-466">The index of the logical network interface, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="14573-467"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-467"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl> <span data-ttu-id="14573-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-468"><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-469">Index de l’interface réseau source pour les paquets transférés, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-469">The index of the source network interface for forwarded packets, as enumerated by the network stack.</span></span><br/> <span data-ttu-id="14573-470"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-470"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl> <span data-ttu-id="14573-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-471"><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-472">Index de l’interface de réseau logique source pour les paquets transférés, tels qu’ils sont énumérés par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-472">The index of the source logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="14573-473"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-473"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl> <span data-ttu-id="14573-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-474"><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-475">Index de l’interface réseau de destination pour les paquets transférés, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-475">The index of the destination network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="14573-476"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-476"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl> <span data-ttu-id="14573-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-477"><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-478">Index de l’interface réseau logique de destination pour les paquets transférés, tel qu’il est énuméré par la pile réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-478">The index of the destination logical network interface for forwarded packets, as enumerated by the network stack.</span></span> <br/> <span data-ttu-id="14573-479"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-479"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl> <span data-ttu-id="14573-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-480"><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-481">Le chemin d’accès complet de l’application, tel que retourné par la fonction <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="14573-481">The fully qualified device path of the application, as returned by the <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> function.</span></span> <br/> <span data-ttu-id="14573-482">(Par exemple, &quot; \device0\hardiskvolume1\Program Files\Application.exe&quot; .)</span><span class="sxs-lookup"><span data-stu-id="14573-482">(For example, &quot;\device0\hardiskvolume1\Program Files\Application.exe&quot;.)</span></span><br/> <span data-ttu-id="14573-483"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-483"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl> <span data-ttu-id="14573-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-484"><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-485">Identification de l’utilisateur local.</span><span class="sxs-lookup"><span data-stu-id="14573-485">The identification of the local user.</span></span> <br/> <span data-ttu-id="14573-486"><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-486"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl> <span data-ttu-id="14573-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-487"><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-488">Identification de l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="14573-488">The identification of the remote user.</span></span> <br/> <span data-ttu-id="14573-489"><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-489"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl> <span data-ttu-id="14573-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-490"><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-491">Identification de l’ordinateur distant.</span><span class="sxs-lookup"><span data-stu-id="14573-491">The identification of the remote machine.</span></span> <br/> <span data-ttu-id="14573-492"><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-492"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl> <span data-ttu-id="14573-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-493"><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-494">Mode de socket brut autorisé ou refusé.</span><span class="sxs-lookup"><span data-stu-id="14573-494">The raw socket mode that is allowed or denied.</span></span><br/> <span data-ttu-id="14573-495"><strong>Valeurs possibles :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-495"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-496">SIO_RCVALL</span><span class="sxs-lookup"><span data-stu-id="14573-496">SIO_RCVALL</span></span></li>
<li><span data-ttu-id="14573-497">SIO_RCVALL_IGMPMCAST</span><span class="sxs-lookup"><span data-stu-id="14573-497">SIO_RCVALL_IGMPMCAST</span></span></li>
<li><span data-ttu-id="14573-498">SIO_RCVALL_MCAST</span><span class="sxs-lookup"><span data-stu-id="14573-498">SIO_RCVALL_MCAST</span></span></li>
</ul>
<span data-ttu-id="14573-499">Pour obtenir une description de ces modes de socket brut, consultez la fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="14573-499">For a description of these raw socket modes, see the <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> function.</span></span><br/> <span data-ttu-id="14573-500"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-500"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl> <span data-ttu-id="14573-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-501"><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-502">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="14573-502">Reserved for internal use.</span></span> <br/> <span data-ttu-id="14573-503"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-503"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl> <span data-ttu-id="14573-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-504"><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-505">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="14573-505">Reserved for internal use.</span></span> <br/> <span data-ttu-id="14573-506"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-506"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



<span data-ttu-id="14573-507">Les constantes suivantes sont disponibles pour le mode utilisateur uniquement.</span><span class="sxs-lookup"><span data-stu-id="14573-507">The following constants are available for user mode only.</span></span>



| <span data-ttu-id="14573-508">Conditions de mode utilisateur disponibles pour Windows 8 et Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="14573-508">User-mode conditions available for Windows 8 and Windows Server 2012</span></span>                                                                                                                       | <span data-ttu-id="14573-509">Description</span><span class="sxs-lookup"><span data-stu-id="14573-509">Description</span></span>                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <span data-ttu-id="14573-510"><dt>**\_ \_ mode QM de condition FWPM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="14573-510"><dt>**FWPM\_CONDITION\_QM\_MODE**</dt></span></span> </dl> | <span data-ttu-id="14573-511">Mode du filtre en mode rapide (QM).</span><span class="sxs-lookup"><span data-stu-id="14573-511">The mode of the quick mode (QM) filter.</span></span> <span data-ttu-id="14573-512">Consultez [**\_ \_ type de trafic IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) pour connaître les valeurs possibles.</span><span class="sxs-lookup"><span data-stu-id="14573-512">See [**IPSEC\_TRAFFIC\_TYPE**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) for possible values.</span></span><br/> <span data-ttu-id="14573-513">**Type de données :** FWP \_ UInt32</span><span class="sxs-lookup"><span data-stu-id="14573-513">**Data type:** FWP\_UINT32</span></span><br/> |





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="14573-514">Conditions de mode utilisateur disponibles pour Windows 7, Windows Server 2008 R2 et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="14573-514">User-mode conditions available for Windows 7, Windows Server 2008 R2, and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="14573-515">Description</span><span class="sxs-lookup"><span data-stu-id="14573-515">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl> <span data-ttu-id="14573-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-516"><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-517">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="14573-517">Reserved for internal use.</span></span><br/> <span data-ttu-id="14573-518"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-518"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl> <span data-ttu-id="14573-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-519"><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-520">Nom de l’homologue.</span><span class="sxs-lookup"><span data-stu-id="14573-520">The name of the peer.</span></span> <span data-ttu-id="14573-521">Par exemple, le nom DNS de l’homologue.</span><span class="sxs-lookup"><span data-stu-id="14573-521">For example, the peer's DNS name.</span></span><br/> <span data-ttu-id="14573-522"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-522"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl> <span data-ttu-id="14573-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-523"><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-524">Identité du principal d’authentification distant.</span><span class="sxs-lookup"><span data-stu-id="14573-524">The identity of the remote authentication principal.</span></span> <br/> <span data-ttu-id="14573-525"><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-525"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="14573-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-526"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-527">Type de méthode d’authentification IKE, IKEv2 ou AuthIP.</span><span class="sxs-lookup"><span data-stu-id="14573-527">The type of IKE, IKEv2, or AuthIP authentication method.</span></span> <br/> <span data-ttu-id="14573-528"><strong>Type de données :</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-528"><strong>Data type:</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl> <span data-ttu-id="14573-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-529"><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-530">Type de module de génération de clé.</span><span class="sxs-lookup"><span data-stu-id="14573-530">The type of keying module.</span></span><br/> <span data-ttu-id="14573-531"><strong>Type de données :</strong> IKEEXT_KEY_MODULE_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-531"><strong>Data type:</strong> IKEEXT_KEY_MODULE_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl> <span data-ttu-id="14573-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-532"><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-533">Mode IPsec dans lequel un jeton peut être obtenu.</span><span class="sxs-lookup"><span data-stu-id="14573-533">The IPsec mode in which a token can be obtained.</span></span><br/> <span data-ttu-id="14573-534"><strong>Type de données :</strong> IPSEC_TOKEN_MODE</span><span class="sxs-lookup"><span data-stu-id="14573-534"><strong>Data type:</strong> IPSEC_TOKEN_MODE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl> <span data-ttu-id="14573-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-535"><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-536">Clé de contexte du fournisseur de stratégie en mode principal (MM) ou en mode rapide (QM) de la SA qui est autorisée.</span><span class="sxs-lookup"><span data-stu-id="14573-536">The main mode (MM) or quick mode (QM) policy provider context key of the SA being authorized.</span></span> <span data-ttu-id="14573-537">Utile pour limiter l’étendue de la règle d’autorisation à la signature d’accès partagé à l’aide d’une clé de stratégie IPsec MM ou QM spécifiée.</span><span class="sxs-lookup"><span data-stu-id="14573-537">Useful for restricting the scope of the authorization rule to SAs formed using a specified IPsec MM or QM policy key.</span></span><br/> <span data-ttu-id="14573-538"><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-538"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl> <span data-ttu-id="14573-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-539"><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-540">Méthode utilisée pour authentifier l’Association de sécurité.</span><span class="sxs-lookup"><span data-stu-id="14573-540">The method used to authenticate the security association.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="14573-541">Disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="14573-541">Available only on Windows Server 2008 R2, Windows 7, and later.</span></span>
</blockquote>
<br/> <span data-ttu-id="14573-542"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-542"><strong>Data type:</strong> FWP_UINT32</span></span> <br/></td>
</tr>
</tbody>
</table>





<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="14573-543">Constantes disponibles pour Windows Vista et versions ultérieures</span><span class="sxs-lookup"><span data-stu-id="14573-543">Constants available for Windows Vista and later</span></span></th>
<th style="text-align: left;"><span data-ttu-id="14573-544">Description</span><span class="sxs-lookup"><span data-stu-id="14573-544">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl> <span data-ttu-id="14573-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-545"><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-546">Identification de l’utilisateur distant.</span><span class="sxs-lookup"><span data-stu-id="14573-546">The identification of the remote user.</span></span><br/> <span data-ttu-id="14573-547"><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-547"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl> <span data-ttu-id="14573-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-548"><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-549">UUID de l’interface RPC.</span><span class="sxs-lookup"><span data-stu-id="14573-549">The UUID of the RPC interface.</span></span> <br/> <span data-ttu-id="14573-550"><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-550"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl> <span data-ttu-id="14573-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-551"><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-552">Version de l’interface RPC.</span><span class="sxs-lookup"><span data-stu-id="14573-552">The version of the RPC interface.</span></span> <br/> <span data-ttu-id="14573-553"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-553"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl> <span data-ttu-id="14573-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-554"><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-555">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="14573-555">Reserved for internal use.</span></span> <br/> <span data-ttu-id="14573-556"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-556"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl> <span data-ttu-id="14573-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-557"><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-558">Identification de l’application COM.</span><span class="sxs-lookup"><span data-stu-id="14573-558">The identification of the COM application.</span></span><br/> <span data-ttu-id="14573-559"><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-559"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl> <span data-ttu-id="14573-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-560"><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-561">Le nom de l’application.</span><span class="sxs-lookup"><span data-stu-id="14573-561">The name of the application.</span></span><br/> <span data-ttu-id="14573-562"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-562"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl> <span data-ttu-id="14573-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-563"><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-564">Protocole RPC.</span><span class="sxs-lookup"><span data-stu-id="14573-564">The RPC protocol.</span></span> <br/> <span data-ttu-id="14573-565"><strong>Valeurs possibles :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-565"><strong>Possible values:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-566">RPC_PROTSEQ_TCP</span><span class="sxs-lookup"><span data-stu-id="14573-566">RPC_PROTSEQ_TCP</span></span></li>
<li><span data-ttu-id="14573-567">RPC_PROTSEQ_NMP</span><span class="sxs-lookup"><span data-stu-id="14573-567">RPC_PROTSEQ_NMP</span></span></li>
<li><span data-ttu-id="14573-568">RPC_PROTSEQ_LRPC</span><span class="sxs-lookup"><span data-stu-id="14573-568">RPC_PROTSEQ_LRPC</span></span></li>
<li><span data-ttu-id="14573-569">RPC_PROTSEQ_HTTP</span><span class="sxs-lookup"><span data-stu-id="14573-569">RPC_PROTSEQ_HTTP</span></span></li>
</ul>
<br/> <span data-ttu-id="14573-570"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-570"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl> <span data-ttu-id="14573-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-571"><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-572">Type de service d’authentification.</span><span class="sxs-lookup"><span data-stu-id="14573-572">The authentication service type.</span></span> <span data-ttu-id="14573-573">Pour plus d’informations sur les types de service d’authentification, consultez la page relative aux <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>constantes de service d'</strong></a>authentification.</span><span class="sxs-lookup"><span data-stu-id="14573-573">For more information about authentication service types, see <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>Authentication-Service Constants</strong></a>.</span></span> <br/> <span data-ttu-id="14573-574"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-574"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl> <span data-ttu-id="14573-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-575"><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-576">Niveau du service d’authentification.</span><span class="sxs-lookup"><span data-stu-id="14573-576">The authentication service level.</span></span> <span data-ttu-id="14573-577">Pour plus d’informations sur les niveaux de service d’authentification, consultez <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>constantes au niveau de l’authentification</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="14573-577">For more information about authentication service levels, see <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>Authentication-Level Constants</strong></a>.</span></span> <br/> <span data-ttu-id="14573-578"><strong>Type de données :</strong> FWP_UINT8</span><span class="sxs-lookup"><span data-stu-id="14573-578"><strong>Data type:</strong> FWP_UINT8</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl> <span data-ttu-id="14573-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-579"><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-580">Algorithme de chiffrement SSPI (Security Service Provider Interface) basé sur les certificats.</span><span class="sxs-lookup"><span data-stu-id="14573-580">The certificate based Security Service Provider Interface (SSPI) encryption algorithm.</span></span><br/> <span data-ttu-id="14573-581"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-581"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl> <span data-ttu-id="14573-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-582"><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-583">Taille de la clé de chiffrement SSPI basée sur le certificat.</span><span class="sxs-lookup"><span data-stu-id="14573-583">The certificate based SSPI encryption key size.</span></span><br/> <span data-ttu-id="14573-584"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-584"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl> <span data-ttu-id="14573-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-585"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-586">Adresse IPv4 locale.</span><span class="sxs-lookup"><span data-stu-id="14573-586">The local IPv4 address.</span></span> <br/> <span data-ttu-id="14573-587"><strong>Type de données :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-587"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-588">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-588">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-589">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-589">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl> <span data-ttu-id="14573-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-590"><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-591">Adresse IPv6 locale.</span><span class="sxs-lookup"><span data-stu-id="14573-591">The local IPv6 address.</span></span> <br/> <span data-ttu-id="14573-592"><strong>Type de données :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-592"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-593">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-593">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-594">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-594">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl> <span data-ttu-id="14573-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-595"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-596">Adresse IPv4 distante.</span><span class="sxs-lookup"><span data-stu-id="14573-596">The remote IPv4 address.</span></span> <br/> <span data-ttu-id="14573-597"><strong>Type de données :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-597"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-598">FWP_V4_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-598">FWP_V4_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-599">FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-599">FWP_UINT32</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl> <span data-ttu-id="14573-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-600"><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-601">Adresse IPv6 distante.</span><span class="sxs-lookup"><span data-stu-id="14573-601">The remote IPv6 address.</span></span> <br/> <span data-ttu-id="14573-602"><strong>Type de données :  </strong>
</span><span class="sxs-lookup"><span data-stu-id="14573-602"><strong>Data type:  </strong>
</span></span><ul>
<li><span data-ttu-id="14573-603">FWP_V6_ADDR_MASK ou</span><span class="sxs-lookup"><span data-stu-id="14573-603">FWP_V6_ADDR_MASK, or</span></span></li>
<li><span data-ttu-id="14573-604">FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-604">FWP_BYTE_ARRAY16_TYPE</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl> <span data-ttu-id="14573-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-605"><dt><strong>FWPM_CONDITION_PIPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-606">Nom du canal nommé distant.</span><span class="sxs-lookup"><span data-stu-id="14573-606">The name of the remote named pipe.</span></span><br/> <span data-ttu-id="14573-607"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-607"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl> <span data-ttu-id="14573-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-608"><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-609">UUID du processus avec l’interface RPC.</span><span class="sxs-lookup"><span data-stu-id="14573-609">The UUID of the process with the RPC interface.</span></span><br/> <span data-ttu-id="14573-610"><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-610"><strong>Data type:</strong> FWP_BYTE_ARRAY16_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl> <span data-ttu-id="14573-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-611"><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-612">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="14573-612">Reserved for internal use.</span></span><br/> <span data-ttu-id="14573-613"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-613"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl> <span data-ttu-id="14573-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-614"><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-615">Réservé à un usage interne.</span><span class="sxs-lookup"><span data-stu-id="14573-615">Reserved for internal use.</span></span><br/> <span data-ttu-id="14573-616"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-616"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl> <span data-ttu-id="14573-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-617"><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-618">Identification du client lors de l’utilisation de RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="14573-618">The identification of the client when using RpcProxy.</span></span><br/> <span data-ttu-id="14573-619"><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-619"><strong>Data type:</strong> FWP_SECURITY_DESCRIPTOR_TYPE</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl> <span data-ttu-id="14573-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-620"><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-621">Nom du serveur RPC lors de l’utilisation de RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="14573-621">The name of the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="14573-622"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-622"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl> <span data-ttu-id="14573-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-623"><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-624">Le port sur le serveur RPC lors de l’utilisation de RpcProxy.</span><span class="sxs-lookup"><span data-stu-id="14573-624">The port on the RPC server when using RpcProxy.</span></span><br/> <span data-ttu-id="14573-625"><strong>Type de données :</strong> FWP_UINT16</span><span class="sxs-lookup"><span data-stu-id="14573-625"><strong>Data type:</strong> FWP_UINT16</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl> <span data-ttu-id="14573-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-626"><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-627">Type de service d’authentification de proxy RPC.</span><span class="sxs-lookup"><span data-stu-id="14573-627">The RPC proxy authentication service type.</span></span><br/> <span data-ttu-id="14573-628"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-628"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl> <span data-ttu-id="14573-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-629"><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-630">Longueur de la clé SSL (Secure Socket Layer) dans le certificat client.</span><span class="sxs-lookup"><span data-stu-id="14573-630">The Secure Socket Layer (SSL) key length in the client certificate.</span></span><br/> <span data-ttu-id="14573-631"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-631"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl> <span data-ttu-id="14573-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-632"><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-633">Identificateur d’objet dans le certificat client.</span><span class="sxs-lookup"><span data-stu-id="14573-633">The object identifier in the client certificate.</span></span><br/> <span data-ttu-id="14573-634"><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE</span><span class="sxs-lookup"><span data-stu-id="14573-634"><strong>Data type:</strong> FWP_BYTE_BLOB_TYPE</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl> <span data-ttu-id="14573-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="14573-635"><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="14573-636">Type d’événement net.</span><span class="sxs-lookup"><span data-stu-id="14573-636">The type of net event.</span></span><br/> <span data-ttu-id="14573-637"><strong>Type de données :</strong> FWP_UINT32</span><span class="sxs-lookup"><span data-stu-id="14573-637"><strong>Data type:</strong> FWP_UINT32</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="14573-638">Notes</span><span class="sxs-lookup"><span data-stu-id="14573-638">Remarks</span></span>

<span data-ttu-id="14573-639">Lorsque les adresses IP sont stockées au \_ format fwp UInt32 ou lorsqu’un port IP est stocké au \_ format fwp UINT16, elles sont stockées dans l’ordre de l’hôte, et non dans l’ordre du réseau.</span><span class="sxs-lookup"><span data-stu-id="14573-639">When IP addresses are stored in FWP\_UINT32 format or when an IP port is stored in FWP\_UINT16 format, they are stored in host-order, not network-order.</span></span>

## <a name="requirements"></a><span data-ttu-id="14573-640">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14573-640">Requirements</span></span>



| <span data-ttu-id="14573-641">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14573-641">Requirement</span></span> | <span data-ttu-id="14573-642">Valeur</span><span class="sxs-lookup"><span data-stu-id="14573-642">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="14573-643">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14573-643">Minimum supported client</span></span><br/> | <span data-ttu-id="14573-644">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14573-644">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="14573-645">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14573-645">Minimum supported server</span></span><br/> | <span data-ttu-id="14573-646">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14573-646">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="14573-647">En-tête</span><span class="sxs-lookup"><span data-stu-id="14573-647">Header</span></span><br/>                   | <dl> <span data-ttu-id="14573-648"><dt>Fwpmu. h</dt></span><span class="sxs-lookup"><span data-stu-id="14573-648"><dt>Fwpmu.h</dt></span></span> </dl> |
