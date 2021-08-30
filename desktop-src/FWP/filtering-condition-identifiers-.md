---
title: Filtrage des identificateurs de condition (Fwpmu. h)
description: les identificateurs de condition de filtrage de la plateforme de filtrage de Windows (WFP) sont représentés par un GUID.
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
ms.openlocfilehash: f5c3823ed750637d595924eb47acc714403751eb
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467976"
---
# <a name="filtering-condition-identifiers"></a>Filtrage des identificateurs de condition

les identificateurs de condition de filtrage de la plateforme de filtrage de Windows (WFP) sont représentés par un **GUID**. Le type de données de la valeur de condition pour chaque condition de filtrage est spécifié sous la forme d’un [**\_ \_ type de données fwp**](/windows/desktop/api/Fwptypes/ne-fwptypes-fwp_data_type). Ces identificateurs et leurs types de données sont définis ici.

Les conditions standard sont répertoriées en premier, suivies des conditions spécifiques du mode utilisateur. Les conditions sont regroupées par système d’exploitation pris en charge, afin que vous puissiez identifier facilement les conditions prises en charge pour un système d’exploitation donné.

> [!Note]  
> Chacune des conditions de filtrage suivantes est disponible uniquement dans un sous-ensemble des couches de filtrage WFP. Pour plus d’informations sur la disponibilité de chaque condition dans une couche donnée, consultez [**conditions de filtrage disponibles à chaque couche de filtrage**](filtering-conditions-available-at-each-filtering-layer.md).

 




| Conditions disponibles pour Windows 8 et Windows Server 2012 | Description | 
|------------------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_INTERFACE_MAC_ADDRESS"></span><span id="fwpm_condition_interface_mac_address"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE_MAC_ADDRESS</strong></dt></dl> | Adresse MAC d’une interface locale particulière.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE <br /> | 
| <span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS"></span><span id="fwpm_condition_mac_local_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS</strong></dt></dl> | Adresse de destination d’un frame entrant, ou adresse source d’un frame sortant.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS"></span><span id="fwpm_condition_mac_remote_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS</strong></dt></dl> | Adresse source d’un frame entrant ou adresse de destination d’un frame sortant.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_ETHER_TYPE"></span><span id="fwpm_condition_ether_type"></span><dl><dt><strong>FWPM_CONDITION_ETHER_TYPE</strong></dt></dl> | Type de données de la charge utile du réseau Ethernet v2. (Voir ETHERNET_TYPE_IPV4, etc. dans netiodef. h.)<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VLAN_ID"></span><span id="fwpm_condition_vlan_id"></span><dl><dt><strong>FWPM_CONDITION_VLAN_ID</strong></dt></dl> | Les 16 bits d’en-tête VLAN, y compris les champs VID, CFI et Priority, conformément à la norme 802.1 q (voir VLAN_TAG dans netiodef. h pour les positions des champs de bits).<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID"></span><span id="fwpm_condition_vswitch_tenant_network_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_TENANT_NETWORK_ID</strong></dt></dl> | Identificateur unique du réseau vSwitch. Ne peut pas être utilisé conjointement avec VLAN_IDs.<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_NDIS_PORT"></span><span id="fwpm_condition_ndis_port"></span><dl><dt><strong>FWPM_CONDITION_NDIS_PORT</strong></dt></dl> | Numéro de port du port NDIS.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_NDIS_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_media_type"></span><dl><dt><strong>FWPM_CONDITION_NDIS_MEDIA_TYPE</strong></dt></dl> | Type de média du port NDIS.<br /><strong>Type de données :</strong> FWP_UINT32<br /><strong>Valeurs possibles :</strong> L’une des <strong>NDIS_MEDIUM</strong> valeurs d’énumération. (Voir ntddndis. h.) <br /> | 
| <span id="FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE"></span><span id="fwpm_condition_ndis_physical_media_type"></span><dl><dt><strong>FWPM_CONDITION_NDIS_PHYSICAL_MEDIA_TYPE</strong></dt></dl> | Type de média physique du port NDIS.<br /><strong>Type de données :</strong> FWP_UINT32<br /><strong>Valeurs possibles :</strong> L’une des <strong>NDIS_PHYSICAL_MEDIUM</strong> valeurs d’énumération. (Voir ntddndis. h.) <br /> | 
| <span id="FWPM_CONDITION_L2_FLAGS"></span><span id="fwpm_condition_l2_flags"></span><dl><dt><strong>FWPM_CONDITION_L2_FLAGS</strong></dt></dl> | Or au niveau du bit d’une combinaison d’indicateurs de condition de filtrage. <br /><strong>Type de données :</strong> FWP_UINT32<br /><strong>Valeurs possibles :  </strong><ul><li>FWP_CONDITION_L2_IS_MOBILE_BROADBAND</li><li>FWP_CONDITION_L2_IS_NATIVE_ETHERNET</li><li>FWP_CONDITION_L2_IS_WIFI</li><li>FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_local_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_LOCAL_ADDRESS_TYPE</strong></dt></dl> | Type d’adresse de l’adresse locale physique.<br /><strong>Type de données :</strong> FWP_UINT8<br /><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_remote_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_REMOTE_ADDRESS_TYPE</strong></dt></dl> | Type d’adresse de l’adresse distante physique.<br /><strong>Type de données :</strong> FWP_UINT8<br /><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS"></span><span id="fwpm_condition_mac_source_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS</strong></dt></dl> | Adresse source physique d’un frame.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS"></span><span id="fwpm_condition_mac_destination_address"></span><dl><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS</strong></dt></dl> | Adresse physique de destination d’une trame.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY6_TYPE<br /> | 
| <span id="FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_source_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_SOURCE_ADDRESS_TYPE</strong></dt></dl> | Type d’adresse de l’adresse de destination physique.<br /><strong>Type de données :</strong> FWP_UINT8<br /><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_mac_destination_address_type"></span><dl><dt><strong>FWPM_CONDITION_MAC_DESTINATION_ADDRESS_TYPE</strong></dt></dl> | Type d’adresse de l’adresse de destination physique.<br /><strong>Type de données :</strong> FWP_UINT8<br /><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <strong>DL_ADDRESS_TYPE</strong> suivantes.<ul><li>DlUnicast</li><li>DlMulticast</li><li>DlBroadcast</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_SOURCE_PORT"></span><span id="fwpm_condition_ip_source_port"></span><dl><dt><strong>FWPM_CONDITION_IP_SOURCE_PORT</strong></dt></dl> | Port source du transport du paquet.<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_ICMP_TYPE"></span><span id="fwpm_condition_vswitch_icmp_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_TYPE</strong></dt></dl> | Champ de type ICMP, tel que spécifié dans le document RFC 792.<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_IP_DESTINATION_PORT"></span><span id="fwpm_condition_ip_destination_port"></span><dl><dt><strong>FWPM_CONDITION_IP_DESTINATION_PORT</strong></dt></dl> | Port de destination du transport du paquet.<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_ICMP_CODE"></span><span id="fwpm_condition_vswitch_icmp_code"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_ICMP_CODE</strong></dt></dl> | Champ de code ICMP, tel que spécifié dans le document RFC 792. <br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_ID"></span><span id="fwpm_condition_vswitch_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_ID</strong></dt></dl> | Identificateur unique d’une instance de vSwitch.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_NETWORK_TYPE"></span><span id="fwpm_condition_vswitch_network_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_NETWORK_TYPE</strong></dt></dl> | Spécifie si l’instance vSwitch fait partie d’un réseau virtuel externe, interne ou privé.<br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_source_interface_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_ID</strong></dt></dl> | Identificateur unique de la source du paquet en cours. (Nom d’une machine virtuelle-NIC, P-NIC ou V-NIC.)<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID"></span><span id="fwpm_condition_vswitch_destination_interface_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_ID</strong></dt></dl> | Identificateur unique de la destination du paquet actuel. (Nom d’une machine virtuelle-NIC, P-NIC ou V-NIC.)<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_SOURCE_VM_ID"></span><span id="fwpm_condition_vswitch_source_vm_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_VM_ID</strong></dt></dl> | Identificateur unique de la machine virtuelle source vSwitch.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID"></span><span id="fwpm_condition_vswitch_destination_vm_id"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_VM_ID</strong></dt></dl> | Identificateur unique de la machine virtuelle de destination vSwitch.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_source_interface_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_SOURCE_INTERFACE_TYPE</strong></dt></dl> | Type d’interface de la source du paquet en cours.<br /><strong>Type de données :</strong> FWP_UINT8<br /><strong>Valeurs possibles :  </strong><ul><li>SwitchNicSyntheticNic (lorsque le type d’interface est VM-NIC)</li><li>SwitchNicEmulatedNic (lorsque le type d’interface est VM-NIC)</li><li>SwitchNicPhysicalNic (lorsque le type d’interface est P-NIC)</li><li>SwitchNicVNic (lorsque le type d’interface est V-NIC, connecté à la partition hôte)</li></ul><br /> | 
| <span id="FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE"></span><span id="fwpm_condition_vswitch_destination_interface_type"></span><dl><dt><strong>FWPM_CONDITION_VSWITCH_DESTINATION_INTERFACE_TYPE</strong></dt></dl> | Type d’interface de la destination du paquet actuel.<br /><strong>Type de données :</strong> FWP_UINT8<br /><strong>Valeurs possibles :  </strong><ul><li>SwitchNicSyntheticNic (lorsque le type d’interface est VM-NIC)</li><li>SwitchNicEmulatedNic (lorsque le type d’interface est VM-NIC)</li><li>SwitchNicPhysicalNic (lorsque le type d’interface est P-NIC)</li><li>SwitchNicVNic (lorsque le type d’interface est V-NIC, connecté à la partition hôte)</li></ul><br /> | 
| <span id="FWPM_CONDITION_INTERFACE"></span><span id="fwpm_condition_interface"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE</strong></dt></dl> | LUID de l’interface réseau associée à l’adresse IP locale. <br /><strong>Type de données :</strong> FWP_UINT64<br /> | 
| <span id="FWPM_CONDITION_ALE_PACKAGE_ID"></span><span id="fwpm_condition_ale_package_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_PACKAGE_ID</strong></dt></dl> | Identificateur de sécurité (SID) d’un conteneur d’application.<br /><strong>Type de données :</strong> FWP_SID<br /> | 
| <span id="FWPM_CONDITION_ALE_ORIGINAL_APP_ID"></span><span id="fwpm_condition_ale_original_app_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_ORIGINAL_APP_ID</strong></dt></dl> | Le chemin d’accès complet de l’appareil de l’application, par exemple « \device0\hardiskvolume1\Program Files\Application.exe ». Lorsqu’une connexion a été redirigée, il s’agit de l’identificateur de l’application d’origine. dans le cas contraire, ce sera le même que <strong>FWPM_CONDITION_ALE_APP_ID</strong>.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 






| Conditions disponibles pour Windows 7, Windows Server 2008 R2 et versions ultérieures                                                                                                                                                                                                    | Description                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_NEXTHOP_ADDRESS"></span><span id="fwpm_condition_ip_nexthop_address"></span><dl> <dt>**\_ \_ \_ adresse IP NEXTHOP \_ de la condition FWPM**</dt> </dl>                                             | Adresse IP de l’interface de saut suivant.<br/> **Type de données :** \_Masque d' \_ ADR v4 v4 \_<br/>                                                                                                                                                                                        |
| <span id="FWPM_CONDITION_IP_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_nexthop_interface"></span><dl> <dt>**\_interface d' \_ IP \_ NEXTHOP \_ d’une condition FWPM**</dt> </dl>                                       | Interface de saut suivant à partir de laquelle le paquet sera en cours de déconditionnement. <br/> **Type de données :** FWP \_ UINT64<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_TYPE"></span><span id="fwpm_condition_nexthop_interface_type"></span><dl> <dt>**\_condition FWPM \_ \_ type d’interface NEXTHOP \_**</dt> </dl>                                 | Type d’interface de l’interface de saut suivant.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                            |
| <span id="FWPM_CONDITION_NEXTHOP_TUNNEL_TYPE"></span><span id="fwpm_condition_nexthop_tunnel_type"></span><dl> <dt>**\_type de \_ tunnel de tronçons de la condition FWPM \_ \_**</dt> </dl>                                          | Type de tunnel de l’interface de saut suivant.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                               |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_interface_index"></span><dl> <dt>**FWPM \_ état \_ d' \_ interface NEXTHOP de la condition \_**</dt> </dl>                              | Index d’interface de l’interface de saut suivant.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_nexthop_sub_interface_index"></span><dl> <dt>**FWPM \_ condition de la \_ sous- \_ \_ interface de tronçons \_**</dt> </dl>                 | Index de sous-interface de l’interface de saut suivant.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                       |
| <span id="FWPM_CONDITION_ORIGINAL_PROFILE_ID"></span><span id="fwpm_condition_original_profile_id"></span><dl> <dt>**\_ID de \_ profil d’origine de la condition FWPM \_ \_**</dt> </dl>                                          | Catégorie réseau de l’interface d’arrivée ou de saut suivant par le biais de laquelle le Flow ALE (entrant ou sortant) est créé. <br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                  |
| <span id="FWPM_CONDITION_CURRENT_PROFILE_ID"></span><span id="fwpm_condition_current_profile_id"></span><dl> <dt>**\_ID de \_ \_ profil actuel de condition \_ FWPM**</dt> </dl>                                             | Catégorie réseau de l’interface d’arrivée ou de saut suivant par le biais de laquelle le paquet en cours (entrant ou sortant) est créé. <br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                            |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_local_interface_profile_id"></span><dl> <dt>**ID de profil de l' \_ \_ interface locale de condition FWPM \_ \_ \_**</dt> </dl>                    | Catégorie de réseau de l’interface de remise.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_arrival_interface_profile_id"></span><dl> <dt>**ID de profil de l’interface d’arrivée de la \_ condition FWPM \_ \_ \_ \_**</dt> </dl>              | Catégorie réseau de l’interface d’arrivée.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_NEXTHOP_INTERFACE_PROFILE_ID"></span><span id="fwpm_condition_nexthop_interface_profile_id"></span><dl> <dt>**ID de profil de l' \_ \_ \_ interface NEXTHOP \_ \_ de la condition FWPM**</dt> </dl>              | Catégorie réseau de l’interface de saut suivant.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_REAUTHORIZE_REASON"></span><span id="fwpm_condition_reauthorize_reason"></span><dl> <dt>**raison de l’autorisation de la \_ condition FWPM \_ \_**</dt> </dl>                                              | Raison de la réautorisation d’une connexion précédemment autorisée.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                         |
| <span id="FWPM_CONDITION_ALE_REAUTH_REASON"></span><span id="fwpm_condition_ale_reauth_reason"></span><dl> <dt>**\_raison de \_ la \_ réauthentification ALE de condition FWPM \_**</dt> </dl>                                                | La raison pour laquelle vous autorisez une connexion précédemment autorisée, telle que la **condition fwp, \_ \_ réautorisez la \_ \_ \_ modification** de la stratégie de motif (ou l’une des autres valeurs indiquées dans [**indicateurs de condition de filtrage**](filtering-condition-flags-.md)).<br/> **Type de données :** FWP \_ UInt32<br/> |
| <span id="FWPM_CONDITION_ORIGINAL_ICMP_TYPE"></span><span id="fwpm_condition_original_icmp_type"></span><dl> <dt>**\_ \_ \_ type ICMP d’origine \_ de la condition FWPM**</dt> </dl>                                             | Type ICMP avec lequel le Flow a été créé.<br/> **Type de données :** FWP \_ UINT16<br/>                                                                                                                                                                                           |
| <span id="FWPM_CONDITION_IP_PHYSICAL_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_physical_arrival_interface"></span><dl> <dt>**\_interface d' \_ \_ arrivée physique \_ IP \_ de condition FWPM**</dt> </dl>           | LUID de l’interface physique associée à l’adresse IP d’arrivée.<br/> **Type de données :** FWP \_ UINT64<br/>                                                                                                                                                               |
| <span id="FWPM_CONDITION_IP_PHYSICAL_NEXTHOP_INTERFACE"></span><span id="fwpm_condition_ip_physical_nexthop_interface"></span><dl> <dt>**\_ \_ \_ \_ interface physique NEXTHOP IP \_ de la condition FWPM**</dt> </dl>           | LUID de l’interface physique du tronçon suivant.<br/> **Type de données :** FWP \_ UINT64<br/>                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_INTERFACE_QUARANTINE_EPOCH"></span><span id="fwpm_condition_interface_quarantine_epoch"></span><dl> <dt>**époque de quarantaine de l' \_ interface de condition FWPM \_ \_ \_**</dt> </dl>                     | Nombre de époques associé à une interface. Réservé.<br/> **Type de données :** FWP \_ UINT64<br/>                                                                                                                                                                                  |
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SOCKET_PROPERTY"></span><span id="fwpm_condition_ale_sio_firewall_socket_property"></span><dl> <dt>**\_propriété de \_ \_ Socket de \_ pare-feu SIO \_ de condition FWPM ALE \_**</dt> </dl> | Réservé à un usage interne. <br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                                              |





| constantes disponibles pour Windows Vista avec SP1, Windows Server 2008 et versions ultérieures                                                                                                                                                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_IP_ARRIVAL_INTERFACE"></span><span id="fwpm_condition_ip_arrival_interface"></span><dl> <dt>**\_interface d' \_ \_ arrivée IP de condition \_ FWPM**</dt> </dl>                       | LUID de l’interface réseau associée à l’adresse IP d’arrivée. <br/> **Type de données :** FWP \_ UINT64<br/>                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_TYPE"></span><span id="fwpm_condition_arrival_interface_type"></span><dl> <dt>**\_type d' \_ interface d’arrivée \_ \_ de la condition FWPM**</dt> </dl>                 | Type de l’interface réseau d’arrivée telle que définie par l’IANA (Internet Assigned Names Authority). Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valeurs possibles :** Valeurs de type d’interface listées dans le fichier d’en-tête Ipifcons. h.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                   |
| <span id="_FWPM_CONDITION_ARRIVAL_TUNNEL_TYPE"></span><span id="_fwpm_condition_arrival_tunnel_type"></span><dl> <dt>**FWPM \_ \_type de \_ tunnel \_ d’arrivée des conditions**</dt> </dl>                       | Méthode d’encapsulation utilisée par un tunnel associé à l’interface réseau d’arrivée si le membre de type est un \_ tunnel de type \_ . Le type de tunnel est défini par l’IANA (Internet Assigned Names Authority). Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valeurs possibles :** \_Valeurs de type d’énumération de type de tunnel listées dans le fichier d’en-tête ifdef. h.<br/> **Type de données :** FWP \_ UInt32<br/> |
| <span id="FWPM_CONDITION_ARRIVAL_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_interface_index"></span><dl> <dt>**INDEX de l’interface d’arrivée de la \_ condition FWPM \_ \_ \_**</dt> </dl>              | Index de l’interface réseau d’arrivée, tel qu’il est énuméré par la pile réseau.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="FWPM_CONDITION_ARRIVAL_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_arrival_sub_interface_index"></span><dl> <dt>**\_index d' \_ interface de sous-interface d’arrivée de condition FWPM \_ \_ \_**</dt> </dl> | Index de l’interface réseau d’arrivée, tel qu’il est énuméré par la pile réseau. <br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                                                                                                                                                                                                     |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_INDEX"></span><span id="fwpm_condition_local_interface_index"></span><dl> <dt>**\_index d' \_ \_ interface locale de condition \_ FWPM**</dt> </dl>                    | Index de l’interface réseau, tel qu’il est énuméré par la pile réseau. <br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FWPM_CONDITION_LOCAL_INTERFACE_TYPE"></span><span id="fwpm_condition_local_interface_type"></span><dl> <dt>**\_type d' \_ \_ interface locale de condition \_ FWPM**</dt> </dl>                       | Type d’interface défini par l’IANA (Internet Assigned Names Authority). Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valeurs possibles :** Valeurs de type d’interface listées dans le fichier d’en-tête Ipifcons. h.<br/> **Type de données :** FWP \_ UInt32<br/>                                                                                                                                          |
| <span id="FWPM_CONDITION_LOCAL_TUNNEL_TYPE"></span><span id="fwpm_condition_local_tunnel_type"></span><dl> <dt>**\_type de \_ \_ tunnel local de condition \_ FWPM**</dt> </dl>                                | Méthode d’encapsulation utilisée par un tunnel si le type du membre est \_ un \_ tunnel de type. Le type de tunnel est défini par l’IANA (Internet Assigned Names Authority). Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br/> **Valeurs possibles :** \_Valeurs de type d’énumération de type de tunnel listées dans le fichier d’en-tête ifdef. h.<br/> **Type de données :** FWP \_ UInt32 <br/>                                              |






| constantes disponibles pour Windows Vista et versions ultérieures | Description | 
|-------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS"></span><span id="fwpm_condition_ip_local_address"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS</strong></dt></dl> | Adresse IP locale. <br /><strong>Type de données :</strong> Pour une adresse IPv4<ul><li>FWP_V4_ADDR_MASK ou</li><li>FWP_UINT32</li></ul><br /><strong>Type de données :</strong> Pour une adresse IPv6<ul><li>FWP_V6_ADDR_MASK ou</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_ADDRESS"></span><span id="fwpm_condition_ip_remote_address"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS</strong></dt></dl> | Adresse IP distante. <br /><strong>Type de données :</strong> Pour une adresse IPv4<ul><li>FWP_V4_ADDR_MASK ou</li><li>FWP_UINT32</li></ul><br /><strong>Type de données :</strong> Pour une adresse IPv6<ul><li>FWP_V6_ADDR_MASK ou</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_SOURCE_ADDRESS"></span><span id="fwpm_condition_ip_source_address"></span><dl><dt><strong>FWPM_CONDITION_IP_SOURCE_ADDRESS</strong></dt></dl> | Adresse IP source pour les paquets transférés. <br /><strong>Type de données :</strong> Pour une adresse IPv4<ul><li>FWP_V4_ADDR_MASK ou</li><li>FWP_UINT32</li></ul><br /><strong>Type de données :</strong> Pour une adresse IPv6<ul><li>FWP_V6_ADDR_MASK ou</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS"></span><span id="fwpm_condition_ip_destination_address"></span><dl><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS</strong></dt></dl> | Adresse IP de destination pour les paquets transférés. <br /><strong>Type de données :</strong> Pour une adresse IPv4<ul><li>FWP_V4_ADDR_MASK ou</li><li>FWP_UINT32</li></ul><br /><strong>Type de données :</strong> Pour une adresse IPv6<ul><li>FWP_V6_ADDR_MASK ou</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_local_address_type"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_TYPE</strong></dt></dl> | Type d’adresse IP locale. <br /><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> suivantes.<ul><li>NlatUnspecified</li><li>NlatUnicast</li><li>NlatAnycast</li><li>NlatMulticast</li><li>NlatBroadcast</li></ul><br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE"></span><span id="fwpm_condition_ip_destination_address_type"></span><dl><dt><strong>FWPM_CONDITION_IP_DESTINATION_ADDRESS_TYPE</strong></dt></dl> | Type d’adresse IP de destination pour les paquets transférés. <br /><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> suivantes.<ul><li>NlatUnspecified</li><li>NlatUnicast</li><li>NlatAnycast</li><li>NlatMulticast</li><li>NlatBroadcast</li></ul><br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_INTERFACE"></span><span id="fwpm_condition_ip_local_interface"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_INTERFACE</strong></dt></dl> | LUID de l’interface réseau associée à l’adresse IP locale. <br /><strong>Type de données :</strong> FWP_UINT64<br /> | 
| <span id="FWPM_CONDITION_INTERFACE_TYPE"></span><span id="fwpm_condition_interface_type"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE_TYPE</strong></dt></dl> | Type d’interface défini par l’IANA (Internet Assigned Names Authority). Pour plus d’informations, consultez [https://www.iana.org/assignments/ianaiftype-mib](https://www.iana.org/assignments/ianaiftype-mib). <br /><strong>Valeurs possibles :</strong> Valeurs de type d’interface listées dans le fichier d’en-tête Ipifcons. h.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_TUNNEL_TYPE"></span><span id="fwpm_condition_tunnel_type"></span><dl><dt><strong>FWPM_CONDITION_TUNNEL_TYPE</strong></dt></dl> | Méthode d’encapsulation utilisée par un tunnel si le membre de type est IF_TYPE_TUNNEL. Le type de tunnel est défini par l’IANA (Internet Assigned Names Authority). Pour plus d’informations, consultez <a href="https://www.iana.org/assignments/ianaiftype-mib">https://www.iana.org/assignments/ianaiftype-mib</a>. <br /><strong>Valeurs possibles :</strong> TUNNEL_TYPE valeurs de type énumération figurant dans le fichier d’en-tête ifdef. h.<br /><strong>Type de données :</strong> FWP_UINT32 <br /> | 
| <span id="FWPM_CONDITION_IP_FORWARD_INTERFACE"></span><span id="fwpm_condition_ip_forward_interface"></span><dl><dt><strong>FWPM_CONDITION_IP_FORWARD_INTERFACE</strong></dt></dl> | LUID de l’interface réseau sur laquelle le paquet transféré doit être envoyé. <br /><strong>Type de données :</strong> FWP_UINT64<br /> | 
| <span id="FWPM_CONDITION_IP_PROTOCOL"></span><span id="fwpm_condition_ip_protocol"></span><dl><dt><strong>FWPM_CONDITION_IP_PROTOCOL</strong></dt></dl> | Numéro de protocole IP, tel que spécifié dans le document RFC 1700. <br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_PORT"></span><span id="fwpm_condition_ip_local_port"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_PORT</strong></dt></dl> | Numéro de port du protocole de transport local.<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_ICMP_TYPE"></span><span id="fwpm_condition_icmp_type"></span><dl><dt><strong>FWPM_CONDITION_ICMP_TYPE</strong></dt></dl> | Champ de type ICMP, tel que spécifié dans le document RFC 792. <br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_PORT"></span><span id="fwpm_condition_ip_remote_port"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_PORT</strong></dt></dl> | Numéro de port du protocole de transport distant. <br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_ICMP_CODE"></span><span id="fwpm_condition_icmp_code"></span><dl><dt><strong>FWPM_CONDITION_ICMP_CODE</strong></dt></dl> | Champ de code ICMP, tel que spécifié dans le document RFC 792. <br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE"></span><span id="fwpm_condition_embedded_local_address_type"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_ADDRESS_TYPE</strong></dt></dl> | Le type d’adresse IP locale qui est incorporé dans le paquet ICMP.<br /><strong>Valeurs possibles :</strong> L’une des valeurs d’énumération <a href="/windows/win32/api/nldef/ne-nldef-nl_address_type">NL_ADDRESS_TYPE</a> suivantes.<ul><li>NlatUnspecified</li><li>NlatUnicast</li><li>NlatAnycast</li><li>NlatMulticast</li><li>NlatBroadcast</li></ul><br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS"></span><span id="fwpm_condition_embedded_remote_address"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_ADDRESS</strong></dt></dl> | L’adresse IP distante qui est incorporée dans le paquet ICMP. <br /><strong>Type de données :</strong> Pour une adresse IPv4<ul><li>FWP_V4_ADDR_MASK ou</li><li>FWP_UINT32</li></ul><br /><strong>Type de données :</strong> Pour une adresse IPv6<ul><li>FWP_V6_ADDR_MASK ou</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_PROTOCOL"></span><span id="fwpm_condition_embedded_protocol"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_PROTOCOL</strong></dt></dl> | Numéro de protocole IP incorporé dans le paquet ICMP, tel que spécifié dans le document RFC 1700. <br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_LOCAL_PORT"></span><span id="fwpm_condition_embedded_local_port"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_LOCAL_PORT</strong></dt></dl> | Numéro de port du protocole de transport local qui est incorporé dans le paquet ICMP. <br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_EMBEDDED_REMOTE_PORT"></span><span id="fwpm_condition_embedded_remote_port"></span><dl><dt><strong>FWPM_CONDITION_EMBEDDED_REMOTE_PORT</strong></dt></dl> | Numéro de port du protocole de transport distant qui est incorporé dans le paquet ICMP. <br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_FLAGS"></span><span id="fwpm_condition_flags"></span><dl><dt><strong>FWPM_CONDITION_FLAGS</strong></dt></dl> | Or au niveau du bit d’une combinaison d’indicateurs de condition de filtrage. <br /><strong>Valeurs possibles :</strong> Voir <a href="filtering-condition-flags-.md"> <strong>indicateurs de condition de filtrage</strong></a><br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DIRECTION"></span><span id="fwpm_condition_direction"></span><dl><dt><strong>FWPM_CONDITION_DIRECTION</strong></dt></dl> | Direction du trafic ou du flux de données. <br /><strong>Valeurs possibles :  </strong><ul><li>FWP_DIRECTION_INBOUND</li><li>FWP_DIRECTION_OUTBOUND</li></ul><br /> Pour les couches de datagrammes (FWPM_LAYER_DATAGRAM_DATA_ *) et les couches de paquets de flux (FWPM_LAYER_STREAM_PACKET_*), la valeur sera la même que la direction du paquet. <br /> Pour les couches de flux (FWPM_LAYER_STREAM_ *) et les couches établies par flux (FWPM_LAYER_ALE_FLOW_ESTABLISHED_*), la valeur sera la même que la direction de la connexion. (Par exemple, lorsqu’une application locale initie la connexion, un paquet entrant a <strong>FWPM_CONDITION_DIRECTION</strong> défini sur <strong>FWP_DIRECTION_OUTBOUND</strong>.) <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_INTERFACE_INDEX"></span><span id="fwpm_condition_interface_index"></span><dl><dt><strong>FWPM_CONDITION_INTERFACE_INDEX</strong></dt></dl> | Index de l’interface réseau, tel qu’il est énuméré par la pile réseau. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_sub_interface_index"></span><dl><dt><strong>FWPM_CONDITION_SUB_INTERFACE_INDEX</strong></dt></dl> | Index de l’interface réseau logique, tel qu’il est énuméré par la pile réseau. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SOURCE_INTERFACE_INDEX"></span><span id="fwpm_condition_source_interface_index"></span><dl><dt><strong>FWPM_CONDITION_SOURCE_INTERFACE_INDEX</strong></dt></dl> | Index de l’interface réseau source pour les paquets transférés, tel qu’il est énuméré par la pile réseau.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_source_sub_interface_index"></span><dl><dt><strong>FWPM_CONDITION_SOURCE_SUB_INTERFACE_INDEX</strong></dt></dl> | Index de l’interface de réseau logique source pour les paquets transférés, tels qu’ils sont énumérés par la pile réseau. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DESTINATION_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_interface_index"></span><dl><dt><strong>FWPM_CONDITION_DESTINATION_INTERFACE_INDEX</strong></dt></dl> | Index de l’interface réseau de destination pour les paquets transférés, tel qu’il est énuméré par la pile réseau. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX"></span><span id="fwpm_condition_destination_sub_interface_index"></span><dl><dt><strong>FWPM_CONDITION_DESTINATION_SUB_INTERFACE_INDEX</strong></dt></dl> | Index de l’interface réseau logique de destination pour les paquets transférés, tel qu’il est énuméré par la pile réseau. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_ALE_APP_ID"></span><span id="fwpm_condition_ale_app_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_APP_ID</strong></dt></dl> | Le chemin d’accès complet de l’application, tel que retourné par la fonction <a href="/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmgetappidfromfilename0"><strong>FwpmGetAppIdFromFileName0</strong></a> . <br /> (Par exemple, « \device0\hardiskvolume1\Program Files\Application.exe ».)<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_USER_ID"></span><span id="fwpm_condition_ale_user_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_USER_ID</strong></dt></dl> | Identification de l’utilisateur local. <br /><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_REMOTE_USER_ID"></span><span id="fwpm_condition_ale_remote_user_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_REMOTE_USER_ID</strong></dt></dl> | Identification de l’utilisateur distant. <br /><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_REMOTE_MACHINE_ID"></span><span id="fwpm_condition_ale_remote_machine_id"></span><dl><dt><strong>FWPM_CONDITION_ALE_REMOTE_MACHINE_ID</strong></dt></dl> | Identification de l’ordinateur distant. <br /><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_ALE_PROMISCUOUS_MODE"></span><span id="fwpm_condition_ale_promiscuous_mode"></span><dl><dt><strong>FWPM_CONDITION_ALE_PROMISCUOUS_MODE</strong></dt></dl> | Mode de socket brut autorisé ou refusé.<br /><strong>Valeurs possibles :  </strong><ul><li>SIO_RCVALL</li><li>SIO_RCVALL_IGMPMCAST</li><li>SIO_RCVALL_MCAST</li></ul>Pour obtenir une description de ces modes de socket brut, consultez la fonction <a href="/windows/desktop/api/winsock2/nf-winsock2-wsaioctl"><strong>WSAIoctl</strong></a> .<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT"></span><span id="fwpm_condition_ale_sio_firewall_system_port"></span><dl><dt><strong>FWPM_CONDITION_ALE_SIO_FIREWALL_SYSTEM_PORT</strong></dt></dl> | Réservé à un usage interne. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_ALE_NAP_CONTEXT"></span><span id="fwpm_condition_ale_nap_context"></span><dl><dt><strong>FWPM_CONDITION_ALE_NAP_CONTEXT</strong></dt></dl> | Réservé à un usage interne. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 




Les constantes suivantes sont disponibles pour le mode utilisateur uniquement.



| conditions de mode utilisateur disponibles pour Windows 8 et Windows Server 2012                                                                                                                       | Description                                                                                                                                                               |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FWPM_CONDITION_QM_MODE"></span><span id="fwpm_condition_qm_mode"></span><dl> <dt>**\_ \_ mode QM de condition FWPM \_**</dt> </dl> | Mode du filtre en mode rapide (QM). Consultez [**\_ \_ type de trafic IPSec**](/windows/desktop/api/Ipsectypes/ne-ipsectypes-ipsec_traffic_type) pour connaître les valeurs possibles.<br/> **Type de données :** FWP \_ UInt32<br/> |






| conditions de mode utilisateur disponibles pour Windows 7, Windows Server 2008 R2 et versions ultérieures | Description | 
|---------------------------------------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_KM_AUTH_NAP_CONTEXT"></span><span id="fwpm_condition_km_auth_nap_context"></span><dl><dt><strong>FWPM_CONDITION_KM_AUTH_NAP_CONTEXT</strong></dt></dl> | Réservé à un usage interne.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_PEER_NAME"></span><span id="fwpm_condition_peer_name"></span><dl><dt><strong>FWPM_CONDITION_PEER_NAME</strong></dt></dl> | Nom de l’homologue. Par exemple, le nom DNS de l’homologue.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_REMOTE_ID"></span><span id="fwpm_condition_remote_id"></span><dl><dt><strong>FWPM_CONDITION_REMOTE_ID</strong></dt></dl> | Identité du principal d’authentification distant. <br /><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt></dl> | Type de méthode d’authentification IKE, IKEv2 ou AuthIP. <br /><strong>Type de données :</strong> IKEEXT_AUTHENTICATION_METHOD_TYPE<br /> | 
| <span id="FWPM_CONDITION_KM_TYPE"></span><span id="fwpm_condition_km_type"></span><dl><dt><strong>FWPM_CONDITION_KM_TYPE</strong></dt></dl> | Type de module de génération de clé.<br /><strong>Type de données :</strong> IKEEXT_KEY_MODULE_TYPE<br /> | 
| <span id="FWPM_CONDITION_KM_MODE"></span><span id="fwpm_condition_km_mode"></span><dl><dt><strong>FWPM_CONDITION_KM_MODE</strong></dt></dl> | Mode IPsec dans lequel un jeton peut être obtenu.<br /><strong>Type de données :</strong> IPSEC_TOKEN_MODE<br /> | 
| <span id="FWPM_CONDITION_IPSEC_POLICY_KEY"></span><span id="fwpm_condition_ipsec_policy_key"></span><dl><dt><strong>FWPM_CONDITION_IPSEC_POLICY_KEY</strong></dt></dl> | Clé de contexte du fournisseur de stratégie en mode principal (MM) ou en mode rapide (QM) de la SA qui est autorisée. Utile pour limiter l’étendue de la règle d’autorisation à la signature d’accès partagé à l’aide d’une clé de stratégie IPsec MM ou QM spécifiée.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_AUTHENTICATION_TYPE"></span><span id="fwpm_condition_authentication_type"></span><dl><dt><strong>FWPM_CONDITION_AUTHENTICATION_TYPE</strong></dt></dl> | Méthode utilisée pour authentifier l’Association de sécurité.<br /><blockquote>[!Note]<br />disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.</blockquote><br /><strong>Type de données :</strong> FWP_UINT32 <br /> | 







| constantes disponibles pour Windows Vista et versions ultérieures | Description | 
|-------------------------------------------------|-------------|
| <span id="FWPM_CONDITION_REMOTE_USER_TOKEN"></span><span id="fwpm_condition_remote_user_token"></span><dl><dt><strong>FWPM_CONDITION_REMOTE_USER_TOKEN</strong></dt></dl> | Identification de l’utilisateur distant.<br /><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_IF_UUID"></span><span id="fwpm_condition_rpc_if_uuid"></span><dl><dt><strong>FWPM_CONDITION_RPC_IF_UUID</strong></dt></dl> | UUID de l’interface RPC. <br /><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_IF_VERSION"></span><span id="fwpm_condition_rpc_if_version"></span><dl><dt><strong>FWPM_CONDITION_RPC_IF_VERSION</strong></dt></dl> | Version de l’interface RPC. <br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_RPC_IF_FLAG"></span><span id="fwpm_condition_rpc_if_flag"></span><dl><dt><strong>FWPM_CONDITION_RPC_IF_FLAG</strong></dt></dl> | Réservé à un usage interne. <br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_DCOM_APP_ID"></span><span id="fwpm_condition_dcom_app_id"></span><dl><dt><strong>FWPM_CONDITION_DCOM_APP_ID</strong></dt></dl> | Identification de l’application COM.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_IMAGE_NAME"></span><span id="fwpm_condition_image_name"></span><dl><dt><strong>FWPM_CONDITION_IMAGE_NAME</strong></dt></dl> | Le nom de l’application.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_PROTOCOL"></span><span id="fwpm_condition_rpc_protocol"></span><dl><dt><strong>FWPM_CONDITION_RPC_PROTOCOL</strong></dt></dl> | Protocole RPC. <br /><strong>Valeurs possibles :  </strong><ul><li>RPC_PROTSEQ_TCP</li><li>RPC_PROTSEQ_NMP</li><li>RPC_PROTSEQ_LRPC</li><li>RPC_PROTSEQ_HTTP</li></ul><br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_RPC_AUTH_TYPE"></span><span id="fwpm_condition_rpc_auth_type"></span><dl><dt><strong>FWPM_CONDITION_RPC_AUTH_TYPE</strong></dt></dl> | Type de service d’authentification. Pour plus d’informations sur les types de service d’authentification, consultez la page relative aux <a href="/windows/desktop/Rpc/authentication-service-constants"><strong>constantes de service d'</strong></a>authentification. <br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_RPC_AUTH_LEVEL"></span><span id="fwpm_condition_rpc_auth_level"></span><dl><dt><strong>FWPM_CONDITION_RPC_AUTH_LEVEL</strong></dt></dl> | Niveau du service d’authentification. Pour plus d’informations sur les niveaux de service d’authentification, consultez <a href="/windows/desktop/Rpc/authentication-level-constants"><strong>constantes au niveau de l’authentification</strong></a>. <br /><strong>Type de données :</strong> FWP_UINT8<br /> | 
| <span id="FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM"></span><span id="fwpm_condition_sec_encrypt_algorithm"></span><dl><dt><strong>FWPM_CONDITION_SEC_ENCRYPT_ALGORITHM</strong></dt></dl> | Algorithme de chiffrement SSPI (Security Service Provider Interface) basé sur les certificats.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_SEC_KEY_SIZE"></span><span id="fwpm_condition_sec_key_size"></span><dl><dt><strong>FWPM_CONDITION_SEC_KEY_SIZE</strong></dt></dl> | Taille de la clé de chiffrement SSPI basée sur le certificat.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V4"></span><span id="fwpm_condition_ip_local_address_v4"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V4</strong></dt></dl> | Adresse IPv4 locale. <br /><strong>Type de données :  </strong><ul><li>FWP_V4_ADDR_MASK ou</li><li>FWP_UINT32</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_LOCAL_ADDRESS_V6"></span><span id="fwpm_condition_ip_local_address_v6"></span><dl><dt><strong>FWPM_CONDITION_IP_LOCAL_ADDRESS_V6</strong></dt></dl> | Adresse IPv6 locale. <br /><strong>Type de données :  </strong><ul><li>FWP_V6_ADDR_MASK ou</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V4"></span><span id="fwpm_condition_ip_remote_address_v4"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V4</strong></dt></dl> | Adresse IPv4 distante. <br /><strong>Type de données :  </strong><ul><li>FWP_V4_ADDR_MASK ou</li><li>FWP_UINT32</li></ul><br /> | 
| <span id="FWPM_CONDITION_IP_REMOTE_ADDRESS_V6"></span><span id="fwpm_condition_ip_remote_address_v6"></span><dl><dt><strong>FWPM_CONDITION_IP_REMOTE_ADDRESS_V6</strong></dt></dl> | Adresse IPv6 distante. <br /><strong>Type de données :  </strong><ul><li>FWP_V6_ADDR_MASK ou</li><li>FWP_BYTE_ARRAY16_TYPE</li></ul><br /> | 
| <span id="FWPM_CONDITION_PIPE"></span><span id="fwpm_condition_pipe"></span><dl><dt><strong>FWPM_CONDITION_PIPE</strong></dt></dl> | Nom du canal nommé distant.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID"></span><span id="fwpm_condition_process_with_rpc_if_uuid"></span><dl><dt><strong>FWPM_CONDITION_PROCESS_WITH_RPC_IF_UUID</strong></dt></dl> | UUID du processus avec l’interface RPC.<br /><strong>Type de données :</strong> FWP_BYTE_ARRAY16_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_EP_VALUE"></span><span id="fwpm_condition_rpc_ep_value"></span><dl><dt><strong>FWPM_CONDITION_RPC_EP_VALUE</strong></dt></dl> | Réservé à un usage interne.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_EP_FLAGS"></span><span id="fwpm_condition_rpc_ep_flags"></span><dl><dt><strong>FWPM_CONDITION_RPC_EP_FLAGS</strong></dt></dl> | Réservé à un usage interne.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_CLIENT_TOKEN"></span><span id="fwpm_condition_client_token"></span><dl><dt><strong>FWPM_CONDITION_CLIENT_TOKEN</strong></dt></dl> | Identification du client lors de l’utilisation de RpcProxy.<br /><strong>Type de données :</strong> FWP_SECURITY_DESCRIPTOR_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_SERVER_NAME"></span><span id="fwpm_condition_rpc_server_name"></span><dl><dt><strong>FWPM_CONDITION_RPC_SERVER_NAME</strong></dt></dl> | Nom du serveur RPC lors de l’utilisation de RpcProxy.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_RPC_SERVER_PORT"></span><span id="fwpm_condition_rpc_server_port"></span><dl><dt><strong>FWPM_CONDITION_RPC_SERVER_PORT</strong></dt></dl> | Le port sur le serveur RPC lors de l’utilisation de RpcProxy.<br /><strong>Type de données :</strong> FWP_UINT16<br /> | 
| <span id="FWPM_CONDITION_RPC_PROXY_AUTH_TYPE"></span><span id="fwpm_condition_rpc_proxy_auth_type"></span><dl><dt><strong>FWPM_CONDITION_RPC_PROXY_AUTH_TYPE</strong></dt></dl> | Type de service d’authentification de proxy RPC.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH"></span><span id="fwpm_condition_client_cert_key_length"></span><dl><dt><strong>FWPM_CONDITION_CLIENT_CERT_KEY_LENGTH</strong></dt></dl> | Longueur de la clé SSL (Secure Socket Layer) dans le certificat client.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 
| <span id="FWPM_CONDITION_CLIENT_CERT_OID"></span><span id="fwpm_condition_client_cert_oid"></span><dl><dt><strong>FWPM_CONDITION_CLIENT_CERT_OID</strong></dt></dl> | Identificateur d’objet dans le certificat client.<br /><strong>Type de données :</strong> FWP_BYTE_BLOB_TYPE<br /> | 
| <span id="FWPM_CONDITION_NET_EVENT_TYPE"></span><span id="fwpm_condition_net_event_type"></span><dl><dt><strong>FWPM_CONDITION_NET_EVENT_TYPE</strong></dt></dl> | Type d’événement net.<br /><strong>Type de données :</strong> FWP_UINT32<br /> | 




## <a name="remarks"></a>Remarques

Lorsque les adresses IP sont stockées au \_ format fwp UInt32 ou lorsqu’un port IP est stocké au \_ format fwp UINT16, elles sont stockées dans l’ordre de l’hôte, et non dans l’ordre du réseau.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |
