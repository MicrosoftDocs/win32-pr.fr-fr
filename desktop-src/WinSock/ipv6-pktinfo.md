---
description: Permet à une application d’activer ou de désactiver le retour des informations de paquet par la fonction WSARecvMsg sur un socket IPv6.
ms.assetid: 7BF17538-BE92-44FE-BA3C-6B44F61D478A
title: Option de socket IPV6_PKTINFO (Ws2ipdef. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1bee015e7a73b803d78ae914e71a863dec83e4f40fc1aea9f631a54b37c586a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119733769"
---
# <a name="ipv6_pktinfo-socket-option"></a>\_Option de socket PKTINFO IPv6

L' \_ option de socket PKTINFO IPv6 permet à une application d’activer ou de désactiver le retour des informations de paquets par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sur un socket IPv6.

Pour interroger l’état de cette option de socket, appelez la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Pour définir cette option, appelez la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avec les paramètres suivants.

## <a name="socket-option-value"></a>Valeur d’option de socket

La constante qui représente cette option de socket est 19.

## <a name="syntax"></a>Syntaxe


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) IPPROTO_IPV6,   // level
  (int) IPV6_PKTINFO, // optname
  (char *) optval, // input buffer,
  (int) optlen,  // size of input buffer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

 \[ dans\]
</dt> <dd>

Descripteur identifiant le Socket.

</dd> <dt>

de *niveau* \[ dans\]
</dt> <dd>

Niveau auquel l’option est définie. Utilisez **IPPROTO \_ IPv6** pour cette opération.

</dd> <dt>

*nom_d* \[ ' $ dans\]
</dt> <dd>

Option de socket pour laquelle obtenir ou définir la valeur. Utilisez IPV6 \_ PKTINFO pour cette opération.

</dd> <dt>

*optval* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon contenant la valeur de l’option à définir. Ce paramètre doit pointer vers une mémoire tampon égale ou supérieure à la taille d’une valeur **DWORD** .

Cette valeur est traitée comme une valeur booléenne avec 0 utilisé pour indiquer **false** (désactivé) et une valeur différente de zéro pour indiquer la valeur **true** (activé).

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Pointeur vers la taille, en octets, de la mémoire tampon *optval* . Cette taille doit être supérieure ou égale à la taille d’une valeur **DWORD** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération se termine avec succès, la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) ou [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retourne la valeur zéro.

Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Code d'erreur                                                                                                                                              | Signification                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le sous-système réseau a échoué.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur. Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une valeur **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | un appel de blocage Windows sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Argument non valide fourni. Cette erreur est retournée si le paramètre de *niveau* est inconnu ou non valide. sur Windows Vista et versions ultérieures, cette erreur est également retournée si le socket est dans un état de transition.<br/>                                     |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L’option est inconnue ou non prise en charge par la famille de protocoles indiquée. Cette erreur est retournée si le paramètre de *type* pour le descripteur de socket passé dans le paramètre *s* n’était pas **chaussette \_ DGRAM** ou **chaussette \_ RAW**. <br/>                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le descripteur n’est pas un Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Remarques

La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l' \_ option de socket IPv6 PKTINFO permet à une application de déterminer si les informations de paquet doivent être retournées par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)pour un socket IPv6.

La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) appelée avec l' \_ option de socket PKTINFO IPv6 permet à une application d’activer ou de désactiver le retour des informations de paquets par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) . L' \_ option IPv6 PKTINFO pour un socket est désactivée (définie sur **false**) par défaut.

Lorsque cette option de socket est activée sur un socket IPv6 de **type chaussette \_ DGRAM** ou **chaussette \_ RAW**, la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) retourne des informations de paquets dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) vers laquelle pointe le paramètre *lpMsg* . L’un des objets de données de contrôle de la structure **WSAMSG** retournée contient une structure [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilisée pour stocker les informations d’adresse de paquet reçues.

Pour les datagrammes reçus par la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) sur IPv6, le membre du **contrôle** de la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) reçu contient une structure [**WSABUF**](/windows/desktop/api/ws2def/ns-ws2def-wsabuf) qui contient une structure **WSACMSGHDR** . Le membre de **\_ niveau CMSG** de cette structure **WSACMSGHDR** contiendra **IPPROTO \_ IPv6**, le membre de **\_ type CMSG** de cette structure contiendrait **IPv6 \_ PKTINFO** et le membre de **\_ données CMSG** contiendrait une structure in6 [**\_ PKTINFO**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) utilisée pour stocker les informations d’adresse de paquet IPv6 reçues. L’adresse IPv6 de la structure **in6 \_ pktinfo** est l’adresse IPv6 à partir de laquelle le paquet a été reçu.

Pour un socket de datagramme à double pile, si une application requiert la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) pour retourner les informations de paquets dans une structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) pour les datagrammes reçus sur IPv4, l’option de socket [IP \_ PKTINFO](ip-pktinfo.md) doit avoir la valeur true sur le Socket. Si seule l' \_ option IPv6 PKTINFO a la valeur true sur le socket, des informations de paquet sont fournies pour les datagrammes reçus via IPv6, mais elles peuvent ne pas être fournies pour les datagrammes reçus sur IPv4.

Notez que le fichier d’en-tête *Ws2ipdef. h* est automatiquement inclus dans *Ws2tcpip. h* et ne doit jamais être utilisé directement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                       |
| En-tête<br/>                   | <dl> <dt>Ws2ipdef. h (inclure Ws2tcpip. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Sockets à double pile](dual-stack-sockets.md)
</dt> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[\_PKTINFO IP](ip-pktinfo.md)
</dt> <dt>

[**\_Options de socket IPv6 IPPROTO**](ipproto-ipv6-socket-options.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**socle**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> </dl>

 

 
