---
description: Notez que toutes les fonctions Windows Sockets 1,1 pour la résolution de noms sont spécifiques aux réseaux TCP/IP IPv4.
ms.assetid: 5a2a37f3-85c5-4b27-9ce3-f5b707b1564a
title: Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2447590b25861abc80bd0a89be173272fb809814
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519301"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-api"></a><span data-ttu-id="18fd6-103">Résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="18fd6-103">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 API</span></span>

> [!Note]  
> <span data-ttu-id="18fd6-104">Toutes les fonctions Windows Sockets 1,1 pour la résolution de noms sont spécifiques aux réseaux TCP/IP IPv4.</span><span class="sxs-lookup"><span data-stu-id="18fd6-104">All of the Windows Sockets 1.1 functions for name resolution are specific to IPv4 TCP/IP networks.</span></span> <span data-ttu-id="18fd6-105">Les développeurs d’applications sont fortement déconseillés de continuer à utiliser ces fonctions spécifiques au transport qui prennent uniquement en charge IPv4.</span><span class="sxs-lookup"><span data-stu-id="18fd6-105">Application developers are strongly discouraged from continuing to utilize these transport-specific functions that only support IPv4.</span></span>

 

<span data-ttu-id="18fd6-106">Les développeurs d’applications doivent utiliser les fonctions suivantes indépendantes du protocole et prendre en charge la résolution de noms IPv6 et IPv4.</span><span class="sxs-lookup"><span data-stu-id="18fd6-106">Application developers should be using the following functions that are protocol-independent and support both IPv6 and IPv4 name resolution.</span></span>

-   [<span data-ttu-id="18fd6-107">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="18fd6-107">**getaddrinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)
-   [<span data-ttu-id="18fd6-108">**API getaddrinfoex**</span><span class="sxs-lookup"><span data-stu-id="18fd6-108">**GetAddrInfoEx**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa)
-   [<span data-ttu-id="18fd6-109">**GetAddrInfoW**</span><span class="sxs-lookup"><span data-stu-id="18fd6-109">**GetAddrInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow)
-   [<span data-ttu-id="18fd6-110">**getnameinfo**</span><span class="sxs-lookup"><span data-stu-id="18fd6-110">**getnameinfo**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
-   [<span data-ttu-id="18fd6-111">**GetNameInfoW**</span><span class="sxs-lookup"><span data-stu-id="18fd6-111">**GetNameInfoW**</span></span>](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow)

<span data-ttu-id="18fd6-112">Windows Sockets 1,1 définissait un certain nombre de routines utilisées pour la résolution de noms avec des réseaux TCP/IP (IP version 4).</span><span class="sxs-lookup"><span data-stu-id="18fd6-112">Windows Sockets 1.1 defined a number of routines used for name resolution with TCP/IP (IP version 4) networks.</span></span> <span data-ttu-id="18fd6-113">Celles-ci sont parfois appelées fonctions **getXbyY** et incluent les éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="18fd6-113">These are sometimes called the **getXbyY** functions and include the following:</span></span>

<dl>

[<span data-ttu-id="18fd6-114">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="18fd6-114">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)  
[<span data-ttu-id="18fd6-115">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="18fd6-115">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)  
[<span data-ttu-id="18fd6-116">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="18fd6-116">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)  
[<span data-ttu-id="18fd6-117">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="18fd6-117">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)  
[<span data-ttu-id="18fd6-118">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="18fd6-118">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)  
[<span data-ttu-id="18fd6-119">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="18fd6-119">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)  
[<span data-ttu-id="18fd6-120">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="18fd6-120">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)  
</dl>

<span data-ttu-id="18fd6-121">Les versions asynchrones de ces fonctions ont également été définies.</span><span class="sxs-lookup"><span data-stu-id="18fd6-121">Asynchronous versions of these functions were also defined.</span></span>

<dl>

[<span data-ttu-id="18fd6-122">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="18fd6-122">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)  
[<span data-ttu-id="18fd6-123">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="18fd6-123">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)  
[<span data-ttu-id="18fd6-124">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="18fd6-124">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)  
[<span data-ttu-id="18fd6-125">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="18fd6-125">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)  
[<span data-ttu-id="18fd6-126">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="18fd6-126">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)  
[<span data-ttu-id="18fd6-127">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="18fd6-127">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)  
</dl>

<span data-ttu-id="18fd6-128">Il existe également deux fonctions, qui sont désormais implémentées dans le Winsock2.dll, utilisées pour convertir la notation d’adresse IPv4 en deux points vers et à partir de représentations de chaîne et binaire, respectivement.</span><span class="sxs-lookup"><span data-stu-id="18fd6-128">There are also two functions, now implemented in the Winsock2.dll, used to convert dotted Ipv4 address notation to and from string and binary representations, respectively.</span></span>

<dl>

[<span data-ttu-id="18fd6-129">**\_ADR inet**</span><span class="sxs-lookup"><span data-stu-id="18fd6-129">**inet\_addr**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_addr)  
[<span data-ttu-id="18fd6-130">**inet \_ NTOA**</span><span class="sxs-lookup"><span data-stu-id="18fd6-130">**inet\_ntoa**</span></span>](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa)  
</dl>

<span data-ttu-id="18fd6-131">Afin de conserver une compatibilité descendante stricte avec Windows Sockets 1,1, toutes les anciennes fonctions IPv4 uniquement continuent d’être prises en charge tant qu’au moins un fournisseur d’espace de noms est présent et prend en charge la \_ famille d’adresses d’inet AF (ces fonctions ne sont pas pertinentes pour la version IP 6, indiquée par AF \_ inet6).</span><span class="sxs-lookup"><span data-stu-id="18fd6-131">In order to retain strict backward compatibility with Windows Sockets 1.1, all of the older IPv4-only functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family (these functions are not relevant to IP version 6, denoted by AF\_INET6).</span></span>

<span data-ttu-id="18fd6-132">Le \_32.dll Ws2 implémente ces fonctions de compatibilité en termes de nouvelles fonctionnalités de résolution de noms indépendantes du protocole à l’aide d' [](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)une séquence appropriée d' /  / appels de fonction **end** Next WSALookupServiceBegin.</span><span class="sxs-lookup"><span data-stu-id="18fd6-132">The Ws2\_32.dll implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina)/**Next**/**End** function calls.</span></span> <span data-ttu-id="18fd6-133">Les détails de la façon dont les fonctions **getXbyY** sont mappées aux fonctions de résolution de noms sont fournis ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="18fd6-133">The details of how the **getXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="18fd6-134">L' \_32.dll WSs2 gère les différences entre les versions asynchrone et synchrone des fonctions **getXbyY** , de sorte que seule l’implémentation des fonctions **getXbyY** synchrones est présentée.</span><span class="sxs-lookup"><span data-stu-id="18fd6-134">The WSs2\_32.dll handles the differences between the asynchronous and synchronous versions of the **getXbyY** functions, so only the implementation of the synchronous **getXbyY** functions are discussed.</span></span>

<span data-ttu-id="18fd6-135">Cette section décrit la résolution de noms compatible pour TCP/IP dans l’API Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="18fd6-135">This section describes compatible name resolution for TCP/IP in the Windows Sockets 1.1 API.</span></span> <span data-ttu-id="18fd6-136">La liste suivante décrit les rubriques de cette section :</span><span class="sxs-lookup"><span data-stu-id="18fd6-136">The following list describes the topics in this section:</span></span>

-   [<span data-ttu-id="18fd6-137">Approche de base pour GetXbyY dans l’API</span><span class="sxs-lookup"><span data-stu-id="18fd6-137">Basic Approach for GetXbyY in the API</span></span>](basic-approach-for-getxbyy-in-the-api-2.md)
-   [<span data-ttu-id="18fd6-138">Fonctions getprotobyname et getprotobynumber dans l’API</span><span class="sxs-lookup"><span data-stu-id="18fd6-138">getprotobyname and getprotobynumber Functions in the API</span></span>](getprotobyname-and-getprotobynumber-functions-in-the-api-2.md)
-   [<span data-ttu-id="18fd6-139">Fonctions getservbyname et getservbyport dans l’API</span><span class="sxs-lookup"><span data-stu-id="18fd6-139">getservbyname and getservbyport Functions in the API</span></span>](getservbyname-and-getservbyport-functions-in-the-api-2.md)
-   [<span data-ttu-id="18fd6-140">Fonction gethostbyname dans l’API</span><span class="sxs-lookup"><span data-stu-id="18fd6-140">gethostbyname Function in the API</span></span>](gethostbyname-function-in-the-api-2.md)
-   [<span data-ttu-id="18fd6-141">Fonction gethostbyaddr dans l’API</span><span class="sxs-lookup"><span data-stu-id="18fd6-141">gethostbyaddr Function in the API</span></span>](gethostbyaddr-function-in-the-api-2.md)
-   [<span data-ttu-id="18fd6-142">GetHostName fonction dans l’API</span><span class="sxs-lookup"><span data-stu-id="18fd6-142">gethostname Function in the API</span></span>](gethostname-function-in-the-api-2.md)

## <a name="related-topics"></a><span data-ttu-id="18fd6-143">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="18fd6-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="18fd6-144">Résolution de noms indépendante du protocole</span><span class="sxs-lookup"><span data-stu-id="18fd6-144">Protocol-Independent Name Resolution</span></span>](protocol-independent-name-resolution-2.md)
</dt> <dt>

[<span data-ttu-id="18fd6-145">Inscription et résolution de noms</span><span class="sxs-lookup"><span data-stu-id="18fd6-145">Registration and Name Resolution</span></span>](registration-and-name-resolution-2.md)
</dt> </dl>

 

 
