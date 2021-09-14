---
description: Est conçu pour permettre à une application de décider s’il faut ou non accepter une connexion entrante sur un socket d’écoute.
ms.assetid: 964683eb-5dfc-4441-abb7-315be8b89a19
title: Option de socket SO_CONDITIONAL_ACCEPT (Ws2def. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: badfdd1f8aac49ae05fa6b77dadb2561ba5ea02f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127292227"
---
# <a name="so_conditional_accept-socket-option"></a>\_Option de \_ Socket d’acceptation conditionnelle

L’option de socket d' **\_ \_ acceptation conditionnelle so** est conçue pour permettre à une application de décider s’il faut ou non accepter une connexion entrante sur un socket d’écoute.

## <a name="socket-option-value"></a>Valeur d’option de socket

La constante qui représente cette option de socket est 0x3002.

## <a name="syntax"></a>Syntaxe


```C++
int setsockopt(
  (SOCKET) s,      // descriptor identifying a socket 
  (int) SOL_SOCKET,   // level
  (int) SO_CONDITIONAL_ACCEPT, // optname
  (char *) optval,         // input buffer,
  (int) optlen,       // size of input buffer
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

Option de socket pour laquelle la valeur doit être définie. Utilisez **l' \_ \_ acceptation conditionnelle** pour cette opération.

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

## <a name="return-value"></a>Valeur de retour

Si l’opération se termine correctement, [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) retourne la valeur zéro.

Si l’opération échoue, une valeur d’erreur de SOCKET \_ est renvoyée et un code d’erreur spécifique peut être récupéré en appelant [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror).



| Code d'erreur                                                                                                                                              | Signification                                                                                                                                                                                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**[WSANOTINITIALISED](windows-sockets-error-codes-2.md)**</dt> </dl> | Un appel [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) réussi doit se produire avant l’utilisation de cette fonction.<br/>                                                                                                                                                     |
| <dl> <dt>**[WSAENETDOWN](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le sous-système réseau a échoué.<br/>                                                                                                                                                                                                               |
| <dl> <dt>**[WSAEFAULT](windows-sockets-error-codes-2.md)**</dt> </dl>                 | L’un des paramètres *optval* ou *optlen* pointent vers la mémoire qui n’est pas dans une partie valide de l’espace d’adressage de l’utilisateur. Cette erreur est également retournée si la valeur vers laquelle pointe le paramètre *optlen* est inférieure à la taille d’une valeur **DWORD** .<br/> |
| <dl> <dt>**[WSAEINPROGRESS](windows-sockets-error-codes-2.md)**</dt> </dl>       | un appel de blocage Windows sockets 1,1 est en cours, ou le fournisseur de services traite toujours une fonction de rappel.<br/>                                                                                                                            |
| <dl> <dt>**[WSAEINVAL](windows-sockets-error-codes-2.md)**</dt> </dl>                 | Le paramètre de *niveau* est inconnu ou non valide. Cette erreur est également retournée si le socket était déjà à l’état d’écoute.<br/>                                                                                                                        |
| <dl> <dt>**[WSAENOPROTOOPT](windows-sockets-error-codes-2.md)**</dt> </dl>       | L’option est inconnue ou non prise en charge par la famille de protocoles indiquée.<br/>                                                                                                                                                                          |
| <dl> <dt>**[WSAENOTSOCK](windows-sockets-error-codes-2.md)**</dt> </dl>             | Le descripteur n’est pas un Socket.<br/>                                                                                                                                                                                                                 |



 

## <a name="remarks"></a>Notes

La fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) appelée avec l’option de socket d' **\_ \_ acceptation conditionnelle** permet à une application de décider s’il faut ou non accepter une connexion entrante sur un socket d’écoute. L’option d’acceptation conditionnelle pour un socket est désactivée (définie sur **false**) par défaut.

Lorsque cette option de socket est activée, la pile TCP n’accepte pas automatiquement les connexions. Elle attend que l’application indique qu’elle accepte la connexion via le rappel d’acceptation conditionnel inscrit avec la fonction [**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) . Une fois qu’une demande de connexion est reçue, Winsock appelle le rappel d’acceptation conditionnel inscrit par l’application. Uniquement lorsque le rappel d’acceptation conditionnelle retourne **CF \_ Accept** , Winsock notifie le transport pour accepter entièrement la connexion.

Lorsque l’option de socket d' **\_ \_ acceptation conditionnelle so** est définie sur Enabled (définie à **true**), cela a plusieurs effets secondaires sur le Socket :

-   Cela désactive les défenses de protection contre les attaques SYN intégrées de la pile TCP, puisque l’application est maintenant propriétaire de l’acceptation des connexions.
-   Cela désactive efficacement le backlog d’écoute, car les connexions ne sont pas acceptées pour le compte d’un socket d’écoute. Une connexion n’est jamais entièrement acceptée tant que l’application n’accepte pas complètement l’utilisation du mécanisme d' **\_ acceptation CF** .
-   Cela signifie également que l’application doit toujours être dans un État pour gérer facilement les rappels d’acceptation afin d’accepter la connexion. Si l’application est occupée par un autre traitement, le côté client peut expirer avant que l’application n’accepte réellement la connexion. Cela provoque une expérience client médiocre.

En règle générale, la raison principale pour laquelle les applications utilisent l’acceptation conditionnelle est d’inspecter l’adresse IP ou le port source utilisé par le client qui se connecte, puis de décider d’accepter ou de refuser la connexion. Toutefois, les applications sont susceptibles d’être plus performantes si l' \_ option accepter la condition conditionnelle \_ n’est pas activée et que l’application autorise la pile TCP et le backlog d’écoute à fonctionner comme prévu. Ensuite, lorsque l’application gère la connexion acceptée, si elle provient d’une adresse ou d’un port source IP incorrect, l’application peut simplement fermer le Socket. L’inconvénient en matière de sécurité de ce comportement est que, à présent, le client a la confirmation que l’application est à l’écoute sur une adresse IP et un port, car elle a forcé de fermer la connexion précédemment acceptée. Toutefois, les inconvénients de l’activation de l' **\_ \_ acceptation conditionnelle** l’emportent généralement sur cette limitation.

La fonction [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) appelée avec l’option de socket d' **\_ \_ acceptation conditionnelle** permet à une application de récupérer l’état actuel de l’option d’acceptation conditionnelle, bien qu’il s’agisse d’une fonctionnalité qui n’est généralement pas utilisée. Si une application doit activer l’acceptation conditionnelle sur un socket, elle appelle la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) pour activer l’option.

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

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**WSAAccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept)
</dt> </dl>

 

 




