---
description: Définit le nombre de couches temporelles vidéo pour un encodeur vidéo.
ms.assetid: 36E1C86B-86D0-40CB-8F96-061FC653E9C3
title: CODECAPI_AVEncVideoTemporalLayerCount, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85402b57c0eaf5c5fe61290eabdfd3e34a64ca4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484113"
---
# <a name="codecapi_avencvideotemporallayercount-property"></a>CODECAPI \_ propriété AVEncVideoTemporalLayerCount

Définit le nombre de couches temporelles vidéo pour un encodeur vidéo.

## <a name="data-type"></a>Type de données

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoTemporalLayerCount**

## <a name="remarks"></a>Notes

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

CODECAPI \_ AVEncVideoTemporalLayerCount, [CODECAPI \_ AVEncVideoUsage](codecapi-avencvideousage.md)et [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sont des propriétés d’encodeur statiques. Une fois définis, ceux-ci prennent effet uniquement après l’appel d’un type de média set sur la broche de sortie de l’appareil photo s.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                           |
| En-tête<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Propriétés de la Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

