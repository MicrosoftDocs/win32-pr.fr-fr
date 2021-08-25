---
title: Identificateurs de protocole
description: les identificateurs de protocole suivants sont également répertoriés dans Routprot. h pour le SDK Windows, et iprtmib. h pour le kit de développement logiciel (SDK) de la plateforme.
ms.assetid: f67138b8-de5d-4907-a464-672d57864ebf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dafcbcd028b5c8d4f58172565b34c93cff8d8f9ff766c055e3d8a956cfbb0aa8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120036469"
---
# <a name="protocol-identifiers"></a>Identificateurs de protocole

les identificateurs de protocole suivants sont également répertoriés dans Routprot. h pour le SDK Windows, et iprtmib. h pour le kit de développement logiciel (SDK) de la plateforme.

## <a name="ip-protocols"></a>Protocoles IP

Les protocoles de routage suivants sont associés au transport IP.



| Protocole                                                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_adresse IP proto \_ , autre \_ IPPROTO \_ MIB                        | Un autre protocole n’est pas spécifié dans le document RFC 1354.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ local, MIB \_ IPPROTO \_ local                        | Interface locale.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ NetMgmt, MIB \_ IPPROTO \_ NetMgmt                    | Itinéraire statique. Cette valeur est utilisée pour identifier les informations d’itinéraire pour le routage IP par le biais de la gestion du réseau, comme le protocole DHCP (Dynamic Host Configuration Protocol), le protocole SNMP (simple Network Management Protocol) ou les appels aux fonctions [**CreateIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-deleteipforwardentry)ou [**SetIpForwardEntry**](/windows/desktop/api/iphlpapi/nf-iphlpapi-setipforwardentry) .                                                                                              |
| PROTO \_ IP \_ ICMP, MIB \_ IPPROTO \_ ICMP                          | Résultat de la redirection ICMP.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| PROTO \_ IP \_ EGP, MIB \_ IPPROTO \_ EGP                            | Protocole EGP (externe Gateway Protocol), un protocole de routage dynamique.                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PROTO \_ IP \_ GGP, MIB \_ IPPROTO \_ GGP                            | Le protocole GGP (Gateway-to-Gateway Protocol), un protocole de routage dynamique.                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ Hello, MIB \_ IPPROTO \_ Hello                        | Protocole Hellospeak, protocole de routage dynamique. Il s’agit d’une entrée d’historique qui n’est plus utilisée et qui était un protocole de routage précoce utilisé par les routeurs ARPANET d’origine qui exécutaient un logiciel spécial appelé le protocole de routage Fuzzball, parfois appelé Hellospeak, comme décrit dans RFC 891 et RFC 1305. Pour plus d’informations, consultez [https://www.ietf.org/rfc/rfc891.txt](https://www.ietf.org/rfc/rfc891.txt) et [https://www.ietf.org/rfc/rfc1305.txt](https://tools.ietf.org/html/rfc1305). |
| PROTO \_ IP \_ RIP, MIB \_ IPPROTO \_ RIP                            | Le protocole RIP (Berkeley Routing Information Protocol) ou RIP-II, un protocole de routage dynamique.                                                                                                                                                                                                                                                                                                                                                                                                                               |
| l' \_ adresse IP proto est \_ \_ , MIB \_ IPPROTO \_ est \_                      | Le protocole intermédiaire système-à-intermédiaire (IS-IS), un protocole de routage dynamique. Le protocole IS-IS a été développé pour être utilisé dans la suite de protocoles OSI (Open Systems Interconnection).                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ es \_ est, MIB \_ IPPROTO \_ es \_                      | Le protocole « ES-IS » de l’ordinateur final est un protocole de routage dynamique. Le protocole ES-IS a été développé pour être utilisé dans la suite de protocoles OSI (Open Systems Interconnection).                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ Cisco, MIB \_ IPPROTO \_ Cisco                        | Le protocole IGRP (Cisco Interior Gateway Routing Protocol), un protocole de routage dynamique.                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| PROTO \_ IP \_ BBN, MIB \_ IPPROTO \_ BBN                            | Protocole IGP, Beranek et Newman (BBN), qui utilisait l’algorithme SPF (Shortest Path First). Il s’agissait d’un protocole de routage dynamique précoce.                                                                                                                                                                                                                                                                                                                                                   |
| PROTO \_ IP \_ OSPF, MIB \_ IPPROTO \_ OSPF                          | Le protocole OSPF (Open Shortest Path First), un protocole de routage dynamique.                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ BGP, MIB \_ IPPROTO \_ BGP                            | Le Border Gateway Protocol (BGP) est un protocole de routage dynamique.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| PROTO \_ IP \_ BOOTP, MIB \_ IPPROTO \_ BOOTP                        | Protocole Bootstrap.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| PROTO \_ IPv6 \_ DHCPRELAY, MIB \_ IPV6PROTO \_ HDCPRELAY            | Protocole DHCPv6 Relay.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| PROTO \_ IP \_ NT \_ autostatique, MIB \_ IPNT \_ autostatic             | une Windows entrée spécifique ajoutée à l’origine par un protocole de routage, mais qui est désormais statique.                                                                                                                                                                                                                                                                                                                                                                                                                            |
| PROTO \_ IP \_ NT \_ static, MIB \_ IPNT \_ static                     | une Windows entrée spécifique ajoutée en tant qu’itinéraire statique à partir de l’interface utilisateur de routage ou d’une commande de routage.                                                                                                                                                                                                                                                                                                                                                                                                               |
| PROTO \_ IP \_ NT \_ static \_ non \_ DOD, MIB \_ IPNT \_ static \_ non \_ DoD | une Windows entrée spécifique ajoutée en tant qu’itinéraire statique à partir de l’interface utilisateur de routage ou d’une commande de routage, sauf que ces itinéraires n’entraînent pas de connexion à la demande (DOD).                                                                                                                                                                                                                                                                                                                                                        |



 

Les itinéraires avec un identificateur de protocole PROTO \_ IP \_ local sont les suivants :

-   Itinéraire de bouclage
-   Itinéraire de sous-réseau
-   Itinéraire de diffusion de tous les réseaux pour les interfaces de sous-réseau
-   Tout l’itinéraire de diffusion « 1 » s
-   Itinéraire de multidiffusion local
-   Itinéraire vers l’extrémité distante d’une liaison PPP

L’identificateur du gestionnaire de routeur IP est le suivant :

\_PID IPRTRMGR

Cet identificateur peut être utilisé à la place d’un identificateur de protocole de routage pour les appels MIB avec le gestionnaire de routeur IP. Cet identificateur est utilisé pour MIB-II, le MIB de transfert et certaines informations spécifiques à l’entreprise. Cet identificateur est également listé dans Iprtrmib. h.

## <a name="ipx-protocols"></a>Protocoles IPX

Les protocoles de routage suivants sont associés au transport IPX.



| Protocole            | Description                          |
|---------------------|--------------------------------------|
| \_RIP de protocole IPX \_  | Protocole d’informations de routage pour IPX |
| \_SAP de protocole IPX \_  | Protocole de publication de service       |
| \_nlsp de protocole IPX \_ | Protocole des services de liaison NetWare       |



 

L’identificateur du gestionnaire de routage IPX est le suivant :

\_base du protocole IPX \_

Utilisez cet identificateur à la place d’un identificateur de protocole de routage pour les appels MIB avec le gestionnaire de routeur IPX.

 

 