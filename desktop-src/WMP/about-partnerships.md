---
title: À propos des partenariats
description: À propos des partenariats
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, partenariats
- Modèle objet du lecteur Windows Media, partenariats
- modèle objet, partenariats
- Contrôle ActiveX du lecteur Windows Media, partenariats
- Contrôle ActiveX, partenariats
- Contrôle ActiveX Windows Media Player Mobile, partenariats
- Windows Media Player Mobile, partenariats
- synchronisation des appareils, partenariats
- synchronisation des appareils, partenariats
- partenariats entre les appareils et le lecteur Windows Media
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104462707"
---
# <a name="about-partnerships"></a>À propos des partenariats

Un partenariat est une relation spéciale entre un appareil portable et le lecteur Windows Media. Les utilisateurs peuvent établir un partenariat pour un appareil particulier à l’aide de l’interface utilisateur du lecteur Windows Media. Vous pouvez gérer les partenariats par programmation à l’aide de [IWMPSyncDevice :: createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) et [IWMPSyncDevice ::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership). La méthode **createPartnership** démarre un processus asynchrone qui se termine lorsque l’événement **CreatePartnershipComplete** est reçu par le biais de l’interface **IWMPEvents2** .

Le lecteur Windows Media 10 ou une version ultérieure prend en charge la création de partenariats avec jusqu’à 16 appareils. Chaque partenariat est associé à un index de partenariat. Vous pouvez récupérer l’index de partenariat pour un appareil particulier en appelant [IWMPSyncDevice :: obtenir \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex). Les indices de partenariat sont numérotés de 1 à 16. Quand un appareil particulier n’a pas de partenariat avec le lecteur Windows Media, **getPartnershipIndex** retourne zéro pour l’index.

Vous pouvez récupérer l’état du partenariat d’un appareil particulier en appelant [IWMPSyncDevice :: obtenir l' \_ État](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) et en inspectant la valeur [WMPDeviceStatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) récupérée. Le lecteur Windows Media autorise un partenariat avec la bibliothèque d’un utilisateur sur un ordinateur pour chaque appareil. Cela signifie que la création d’un partenariat détruit tout partenariat existant que l’appareil actuel peut avoir avec un autre ordinateur. Pour savoir quand l’état change pour un appareil, vous pouvez recevoir l’événement **DeviceStatusChange** .

Le lecteur Windows Media ne peut pas créer de partenariat avec un appareil dont l’État est **wmpdsManualDevice**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**À propos de la synchronisation des appareils**](about-device-synchronization.md)
</dt> <dt>

[**Interface IWMPEvents2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Utilisation d’appareils mobiles**](working-with-portable-devices.md)
</dt> </dl>

 

 




