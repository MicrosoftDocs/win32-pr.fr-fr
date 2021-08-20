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
ms.openlocfilehash: 960362e7f6bc6388d3b93bd6e0329e405bdb33ed6e796a5ec5793d402ba0557c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081133"
---
# <a name="bluetooth-and-blob"></a>Bluetooth et objet BLOB

Bluetooth utilise la structure d' [**objets BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) pour transmettre ou recevoir des données spécifiques au transport vers la structure [**WSAQUERYSET**](bluetooth-and-wsaqueryset-for-set-service.md) lors des appels aux fonctions [**WSASetService**](bluetooth-and-wsasetservice.md) ou **WSALookupService** \* .

pour une utilisation avec Bluetooth et la fonction [**WSASetService**](bluetooth-and-wsasetservice.md) , les membres de la structure d' [**objets BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob) doivent avoir les paramètres suivants :

-   Le membre **cbSize** doit être défini sur la taille de la structure de service de l' [**\_ ensemble \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) utilisée dans le membre **pBlobData** , en octets.
-   Le membre **pBlobData** doit être un pointeur vers une structure de [**\_ \_ service d’ensemble BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

pour une utilisation avec Bluetooth et [WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md), utilisez les paramètres suivants :

-   Le membre **cbSize** doit être défini sur la taille de la structure de l' [**\_ \_ appareil de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) utilisée dans le membre **pBlobData** , en octets.
-   Le membre **pBlobData** doit être un pointeur vers une structure d' [**\_ \_ appareil de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device) .

pour une utilisation avec Bluetooth et [WSALookupServiceBegin pour la découverte de Service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md), utilisez les paramètres suivants :

-   Le membre **cbSize** doit être défini sur la taille de la structure du [**\_ \_ service de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) utilisée dans le membre **pBlobData** , en octets.
-   Le membre **pBlobData** doit être un pointeur vers une structure de [**\_ \_ service de requête BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service) .

Pour plus d’informations, consultez la section Notes de la page de référence de la structure de [**\_ \_ service de BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Bluetooth et WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la détection de Service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth et WSASetService](bluetooth-and-wsasetservice.md)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> <dt>

[**OBJET BLOB**](/windows/desktop/api/nspapi/ns-nspapi-blob)
</dt> <dt>

[**\_périphérique de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_device)
</dt> <dt>

[**\_service de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**BTH \_ Set \_ service**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_set_service)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[**WSASetService**](bluetooth-and-wsasetservice.md)
</dt> </dl>

 

 