---
description: Obtient la configuration de l’orateur pour les canaux audio dans le flux de bits audio.
ms.assetid: ec13bb55-47af-4d79-9560-d297bce8e236
title: Propriété AVAudioChannelConfig (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 52ee1bc7897d92f7efa1b6d351d2f73c32867529
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127112130"
---
# <a name="avaudiochannelconfig-property"></a>Propriété AVAudioChannelConfig

Obtient la configuration de l’orateur pour les canaux audio dans le flux de bits audio.

Cette propriété est en lecture seule.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVAudioChannelConfig**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est une opération or au niveau du bit de l’énumération [**eAVAudioChannelConfig**](/windows/desktop/api/codecapi/ne-codecapi-eavaudiochannelconfig) .

## <a name="remarks"></a>Notes

Le nombre de canaux comprend le canal de l’effet de fréquence faible (LFE), le cas échéant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications Windows 2000 Professional \[ desktop apps \| UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | applications de bureau Windows 2000 Server apps-applications \[ \| UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




