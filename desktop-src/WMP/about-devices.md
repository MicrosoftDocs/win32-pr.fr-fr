---
title: À propos des appareils
description: À propos des appareils
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Lecteur Windows Media, synchronisation des appareils
- Modèle objet du lecteur Windows Media, synchronisation des appareils
- modèle objet, synchronisation des appareils
- Contrôle ActiveX du lecteur Windows Media, synchronisation des appareils
- Contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile contrôle ActiveX, synchronisation des appareils
- Windows Media Player Mobile, synchronisation des appareils
- synchronisation des appareils, à propos de
- synchronisation des appareils, à propos de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "106509237"
---
# <a name="about-devices"></a>À propos des appareils

Les périphériques portables sont des périphériques matériels que les utilisateurs utilisent pour profiter d’un contenu multimédia numérique lorsqu’ils sont à l’extérieur de leur ordinateur. En règle générale, les périphériques portables sont exploités par une batterie. Certains appareils peuvent lire uniquement de la musique. D’autres appareils peuvent lire des vidéos et de la musique.

Certains appareils prennent en charge la synchronisation automatique du contenu multimédia numérique avec le lecteur Windows Media. Les autres périphériques prennent uniquement en charge le transfert manuel. Vous pouvez déterminer si un appareil particulier prend en charge la synchronisation automatique en appelant [IWMPSyncDevice :: obtenir l' \_ État](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) et en inspectant la valeur [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) récupérée. Si la valeur récupérée est **wmpdsManualDevice**, l’appareil ne prend pas en charge la synchronisation automatique.

Vous pouvez énumérer les appareils connectés à l’ordinateur de l’utilisateur. Pour ce faire, utilisez d’abord [IWMPSyncServices :: obtenir \_ deviceCount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) pour récupérer le nombre d’appareils. Ensuite, dans une boucle, appelez [IWMPSyncServices :: getDevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), en passant chaque fois la valeur d’index appropriée. Vous pouvez utiliser [IWMPSyncDevice :: obtenir la \_ connexion](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) pour évaluer si un appareil particulier est actuellement connecté.

Pour savoir quand les appareils se connectent ou se déconnectent, vous pouvez recevoir les événements **DeviceConnect** et **DeviceDisconnect** . Ces événements sont reçus via l’interface **IWMPEvents2** .

L’interface **IWMPSyncDevice** fournit des méthodes supplémentaires pour vous permettre d’obtenir ou de définir des informations sur un appareil. Par exemple :

-   Les méthodes **obtenir \_ FriendlyName** et **put \_ FriendlyName** vous permettent de récupérer et de spécifier le nom de périphérique défini par l’utilisateur.
-   La méthode **obtenir \_ DeviceName** vous permet de récupérer le nom de l’appareil que les utilisateurs voient dans le shell Windows XP.
-   La méthode **getItemInfo** vous permet de récupérer les métadonnées des appareils.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos de la synchronisation des appareils**](about-device-synchronization.md)
</dt> <dt>

[**Interface IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Interface IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Utilisation d’appareils mobiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




