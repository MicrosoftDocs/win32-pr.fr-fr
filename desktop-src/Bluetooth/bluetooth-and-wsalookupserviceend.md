---
title: Bluetooth et WSALookupServiceEnd
description: Bluetooth utilise la fonction WSALookupServiceEnd pour terminer une requête lancée dans un appel précédent à WSALookupServiceBegin, et peut-être étendue dans les appels suivants à WSALookupServiceNext.
ms.assetid: 3f901176-2433-4d51-ae52-648abbd2e318
keywords:
- Bluetooth
- WSALookupServiceEnd
- Bluetooth et WSALookupServiceEnd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a032ef5d0e4fa785626ad10c64d6ddc5d383be2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095161"
---
# <a name="bluetooth-and-wsalookupserviceend"></a>Bluetooth et WSALookupServiceEnd

Bluetooth utilise la fonction [**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend) pour terminer une requête lancée dans un appel précédent à [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina), et peut-être étendue dans les appels suivants à [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta). L’appel à **WSALookupServiceEnd** met fin à la requête et nettoie le contexte.

les étapes relatives à la consultation des appareils et à la découverte de service dans Bluetooth sont suffisamment différentes pour mériter un traitement séparé. pour plus d’informations sur les Bluetooth et la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour les demandes d’appareils, consultez [Bluetooth et WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). pour plus d’informations sur les Bluetooth et la fonction **WSALookupServiceBegin** pour la découverte de service, consultez [Bluetooth et WSALookupServiceBegin pour la découverte de service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Détection des appareils et services Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la détection de Service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth et WSALookupServiceNext](bluetooth-and-wsalookupservicenext.md)
</dt> <dt>

[**\_service de requête BTH \_**](/windows/desktop/api/Ws2bth/ns-ws2bth-bth_query_service)
</dt> <dt>

[**entre**](/windows/desktop/api/winsock2/nf-winsock2-connect)
</dt> <dt>

[**SOCKADDR \_ BTH**](/windows/desktop/api/Ws2bth/ns-ws2bth-sockaddr_bth)
</dt> <dt>

[**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina)
</dt> <dt>

[**WSALookupServiceEnd**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupserviceend)
</dt> <dt>

[**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta)
</dt> <dt>

[**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw)
</dt> <dt>

[Windows Sockets](/windows/desktop/WinSock/windows-sockets-start-page-2)
</dt> </dl>

 

 