---
title: Bluetooth et WSALookupServiceEnd
description: Bluetooth utilise la fonction WSALookupServiceEnd pour terminer une requête lancée lors d’un appel précédent à WSALookupServiceBegin, et peut-être étendue dans les appels suivants à WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth et WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103941077"
---
# <a name="bluetooth-and-wsalookupserviceend"></a><span data-ttu-id="d42fc-106">Bluetooth et WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="d42fc-106">Bluetooth and WSALookupServiceEnd</span></span>

<span data-ttu-id="d42fc-107">Bluetooth utilise la fonction [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) pour terminer une requête lancée lors d’un appel précédent à [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), et peut-être étendue dans les appels suivants à [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span><span class="sxs-lookup"><span data-stu-id="d42fc-107">Bluetooth uses the [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) function to terminate a query initiated in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), and perhaps extended in subsequent calls to [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta).</span></span> <span data-ttu-id="d42fc-108">L’appel à **WSALookupServiceEnd** met fin à la requête et nettoie le contexte.</span><span class="sxs-lookup"><span data-stu-id="d42fc-108">The call to **WSALookupServiceEnd** terminates the query and cleans up the context.</span></span>

<span data-ttu-id="d42fc-109">Les étapes de la consultation des appareils et de la découverte de service dans Bluetooth sont suffisamment différentes pour mériter un traitement séparé.</span><span class="sxs-lookup"><span data-stu-id="d42fc-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="d42fc-110">Pour plus d’informations sur Bluetooth et la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour les demandes d’appareils, consultez [Bluetooth and WSALookupServiceBegin for Device](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)Inquiry.</span><span class="sxs-lookup"><span data-stu-id="d42fc-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="d42fc-111">Pour plus d’informations sur Bluetooth et la fonction **WSALookupServiceBegin** pour la découverte de service, consultez [Bluetooth et WSALookupServiceBegin pour la découverte de service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="d42fc-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="d42fc-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d42fc-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d42fc-113">Détection des appareils et services Bluetooth</span><span class="sxs-lookup"><span data-stu-id="d42fc-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="d42fc-114">Bluetooth et WSALookupServiceBegin pour la consultation des appareils</span><span class="sxs-lookup"><span data-stu-id="d42fc-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="d42fc-115">Bluetooth et WSALookupServiceBegin pour la détection de service</span><span class="sxs-lookup"><span data-stu-id="d42fc-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="d42fc-116">Bluetooth et WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="d42fc-116">Bluetooth and WSALookupServiceNext</span></span>](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[<span data-ttu-id="d42fc-117">**\_service de requête BTH \_**</span><span class="sxs-lookup"><span data-stu-id="d42fc-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="d42fc-118">**entre**</span><span class="sxs-lookup"><span data-stu-id="d42fc-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="d42fc-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="d42fc-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="d42fc-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="d42fc-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="d42fc-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="d42fc-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="d42fc-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="d42fc-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="d42fc-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="d42fc-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="d42fc-124">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d42fc-124">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 