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
# <a name="bluetooth-and-wsalookupservicenext"></a>Bluetooth et WSALookupServiceNext

Bluetooth utilise la fonction [**WSALookupServiceNext**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicenexta) pour faire correspondre les requêtes spécifiées dans un appel précédent à [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina). Les résultats de la fonction **WSALookupServiceNext** sont déterminés par les paramètres définis dans la structure [**WSAQUERYSET**](/windows/desktop/api/winsock2/ns-winsock2-wsaquerysetw) passée dans l’appel de fonction **WSALookupServiceBegin** initial.

Les étapes de la consultation des appareils et de la découverte de service dans Bluetooth sont suffisamment différentes pour mériter un traitement séparé. Pour plus d’informations sur Bluetooth et la fonction [**WSALookupServiceBegin**](/windows/desktop/api/winsock2/nf-winsock2-wsalookupservicebegina) pour les demandes d’appareils, consultez [Bluetooth and WSALookupServiceBegin for Device](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)Inquiry. Pour plus d’informations sur Bluetooth et la fonction **WSALookupServiceBegin** pour la découverte de service, consultez [Bluetooth et WSALookupServiceBegin pour la découverte de service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Détection des appareils et services Bluetooth](discovering-bluetooth-devices-and-services.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la consultation des appareils](bluetooth-and-wsalookupservicebegin-for-device-inquiry.md)
</dt> <dt>

[Bluetooth et WSALookupServiceBegin pour la détection de service](bluetooth-and-wsalookupservicebegin-for-service-discovery.md)
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

 

 