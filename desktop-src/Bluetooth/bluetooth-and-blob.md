---
title: Bluetooth et objet BLOB
description: Bluetooth utilise la structure d’objets BLOB pour transmettre ou recevoir des données spécifiques au transport vers la structure WSAQUERYSET lors des appels aux fonctions WSASetService ou WSALookupService \.
ms.assetid: d71f3661-0efb-4376-966c-fb5c340ce1c5
keywords:
- BLOB
- Bluetooth
- Bluetooth
- Bluetooth et objet BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 385f4fab053f975672d3b94fa231b3d7632e58eb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106511709"
---
# <a name="bluetooth-and-blob"></a><span data-ttu-id="d6390-107">Bluetooth et objet BLOB</span><span class="sxs-lookup"><span data-stu-id="d6390-107">Bluetooth and BLOB</span></span>

<span data-ttu-id="d6390-108">Bluetooth utilise la structure d' [**objets BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) pour transmettre ou recevoir des données spécifiques au transport vers la structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) lors des appels aux fonctions [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService** \* .</span><span class="sxs-lookup"><span data-stu-id="d6390-108">Bluetooth uses the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure to pass or receive transport-specific data to the [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) structure during calls to the [**WSASetService**](bluetooth-and-wsasetservice.md) or **WSALookupService**\* functions.</span></span>

<span data-ttu-id="d6390-109">Pour une utilisation avec Bluetooth et la fonction [**WSASetService**](bluetooth-and-wsasetservice.md) , les membres de la structure d' [**objets BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) doivent avoir les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6390-109">For use with Bluetooth and the [**WSASetService**](bluetooth-and-wsasetservice.md) function, the [**BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) structure members are required to have the following settings:</span></span>

-   <span data-ttu-id="d6390-110">Le membre **cbSize** doit être défini sur la taille de la structure de service de l' [**\_ ensemble \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) utilisée dans le membre **pBlobData** , en octets.</span><span class="sxs-lookup"><span data-stu-id="d6390-110">The **cbsize** member must be set to the size of the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="d6390-111">Le membre **pBlobData** doit être un pointeur vers une structure de [**\_ \_ service d’ensemble BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="d6390-111">The **pBlobData** member must be a pointer to a [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure.</span></span>

<span data-ttu-id="d6390-112">Pour une utilisation avec Bluetooth et [WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), utilisez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6390-112">For use with Bluetooth and [WSALookupServiceBegin for Device Inquiry](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), use the following settings:</span></span>

-   <span data-ttu-id="d6390-113">Le membre **cbSize** doit être défini sur la taille de la structure de l' [**\_ \_ appareil de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) utilisée dans le membre **pBlobData** , en octets.</span><span class="sxs-lookup"><span data-stu-id="d6390-113">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="d6390-114">Le membre **pBlobData** doit être un pointeur vers une structure d' [**\_ \_ appareil de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .</span><span class="sxs-lookup"><span data-stu-id="d6390-114">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_DEVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) structure.</span></span>

<span data-ttu-id="d6390-115">Pour une utilisation avec Bluetooth et [WSALookupServiceBegin pour la découverte de service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), utilisez les paramètres suivants :</span><span class="sxs-lookup"><span data-stu-id="d6390-115">For use with Bluetooth and [WSALookupServiceBegin for Service Discovery](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), use the following settings:</span></span>

-   <span data-ttu-id="d6390-116">Le membre **cbSize** doit être défini sur la taille de la structure du [**\_ \_ service de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) utilisée dans le membre **pBlobData** , en octets.</span><span class="sxs-lookup"><span data-stu-id="d6390-116">The **cbsize** member must be set to the size of the [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure used in the **pBlobData** member, in bytes.</span></span>
-   <span data-ttu-id="d6390-117">Le membre **pBlobData** doit être un pointeur vers une structure de [**\_ \_ service de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .</span><span class="sxs-lookup"><span data-stu-id="d6390-117">The **pBlobData** member must be a pointer to a [**BTH\_QUERY\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) structure.</span></span>

<span data-ttu-id="d6390-118">Pour plus d’informations, consultez la section Notes de la page de référence de la structure de [**\_ \_ service de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .</span><span class="sxs-lookup"><span data-stu-id="d6390-118">For more information, see the Remarks section in the [**BTH\_SET\_SERVICE**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) structure reference page.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d6390-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d6390-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6390-120">Bluetooth et WSALookupServiceBegin pour la consultation des appareils</span><span class="sxs-lookup"><span data-stu-id="d6390-120">Bluetooth and WSALookupServiceBegin for Device Inquiry</span></span>](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[<span data-ttu-id="d6390-121">Bluetooth et WSALookupServiceBegin pour la détection de service</span><span class="sxs-lookup"><span data-stu-id="d6390-121">Bluetooth and WSALookupServiceBegin for Service Discovery</span></span>](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[<span data-ttu-id="d6390-122">Bluetooth et WSASetService</span><span class="sxs-lookup"><span data-stu-id="d6390-122">Bluetooth and WSASetService</span></span>](bluetooth-and-wsasetservice.md)
</dt> <dt>

[<span data-ttu-id="d6390-123">Windows Sockets</span><span class="sxs-lookup"><span data-stu-id="d6390-123">Windows Sockets</span></span>](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[<span data-ttu-id="d6390-124">**OBJET BLOB**</span><span class="sxs-lookup"><span data-stu-id="d6390-124">**BLOB**</span></span>](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[<span data-ttu-id="d6390-125">**\_périphérique de requête BTH \_**</span><span class="sxs-lookup"><span data-stu-id="d6390-125">**BTH\_QUERY\_DEVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[<span data-ttu-id="d6390-126">**\_service de requête BTH \_**</span><span class="sxs-lookup"><span data-stu-id="d6390-126">**BTH\_QUERY\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[<span data-ttu-id="d6390-127">**BTH \_ Set \_ service**</span><span class="sxs-lookup"><span data-stu-id="d6390-127">**BTH\_SET\_SERVICE**</span></span>](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[<span data-ttu-id="d6390-128">**WSALookupServiceBegin**</span><span class="sxs-lookup"><span data-stu-id="d6390-128">**WSALookupServiceBegin**</span></span>](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[<span data-ttu-id="d6390-129">**WSAQUERYSET**</span><span class="sxs-lookup"><span data-stu-id="d6390-129">**WSAQUERYSET**</span></span>](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[<span data-ttu-id="d6390-130">**WSASetService**</span><span class="sxs-lookup"><span data-stu-id="d6390-130">**WSASetService**</span></span>](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 