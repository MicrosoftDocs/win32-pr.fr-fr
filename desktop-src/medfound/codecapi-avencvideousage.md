---
description: Définit l’utilisation de la vidéo pour un encodeur vidéo.
ms.assetid: 2A6941A3-CCA0-467C-AC8A-DADC2CD1D405
title: CODECAPI_AVEncVideoUsage, propriété (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b6d3ee174fbc22ca7b1ab4e309d87112463740a075b497cc35033f8c96bbe8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777709"
---
# <a name="codecapi_avencvideousage-property"></a>CODECAPI \_ propriété AVEncVideoUsage

Définit l’utilisation de la vidéo pour un encodeur vidéo.

## <a name="data-type"></a>Type de données

**ULONG (VT \_ UI4)**

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncVideoUsage**

## <a name="remarks"></a>Remarques

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

[CODECAPI \_ AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md), CODECAPI \_ AVEncVideoUsage et [CODECAPI \_ AVEncCommonRateControlMode](/windows/desktop/DirectShow/avenccommonratecontrolmode-property) sont des propriétés d’encodeur statiques. Une fois définis, ceux-ci prennent effet uniquement après l’appel d’un type de média set sur la broche de sortie de l’appareil photo s.

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

 

