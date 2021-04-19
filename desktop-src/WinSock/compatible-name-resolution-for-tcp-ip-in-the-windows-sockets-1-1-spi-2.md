---
description: Windows Sockets 1,1 a défini un certain nombre de routines qui ont été utilisées pour la résolution de noms IPv4 avec des réseaux TCP/IP. Ils sont habituellement appelés les fonctions GetXbyY et incluent les éléments suivants.
ms.assetid: 7a3ff7f3-d4b9-4900-8fd8-708a89c78c0a
title: Résolution de noms compatible pour TCP/IP dans le SPI Windows Sockets 1,1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3ca58f8868c17c9dad7c67fed083e9460272944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517270"
---
# <a name="compatible-name-resolution-for-tcpip-in-the-windows-sockets-11-spi"></a><span data-ttu-id="d7506-104">Résolution de noms compatible pour TCP/IP dans le SPI Windows Sockets 1,1</span><span class="sxs-lookup"><span data-stu-id="d7506-104">Compatible Name Resolution for TCP/IP in the Windows Sockets 1.1 SPI</span></span>

<span data-ttu-id="d7506-105">Windows Sockets 1,1 a défini un certain nombre de routines qui ont été utilisées pour la résolution de noms IPv4 avec des réseaux TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="d7506-105">Windows Sockets 1.1 defined a number of routines that were used for IPv4 name resolution with TCP/IP networks.</span></span> <span data-ttu-id="d7506-106">Ils sont habituellement appelés les fonctions **GetXbyY** et incluent les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="d7506-106">These are customarily called the **GetXbyY** functions and include the following.</span></span>

[<span data-ttu-id="d7506-107">**GetHostName**</span><span class="sxs-lookup"><span data-stu-id="d7506-107">**gethostname**</span></span>](/windows/desktop/api/winsock/nf-winsock-gethostname)

[<span data-ttu-id="d7506-108">**gethostbyaddr**</span><span class="sxs-lookup"><span data-stu-id="d7506-108">**gethostbyaddr**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)

[<span data-ttu-id="d7506-109">**gethostbyname**</span><span class="sxs-lookup"><span data-stu-id="d7506-109">**gethostbyname**</span></span>](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname)

[<span data-ttu-id="d7506-110">**getprotobyname**</span><span class="sxs-lookup"><span data-stu-id="d7506-110">**getprotobyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobyname)

[<span data-ttu-id="d7506-111">**getprotobynumber**</span><span class="sxs-lookup"><span data-stu-id="d7506-111">**getprotobynumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-getprotobynumber)

[<span data-ttu-id="d7506-112">**getservbyname**</span><span class="sxs-lookup"><span data-stu-id="d7506-112">**getservbyname**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyname)

[<span data-ttu-id="d7506-113">**getservbyport**</span><span class="sxs-lookup"><span data-stu-id="d7506-113">**getservbyport**</span></span>](/windows/desktop/api/winsock/nf-winsock-getservbyport)

<span data-ttu-id="d7506-114">Les versions asynchrones de ces fonctions ont également été définies.</span><span class="sxs-lookup"><span data-stu-id="d7506-114">Asynchronous versions of these functions were also defined.</span></span>

[<span data-ttu-id="d7506-115">**WSAAsyncGetHostByAddr**</span><span class="sxs-lookup"><span data-stu-id="d7506-115">**WSAAsyncGetHostByAddr**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr)

[<span data-ttu-id="d7506-116">**WSAAsyncGetHostByName**</span><span class="sxs-lookup"><span data-stu-id="d7506-116">**WSAAsyncGetHostByName**</span></span>](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname)

[<span data-ttu-id="d7506-117">**WSAAsyncGetProtoByName**</span><span class="sxs-lookup"><span data-stu-id="d7506-117">**WSAAsyncGetProtoByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobyname)

[<span data-ttu-id="d7506-118">**WSAAsyncGetProtoByNumber**</span><span class="sxs-lookup"><span data-stu-id="d7506-118">**WSAAsyncGetProtoByNumber**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetprotobynumber)

[<span data-ttu-id="d7506-119">**WSAAsyncGetServByName**</span><span class="sxs-lookup"><span data-stu-id="d7506-119">**WSAAsyncGetServByName**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyname)

[<span data-ttu-id="d7506-120">**WSAAsyncGetServByPort**</span><span class="sxs-lookup"><span data-stu-id="d7506-120">**WSAAsyncGetServByPort**</span></span>](/windows/desktop/api/winsock/nf-winsock-wsaasyncgetservbyport)

<span data-ttu-id="d7506-121">Ces fonctions sont spécifiques aux réseaux TCP/IP ; les développeurs d’applications indépendantes du protocole sont déconseillés de continuer à utiliser ces fonctions spécifiques au transport.</span><span class="sxs-lookup"><span data-stu-id="d7506-121">These functions are specific to TCP/IP networks; developers of protocol-independent applications are discouraged from continuing to utilize these transport-specific functions.</span></span> <span data-ttu-id="d7506-122">Toutefois, pour conserver une compatibilité descendante stricte avec Windows Sockets 1,1, les fonctions précédentes continuent à être prises en charge tant qu’au moins un fournisseur d’espace de noms est présent et prend en charge la \_ famille d’adresses d’inet AF.</span><span class="sxs-lookup"><span data-stu-id="d7506-122">However, to retain strict backward compatibility with Windows Sockets 1.1, the preceding functions continue to be supported as long as at least one namespace provider is present that supports the AF\_INET address family.</span></span>

<span data-ttu-id="d7506-123">Le *\_32.dllWs2* implémente ces fonctions de compatibilité en termes de nouvelles fonctionnalités de résolution de noms indépendantes du protocole à l’aide d’une séquence appropriée d’appels de fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .</span><span class="sxs-lookup"><span data-stu-id="d7506-123">The *Ws2\_32.dll* implements these compatibility functions in terms of the new, protocol-independent name resolution facilities using an appropriate sequence of [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) function calls.</span></span> <span data-ttu-id="d7506-124">Les détails de la façon dont les fonctions **GetXbyY** sont mappées aux fonctions de résolution de noms sont fournis ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="d7506-124">The details of how the **GetXbyY** functions are mapped to name resolution functions are provided below.</span></span> <span data-ttu-id="d7506-125">Le \_32.dll Ws2 gère les différences entre les versions asynchrone et synchrone des fonctions **GetXbyY** , de sorte que seule l’implémentation des fonctions **GetXbyY** synchrones soit discutée.</span><span class="sxs-lookup"><span data-stu-id="d7506-125">The Ws2\_32.dll handles the differences between the asynchronous and synchronous versions of the **GetXbyY** functions, so that only the implementation of the synchronous **GetXbyY** functions are discussed.</span></span>

 

 
