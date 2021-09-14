---
description: La \_ propriété hyperAudioEndpoint \_ ControlPanelPageProvider spécifie le CLSID du fournisseur inscrit de l’extension Device-Properties pour l’appareil de point de terminaison audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (MMDeviceAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127114881"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>\_AudioEndpoint \_ ControlPanelPageProvider

La **propriété \_ hyperAudioEndpoint \_ ControlPanelPageProvider** spécifie le CLSID du fournisseur inscrit de l’extension Device-Properties pour l’appareil de point de terminaison audio. l’extension fournit les propriétés de point de terminaison audio qui sont affichées dans la page propriétés de l’appareil du panneau de configuration Windows multimédia, Mmsys.cpl. pour plus d’informations sur Mmsys.cpl, consultez la documentation Windows DDK.

Le membre **VT** de la structure **PROPVARIANT** est défini sur VT \_ LPWStr.

Le membre **pwszVal** de la structure **PROPVARIANT** pointe vers une chaîne de caractères larges se terminant par un caractère null qui contient un GUID qui identifie le fournisseur de l’extension du panneau de contrôle.

## <a name="requirements"></a>Spécifications



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

 

 




