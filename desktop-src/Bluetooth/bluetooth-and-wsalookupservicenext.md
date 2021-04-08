---
title: Bluetooth et WSALookupServiceNext
description: Bluetooth utilise la fonction WSALookupServiceNext pour faire correspondre les requêtes spécifiées dans un appel précédent à WSALookupServiceBegin.
ms.assetid: d43cf444-adb6-4313-9614-a8d6d868a88f
keywords:
- Bluetooth
- WSALookupServiceNext
- Bluetooth et WSALookupServiceNext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d3ece06e27c9e80e25f22ef0fb09a5790cdf69b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842350"
---
# <a name="bluetooth-and-wsalookupservicenext"></a><span data-ttu-id="3e3e5-106">Bluetooth et WSALookupServiceNext</span><span class="sxs-lookup"><span data-stu-id="3e3e5-106">Bluetooth and WSALookupServiceNext</span></span>

<span data-ttu-id="3e3e5-107">Bluetooth utilise la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) pour faire correspondre les requêtes spécifiées dans un appel précédent à [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span><span class="sxs-lookup"><span data-stu-id="3e3e5-107">Bluetooth uses the [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) function to match queries specified in a previous call to [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina).</span></span> <span data-ttu-id="3e3e5-108">Les résultats de la fonction **WSALookupServiceNext** sont déterminés par les paramètres définis dans la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passée dans l’appel de fonction **WSALookupServiceBegin** initial.</span><span class="sxs-lookup"><span data-stu-id="3e3e5-108">The results of the **WSALookupServiceNext** function are determined by settings set forth in the [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) structure passed in the initial **WSALookupServiceBegin** function call.</span></span>

<span data-ttu-id="3e3e5-109">Les étapes de la consultation des appareils et de la découverte de service dans Bluetooth sont suffisamment différentes pour mériter un traitement séparé.</span><span class="sxs-lookup"><span data-stu-id="3e3e5-109">The steps for device inquiry and service discovery in Bluetooth are sufficiently different to merit separate treatment.</span></span> <span data-ttu-id="3e3e5-110">Pour plus d’informations sur Bluetooth et la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour les demandes d’appareils, consultez [Bluetooth and WSALookupServiceBegin for Device](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)Inquiry.</span><span class="sxs-lookup"><span data-stu-id="3e3e5-110">For more information on Bluetooth and the [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) function for device inquiries, see [Bluetooth and WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md).</span></span> <span data-ttu-id="3e3e5-111">Pour plus d’informations sur Bluetooth et la fonction **WSALookupServiceBegin** pour la découverte de service, consultez [Bluetooth et WSALookupServiceBegin pour la découverte de service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span><span class="sxs-lookup"><span data-stu-id="3e3e5-111">For more information on Bluetooth and the **WSALookupServiceBegin** function for service discovery, see [Bluetooth and WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3e3e5-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3e3e5-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3e3e5-113">Détection des appareils et services Bluetooth</span><span class="sxs-lookup"><span data-stu-id="3e3e5-113">Discovering Bluetooth Devices and Services</span></span>](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[<span data-ttu-id="3e3e5-114">Bluetooth et WSALookupServiceBegin pour la consultation des appareils</span><span class="sxs-lookup"><span data-stu-id="3e3e5-114">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="3e3e5-115">Bluetooth et WSALookupServiceBegin pour la détection de service</span><span class="sxs-lookup"><span data-stu-id="3e3e5-115">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="3e3e5-116">Bluetooth et WSALookupServiceEnd</span><span class="sxs-lookup"><span data-stu-id="3e3e5-116">Bluetooth and WSALookupServiceEnd</span></span>](bluetooth-and-wsalookupserviceend.md)
</dt> <dt>

[<span data-ttu-id="3e3e5-117">**\_service de requête BTH \_**</span><span class="sxs-lookup"><span data-stu-id="3e3e5-117">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="3e3e5-118">**entre**</span><span class="sxs-lookup"><span data-stu-id="3e3e5-118">**connect**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[<span data-ttu-id="3e3e5-119">**SOCKADDR \_ BTH**</span><span class="sxs-lookup"><span data-stu-id="3e3e5-119">**SOCKADDR\_BTH**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[<span data-ttu-id="3e3e5-120">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="3e3e5-120">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="3e3e5-121">**WSALookupServiceEnd**</span><span class="sxs-lookup"><span data-stu-id="3e3e5-121">**WSALookupServiceEnd**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[<span data-ttu-id="3e3e5-122">**WSALookupServiceNext**</span><span class="sxs-lookup"><span data-stu-id="3e3e5-122">**WSALookupServiceNext**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[<span data-ttu-id="3e3e5-123">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="3e3e5-123">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> </dl>

 

 