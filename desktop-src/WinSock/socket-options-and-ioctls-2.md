---
description: Certaines options de socket pour Windows Sockets 2 sont résumées dans le tableau suivant.
ms.assetid: 6731d27c-fb7d-421a-badf-0cad6a4712ea
title: Options de socket et IOCTL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472d37bd8d2d97eead66d7c9d2319e57fc5dafde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106524354"
---
# <a name="socket-options-and-ioctls"></a>Options de socket et IOCTL

Certaines options de socket pour Windows Sockets 2 sont résumées dans le tableau suivant. Des informations plus détaillées sont fournies dans la section 4 sous [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)) et/ou [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)). Il existe d’autres nouvelles options de socket spécifiques au protocole qui se trouvent dans l’annexe Protocol-Specific. La liste complète des [**options de socket**](socket-options.md) pour Windows Sockets est disponible dans les informations de référence sur Winsock.

Pour obtenir un résumé de certains des IOCTL Winsock, consultez [Résumé des OpCodes IOCTL de socket](summary-of-socket-ioctl-opcodes-2.md). Une liste complète des [**IOCTL Winsock**](winsock-ioctls.md) est disponible dans les informations de référence sur Winsock.

## <a name="summary-of-common-socket-options"></a>Résumé des options de socket courantes

Un fournisseur de services Winsock doit reconnaître toutes ces options et (pour [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85))) retourner des valeurs plausibles pour chaque. La valeur par défaut de chaque option est indiquée dans le tableau suivant.

Valeur

Type

Signification

Default

Remarque

<span id="SO_ACCEPTCONN"></span><span id="so_acceptconn"></span>\_ACCEPTCONN

BOOL

Le socket est à l’écoute.

FALSe, sauf si un [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)) a été exécuté.

<span id="SO_BROADCAST"></span><span id="so_broadcast"></span>\_diffusion

BOOL

Le socket est configuré pour la transmission et la réception des messages de diffusion.

FALSE

<span id="SO_DEBUG"></span><span id="so_debug"></span>\_Déboguer

BOOL

Le débogage est activé.

FALSE

cliqu

<span id="SO_DONTLINGER"></span><span id="so_dontlinger"></span>\_DONTLINGER

BOOL

Si la valeur est true, l’option si oui \_ est désactivée.

TRUE

<span id="SO_DONTROUTE"></span><span id="so_dontroute"></span>\_DONTROUTE

BOOL

Le routage est désactivé. Réussit mais est ignoré sur \_ les sockets d’inet AF ; échoue sur \_ les sockets de l’aide de [WSAENOPROTOOPT](windows-sockets-error-codes-2.md). Non pris en charge sur les sockets ATM (génère une erreur).

FALSE

cliqu

<span id="SO_ERROR"></span><span id="so_error"></span>\_erreur

int

Récupère l’état d’erreur et l’efface.

0

<span id="SO_GROUP_ID"></span><span id="so_group_id"></span>\_ID de groupe \_

GROUP

Réservé.

NULL

Récupérer uniquement

<span id="SO_GROUP_PRIORITY"></span><span id="so_group_priority"></span>\_priorité de groupe \_

int

Réservé.

0

[**\_KeepAlive**](so-keepalive.md)

BOOL

Les KeepAlive sont envoyées. Non pris en charge sur les sockets ATM (génère une erreur).

FALSE

cliqu

<span id="SO_LINGER"></span><span id="so_linger"></span>DONC \_

Lingo de structure

Retourne les options de Lingo actuelles.

l \_ microphone est 0

<span id="SO_MAX_MSG_SIZE"></span><span id="so_max_msg_size"></span>\_taille maximale des \_ messages \_

int

Taille maximale sortante d’un message pour les types de sockets de message. Il n’existe aucune provision pour déterminer la taille maximale du message entrant. N’a aucune signification pour les sockets orientés flux.

Dépend de l’implémentation

Récupérer uniquement

<span id="SO_OOBINLINE"></span><span id="so_oobinline"></span>\_OOBINLINE

BOOL

Les données OOB sont reçues dans le flux de données normal.

FALSE

<span id="SO_PROTOCOL_INFOW"></span><span id="so_protocol_infow"></span>\_INFOW de protocole \_

[ **\_ informations sur** la structure WSAPROTOCOL](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa)

Description des informations de protocole pour le protocole qui est lié à ce Socket.

Dépendant du protocole

Récupérer uniquement

<span id="SO_RCVBUF"></span><span id="so_rcvbuf"></span>\_RCVBUF

int

Espace de la mémoire tampon par socket total réservé aux réceptions. Cela n’est pas lié à \_ \_ \_ la taille de message maximale et ne correspond pas nécessairement à la taille de la fenêtre de réception TCP.

Dépend de l’implémentation

cliqu

<span id="SO_REUSEADDR"></span><span id="so_reuseaddr"></span>\_REUSEADDR

BOOL

L’adresse à laquelle ce Socket est lié peut être utilisée par d’autres. Non applicable sur les sockets ATM.

FALSE

<span id="SO_SNDBUF"></span><span id="so_sndbuf"></span>\_SNDBUF

int

Espace de mémoire tampon par socket total réservé aux envois. Cela n’est pas lié à \_ \_ \_ la taille de message maximale et ne correspond pas nécessairement à la taille d’une fenêtre d’envoi TCP.

Dépend de l’implémentation

cliqu

<span id="SO_TYPE"></span><span id="so_type"></span>\_type

int

Type du socket (par exemple, flux de chaussette \_ ).

Tel qu’il a été créé via le Socket.

<span id="PVD_CONFIG"></span><span id="pvd_config"></span>configuration de PVD \_

caractère FAR \*

Objet de structure de données opaque contenant les informations de configuration du fournisseur de services.

Dépend de l’implémentation

<span id="TCP_NODELAY"></span><span id="tcp_nodelay"></span>TCP- \_ délai

BOOL

Désactive l'algorithme Nagle pour la fusion des envois.

Dépend de l’implémentation

(i) un fournisseur de services peut ignorer cette option en mode silencieux sur [**WSPSetSockOpt**](/previous-versions/windows/hardware/network/ff566318(v=vs.85)) et retourner une valeur constante pour [**WSPGetSockOpt**](/previous-versions/windows/hardware/network/ff566292(v=vs.85)), ou il peut accepter une valeur pour **WSPSetSockOpt** et retourner la valeur correspondante dans **WSPGetSockOpt** sans utiliser la valeur de quelque manière que ce soit.



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Options de socket**](socket-options.md)
</dt> <dt>

[**Options de socket de socket SOL \_**](sol-socket-socket-options.md)
</dt> <dt>

[**\_Options de socket TCP IPPROTO**](ipproto-tcp-socket-options.md)
</dt> <dt>

[**\_Options de socket UDP IPPROTO**](ipproto-udp-socket-options.md)
</dt> <dt>

[**IOCTL Winsock**](winsock-ioctls.md)
</dt> </dl>

 

 
