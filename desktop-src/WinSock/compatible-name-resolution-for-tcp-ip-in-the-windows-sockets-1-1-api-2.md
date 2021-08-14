---
description: notez que toutes les fonctions de Windows sockets 1,1 pour la résolution de noms sont spécifiques aux réseaux TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: résolution de noms Compatible pour TCP/IP dans l’API Windows sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13dfb1a403f782d0349e20729117fe1f4aed01479b01a6c2b5968f1d9bf15f38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322299"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a>résolution de noms Compatible pour TCP/IP dans l’API Windows sockets 1,1

> [!Note]  
> toutes les fonctions de Windows sockets 1,1 pour la résolution de noms sont spécifiques aux réseaux TCP/IP IPv4. Les développeurs d’applications sont fortement déconseillés de continuer à utiliser ces fonctions spécifiques au transport qui prennent uniquement en charge IPv4.

 

Les développeurs d’applications doivent utiliser les fonctions suivantes indépendantes du protocole et prendre en charge la résolution de noms IPv6 et IPv4.

-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [**API getaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

Windows Les sockets 1,1 définissaient un certain nombre de routines utilisées pour la résolution de noms avec des réseaux TCP/IP (IP version 4). Celles-ci sont parfois appelées fonctions **getXbyY** et incluent les éléments suivants :

<dl>

[**GetHostName**](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[**getprotobyname**](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[**getprotobynumber**](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[**getservbyname**](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[**getservbyport**](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

Les versions asynchrones de ces fonctions ont également été définies.

<dl>

[**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[**WSAAsyncGetProtoByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[**WSAAsyncGetProtoByNumber**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[**WSAAsyncGetServByName**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[**WSAAsyncGetServByPort**](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

Il existe également deux fonctions, qui sont désormais implémentées dans le Winsock2.dll, utilisées pour convertir la notation d’adresse IPv4 en deux points vers et à partir de représentations de chaîne et binaire, respectivement.

<dl>

[**\_ADR inet**](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

afin de conserver une compatibilité descendante stricte avec Windows sockets 1,1, toutes les anciennes fonctions IPv4 uniquement continuent à être prises en charge tant qu’au moins un fournisseur d’espace de noms est présent et prend en charge la \_ famille d’adresses d’INET af (ces fonctions ne sont pas pertinentes pour la version IP 6, dénotée par AF \_ INET6).

Le \_32.dll Ws2 implémente ces fonctions de compatibilité en termes de nouvelles fonctionnalités de résolution de noms indépendantes du protocole à l’aide d' [](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)une séquence appropriée d' /  / appels de fonction **end** Next WSALookupServiceBegin. Les détails de la façon dont les fonctions **getXbyY** sont mappées aux fonctions de résolution de noms sont fournis ci-dessous. L' \_32.dll WSs2 gère les différences entre les versions asynchrone et synchrone des fonctions **getXbyY** , de sorte que seule l’implémentation des fonctions **getXbyY** synchrones est présentée.

cette section décrit la résolution de noms compatible pour TCP/IP dans l’API Windows sockets 1,1. La liste suivante décrit les rubriques de cette section :

-   [Approche de base pour GetXbyY dans l’API](basic-approach-for-getxbyy-in-the-api-2.md)
-   [Fonctions getprotobyname et getprotobynumber dans l’API](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [Fonctions getservbyname et getservbyport dans l’API](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [Fonction gethostbyname dans l’API](gethostbyname-function-in-the-api-2.md)
-   [Fonction gethostbyaddr dans l’API](gethostbyaddr-function-in-the-api-2.md)
-   [GetHostName fonction dans l’API](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution de noms indépendante du protocole](protocol-independent-name-resolution-2.md)
</dt> <dt>

[Inscription et résolution de noms](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
