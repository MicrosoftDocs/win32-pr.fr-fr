---
description: Active ou désactive l’accélération matérielle pour le décodage vidéo H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: AVDecVideoAcceleration_H264, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84279c49e65586d07dbf1efa4c372a1b1f8770e19bd00eb827ba44b6ad43bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663963"
---
# <a name="avdecvideoacceleration_h264-property"></a>AVDecVideoAcceleration \_ propriété H264 –

Active ou désactive l’accélération matérielle pour le décodage vidéo H. 264.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoAcceleration \_ H264 –**

## <a name="remarks"></a>Remarques

Si la valeur est égale à zéro, le décodeur n’utilise pas DirectX Video Acceleration (DXVA) pour le décodage vidéo H. 264. pour les filtres de DirectShow, définissez cette propriété avant que la broche de sortie du décodeur soit connectée.

## <a name="requirements"></a>Configuration requise



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

 

 




