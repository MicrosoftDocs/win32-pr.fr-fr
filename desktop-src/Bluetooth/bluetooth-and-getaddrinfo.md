---
title: Bluetooth et getaddrinfo
description: La fonction getaddrinfo permet de traduire le nom d’hôte en adresse pour les transports basés sur IP. Étant donné que la fonction getaddrinfo est spécifique aux transports basés sur IP, elle échoue sur les sockets Bluetooth.
ms.assetid: e17d8542-d4bc-499c-bae4-1f41bff493c3
keywords:
- Bluetooth et getaddrinfo Bluetooth
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96c2e62b83ac947b74479ff435b93914661aa8da
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729852"
---
# <a name="bluetooth-and-getaddrinfo"></a><span data-ttu-id="4408f-105">Bluetooth et getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="4408f-105">Bluetooth and getaddrinfo</span></span>

<span data-ttu-id="4408f-106">La fonction [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) permet de traduire le nom d’hôte en adresse pour les transports basés sur IP.</span><span class="sxs-lookup"><span data-stu-id="4408f-106">The [**getaddrinfo**](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo) function provides translation from host name to address for IP-based transports.</span></span> <span data-ttu-id="4408f-107">Étant donné que la fonction **getaddrinfo** est spécifique aux transports basés sur IP, elle échoue sur les sockets Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="4408f-107">Because the **getaddrinfo** function is specific to IP-based transports, it fails on Bluetooth sockets.</span></span>

<span data-ttu-id="4408f-108">Pour effectuer la traduction du nom d’hôte vers l’adresse pour les sockets Bluetooth, utilisez la fonction [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) avec des **\_ conteneurs lup** pour interroger des appareils distants, puis recherchez un nom distant et une adresse correspondants spécifiques.</span><span class="sxs-lookup"><span data-stu-id="4408f-108">To perform translation from host name to address for Bluetooth sockets, use the [**WSALookupServiceBegin**](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md) function with **LUP\_CONTAINERS** to query remote devices, then search for a specific matching Remote Name and corresponding address.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4408f-109">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4408f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4408f-110">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="4408f-110">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="4408f-111">**getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="4408f-111">**getaddrinfo**</span></span>](/windows/desktop/api/ws2tcpip/nf-ws2tcpip-getaddrinfo)
</dt> <dt>

[<span data-ttu-id="4408f-112">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="4408f-112">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> </dl>

 

 