---
description: pour prendre en charge à la fois IPv4 et IPv6 sur Windows XP avec Service Pack 1 (SP1) et sur Windows Server 2003, une application doit créer deux sockets, un socket à utiliser avec IPv4 et un socket pour une utilisation avec IPv6.
ms.assetid: 7ae49081-ffb5-4eee-b488-2541398e7acc
title: Dual-Stack Sockets pour les applications Winsock IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 424580569fb3bed5e81c6232cb99dc2d53a30af1ab2c23c9b4afa6945c0a6eb9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132662"
---
# <a name="dual-stack-sockets-for-ipv6-winsock-applications"></a>Dual-Stack Sockets pour les applications Winsock IPv6

pour prendre en charge à la fois IPv4 et IPv6 sur Windows XP avec Service Pack 1 (SP1) et sur Windows Server 2003, une application doit créer deux sockets, un socket à utiliser avec IPv4 et un socket pour une utilisation avec IPv6. Ces deux sockets doivent être gérés séparément par l’application.

Windows Vista et les versions ultérieures offrent la possibilité de créer un seul socket IPv6 pouvant gérer le trafic IPv6 et IPv4. Par exemple, un socket d’écoute TCP pour IPv6 est créé, placé en mode pile double et lié au port 5001. Ce socket à double pile peut accepter les connexions des clients TCP IPv6 se connectant au port 5001 et à partir de clients TCP IPv4 se connectant au port 5001. Cette fonctionnalité permet une conception d’application considérablement simplifiée et réduit la charge de ressources requise pour la publication d’opérations sur deux sockets distincts.

## <a name="creating-a-dual-stack-socket"></a>Création d’un socket Dual-Stack

par défaut, un socket ipv6 créé sur Windows Vista et versions ultérieures fonctionne uniquement via le protocole IPv6. Pour créer un socket IPv6 dans un socket à double pile, la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) doit être appelée avec l’option de socket **IPv6 \_ V6ONLY** pour définir cette valeur sur zéro avant que le socket ne soit lié à une adresse IP. Lorsque l’option de socket **IPv6 \_ V6ONLY** a la valeur zéro, un socket créé pour la famille d’adresses **\_ inet6** de la même façon peut être utilisé pour envoyer et recevoir des paquets vers et à partir d’une adresse IPv6 ou d’une adresse mappée IPv4.

## <a name="ip-addresses-with-a-dual-stack-socket"></a>Adresses IP avec un socket Dual-Stack

Les sockets à double pile nécessitent toujours des adresses IPv6. La possibilité d’interagir avec une adresse IPv4 nécessite l’utilisation du format d’adresse IPv6 mappée IPv4. Toutes les adresses IPv4 doivent être représentées dans le format d’adresse IPv6 mappée IPv4, ce qui permet à une application IPv6 uniquement de communiquer avec un nœud IPv4. Le format d’adresse IPv6 mappée IPv4 permet à l’adresse IPv4 d’un nœud IPv4 d’être représentée comme une adresse IPv6. L’adresse IPv4 est encodée dans les bits de poids faible 32 de l’adresse IPv6, et les bits de poids fort 96 contiennent le préfixe fixe 0:0 : 0:0 : 0 : FFFF. Le format d’adresse IPv6 mappée IPv4 est spécifié dans le document RFC 4291. Pour plus d’informations, consultez [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). La \_ macro IN6ADDR SETV4MAPPED dans *Mstcpip. h* peut être utilisée pour convertir une adresse IPv4 au format d’adresse IPv6 mappé IPv4 requis.

Si le protocole sous-jacent est en fait IPv4, l’adresse IPv4 est mappée dans un format d’adresse IPv6 mappée IPv4. Autrement dit, le champ Family de la structure [sockaddr](sockaddr-2.md) indique AF \_ inet6, mais une adresse IPv6 mappée IPv4 est encodée dans la structure d’adresse IPv6. Pour un socket à double pile en mode d’écoute, cela signifie que toutes les connexions IPv4 acceptées renverront une adresse IPv6 mappée IPv4. Pour un socket à double pile qui se connecte à une destination IPv4, la structure SOCKADDR transmise à la connexion doit être une adresse IPv6 mappée IPv4. Les applications doivent prendre soin de gérer ces adresses IPv6 mappées IPv4 de manière appropriée et de les utiliser uniquement avec des sockets à double pile. Si une adresse IP doit être transmise à un socket IPv4 standard, l’adresse doit être une adresse IPv4 normale et non une adresse IPv6 mappée IPv4.

## <a name="potential-issues-using-a-dual-stack-socket"></a>Problèmes potentiels à l’aide d’un socket Dual-Stack

Un piège potentiel pour les applications consiste à obtenir une adresse IPv6 mappée IPv4 sur un socket à double pile, puis à essayer d’utiliser l’adresse IP renvoyée sur un socket IPv6 différent. Par exemple, les fonctions [**GetSockName**](/windows/desktop/api/winsock/nf-winsock-getsockname) ou [**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername) peuvent retourner une adresse IPv6 mappée IPv4 lorsqu’elles sont utilisées sur un socket à double pile. Si l’adresse IPv6 mappée IPv4 renvoyée est ensuite utilisée sur un autre socket qui n’a pas été défini sur Double Stack (un socket IPv6 uniquement qui est le comportement par défaut lors de la création d’un socket), toute utilisation de ce Socket IPv6 uniquement avec une adresse IPv6 mappée IPv4 échoue. Le format d’adresse IPv6 mappée IPv4 ne peut être utilisé que sur un socket à double pile.

Sur un socket de datagramme à double pile, si une application requiert la fonction [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) pour retourner les informations de paquets dans une structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) pour les datagrammes reçus sur IPv4, l’option de socket [IP \_ PKTINFO](ip-pktinfo.md) doit avoir la valeur true sur le Socket. Si seule l’option [IPv6 \_ PKTINFO](ipv6-pktinfo.md) a la valeur true sur le socket, des informations de paquet sont fournies pour les datagrammes reçus via IPv6, mais elles peuvent ne pas être fournies pour les datagrammes reçus sur IPv4.

Si une application tente de définir l’option de socket [IP \_ PKTINFO](ip-pktinfo.md) sur un socket de datagramme à double pile et que IPv4 est désactivé sur le système, la fonction [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) échoue et [**WSAGetLastError**](/windows/desktop/api/winsock/nf-winsock-wsagetlasterror) retourne avec une erreur de [WSAEINVAL](windows-sockets-error-codes-2.md). Cette même erreur est également retournée par la fonction **setsockopt** à la suite d’autres erreurs. Si une application tente de définir une \_ option de socket de niveau IP IPPROTO sur un socket à double pile et échoue avec [WSAEINVAL](windows-sockets-error-codes-2.md), l’application doit déterminer si IPv4 est désactivé sur l’ordinateur local. Une méthode qui peut être utilisée pour détecter si IPv4 est activé ou désactivé consiste à appeler la fonction [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) avec le paramètre *AF* défini sur AF \_ inet pour essayer de créer un socket IPv4. Si la fonction **Socket** échoue et que **WSAGetLastError** retourne une erreur de [WSAEAFNOSUPPORT](windows-sockets-error-codes-2.md), cela signifie que IPv4 n’est pas activé. Dans ce cas, une fonction **setsockopt** ayant échoué lors de la tentative de définition de l' \_ option de socket IP PKTINFO peut être ignorée par l’application. Sinon, un échec lors de la tentative de définition de l' \_ option de socket PKTINFO IP doit être traité comme une erreur inattendue.

Pour un socket à double pile lors de l’envoi de datagrammes avec la fonction [**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) et où une application souhaite spécifier une adresse source IP locale spécifique à utiliser, la méthode pour gérer cela dépend de l’adresse IP de destination. Lors de l’envoi à une adresse de destination IPv4 ou à une adresse de destination IPv6 mappée IPv4, l’un des objets de données de contrôle transmis dans la structure [**WSAMSG**](/windows/desktop/api/Ws2def/ns-ws2def-wsamsg) vers laquelle pointe le paramètre *lpMsg* doit contenir une structure [**in \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo) contenant l’adresse source IPv4 locale à utiliser pour l’envoi. Lors de l’envoi à une adresse de destination IPv6 qui n’est pas une adresse IPv6 mappée IPv4, l’un des objets de données de contrôle transmis dans la structure **WSAMSG** vers laquelle pointe le paramètre *lpMsg* doit contenir une structure [**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo) contenant l’adresse source IPv6 locale à utiliser pour l’envoi.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide IPv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Modification des structures de données pour IPv6 Winsock appications](changing-data-structures-2.md)
</dt> <dt>

[Appels de fonction pour les applications Winsock IPv6](function-calls-2.md)
</dt> <dt>

[Utilisation d’adresses IPv4 codées en dur](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Problèmes d’interface utilisateur pour les applications Winsock IPv6](user-interface-issues-2.md)
</dt> <dt>

[Protocoles sous-jacents pour les applications Winsock IPv6](underlying-protocols-2.md)
</dt> <dt>

[**getpeername**](/windows/desktop/api/winsock/nf-winsock-getpeername)
</dt> <dt>

[**getsockname**](/windows/desktop/api/winsock/nf-winsock-getsockname)
</dt> <dt>

[**dans \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in_pktinfo)
</dt> <dt>

[**in6 \_ pktinfo**](/windows/desktop/api/Ws2ipdef/ns-ws2ipdef-in6_pktinfo)
</dt> <dt>

[\_PKTINFO IP](ip-pktinfo.md)
</dt> <dt>

[\_PKTINFO IPv6](ipv6-pktinfo.md)
</dt> <dt>

[**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt)
</dt> <dt>

[**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)
</dt> <dt>

[**WSASendMsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg)
</dt> </dl>

 

 
