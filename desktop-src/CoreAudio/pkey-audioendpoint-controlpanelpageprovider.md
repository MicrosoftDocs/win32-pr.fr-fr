---
description: La \_ propriété hyperAudioEndpoint \_ ControlPanelPageProvider spécifie le CLSID du fournisseur inscrit de l’extension Device-Properties pour l’appareil de point de terminaison audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc39f471649487dcdbfc2fa94371466eabd9ec59a8f9de19bdeafcec9d4283b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695349"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>\_AudioEndpoint \_ ControlPanelPageProvider

La **propriété \_ hyperAudioEndpoint \_ ControlPanelPageProvider** spécifie le CLSID du fournisseur inscrit de l’extension Device-Properties pour l’appareil de point de terminaison audio. l’extension fournit les propriétés de point de terminaison audio qui sont affichées dans la page propriétés de l’appareil du panneau de configuration Windows multimédia, Mmsys.cpl. pour plus d’informations sur Mmsys.cpl, consultez la documentation Windows DDK.

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID qui identifie le fournisseur de l’extension du panneau de contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>MMDeviceAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés du point de terminaison audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propriétés audio principales](core-audio-properties.md)
</dt> </dl>

 

 




