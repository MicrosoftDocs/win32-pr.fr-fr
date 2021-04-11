---
description: Prise en charge D’ipv6, TCP/IP annexe et Windows Sockets.
ms.assetid: 03e29ef1-2105-4cec-8b80-0f9acab046f6
title: Prise en charge D’ipv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0ffc720a41c896653c74df2cb76f944cbbb310a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113051"
---
# <a name="ipv6-support"></a><span data-ttu-id="6b95f-103">Prise en charge D’ipv6</span><span class="sxs-lookup"><span data-stu-id="6b95f-103">IPv6 Support</span></span>

<span data-ttu-id="6b95f-104">Pour prendre en charge à la fois IPv4 et IPv6 sur Windows XP avec Service Pack 1 (SP1) et sur Windows Server 2003, une application doit créer deux sockets, un socket à utiliser avec IPv4 et un socket pour une utilisation avec IPv6.</span><span class="sxs-lookup"><span data-stu-id="6b95f-104">In order to support both IPv4 and IPv6 on Windows XP with Service Pack 1 (SP1) and on Windows Server 2003, an application has to create two sockets, one socket for use with IPv4 and one socket for use with IPv6.</span></span> <span data-ttu-id="6b95f-105">Ces deux sockets doivent être gérés séparément par l’application.</span><span class="sxs-lookup"><span data-stu-id="6b95f-105">These two sockets must be handled separately by the application.</span></span>

<span data-ttu-id="6b95f-106">Si un fournisseur de services TCP/IP sur Windows XP avec SP1 et sur Windows Server 2003 prend en charge l’adressage IPv4 et IPv6, il doit créer deux sockets distincts et écouter séparément sur ces Sockets :</span><span class="sxs-lookup"><span data-stu-id="6b95f-106">If a TCP/IP service provider on Windows XP with SP1 and on Windows Server 2003 supports IPv4 and IPv6 addressing, it must create two separate sockets and listen separately on these sockets:</span></span>

-   <span data-ttu-id="6b95f-107">Une fois pour IPv4.</span><span class="sxs-lookup"><span data-stu-id="6b95f-107">Once for IPv4.</span></span>
-   <span data-ttu-id="6b95f-108">Une fois pour la famille d’adresses IPv6.</span><span class="sxs-lookup"><span data-stu-id="6b95f-108">Once for the IPv6 address family.</span></span>

<span data-ttu-id="6b95f-109">Windows Vista et les versions ultérieures offrent la possibilité de créer un seul socket IPv6 pouvant gérer à la fois le trafic IPv6 et IPv4.</span><span class="sxs-lookup"><span data-stu-id="6b95f-109">Windows Vista and later offer the ability to create a single IPv6 socket which can handle both IPv6 and IPv4 traffic.</span></span> <span data-ttu-id="6b95f-110">Par exemple, un socket d’écoute TCP pour IPv6 est créé, placé en mode pile double et lié au port 5001.</span><span class="sxs-lookup"><span data-stu-id="6b95f-110">For example, a TCP listening socket for IPv6 is created, put into dual stack mode, and bound to port 5001.</span></span> <span data-ttu-id="6b95f-111">Ce socket à double pile peut accepter les connexions des clients TCP IPv6 se connectant au port 5001 et à partir de clients TCP IPv4 se connectant au port 5001.</span><span class="sxs-lookup"><span data-stu-id="6b95f-111">This dual-stack socket can accept connections from IPv6 TCP clients connecting to port 5001 and from IPv4 TCP clients connecting to port 5001.</span></span> <span data-ttu-id="6b95f-112">Cette fonctionnalité permet une conception d’application considérablement simplifiée et réduit la charge de ressources requise pour la publication d’opérations sur deux sockets distincts.</span><span class="sxs-lookup"><span data-stu-id="6b95f-112">This feature allows for greatly simplified application design and reduces the resource overhead required of posting operations on two separate sockets.</span></span> <span data-ttu-id="6b95f-113">Toutefois, il existe des restrictions qui doivent être satisfaites pour pouvoir utiliser un socket à double pile.</span><span class="sxs-lookup"><span data-stu-id="6b95f-113">However, there are some restrictions that must be met in order to use a dual-stack socket.</span></span> <span data-ttu-id="6b95f-114">Pour plus d’informations, consultez [sockets à double pile](dual-stack-sockets.md).</span><span class="sxs-lookup"><span data-stu-id="6b95f-114">For more information, see [Dual-Stack Sockets](dual-stack-sockets.md).</span></span>

<span data-ttu-id="6b95f-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) retourne deux structures d' [**\_ informations WSAPROTOCOL**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) pour chacun des types de socket pris en charge ( \_ flux de chaussette, chaussette \_ DGRAM, chaussette \_ RAW).</span><span class="sxs-lookup"><span data-stu-id="6b95f-115">[**WSAEnumProtocols**](/windows/desktop/api/Winsock2/nf-winsock2-wsaenumprotocolsa) returns two [**WSAPROTOCOL\_INFO**](/windows/win32/api/winsock2/ns-winsock2-wsaprotocol_infoa) structures for each of the supported socket types (SOCK\_STREAM, SOCK\_DGRAM, SOCK\_RAW).</span></span> <span data-ttu-id="6b95f-116">Le **iAddressFamily** doit être défini sur AF \_ inet pour l’adressage IPv4 et sur AF \_ inet6 pour l’adressage IPv6.</span><span class="sxs-lookup"><span data-stu-id="6b95f-116">The **iAddressFamily** must by set to AF\_INET for IPv4 addressing, and to AF\_INET6 for IPv6 addressing.</span></span>

<span data-ttu-id="6b95f-117">Les adresses IPv6 sont décrites dans les structures suivantes.</span><span class="sxs-lookup"><span data-stu-id="6b95f-117">The IPv6 addresses are described in the following structures.</span></span>

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

<span data-ttu-id="6b95f-118">Si une application utilise des fonctions Windows Sockets 1,1 et souhaite utiliser des adresses IPv6, elle peut continuer à utiliser toutes les anciennes fonctions qui utilisent la structure [**sockaddr**](sockaddr-2.md) comme l’un des paramètres ([**Bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto)et [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), etc.).</span><span class="sxs-lookup"><span data-stu-id="6b95f-118">If an application uses Windows Sockets 1.1 functions and wants to use IPv6 addresses, it may continue to use all the old functions that take the [**sockaddr**](sockaddr-2.md) structure as one of the parameters ([**bind**](/windows/desktop/api/winsock/nf-winsock-bind), [**connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect), [**sendto**](/windows/desktop/api/winsock/nf-winsock-sendto), and [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom), [**accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept), and so forth).</span></span> <span data-ttu-id="6b95f-119">La seule modification requise consiste à utiliser **sockaddr \_ in6** au lieu de **sockaddr \_ dans**.</span><span class="sxs-lookup"><span data-stu-id="6b95f-119">The only change that is required is to use **sockaddr\_in6** instead of **sockaddr\_in**.</span></span>

<span data-ttu-id="6b95f-120">Toutefois, les fonctions de résolution de noms ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), etc.) et les fonctions de conversion d’adresses ([**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet \_ NTOA**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) ne peuvent pas être réutilisées, car elles supposent une adresse IP d’une longueur de 4 octets.</span><span class="sxs-lookup"><span data-stu-id="6b95f-120">However, the name resolution functions ([**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and so forth) and address conversion functions ([**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr), [**inet\_ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)) cannot be reused because they assume an IP address is 4 bytes in length.</span></span> <span data-ttu-id="6b95f-121">Une application qui souhaite effectuer la résolution de noms et la conversion d’adresses pour les adresses IPv6 doit utiliser des fonctions spécifiques de Windows Sockets 2.</span><span class="sxs-lookup"><span data-stu-id="6b95f-121">An application that wants to perform name resolution and address conversion for IPv6 addresses must use Windows Sockets 2-specific functions.</span></span> <span data-ttu-id="6b95f-122">De nombreuses nouvelles fonctions ont été introduites pour permettre aux applications Windows Sockets 2 de tirer parti du protocole IPv6, y compris les fonctions [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) et [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="6b95f-122">Many new functions have been introduced to enable Windows Sockets 2 applications to take advantage of IPv6, including the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

<span data-ttu-id="6b95f-123">Pour plus d’informations sur l’activation des fonctionnalités IPv6 dans une application, consultez le [Guide IPv6 pour les applications Windows Sockets](ipv6-guide-for-windows-sockets-applications-2.md).</span><span class="sxs-lookup"><span data-stu-id="6b95f-123">For more information on how to enable IPv6 capabilities in an application, see the [IPv6 Guide for Windows Sockets Applications](ipv6-guide-for-windows-sockets-applications-2.md).</span></span>

 

 
