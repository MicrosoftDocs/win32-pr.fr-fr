---
description: Définit le nombre de couches temporelles vidéo pour un encodeur vidéo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81ceaf82d9d202e97927e0e141aa03a4e8e27c49a28880509aa9bb3c24f9319
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118743840"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>CODECAPI \_ propriété AVEncVideoTemporalLayerCount

Définit le nombre de couches temporelles vidéo pour un encodeur vidéo.

## <a name="data-type"></a>Type de données

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoTemporalLayerCount**

## <a name="remarks"></a>Remarques

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)et [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sont des propriétés d’encodeur statiques. Une fois définis, ceux-ci prennent effet uniquement après l’appel d’un type de média set sur la broche de sortie de l’appareil photo s.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

