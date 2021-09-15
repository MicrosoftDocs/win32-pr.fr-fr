---
description: Retourne l’adresse locale, le port local, l’adresse distante, le port distant, le type de socket et le protocole utilisés par un Socket.
ms.assetid: 2628f47e-3e73-4e02-91b8-ba4cb0800864
title: Option de socket SO_BSP_STATE (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10e391d70dd67190e1aec803036d019261c9000
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403891"
---
# <a name="so_bsp_state-socket-option"></a>\_Option de \_ Socket d’État BSP

L’option de socket de l' **\_ \_ État BSP** retourne l’adresse locale, le port local, l’adresse distante, le port distant, le type de socket et le protocole utilisés par un Socket.

Pour effectuer cette opération, appelez la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) avec les paramètres suivants.

## <a name="socket-option-value"></a>Valeur d’option de socket

La constante qui représente cette option de socket est 0x1009.

## <a name="syntax"></a>Syntaxe


```C++
int getsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_BSP_STATE, // optname
  (char *) optval,         // output buffer,
  (int) *optlen,       // size of output buffer
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

Option de socket pour laquelle la valeur doit être récupérée. Utilisez **l' \_ \_ État BSP** pour cette opération.

</dd> <dt>

*optval* \[ à\]
</dt> <dd>

Pointeur vers la mémoire tampon dans laquelle la valeur de l’option demandée doit être retournée. Ce paramètre doit pointer vers une mémoire tampon égale ou supérieure à la taille d’une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> <dt>

*optlen* \[ in, out\]
</dt> <dd>

Pointeur vers la taille, en octets, de la mémoire tampon *optval* . Cette taille doit être supérieure ou égale à la taille d’une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération se termine avec succès, [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) retourne la valeur zéro.

Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Code d'erreur                                                                                                                                              | Signification                                                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.<br/>                                                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le sous-système réseau a échoué.<br/>                                                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur. Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | un appel de blocage Windows sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.<br/>                                                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Le paramètre de *niveau* est inconnu ou non valide.<br/>                                                                                                                                                                                                                                    |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L’option est inconnue ou non prise en charge par la famille de protocoles indiquée.<br/>                                                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le descripteur n’est pas un Socket.<br/>                                                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Notes

La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l’option de socket d' **\_ \_ État BSP** récupère l’adresse locale, le port local, l’adresse distante, le port distant, le type de socket et le protocole utilisés par un Socket. L’option de socket d' **\_ \_ État BSP so** fonctionne avec les sockets IPv6 ou IPv4 (familles d’adresses **AF \_ inet6** et **AF \_ inet** ).

Si la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) réussit, les informations sont retournées dans une structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) dans la mémoire tampon vers laquelle pointe le paramètre *optval* . L’entier pointé par *optlen* doit contenir initialement la taille de cette mémoire tampon. lors du retour, elle est définie sur la longueur, en octets, de la valeur retournée dans le paramètre *optval* .

Les membres **iSocketType** et **iProtocol** de la structure [**d' \_ informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée sont renseignés pour le descripteur de socket dans le paramètre *s* .

Si le socket est dans un état connecté ou lié, le membre **LocalAddr** de la structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée est défini sur une structure [sockaddr](sockaddr-2.md) représentant l’adresse et le port locaux. Si le socket est dans un état connecté, le membre **RemoteAddr** de la structure **CSADDR \_ info** retournée est défini sur une structure sockaddr représentant l’adresse et le port distants.

Si le socket n’est pas dans un état connecté ou lié, le membre **LocalAddr** de la structure [**CSADDR \_ info**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée est retourné avec un pointeur **null** dans le membre **lpSockaddr** et le membre **iSockaddrLength** défini à zéro. Si le socket n’est pas dans un État lié, le membre **RemoteAddr** de la structure **CSADDR \_ info** retournée est retourné avec un pointeur **null** dans le membre **lpSockaddr** et le membre **iSockaddrLength** défini à zéro.

Si la fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) échoue, les *paramètres optval* et *optlen* restent inchangés et le paramètre *optval* ne pointe pas vers une structure [**\_ info CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info) retournée.

Notez que le fichier d’en-tête *Ws2def. h* est automatiquement inclus dans *Winsock2. h* et ne doit jamais être utilisé directement.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Ws2def. h (inclure Winsock2. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt)
</dt> <dt>

[**\_informations CSADDR**](/windows/win32/api/ws2def/ns-ws2def-csaddr_info)
</dt> <dt>

[SOCKADDR](sockaddr-2.md)
</dt> </dl>

 

 
