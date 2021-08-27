---
description: Est conçu pour permettre à une application d’activer des paquets Keep-Alive pour une connexion de Socket.
ms.assetid: d6da7761-7a09-4c91-9737-550590a773b3
title: Option de socket SO_KEEPALIVE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d3590b8813f584aad16896a5b990baa2e3ad5607b76a13bd987d87961ee5f6f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097469"
---
# <a name="so_keepalive-socket-option"></a>\_Option de socket KeepAlive

L’option **so \_ KeepAlive** Socket est conçue pour permettre à une application d’activer des paquets Keep-Alive pour une connexion de Socket.

Pour interroger l’état de cette option de socket, appelez la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) . Pour définir cette option, appelez la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) avec les paramètres suivants.

## <a name="socket-option-value"></a>Valeur d’option de socket

La constante qui représente cette option de socket est 0x0008.

## <a name="syntax"></a>Syntaxe


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
  (char *) optval, // output buffer,
  (int) optlen,  // size of output buffer
);
```




```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_KEEPALIVE, // optname
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

Niveau auquel l’option est définie. Utilisez **le \_ Socket sol** pour cette opération.

</dd> <dt>

*nom_d* \[ ' $ dans\]
</dt> <dd>

Option de socket pour laquelle la valeur doit être définie. Utilisez **donc \_ KeepAlive** pour cette opération.

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

Si l’opération se termine correctement, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retourne la valeur zéro.

Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Code d'erreur                                                                                                                                              | Signification                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le sous-système réseau a échoué.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur. Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une valeur **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | un appel de blocage Windows sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Le paramètre de *niveau* est inconnu ou non valide. sur Windows Vista et versions ultérieures, cette erreur est également retournée si le socket est dans un état de transition.<br/>                                                                                                 |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L’option est inconnue ou non prise en charge par la famille de protocoles indiquée. Cette erreur est retournée si le descripteur de socket passé dans le paramètre *s* était pour un socket datagramme.<br/>                                                                   |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le descripteur n’est pas un Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Remarques

La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l’option de socket **\_ KeepAlive** permet à une application de récupérer l’état actuel de l’option KeepAlive, bien qu’il s’agisse d’une fonctionnalité qui n’est généralement pas utilisée. Si une application doit activer des paquets KeepAlive sur un socket, elle appelle simplement la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour activer l’option.

La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) appelée avec l’option de socket **\_ KeepAlive** permet à une application d’activer des paquets Keep-Alive pour une connexion de Socket. L’option **so \_ KeepAlive** pour un socket est désactivée (définie sur **false**) par défaut.

Lorsque cette option de socket est activée, la pile TCP envoie des paquets Keep-Alive quand aucun paquet de données ou d’accusé de réception n’a été reçu pour la connexion dans un intervalle. Pour plus d’informations sur l’option Keep-Alive, consultez la section 4.2.3.6 sur la *Configuration requise pour les hôtes Internet — couches de communication* spécifiées dans le document RFC 1122 disponible sur le [site Web](https://www.ietf.org/rfc/rfc1122.txt)de l’IETF. (Cette ressource peut uniquement être disponible en anglais.)

L’option **so \_ KeepAlive** Socket est valide uniquement pour les protocoles qui prennent en charge la notion de Keep-Alive (protocoles orientés connexion). Pour TCP, le délai d’expiration de la conservation par défaut est de 2 heures et l’intervalle de maintien de l’activité est de 1 seconde. Le nombre par défaut de sondes KeepAlive varie en fonction de la version de Windows.

Le code de contrôle [**\_ KeepAlive \_ Vals SIO**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85)) peut être utilisé pour activer ou désactiver Keep-Alive, et ajuster le délai d’expiration et l’intervalle pour une connexion unique. Si Keep-Alive est activé avec **\_ KeepAlive**, les paramètres TCP par défaut sont utilisés pour le délai d’expiration et l’intervalle Keep-Alive, sauf si ces valeurs ont été modifiées à l’aide de **SIO \_ KeepAlive \_ Vals**.

La valeur par défaut au niveau du système du délai d’expiration Keep-Alive est contrôlable via le paramètre de Registre [keepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10)) qui prend une valeur en millisecondes. La valeur par défaut à l’ensemble du système de l’intervalle Keep-Alive est contrôlable via le paramètre de Registre [keepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10)) qui prend une valeur en millisecondes.

sur Windows Vista et versions ultérieures, le nombre de sondes keepalive (retransmissions de données) est défini sur 10 et ne peut pas être modifié.

sur Windows Server 2003, Windows XP et Windows 2000, le paramètre par défaut pour le nombre de sondes keep-alive est 5. Le nombre de sondes KeepAlive est contrôlable via les paramètres de Registre [TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10)) et [PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10)) . Le nombre de sondes KeepAlive est défini sur la plus grande des deux valeurs de clé de registre. Si ce nombre est 0, les sondes de conservation des connexions actives ne sont pas envoyées. Si ce nombre est supérieur à 255, il est ajusté à 255.

sur Windows Vista et versions ultérieures, l’option de socket **\_ KEEPALIVE** ne peut être définie qu’à l’aide de la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) lorsque le socket est dans un état connu et non transitoire. Pour TCP, l’option de socket **\_ KeepAlive de ce** type doit être définie avant que la fonction Connect ([**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), [**WSAConnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect), [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)ou [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)) soit appelée, ou une fois que la demande de connexion est effectivement terminée. Si la fonction Connect a été appelée de façon asynchrone, cela nécessite l’attente de la fin de la connexion avant d’essayer de définir l’option **so \_ KeepAlive** Socket. Si une application tente de définir l’option de socket **\_ KeepAlive** si une demande de connexion est toujours en cours, la fonction **setsockopt** échoue et retourne [WSAEINVAL](windows-sockets-error-codes-2.md).

sur Windows Server 2003, Windows XP et Windows 2000, l’option de socket **\_ KEEPALIVE** peut être définie à l’aide de la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) lorsque le socket est un état transitoire (une demande de connexion est toujours en cours), ainsi qu’un état connu.

Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Ws2def. h (inclure Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[KeepAliveTime](/previous-versions/windows/it-pro/windows-server-2003/cc782936(v=ws.10))
</dt> <dt>

[KeepAliveInterval](/previous-versions/windows/it-pro/windows-server-2003/cc758083(v=ws.10))
</dt> <dt>

[PPTPTcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc775408(v=ws.10))
</dt> <dt>

[**socle**](/windows/desktop/api/Winsock2/nf-winsock2-socket)
</dt> <dt>

[**SIO \_ KeepAlive \_ Vals**](/previous-versions/windows/desktop/legacy/dd877220(v=vs.85))
</dt> <dt>

[TcpMaxDataRetransmissions](/previous-versions/windows/it-pro/windows-server-2003/cc780586(v=ws.10))
</dt> <dt>

[**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror)
</dt> </dl>

 

 
