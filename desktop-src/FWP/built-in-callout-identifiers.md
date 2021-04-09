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
# <a name="built-in-callout-identifiers"></a>Identificateurs de légende intégrés

Les identificateurs des fonctions de légende intégrées à la plateforme de filtrage Windows (WFP) sont chacun représentés par un GUID. Ces identificateurs sont définis comme suit.

Les suffixes V4 et V6 à la fin des identificateurs de légende indiquent si la légende est pour la pile réseau IPv4 ou pour la pile réseau IPv6.

<dl> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_inbound_transport_v4___fwpm_callout_ipsec_inbound_transport_v6_"></span>**FWPM \_ de \_ transport entrant IPSec \_ \_ \_ v4/FWPM \_ \_ \_ \_ \_ , appel de transport entrant IPSec V6** 
</dt> <dd> <dl> <dt>



Vérifie que chaque paquet reçu supposé arriver sur une association de sécurité en mode de transport arrive en toute sécurité.

Cette légende est applicable au niveau de la couche de transport.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TRANSPORT_V6_"></span><span id="fwpm_callout_ipsec_outbound_transport_v4___fwpm_callout_ipsec_outbound_transport_v6_"></span>**FWPM \_ de \_ \_ transport sortant IPSec \_ \_ v4/FWPM, \_ appel \_ \_ \_ \_ de transport sortant IPSec V6** 
</dt> <dd> <dl> <dt>



Indique à IPsec le trafic sortant qui doit être sécurisé via des associations de sécurité en mode de transport.

Cette légende est applicable au niveau de la couche de transport.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_inbound_tunnel_v4___fwpm_callout_ipsec_inbound_tunnel_v6_"></span>**FWPM \_ \_ tunnel entrant IPSec \_ \_ \_ v4/FWPM appel tunnel \_ \_ entrant IPSec \_ \_ \_ V6** 
</dt> <dd> <dl> <dt>



Vérifie que chaque paquet reçu supposé arriver sur une association de sécurité en mode de tunnel arrive en toute sécurité.

Cette légende est applicable au niveau de la couche de transport.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_OUTBOUND_TUNNEL_V6_"></span><span id="fwpm_callout_ipsec_outbound_tunnel_v4___fwpm_callout_ipsec_outbound_tunnel_v6_"></span>**\_Appel FWPM \_ \_ tunnel sortant IPSec \_ \_ v4/FWPM appel tunnel \_ \_ \_ sortant IPSec \_ \_ V6** 
</dt> <dd> <dl> <dt>



Indique à IPsec le trafic sortant qui doit être sécurisé par rapport aux associations de sécurité en mode tunnel.

Cette légende est applicable au niveau de la couche de transport.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_INBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_inbound_tunnel_v4___fwpm_callout_ipsec_forward_inbound_tunnel_v6"></span>**FWPM \_ appel \_ IPSec \_ Forward \_ entrant \_ tunnel \_ v4/FWPM \_ appel du \_ \_ tunnel entrant de transfert IPSec \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Vérifie que chaque paquet reçu supposé arriver sur une association de sécurité en mode de tunnel arrive en toute sécurité.

Cette légende est applicable au niveau de la couche de transfert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V4___FWPM_CALLOUT_IPSEC_FORWARD_OUTBOUND_TUNNEL_V6"></span><span id="fwpm_callout_ipsec_forward_outbound_tunnel_v4___fwpm_callout_ipsec_forward_outbound_tunnel_v6"></span>**\_Appel du \_ tunnel sortant IPSec de \_ \_ tunnel sortant FWPM \_ \_ v4/FWPM, \_ appel de \_ \_ tunnel sortant en aval IPSec \_ \_ \_ V6**
</dt> <dd> <dl> <dt>



Indique à IPsec le trafic sortant qui doit être sécurisé via une association de sécurité en mode tunnel.

Cette légende est applicable au niveau de la couche de transfert.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V4___FWPM_CALLOUT_IPSEC_INBOUND_INITIATE_SECURE_V6_"></span><span id="fwpm_callout_ipsec_inbound_initiate_secure_v4___fwpm_callout_ipsec_inbound_initiate_secure_v6_"></span>**FWPM d' \_ appel \_ IPSec \_ entrant \_ initiate \_ Secure \_ v4/FWPM, \_ appel de \_ \_ \_ \_ Secure \_ V6 sécurisé** 
</dt> <dd> <dl> <dt>



Vérifie que chaque connexion entrante censée arriver en sécurité arrive en toute sécurité.

Cette légende s’applique à la couche d’acceptation ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V4___FWPM_CALLOUT_IPSEC_INBOUND_TUNNEL_ALE_ACCEPT_V6"></span><span id="fwpm_callout_ipsec_inbound_tunnel_ale_accept_v4___fwpm_callout_ipsec_inbound_tunnel_ale_accept_v6"></span>**FWPM \_ appel \_ IPSec de \_ \_ tunnel entrant \_ ALE \_ accepter \_ v4/FWPM \_ appel \_ du \_ tunnel entrant \_ ALE \_ - \_ accepter \_ V6**
</dt> <dd> <dl> <dt>



Autorise les paquets IP en mode de tunnel IPsec lorsqu’ils sont classés au niveau de la couche d’acceptation ALE.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_ALE_CONNECT_V4___FWPM_CALLOUT_IPSEC_ALE_CONNECT_V6"></span><span id="fwpm_callout_ipsec_ale_connect_v4___fwpm_callout_ipsec_ale_connect_v6"></span>**FWPM d' \_ appel \_ IPSec \_ ALE \_ Connect \_ v4/FWPM, \_ appel \_ \_ \_ \_ V6 de connexion ALE IPSec**
</dt> <dd> <dl> <dt>



Applique les modificateurs de stratégie IPsec aux applications clientes.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V4___FWPM_CALLOUT_IPSEC_DOSP_FORWARD_V6"></span><span id="fwpm_callout_ipsec_dosp_forward_v4___fwpm_callout_ipsec_dosp_forward_v6"></span>**Appel \_ FWPM \_ \_ DOSP \_ \_ v4/FWPM \_ \_ \_ \_ \_ de l’appel de la sortie de la sortie d’IPSec DOSP de la sortie V6**
</dt> <dd> <dl> <dt>



Signale à la protection DoS IPsec que le trafic doit être vérifié pour les attaques potentielles et peut nécessiter un débit limité.

> [!Note]  
> Disponible uniquement dans Windows 7 et Windows Server 2008 R2.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V4_SILENT_DROP___FWPM_CALLOUT_WFP_TRANSPORT_LAYER_V6_SILENT_DROP"></span><span id="fwpm_callout_wfp_transport_layer_v4_silent_drop___fwpm_callout_wfp_transport_layer_v6_silent_drop"></span>**FWPM \_ légende de la \_ couche de \_ transport WFP \_ \_ \_ \_ -suppression silencieuse/FWPM \_ légende mode \_ \_ \_ \_ \_ silencieux \_ de la couche de transport**
</dt> <dd> <dl> <dt>



Implémente le filtrage en mode furtif en supprimant silencieusement tous les paquets entrants pour lesquels TCP n’a pas de point de terminaison d’écoute.

Cette légende s’applique à la couche rejet de transport entrant.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_connect_layer_v4___fwpm_callout_tcp_chimney_connect_layer_v6"></span>**FWPM de connexion \_ \_ TCP \_ Chimney de \_ \_ couche \_ v4/FWPM, appel de couche \_ \_ V6 de connexion TCP \_ Chimney \_ \_ \_**
</dt> <dd> <dl> <dt>



Active ou désactive le déchargement TCP Chimney pour chaque connexion sortante.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_CHIMNEY_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_chimney_accept_layer_v4___fwpm_callout_tcp_chimney_accept_layer_v6"></span>**FWPM \_ de \_ protocole TCP \_ Chimney \_ Accept \_ couche \_ v4/FWPM avec appel de \_ \_ \_ \_ couche accepter la \_ couche \_ V6**
</dt> <dd> <dl> <dt>



Active ou désactive le déchargement TCP Chimney pour chaque connexion entrante.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_connect_layer_v4___fwpm_callout_set_options_auth_connect_layer_v6"></span>**FWPM \_ Callout \_ Set \_ options \_ Set \_ Connect \_ couche \_ v4/FWPM \_ appel \_ Set \_ options \_ Set \_ Connect \_ couche \_ V6**
</dt> <dd> <dl> <dt>



Définit les options de classification sur les flux sortants.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V4___FWPM_CALLOUT_SET_OPTIONS_AUTH_RECV_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_set_options_auth_recv_accept_layer_v4___fwpm_callout_set_options_auth_recv_accept_layer_v6"></span>**FWPM \_ Callout \_ Set \_ options \_ d' \_ authentification \_ recevoir accepter \_ couche \_ v4/FWPM \_ appel des \_ options SET \_ \_ autorisation \_ recv \_ accepter \_ couche \_ V6**
</dt> <dd> <dl> <dt>



Définit les options de classification sur les flux entrants.

> [!Note]  
> Disponible uniquement dans Windows 8 et Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V4___FWPM_CALLOUT_RESERVED_AUTH_CONNECT_LAYER_V6"></span><span id="fwpm_callout_reserved_auth_connect_layer_v4___fwpm_callout_reserved_auth_connect_layer_v6"></span>**FWPM de la couche connexion \_ \_ auth Connect réservée \_ \_ \_ v4/FWPM, appel de la couche d’authentification \_ \_ \_ réservée \_ auth \_ Connect \_ \_**
</dt> <dd> <dl> <dt>



Cet identificateur est réservé à un usage interne.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V6___FWPM_CALLOUT_TEREDO_ALE_LISTEN_V6"></span><span id="fwpm_callout_edge_traversal_ale_listen_v6___fwpm_callout_teredo_ale_listen_v6"></span>**FWPM de l' \_ \_ \_ écoute ALE Traversal d' \_ écoute ALE de l' \_ écoute ALE/FWPM, légende de l' \_ \_ \_ \_ écoute ALE de TEREDO ALE \_ \_**
</dt> <dd> <dl> <dt>



Signale au service Teredo qu’une application requiert une adresse Teredo.

> [!Note]  
> Pour Windows 7 et les versions ultérieures, utilisez la **FWPM d' \_ \_ \_ \_ \_ écoute \_ ALE Traversal de traversée** de la légende.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V6___FWPM_CALLOUT_TEREDO_ALE_RESOURCE_ASSIGNMENT_V6"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v6___fwpm_callout_teredo_ale_resource_assignment_v6"></span>**\_Assignation de \_ \_ ressource ALE Traversal de l' \_ \_ affectation de ressources ALE \_ \_ \_ \_ \_ \_ \_ \_ FWPM**
</dt> <dd> <dl> <dt>



Signale au service Teredo qu’une application requiert une adresse Teredo.

> [!Note]  
> Pour Windows 7 et les versions ultérieures, utilisez la version d' **\_ affectation de \_ \_ \_ ressources ALE Traversal \_ \_ \_ de l’appel Edge FWPM V6**.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_RESOURCE_ASSIGNMENT_V4_"></span><span id="fwpm_callout_edge_traversal_ale_resource_assignment_v4_"></span>**FWPM de l' \_ \_ \_ affectation de \_ ressources ALE Traversal \_ de \_ l' \_ appel Edge** 
</dt> <dd> <dl> <dt>



Cet identificateur est réservé à une utilisation ultérieure.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_EDGE_TRAVERSAL_ALE_LISTEN_V4"></span><span id="fwpm_callout_edge_traversal_ale_listen_v4"></span>**\_V4 d' \_ \_ \_ écoute ALE TRAVERSée \_ de l’FWPM de la \_ légende**
</dt> <dd> <dl> <dt>



Cet identificateur est réservé à une utilisation ultérieure.


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_CONNECT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_connect_layer_v4___fwpm_callout_tcp_templates_connect_layer_v6"></span>**FWPM \_ appels \_ TCP \_ modèles \_ TCP \_ \_ v4 couche v4/FWPM appel de la \_ \_ \_ \_ \_ couche \_ V6 de connexion**
</dt> <dd> <dl> <dt>



Applique les paramètres de modèle TCP pour les connexions sortantes correspondantes.

> [!Note]  
> Disponible uniquement dans Windows 8 et Windows Server 2012.

 


</dt> </dl> </dd> <dt>

<span id="FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V4___FWPM_CALLOUT_TCP_TEMPLATES_ACCEPT_LAYER_V6"></span><span id="fwpm_callout_tcp_templates_accept_layer_v4___fwpm_callout_tcp_templates_accept_layer_v6"></span>**FWPM \_ de \_ modèles TCP Accept de la \_ \_ \_ couche \_ v4/FWPM appel \_ \_ \_ \_ \_ \_ de la couche accepter la couche V6**
</dt> <dd> <dl> <dt>



Applique les paramètres de modèle TCP pour les connexions entrantes correspondantes.

> [!Note]  
> Disponible uniquement dans Windows 8 et Windows Server 2012.

 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



 

 





