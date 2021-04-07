---
description: Active ou désactive l’accélération matérielle pour le décodage vidéo H. 264.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: AVDecVideoAcceleration_H264, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846681"
---
# <a name="avdecvideoacceleration_h264-property"></a>AVDecVideoAcceleration \_ propriété H264 –

Active ou désactive l’accélération matérielle pour le décodage vidéo H. 264.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVDecVideoAcceleration \_ H264 –**

## <a name="remarks"></a>Notes

Si la valeur est égale à zéro, le décodeur n’utilise pas DirectX Video Acceleration (DXVA) pour le décodage vidéo H. 264. Pour les filtres DirectShow, définissez cette propriété avant que la broche de sortie du décodeur soit connectée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 2000 professionnel- \[ \| applications UWP\]<br/>                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows 2000 Server \[ apps- \| applications UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de l’API codec](codec-api-properties.md)
</dt> <dt>

[**Interface ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




