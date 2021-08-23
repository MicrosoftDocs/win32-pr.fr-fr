---
description: prise en charge d’ipv6, TCP/IP annexe et Windows sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Prise en charge D’ipv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f48e5b46ef1fcf1a2257db4a04b5435443552bb49f6c3c2b2dc4784077dcbd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794799"
---
# <a name="ipv6-support"></a>Prise en charge D’ipv6

pour prendre en charge à la fois IPv4 et IPv6 sur Windows XP avec Service Pack 1 (SP1) et sur Windows Server 2003, une application doit créer deux sockets, un socket à utiliser avec IPv4 et un socket pour une utilisation avec IPv6. Ces deux sockets doivent être gérés séparément par l’application.

si un fournisseur de services TCP/IP sur Windows XP avec SP1 et sur Windows Server 2003 prend en charge l’adressage IPv4 et IPv6, il doit créer deux sockets distincts et écouter séparément sur ces sockets :

-   Une fois pour IPv4.
-   Une fois pour la famille d’adresses IPv6.

Windows Vista et les versions ultérieures offrent la possibilité de créer un seul socket IPv6 pouvant gérer le trafic IPv6 et IPv4. Par exemple, un socket d’écoute TCP pour IPv6 est créé, placé en mode pile double et lié au port 5001. Ce socket à double pile peut accepter les connexions des clients TCP IPv6 se connectant au port 5001 et à partir de clients TCP IPv4 se connectant au port 5001. Cette fonctionnalité permet une conception d’application considérablement simplifiée et réduit la charge de ressources requise pour la publication d’opérations sur deux sockets distincts. Toutefois, il existe des restrictions qui doivent être satisfaites pour pouvoir utiliser un socket à double pile. Pour plus d’informations, consultez [sockets à double pile](dual-stack-sockets.md).

[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) retourne deux structures d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour chacun des types de socket pris en charge ( \_ flux de chaussette, chaussette \_ DGRAM, chaussette \_ RAW). Le **iAddressFamily** doit être défini sur AF \_ inet pour l’adressage IPv4 et sur AF \_ inet6 pour l’adressage IPv6.

Les adresses IPv6 sont décrites dans les structures suivantes.

``` syntax
struct in_addr6 {
    u_char    s6_addr[16];             /* IPv6 address */
};

struct sockaddr_in6 {
    short             sin6_family;     /* AF_INET6 */
    u_short           sin6_port;       /* Transport level port number */
    u_long            sin6_flowinfo;   /* IPv6 flow information */
    struct in_addr6   sin6_addr;       /* IPv6 address */
    u_long            sin6_scope_id;   /* set of interfaces for a scope */
   };
```

si une application utilise Windows fonctions sockets 1,1 et souhaite utiliser des adresses IPv6, elle peut continuer à utiliser toutes les anciennes fonctions qui utilisent la structure [**sockaddr**](sockaddr-2.md) comme l’un des paramètres ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)et [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), etc.). La seule modification requise consiste à utiliser **sockaddr \_ in6** au lieu de **sockaddr \_ dans**.

Toutefois, les fonctions de résolution de noms ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), etc.) et les fonctions de conversion d’adresses ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) ne peuvent pas être réutilisées, car elles supposent une adresse IP d’une longueur de 4 octets. une application qui souhaite effectuer la résolution de noms et la conversion d’adresses pour les adresses IPv6 doit utiliser des fonctions spécifiques à Windows sockets 2. de nombreuses nouvelles fonctions ont été introduites pour permettre à Windows applications sockets 2 de tirer parti du protocole IPv6, y compris les fonctions [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .

pour plus d’informations sur l’activation des fonctionnalités ipv6 dans une application, consultez le [Guide ipv6 pour les Applications Windows sockets](ipv6-guide-for-windows-sockets-applications-2.md).

 

 
