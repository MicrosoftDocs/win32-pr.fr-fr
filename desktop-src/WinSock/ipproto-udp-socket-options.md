---
description: Le tableau suivant décrit les \_ options de socket UDP IPPROTO qui s’appliquent aux sockets créés pour les familles d’adresses IPv4 et IPv6 (AF \_ inet et AF \_ inet6) avec le paramètre de protocole à la fonction de socket spécifiée comme UDP (IPPROTO \_ UDP).
ms.assetid: 579448a1-22af-488f-a1f5-97ba69a15524
title: IPPROTO_UDP socket, options
ms.topic: article
ms.date: 10/02/2019
ms.openlocfilehash: 763e45a78ffd8bfed15d09f4e77bc17be71ccc110499d8937b60b49294f499c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051477"
---
# <a name="ipproto_udp-socket-options"></a>\_Options de socket UDP IPPROTO

Le tableau suivant décrit les options de socket **\_ UDP IPPROTO** qui s’appliquent aux sockets créés pour les familles d’adresses IPv4 et IPv6 (AF \_ inet et AF \_ inet6) avec le paramètre de *protocole* à la fonction de [**Socket**](/windows/win32/api/Winsock2/nf-winsock2-socket) spécifiée comme UDP (IPPROTO \_ UDP). Consultez les pages de référence des fonctions [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) et [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) pour plus d’informations sur l’obtention et la définition des options de Socket.

Pour énumérer les protocoles et découvrir les propriétés prises en charge pour chaque protocole installé, utilisez la fonction [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa), [**WSCEnumProtocols**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols)ou [**WSCEnumProtocols32**](/windows/win32/api/Ws2spi/nf-ws2spi-wscenumprotocols32) .

## <a name="options"></a>Options

| Option | Obtenir | Définissez | Type Optval | Description |
|-|-|-|-|-|
| \_Couverture de la somme de contrôle Udp \_ (ws2tcpip. h) | oui | oui | DWORD (booléen) | Lorsque la **valeur est true**, les datagrammes UDP sont envoyés avec une somme de contrôle. |
| UDP \_ NOcheckes (ws2tcpip. h) | oui | oui | DWORD (booléen) | Lorsque la **valeur est true**, les datagrammes UDP sont envoyés avec la somme de contrôle égale à zéro. Requis pour les fournisseurs de services. Si un fournisseur de services ne dispose pas d’un mécanisme permettant de désactiver le calcul de la somme de contrôle UDP, il peut simplement stocker cette option sans entreprendre aucune action. Cette option n’est pas prise en charge pour IPv6. |
| UDP_RECV_MAX_COALESCED_SIZE (ws2ipdef. h ; include ws2tcpip. h) | oui | oui | DWORD | Lorsqu’il est défini sur une valeur différente de zéro, plusieurs Datagrammes reçus peuvent être fusionnés dans une mémoire tampon de messages unique avant d’être signalés à votre application. La valeur de l’option représente la taille maximale du message, en octets, pour les messages fusionnés qui peuvent être indiqués à votre application. Les messages non fusionnés supérieurs à la valeur de l’option peuvent toujours être indiqués. La valeur par défaut est 0 (aucune fusion). Les datagrammes sont fusionnés uniquement s’ils proviennent de la même adresse source et du même port. Tous les datagrammes fusionnés auront la même taille &mdash; , sauf le dernier datagramme, qui peut être plus petit. Si votre application souhaite récupérer les tailles des datagrammes (à l’exception du dernier datagramme, qui peut différer) qui ont été fusionnés, vous devez utiliser une API de réception qui prend en charge les informations de contrôle (par exemple, [**LPFN_WSARECVMSG (WSARECVMSG)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg)). La taille de tous les messages sauf le dernier se trouve dans le message de contrôle **UDP_COALESCED_INFO** , qui est de type DWORD. Pour la sécurité de type, votre application doit utiliser les fonctions [WSAGetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) et [WSASetUdpRecvMaxCoalescedSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) au lieu de l’option de socket directement. |
| UDP_SEND_MSG_SIZE (ws2ipdef. h ; include ws2tcpip. h) | oui | oui | DWORD | Lorsqu’elle est définie sur une valeur différente de zéro, les mémoires tampons envoyées par votre application sont réparties en plusieurs messages par la pile de mise en réseau. La valeur de l’option représente la taille de chaque message interrompu. La valeur de l’option est représentée en octets. La taille du dernier segment peut être inférieure à la valeur de l’option. La valeur par défaut est 0 (aucune segmentation). Votre application doit définir une valeur inférieure à la MTU du chemin d’accès aux destinations afin d’éviter la fragmentation IP. Pour la sécurité de type, votre application doit utiliser les fonctions [WSAGetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) et [WSASetUdpSendMessageSize](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) au lieu de l’option de socket directement. |

## <a name="legacy-windows-support-for-ipproto_udp-options"></a>prise en charge des Windows héritées pour les \_ options UDP IPPROTO

**UDP \_ la \_ couverture** de la somme de contrôle n’est pas disponible sur Windows 2000 et sur Windows NT4. **UDP \_ la \_ couverture de somme de contrôle** et les **\_ nochecks UDP** ne sont pas disponibles sur Windows 9x/Me. 

## <a name="remarks"></a>Remarques

dans le kit de développement logiciel (SDK) Microsoft Windows publié pour Windows Vista et versions ultérieures, l’organisation des fichiers d’en-tête a changé et le niveau **IPPROTO \_ UDP** est défini dans le fichier d’en-tête *Ws2def. h* qui est automatiquement inclus dans le fichier d’en-tête *Winsock2. h* . Les options de socket **\_ UDP IPPROTO** sont définies dans le fichier d’en-tête *Ws2tcpip. h* . Le fichier d’en-tête *Ws2def. h* ne doit jamais être utilisé directement.

## <a name="requirements"></a>Configuration requise

| Condition requise | Valeur |
|-|-|
| En-tête<br/> | <dl> <dt>ws2ipdef. h (include ws2tcpip. h) et ws2tcpip. h</dt> <dt>Winsock2. h sur Windows Server 2003, Windows XP et Windows 2000</dt> </dl> |
