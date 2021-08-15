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
ms.openlocfilehash: 7ac95ee58bc0c7da8c95d1b9d4577bdc18bba2236ea1ee13cdbc12fc0d852f5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118010391"
---
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth et WSALookupServiceNext

Bluetooth utilise la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) pour faire correspondre les requêtes spécifiées dans un appel précédent à [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina). Les résultats de la fonction **WSALookupServiceNext** sont déterminés par les paramètres définis dans la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passée dans l’appel de fonction **WSALookupServiceBegin** initial.

les étapes relatives à la consultation des appareils et à la découverte de service dans Bluetooth sont suffisamment différentes pour mériter un traitement séparé. pour plus d’informations sur les Bluetooth et la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour les demandes d’appareils, consultez [Bluetooth et WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md). pour plus d’informations sur les Bluetooth et la fonction **WSALookupServiceBegin** pour la découverte de service, consultez [Bluetooth et WSALookupServiceBegin pour la découverte de service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Détection des appareils et services Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la détection de Service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
</dt> <dt>

[Bluetooth et WSALookupServiceEnd](bluetooth-and-wsalookupserviceend.md)
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
</dt> </dl>

 

 