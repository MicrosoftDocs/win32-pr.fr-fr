---
description: Page de navigation pour les options de socket Windows Sockets (Winsock).
ms.assetid: e2831f76-4499-45b6-bc60-2908ec3a246c
title: Options de socket
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IPPROTO_IP
- IPPROTO_IPV6
- IPPROTO_RM
- IPPROTO_TCP
- IPPROTO_UDP
- NSPROTO_IPX
- SOL_APPLETALK
- SOL_IRLMP
- SOL_SOCKET
api_type:
- NA
api_location: ''
ms.openlocfilehash: 805f779965afc808e32952b58815c7b6bc528fbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540820"
---
# <a name="socket-options"></a>Options de socket

Cette section décrit les options de socket Winsock pour différentes éditions des systèmes d’exploitation Windows. Utilisez les fonctions [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket. Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) .

Certaines options de socket requièrent plus d’explications que celles pouvant être transmises par ces tables. ces options contiennent des liens vers des pages supplémentaires.

<dl> <dt>

<span id="IPPROTO_IP"></span><span id="ipproto_ip"></span>**IPPROTO \_ IP**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau IPv4. Pour plus d’informations, consultez [**les \_ options de socket IP IPPROTO**](ipproto-ip-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_IPV6"></span><span id="ipproto_ipv6"></span>**\_IPv6 IPPROTO**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau IPv6. Pour plus d’informations, consultez [**les \_ options de socket IPv6 IPPROTO**](ipproto-ipv6-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_RM"></span><span id="ipproto_rm"></span>**IPPROTO \_ RM**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau de la multidiffusion fiable. Pour plus d’informations, consultez [**les \_ options de socket RM IPPROTO**](ipproto-rm-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_TCP"></span><span id="ipproto_tcp"></span>**IPPROTO \_ TCP**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau TCP. Pour plus d’informations, consultez [**les \_ options de socket TCP IPPROTO**](ipproto-tcp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="IPPROTO_UDP"></span><span id="ipproto_udp"></span>**\_UDP IPPROTO**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau du protocole UDP. Pour plus d’informations, consultez [**les \_ options de socket UDP IPPROTO**](ipproto-udp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="NSPROTO_IPX"></span><span id="nsproto_ipx"></span>**\_IPX NSPROTO**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau IPX. Pour plus d’informations, consultez [**les \_ options de socket IPX NSPROTO**](nsproto-ipx-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_APPLETALK"></span><span id="sol_appletalk"></span>**\_AppleTalk AppleTalk**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau du protocole AppleTalk. Pour plus d’informations, consultez [**les \_ options de socket AppleTalk AppleTalk**](sol-appletalk-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_IRLMP"></span><span id="sol_irlmp"></span>**\_IRLMP sol**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau du protocole de gestion des liaisons infrarouges. Pour plus d’informations, consultez [**les \_ options de socket sol IRLMP**](sol-irlmp-socket-options.md).


</dt> </dl> </dd> <dt>

<span id="SOL_SOCKET"></span><span id="sol_socket"></span>**\_Socket sol**
</dt> <dd> <dl> <dt>



Options de socket applicables au niveau du Socket. Pour plus d’informations, consultez [**les \_ options de socket de socket sol**](sol-socket-socket-options.md).


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Notes

Toutes les \_ \* options de socket s’appliquent également aux protocoles IPv4 et IPv6 (à l’exception de la \_ diffusion, car la diffusion n’est pas implémentée dans IPv6).

 

 



