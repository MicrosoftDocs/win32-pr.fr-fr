---
title: Constantes de séquence de protocole
description: Microsoft RPC prend en charge les séquences de protocole suivantes.
ms.assetid: 51284532-b0ac-4bf2-b322-91393b2b9dc6
topic_type:
- apiref
api_name:
- ncacn_nb_tcp
- ncacn_nb_ipx
- ncacn_nb_nb
- ncacn_ip_tcp
- ncacn_np
- ncacn_spx
- ncacn_dnet_nsp
- ncacn_at_dsp
- ncacn_vns_spp
- ncadg_ip_udp
- ncadg_ipx
- ncadg_mq
- ncacn_http
- ncalrpc
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e2dd716cdd969040f5315ef05200912acc54878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104031686"
---
# <a name="protocol-sequence-constants"></a>Constantes de séquence de protocole

Microsoft RPC prend en charge les séquences de protocole suivantes.



| Constante/valeur                                                                                                                                                                                                                                                                                 | Description                                                                                                                                                                         |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ncacn_nb_tcp"></span><span id="NCACN_NB_TCP"></span><dl> <dt>**ncacn \_ NB \_**</dt> <dt>NetBIOS orienté connexion TCP via le protocole TCP (Transmission Control Protocol)</dt> </dl>          | Client uniquement : MS-DOS, Windows 3. Client *x* et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_ipx"></span><span id="NCACN_NB_IPX"></span><dl> <dt>**ncacn \_ NB \_ IPX**</dt> <dt>connexion-orienté NetBIOS sur Internet Packet Exchange (IPX)</dt> </dl>               | Client uniquement : MS-DOS, Windows 3. Client *x* et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncacn_nb_nb"></span><span id="NCACN_NB_NB"></span><dl> <dt>**ncacn \_ NB \_ NB**</dt> <dt>: NetBEUI (interface utilisateur améliorée) orientée connexion</dt> </dl>                    | Client uniquement : MS-DOS, Windows 3. *x* client et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_ip_tcp"></span><span id="NCACN_IP_TCP"></span><dl> protocole <dt>TCP/IP (TCP/IP) de connexion</dt> <dt>**\_ \_ TCP**</dt> /IP ncacn </dl>  | Client uniquement : MS-DOS, Windows 3. *x* et client Apple Macintosh et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/> |
| <span id="ncacn_np"></span><span id="NCACN_NP"></span><dl> <dt>canaux nommés orientés connexion</dt> <dt>**ncacn \_ NP**</dt> </dl>                                                            | Client uniquement : MS-DOS, Windows 3. *x*, client et serveur Windows 95 : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                              |
| <span id="ncacn_spx"></span><span id="NCACN_SPX"></span><dl> <dt>**ncacn \_ SPX**</dt> <dt>Connection-Oriented Packet Exchange (SPX)</dt> </dl>                                     | Client uniquement : MS-DOS, Windows 3. *x* client et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                      |
| <span id="ncacn_dnet_nsp"></span><span id="NCACN_DNET_NSP"></span><dl> <dt>**ncacn \_ dnet \_**</dt> <dt>connexion-transport décnet orienté connexion</dt> </dl>                                    | Client uniquement : MS-DOS, Windows 3. *x*<br/>                                                                                                                                       |
| <span id="ncacn_at_dsp"></span><span id="NCACN_AT_DSP"></span><dl> <dt>**ncacn \_ au \_**</dt> fournisseur de <dt>DSP AppleTalk orienté connexion</dt> DSP </dl>                                             | Client : serveur Apple Macintosh : Windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                                                |
| <span id="ncacn_vns_spp"></span><span id="NCACN_VNS_SPP"></span><dl> <dt>transport de traitement parallèle évolutif (spp) de la connexion</dt> <dt>**ncacn \_ réseaux virtuels \_ spp**</dt> </dl>     | Client uniquement : MS-DOS, Windows 3. Client *x* et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ip_udp"></span><span id="NCADG_IP_UDP"></span><dl> <dt>**datagramme \_ \_ UDP IP ncadg**</dt> <dt>(sans connexion) protocole Internet (UDP/IP)</dt> </dl>   | Client uniquement : MS-DOS, Windows 3. Client *x* et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_ipx"></span><span id="NCADG_IPX"></span><dl> <dt>**ncadg \_**</dt> IPX <dt>datagramme (sans connexion)</dt> </dl>                                                           | Client uniquement : MS-DOS, Windows 3. Client *x* et serveur : windows Server 2003, Windows XP, Windows 2000, Windows NT<br/>                                                          |
| <span id="ncadg_mq"></span><span id="NCADG_MQ"></span><dl> <dt>**ncadg \_ MQ**</dt> <dt>Datagram (sans connexion) sur Microsoft Message Queue Server (MSMQ)</dt> </dl>                   | Client uniquement : client et serveur Windows Me/98/95 : Windows Server 2003, Windows XP, Windows 2000, Windows NT Server 4,0 avec SP3 et versions ultérieures<br/>                                 |
| <span id="ncacn_http"></span><span id="NCACN_HTTP"></span><dl> <dt>**NCACN \_**</dt> <dt>TCP/IP orienté connexion http à l’aide de Microsoft Internet Information Server en tant que proxy http</dt> </dl> | Client uniquement : client et serveur Windows Me/98/95 : Windows Server 2003, Windows XP, Windows 2000<br/>                                                                           |
| <span id="ncalrpc"></span><span id="NCALRPC"></span><dl> <dt></dt> <dt>appel de procédure locale</dt> Ncalrpc </dl>                                                                           | Client et serveur : Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, Windows 95<br/>                                                         |



## <a name="remarks"></a>Notes

Le transport [**Ncalrpc**](/windows/desktop/Midl/ncalrpc) prend uniquement en charge \_ \_ \_ l’authentification Winnt RPC C Authn. Pour plus d’informations, consultez [sécurité](security.md) et [authentification-constantes de service](authentication-service-constants.md).

Microsoft RPC prend en charge [**RpcBindingCopy**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingcopy) uniquement dans les applications clientes, pas dans les applications serveur.

 

