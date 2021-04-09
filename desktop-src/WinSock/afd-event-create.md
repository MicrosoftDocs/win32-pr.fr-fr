---
description: Événement de traçage réseau Winsock pour une opération de création de Socket.
ms.assetid: 59B9A570-5AEC-429D-AF71-AB6D8325C341
title: Événement AFD_EVENT_CREATE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CREATE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 3216e1adccca6c7c7d64a22f77babe3cbb699c05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862597"
---
# <a name="afd_event_create-event"></a>Événement de création d' \_ événement AFD \_

L’événement de **\_ \_ création d’événement AFD** est un événement de traçage réseau Winsock pour une opération de création de Socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CREATE = {0x3e8, 0x0, 0x10, 0x4, 0xa, 0x3e8, 0x8000000000000004};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informations sur cet événement.

Le tableau suivant répertorie les valeurs possibles pour le paramètre *EnterExit* :



| Valeur                                                                        | Signification                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Début d’une demande Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | La demande Winsock est terminée.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Le pilote AFD Winsock a effectué une action interne (en abandonnant une connexion, par exemple).<br/>      |
| <dl> <dt>3</dt> </dl> | Le pilote TCP/IP a entraîné l’apparition de cet événement. Cela indique généralement une notification de données.<br/> |
| <dl> <dt>4</dt> </dl> | Le pilote AFD Winsock a entraîné l’apparition de cet événement (par exemple, la définition d’une option de socket).<br/> |



 

</dd> <dt>

*Lieu* 
</dt> <dd>

Champ privé utilisé en interne.

</dd> <dt>

*Processus* 
</dt> <dd>

Adresse [EPROCESS](/windows-hardware/drivers/kernel/eprocess) du processus qui possède le socket associé. Il s’agit d’une structure opaque qui sert d’objet de processus pour un processus. Pour plus d’informations, consultez la documentation du kit de pilotes Windows pour la structure [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Point de terminaison* 
</dt> <dd>

\_Adresse du point de terminaison AFD du Socket.

</dd> <dt>

*AddressFamily* 
</dt> <dd>

Spécification de la famille d’adresses pour le Socket. Les valeurs possibles pour la famille d’adresses sont définies dans le fichier d’en-tête *Ws2def. h* . Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.

Les valeurs actuellement prises en charge sont AF \_ inet ou AF \_ inet6, qui sont les formats de famille d’adresses Internet pour IPv4 et IPv6. D’autres options pour la famille d’adresses (AF \_ NetBIOS pour une utilisation avec NetBIOS, par exemple) sont prises en charge si un fournisseur de services Windows Sockets pour la famille d’adresses est installé.

Le tableau ci-dessous répertorie les valeurs courantes pour la famille d’adresses, même si de nombreuses autres valeurs sont possibles.



| AF                                                                                                                                                                                                                 | Signification                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AF_UNSPEC"></span><span id="af_unspec"></span><dl> <dt>**AF \_ Inspec**</dt> <dt>0</dt> </dl>           | La famille d’adresses n’est pas spécifiée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_ INET**</dt> <dt>2</dt> </dl>                 | Famille d’adresses IPv4 (Internet Protocol version 4).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IPX"></span><span id="af_ipx"></span><dl> <dt>**AF \_ IPX**</dt> <dt>6</dt> </dl>                    | Famille d’adresses IPX/SPX. Cette famille d’adresses est uniquement prise en charge si le protocole de transport NWLink IPX/SPX NetBIOS compatible est installé. <br/> Cette famille d’adresses n’est pas prise en charge sur Windows Vista et versions ultérieures.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_APPLETALK"></span><span id="af_appletalk"></span><dl> <dt>**AF \_ APPLETALK**</dt> <dt>16</dt> </dl> | Famille d’adresses AppleTalk. Cette famille d’adresses est uniquement prise en charge si le protocole AppleTalk est installé. <br/> Cette famille d’adresses n’est pas prise en charge sur Windows Vista et versions ultérieures.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="AF_NETBIOS"></span><span id="af_netbios"></span><dl> <dt>**AF \_ NETBIOS**</dt> <dt>17</dt> </dl>       | Famille d’adresses NetBIOS. Cette famille d’adresses est uniquement prise en charge si le fournisseur Windows Sockets pour NetBIOS est installé. <br/> Le fournisseur Windows Sockets pour NetBIOS est pris en charge sur les versions 32 bits de Windows. Ce fournisseur est installé par défaut sur les versions 32 bits de Windows. <br/> Le fournisseur Windows Sockets pour NetBIOS n’est pas pris en charge sur les versions 64 bits de Windows. <br/> Le fournisseur Windows Sockets pour NetBIOS prend en charge uniquement les sockets où le paramètre de *type* est défini sur **chaussette \_ DGRAM**.<br/> Le fournisseur Windows Sockets pour NetBIOS n’est pas directement lié à l’interface de programmation [NetBIOS](/previous-versions/windows/desktop/netbios/portal) . L’interface de programmation NetBIOS n’est pas prise en charge sur Windows Vista, Windows Server 2008 et versions ultérieures.<br/> |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_ INET6**</dt> <dt>23</dt> </dl>             | Famille d’adresses IPv6 (Internet Protocol version 6).<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="AF_IRDA"></span><span id="af_irda"></span><dl> <dt>**AF \_ IRDA**</dt> <dt>26</dt> </dl>                | Famille d’adresses IrDA (Infrared Data Association). <br/> Cette famille d’adresses est uniquement prise en charge si un port infrarouge et un pilote sont installés sur l’ordinateur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span id="AF_BTH"></span><span id="af_bth"></span><dl> <dt>**AF \_ BTH**</dt> <dt>32</dt> </dl>                   | Famille d’adresses Bluetooth. <br/> Cette famille d’adresses est uniquement prise en charge si l’adaptateur et le pilote Bluetooth sont installés sur l’ordinateur.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

</dd> <dt>

*SocketType* 
</dt> <dd>

Spécification de type pour le nouveau Socket. Les valeurs possibles pour le type de socket sont définies dans le fichier d’en-tête *Winsock2. h* .

Le tableau suivant répertorie les valeurs possibles pour le paramètre de *type* pris en charge pour Windows Sockets 2 :



| Type                                                                                                                                                                                                                    | Signification                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SOCK_STREAM"></span><span id="sock_stream"></span><dl> <dt>**Chaussette \_ FLUX**</dt> <dt>1</dt> </dl>          | Type de socket qui fournit des flux d’octets en séquence, fiables, bidirectionnels et basés sur une connexion avec un mécanisme de transmission de données OOB. Ce type de socket utilise le protocole TCP (Transmission Control Protocol) pour la famille d’adresses Internet (AF \_ inet ou AF \_ inet6).<br/>                                                                                                                                |
| <span id="SOCK_DGRAM"></span><span id="sock_dgram"></span><dl> <dt>**Chaussette \_ DGRAM**</dt> <dt>2</dt> </dl>             | Type de socket qui prend en charge les datagrammes, qui sont des mémoires tampons non fiables, sans connexion, d’une longueur maximale fixe (généralement petite). Ce type de socket utilise le protocole UDP (User Datagram Protocol) pour la famille d’adresses Internet (AF \_ inet ou AF \_ inet6).<br/>                                                                                                                                       |
| <span id="SOCK_RAW"></span><span id="sock_raw"></span><dl> <dt>**Chaussette \_ BRUT**</dt> <dt>3</dt> </dl>                   | Type de socket qui fournit un socket brut qui permet à une application de manipuler l’en-tête de protocole de couche supérieure suivant. Pour manipuler l’en-tête IPv4, vous devez définir l’option de socket [**IP \_ HDRINCL**](ipproto-ip-socket-options.md) sur le Socket. Pour manipuler l’en-tête IPv6, l’option de socket [**IPv6 \_ HDRINCL**](ipproto-ipv6-socket-options.md) doit être définie sur le Socket. <br/> |
| <span id="SOCK_RDM"></span><span id="sock_rdm"></span><dl> <dt>**Chaussette \_ RDM**</dt> <dt>4</dt> </dl>                   | Type de socket qui fournit un datagramme de message fiable. Un exemple de ce type est l’implémentation du protocole de multidiffusion PGM (Pragmatic General Multicast) dans Windows, souvent appelée [programmation de multidiffusion fiable](reliable-multicast-programming--pgm-.md). <br/> Cette valeur de *type* est prise en charge uniquement si le protocole Reliable multicast est installé.<br/>              |
| <span id="SOCK_SEQPACKET"></span><span id="sock_seqpacket"></span><dl> <dt>**Chaussette \_ SEQPACKET**</dt> <dt>5</dt> </dl> | Type de socket qui fournit un paquet de Pseudo-flux basé sur des datagrammes. <br/>                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

*Protocole* 
</dt> <dd>

Protocole à utiliser. Les options possibles pour le paramètre de *protocole* sont spécifiques à la famille d’adresses et au type de socket spécifiés. Les valeurs possibles pour le *protocole* sont définies dans le fichier d’en-tête *wsrm. h* et le type d’énumération **IPPROTO** défini dans le fichier d’en-tête *Ws2def. h* . Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.

Si la valeur 0 est spécifiée, l’appelant ne souhaite pas spécifier de protocole et le fournisseur de services choisira le *protocole* à utiliser.

Le tableau ci-dessous répertorie les valeurs courantes du *protocole* , même si de nombreuses autres valeurs sont possibles.



| protocol                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="IPPROTO_ICMP"></span><span id="ipproto_icmp"></span><dl> <dt>**IPPROTO \_ ICMP**</dt> <dt>1</dt> </dl>          | Protocole ICMP (Internet Control Message Protocol). Il s’agit d’une valeur possible lorsque le paramètre *AF* est **AF \_ unspec**, **AF \_ inet** ou **AF \_ inet6** et que le paramètre de *type* est un **chaussette \_ brut** ou non spécifié.<br/>                                                                                               |
| <span id="IPPROTO_IGMP"></span><span id="ipproto_igmp"></span><dl> <dt>**IPPROTO \_ IGMP**</dt> <dt>2</dt> </dl>          | Protocole IGMP (Internet Group Management Protocol). Il s’agit d’une valeur possible lorsque le paramètre *AF* est **AF \_ unspec**, **AF \_ inet** ou **AF \_ inet6** et que le paramètre de *type* est un **chaussette \_ brut** ou non spécifié.<br/>                                                                                              |
| <span id="BTHPROTO_RFCOMM"></span><span id="bthproto_rfcomm"></span><dl> <dt>**BTHPROTO \_ RFCOMM**</dt> <dt>3</dt> </dl> | Protocole Bluetooth RFCOMM (Radio Frequency communications) Bluetooth. Il s’agit d’une valeur possible lorsque le paramètre *AF* est **AF \_ BTH** et que le paramètre de *type* est **\_ Stream de chaussette**. <br/>                                                                                                                 |
| <span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span><dl> <dt>**IPPROTO \_ TCP**</dt> <dt>6</dt> </dl>             | Protocole TCP (Transmission Control Protocol). Il s’agit d’une valeur possible lorsque le paramètre *AF* est **AF \_ inet** ou **AF \_ inet6** et que le paramètre de *type* est **\_ Stream de chaussette**.<br/>                                                                                                                                 |
| <span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span><dl> <dt>**IPPROTO \_ UDP**</dt> <dt>17</dt> </dl>            | Protocole UDP (User Datagram Protocol). Il s’agit d’une valeur possible lorsque le paramètre *AF* est **AF \_ inet** ou **AF \_ inet6** et que le paramètre de *type* est **chaussette \_ DGRAM**.<br/>                                                                                                                                         |
| <span id="IPPROTO_ICMPV6"></span><span id="ipproto_icmpv6"></span><dl> <dt>**IPPROTO \_ ICMPV6**</dt> <dt>58</dt> </dl>   | ICMPv6 (Internet Control Message Protocol version 6). Il s’agit d’une valeur possible lorsque le paramètre *AF* est **AF \_ unspec**, **AF \_ inet** ou **AF \_ inet6** et que le paramètre de *type* est un **chaussette \_ brut** ou non spécifié.<br/>                                                                                   |
| <span id="IPPROTO_RM"></span><span id="ipproto_rm"></span><dl> <dt>**IPPROTO \_ RM**</dt> <dt>113</dt> </dl>              | Protocole PGM pour la multidiffusion fiable. Il s’agit d’une valeur possible lorsque le paramètre *AF* est **AF \_ inet** et que le paramètre de *type* est un **\_ RDM de chaussette**. Ce protocole est également appelé **IPPROTO \_ PGM**. <br/> Cette valeur de *protocole* est prise en charge uniquement si le protocole Reliable multicast est installé.<br/> |



 

</dd> <dt>

*ProcessId* 
</dt> <dd>

L’ID de processus réel ou un indicateur si l’événement est le résultat d’une exécution de code Winsock dans un processus système ou dans un contexte de l’appel de procédure différé (DPC) (contextes en dehors du processus utilisateur).

</dd> <dt>

*État* 
</dt> <dd>

Code NTSTATUS pour l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

L’événement de **\_ \_ création d’événement AFD** est suivi pour une opération réseau Winsock afin de créer un Socket. Le canal de cet événement est Winsock-AFD. Le niveau de cet événement est informatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle du suivi Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**descripteur d’événement \_**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Niveaux de suivi Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

