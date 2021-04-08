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
# <a name="filtering-condition-flags"></a>Indicateurs de condition de filtrage

Les indicateurs de condition de filtrage de la plateforme de filtrage Windows (WFP) sont tous représentés par un champ de champ.

Ces indicateurs et les couches de filtrage dans lesquelles ils peuvent être utilisés sont définis comme suit.

<dl> <dt>

<span id="FWP_CONDITION_FLAG_IS_LOOPBACK"></span><span id="fwp_condition_flag_is_loopback"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ loopback**
</dt> <dd> <dl> <dt>



Teste si le trafic réseau est en boucle.

Filtrage des couches :

-   \_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}
-   \_Couche FWPM \_ sortante \_ IPPACKET \_ V {4 \| 6}
-   \_Transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6}
-   \_Transport sortant de la couche FWPM \_ \_ \_ V {4 \| 6}
-   \_Flux de couche FWPM \_ \_ {v4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     

-   \_Couche FWPM \_ \_ erreur ICMP entrante \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     

-   \_Erreur ICMP sortie de la couche FWPM \_ \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     

-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     

-   FWPM \_ de \_ couche \_ ALE \_ établi \_ V {4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_SECURED"></span><span id="fwp_condition_flag_is_ipsec_secured"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ sécurisé par IPSec \_**
</dt> <dd> <dl> <dt>



Teste si le trafic réseau est protégé par IPsec.

Filtrage des couches :

-   \_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}
-   \_Transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REAUTHORIZE"></span><span id="fwp_condition_flag_is_reauthorize"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ Reauthorize**
</dt> <dd> <dl> <dt>



Teste une modification de stratégie au lieu d’une nouvelle connexion.

Filtrage des couches :

-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_WILDCARD_BIND"></span><span id="fwp_condition_flag_is_wildcard_bind"></span>**l' \_ indicateur de condition fwp \_ est une liaison de \_ \_ caractères génériques \_**
</dt> <dd> <dl> <dt>



Teste si l’application a spécifié une adresse générique lors de la liaison à une adresse de réseau local.

Couche de filtrage :

-   \_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RAW_ENDPOINT"></span><span id="fwp_condition_flag_is_raw_endpoint"></span>**l' \_ indicateur de condition fwp \_ est un point de \_ \_ \_ terminaison brut**
</dt> <dd> <dl> <dt>



Teste si le point de terminaison local qui envoie et reçoit le trafic est un point de terminaison brut.

Filtrage des couches :

-   \_Transport entrant de la couche FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     

-   \_Transport sortant de la couche FWPM \_ \_ \_ V {4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     

-   Données de datagramme de la \_ couche FWPM \_ \_ \_ {v4 \| 6}
    > [!Note]  
    > Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

     

-   \_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT"></span><span id="fwp_condition_flag_is_fragment"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ fragment**
</dt> <dd> <dl> <dt>



Teste si la \_ structure de liste de mémoires tampons nette \_ transmise à un pilote de légende est un fragment de paquet IP.

Filtrage des couches :

-   \_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}
-   FWPM \_ couche \_ entrante \_ IPPACKET \_ V {4 \| 6} \_ Ignorer


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_FRAGMENT_GROUP"></span><span id="fwp_condition_flag_is_fragment_group"></span>**l' \_ indicateur de condition fwp \_ est un groupe de \_ \_ fragments \_**
</dt> <dd> <dl> <dt>



Teste si la \_ \_ structure de liste de mémoires TAMPONs nette transmise à un pilote de légende décrit une liste liée de fragments de paquets.

Couche de filtrage :

-   FWPM \_ couche \_ IPFORWARD \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IPSEC_NATT_RECLASSIFY"></span><span id="fwp_condition_flag_is_ipsec_natt_reclassify"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ \_ \_ reclassifier IPSec Natt**
</dt> <dd> <dl> <dt>



Indique que le même paquet est reclassifié au niveau de la couche de transport, lorsque le shim NAT IPsec traduit la valeur du port distant.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_REQUIRES_ALE_CLASSIFY"></span><span id="fwp_condition_flag_requires_ale_classify"></span>**l' \_ indicateur de condition fwp \_ requiert une \_ \_ \_ classification ALE**
</dt> <dd> <dl> <dt>



Indique que le paquet sera reclassé au niveau de la couche de réception/acceptation ALE.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_IMPLICIT_BIND"></span><span id="fwp_condition_flag_is_implicit_bind"></span>**l' \_ indicateur de condition fwp \_ est une \_ \_ liaison implicite \_**
</dt> <dd> <dl> <dt>



Teste si Windows Sockets effectue une liaison implicite.

Disponible uniquement sur Windows Vista et Windows Server 2008.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_REASSEMBLED"></span><span id="fwp_condition_flag_is_reassembled"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ réassemblé**
</dt> <dd> <dl> <dt>



Teste si le paquet a été réassemblé.

> [!Note]  
> Disponible uniquement sur Windows Server 2008, Windows Vista avec SP1 et versions ultérieures.

 

Couche de filtrage :

-   \_Couche FWPM \_ entrée \_ IPPACKET \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NAME_APP_SPECIFIED"></span><span id="fwp_condition_flag_is_name_app_specified"></span>**l' \_ indicateur de condition fwp \_ est l’application de \_ \_ nom \_ \_ spécifiée**
</dt> <dd> <dl> <dt>



Teste si le nom de l’ordinateur homologue auquel l’application s’attend à se connecter a été reçu via une API telle que [**WSASetSocketPeerTargetName**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) et n’est pas obtenue via les heuristiques de mise en cache.

> [!Note]  
> Disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.

 

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROMISCUOUS"></span><span id="fwp_condition_flag_is_promiscuous"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ promiscuité**
</dt> <dd> <dl> <dt>



Réservé.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_AUTH_FW"></span><span id="fwp_condition_flag_is_auth_fw"></span>**l' \_ indicateur de condition fwp \_ est le \_ \_ \_ FW auth**
</dt> <dd> <dl> <dt>



Teste si la connexion est authentifiée de bout en bout, même si les paquets individuels n’ont pas été vérifiés.

> [!Note]  
> Disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.

 

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RECLASSIFY"></span><span id="fwp_condition_flag_is_reclassify"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ reclassifier**
</dt> <dd> <dl> <dt>



Teste si le moteur de filtrage reclasse une demande de liaison ou d’écoute précédente.

> [!Note]  
> Disponible uniquement sur Windows Server 2008 R2, Windows 7 et versions ultérieures.

 

Couche de filtrage :

-   Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}
-   \_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_PROXY_CONNECTION"></span><span id="fwp_condition_flag_is_proxy_connection"></span>**l' \_ indicateur de condition fwp \_ est une \_ \_ \_ connexion proxy**
</dt> <dd> <dl> <dt>



Teste si la connexion utilise un proxy.

> [!Note]  
> Disponible uniquement sur Windows 8 et Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_appcontainer_loopback"></span>**l' \_ indicateur de condition fwp \_ est un \_ \_ \_ bouclage APPCONTAINER**
</dt> <dd> <dl> <dt>



Teste si le trafic réseau est un trafic de bouclage de conteneur d’application.

> [!Note]  
> Disponible uniquement sur Windows 8 et Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_NON_APPCONTAINER_LOOPBACK"></span><span id="fwp_condition_flag_is_non_appcontainer_loopback"></span>**l' \_ indicateur de condition fwp \_ est un \_ \_ \_ bouclage non APPCONTAINER \_**
</dt> <dd> <dl> <dt>



Teste si le trafic réseau est un trafic de bouclage de conteneur non-App.

> [!Note]  
> Disponible uniquement sur Windows 8 et Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_RESERVED"></span><span id="fwp_condition_flag_is_reserved"></span>**l' \_ indicateur de condition fwp \_ \_ est \_ réservé**
</dt> <dd> <dl> <dt>



Réservé.


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_FLAG_IS_HONORING_POLICY_AUTHORIZE"></span><span id="fwp_condition_flag_is_honoring_policy_authorize"></span>**l’indicateur de condition FWP respecte l' \_ \_ \_ autorisation de \_ \_ stratégie \_**
</dt> <dd> <dl> <dt>



Indique que la classification en cours est en cours d’exécution pour honorer l’intention d’une application du Windows Store redirigée pour se connecter à un ordinateur hôte spécifié. Une telle classification contient les mêmes valeurs de champ de classement que si l’application n’a jamais été redirigée. L’indicateur indique également qu’une classification future sera appelée pour correspondre à la destination redirigée effective. Si l’application est redirigée vers un service proxy pour inspection, cela signifie également qu’une classification future sera appelée sur la connexion proxy. Les pilotes de légende doivent généralement autoriser cette classification.

> [!Note]  
> Disponible uniquement sur Windows 8 et Windows Server 2012.

 

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Les indicateurs suivants spécifient la raison de la réautorisation d’une connexion précédemment autorisée. Ces indicateurs et les couches de filtrage dans lesquelles ils peuvent être utilisés sont définis comme suit.

> [!Note]  
> Ces conditions de filtrage sont uniquement disponibles sur Windows Server 2008 R2, Windows 7 et versions ultérieures.

 

<dl> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_POLICY_CHANGE"></span><span id="fwp_condition_reauthorize_reason_policy_change"></span>**CONDITION FWP-autoriser la modification de la \_ \_ \_ stratégie de motif \_ \_**
</dt> <dd> <dl> <dt>



Indique que la connexion a été réautorisée en raison de l’ajout ou de la suppression de filtres.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_ARRIVAL_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_arrival_interface"></span>**\_condition fwp \_ réautoriser la \_ raison \_ de la nouvelle \_ interface d’arrivée \_**
</dt> <dd> <dl> <dt>



Indique que le paquet est arrivé à partir d’une interface inconnue.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_NEXTHOP_INTERFACE"></span><span id="fwp_condition_reauthorize_reason_new_nexthop_interface"></span>**\_condition fwp \_ réautoriser la \_ raison \_ de la nouvelle \_ \_ interface NEXTHOP**
</dt> <dd> <dl> <dt>



Indique que le paquet sera en cours de départiment d’une interface inconnue.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_PROFILE_CROSSING"></span><span id="fwp_condition_reauthorize_reason_profile_crossing"></span>**\_condition fwp \_ réautoriser le \_ \_ franchissement du profil \_**
</dt> <dd> <dl> <dt>



Indique que le paquet est passé par les interfaces de plusieurs catégories réseau.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_CLASSIFY_COMPLETION"></span><span id="fwp_condition_reauthorize_reason_classify_completion"></span>**\_condition fwp \_ réautoriser le \_ motif de la \_ \_ fin de la classification**
</dt> <dd> <dl> <dt>



Indique qu’une connexion précédemment maintenue est maintenant autorisée à se terminer.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_IPSEC_PROPERTIES_CHANGED"></span><span id="fwp_condition_reauthorize_reason_ipsec_properties_changed"></span>**\_condition fwp \_ réautoriser la \_ raison pour laquelle les \_ \_ Propriétés IPSec \_ ont changé**
</dt> <dd> <dl> <dt>



Indique que les propriétés IPsec ont changé, ou que la connexion est passée d’un texte en clair à une connexion sécurisée.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_MID_STREAM_INSPECTION"></span><span id="fwp_condition_reauthorize_reason_mid_stream_inspection"></span>**\_condition fwp \_ réautoriser raison de l' \_ inspection du \_ \_ flux moyen \_**
</dt> <dd> <dl> <dt>



Indique qu’une connexion TCP précédemment établie est actuellement en cours d’inspection.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_SOCKET_PROPERTY_CHANGED"></span><span id="fwp_condition_reauthorize_reason_socket_property_changed"></span>**\_condition fwp \_ réautoriser la \_ raison pour laquelle la \_ propriété de socket \_ \_ a changé**
</dt> <dd> <dl> <dt>



Indique que les propriétés de socket ont été définies après l’autorisation et l’établissement d’une connexion.

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de couche ALE \_ \_ \_ V {4 \| 6}
-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_REAUTHORIZE_REASON_NEW_INBOUND_MCAST_BCAST_PACKET"></span><span id="fwp_condition_reauthorize_reason_new_inbound_mcast_bcast_packet"></span>**\_condition fwp \_ réautoriser la \_ raison du \_ nouveau \_ \_ \_ \_ paquet Bcast de trafic entrant**
</dt> <dd> <dl> <dt>



Indique que les nouveaux paquets de multidiffusion ou de diffusion entrants sont à nouveau autorisés au niveau des \_ appels de réception ALE \_ .

Couche de filtrage :

-   FWPM \_ d' \_ authentification ALE de la couche ALE \_ \_ reçues \_ accepter \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Les indicateurs suivants spécifient les propriétés de socket qui sont liées au fait qu’une application souhaite recevoir le trafic de traversée latérale. Ces indicateurs et les couches de filtrage dans lesquelles ils peuvent être utilisés sont définis comme suit.

> [!Note]  
> Ces conditions de filtrage sont uniquement disponibles sur Windows Server 2008 R2, Windows 7 et versions ultérieures.

 

<dl> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_IS_SYSTEM_PORT_RPC"></span><span id="fwp_condition_socket_property_flag_is_system_port_rpc"></span>**l' \_ indicateur de propriété de socket de condition fwp \_ est le \_ \_ \_ \_ \_ port système \_ RPC**
</dt> <dd> <dl> <dt>



Indique que l’application communique avec un port RPC dynamique.

Couche de filtrage :

-   Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}
-   \_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_ALLOW_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_allow_edge_traffic"></span>**\_indicateur de propriété de socket de condition fwp \_ \_ \_ \_ autoriser \_ \_ le trafic Edge**
</dt> <dd> <dl> <dt>



Indique que l’application souhaite recevoir le trafic spécifique à la traversée latérale.

Couche de filtrage :

-   Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}
-   \_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_SOCKET_PROPERTY_FLAG_DENY_EDGE_TRAFFIC"></span><span id="fwp_condition_socket_property_flag_deny_edge_traffic"></span>**\_indicateur de propriété de socket de condition fwp \_ \_ \_ \_ refuser \_ \_ le trafic de périphérie**
</dt> <dd> <dl> <dt>



Indique que l’application ne souhaite pas recevoir ou traiter le trafic spécifique à travers la périphérie.

Couche de filtrage :

-   Écoute de l' \_ écoute d’authentification ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}
-   \_Attribution de ressources ALE de la couche FWPM \_ \_ \_ \_ V {4 \| 6}


</dt> </dl> </dd> </dl>

Les indicateurs suivants spécifient les détails de connexion relatifs au filtrage L2.

> [!Note]  
> Ces conditions de filtrage sont uniquement disponibles sur Windows 8 et Windows Server 2012.

 

<dl> <dt>

<span id="FWP_CONDITION_L2_IS_NATIVE_ETHERNET"></span><span id="fwp_condition_l2_is_native_ethernet"></span>**La \_ condition fwp \_ L2 \_ est \_ native \_ Ethernet**
</dt> <dd> <dl> <dt>



Indique que la connexion est native Ethernet.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI"></span><span id="fwp_condition_l2_is_wifi"></span>**La \_ condition fwp \_ L2 \_ est \_ WiFi**
</dt> <dd> <dl> <dt>



Indique que la connexion est Wi-Fi.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MOBILE_BROADBAND"></span><span id="fwp_condition_l2_is_mobile_broadband"></span>**La \_ condition fwp \_ L2 \_ est \_ Mobile \_ Broadband**
</dt> <dd> <dl> <dt>



Indique que la connexion est de haut débit mobile.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_WIFI_DIRECT_DATA"></span><span id="fwp_condition_l2_is_wifi_direct_data"></span>**\_La condition fwp \_ L2 \_ est \_ WiFi \_ direct \_ Data**
</dt> <dd> <dl> <dt>



Indique que la connexion est Wi-Fi directe.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_VM2VM"></span><span id="fwp_condition_l2_is_vm2vm"></span>**La \_ condition fwp \_ L2 \_ est \_ VM2VM**
</dt> <dd> <dl> <dt>



Indique que la connexion se fait entre des machines virtuelles.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_MALFORMED_PACKET"></span><span id="fwp_condition_l2_is_malformed_packet"></span>**La \_ condition fwp \_ L2 \_ est un \_ paquet mal formé \_**
</dt> <dd> <dl> <dt>



Indique qu’un paquet semble incorrect.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IS_IP_FRAGMENT_GROUP"></span><span id="fwp_condition_l2_is_ip_fragment_group"></span>**La \_ condition fwp \_ L2 \_ est un \_ \_ groupe de fragments IP \_**
</dt> <dd> <dl> <dt>



Indique un groupe de fragments de paquets IP.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> <dt>

<span id="FWP_CONDITION_L2_IF_CONNECTOR_PRESENT"></span><span id="fwp_condition_l2_if_connector_present"></span>**\_Condition fwp \_ L2 \_ si le \_ connecteur est \_ présent**
</dt> <dd> <dl> <dt>



Indique qu’un connecteur est présent.

Couche de filtrage :

-   couche FWPM de \_ \_ \_ TRAMe Mac entrante \_ \_ Ethernet
-   couche FWPM- \_ \_ \_ Frame Mac \_ entrant \_ natif
-   couche FWPM de \_ \_ \_ \_ trame Mac sortante de la couche \_
-   \_ \_ trame Mac sortante de la couche FWPM \_ \_ \_ Native


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Fwptypes. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Filtrage des identificateurs de couche**](management-filtering-layer-identifiers-.md)
</dt> </dl>

 

