---
description: Spécifie le mode de contrôle de la fréquence.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: Propriété AVEncCommonRateControlMode (Codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d18d0d7cb68936326fb4c4ba08188e362fdc91d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200823"
---
# <a name="avenccommonratecontrolmode-property"></a>Propriété AVEncCommonRateControlMode

Spécifie le mode de contrôle de la fréquence.

Les applications peuvent définir cette propriété pour spécifier le mode de contrôle de la fréquence. Les encodeurs peuvent également retourner cette propriété en tant que fonctionnalité.

Cette propriété est en lecture/écriture.

## <a name="data-type"></a>Type de données

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Guid de propriété

**CODECAPI \_ AVEncCommonRateControlMode**

## <a name="property-value"></a>Valeur de la propriété

La valeur de cette propriété est un membre de l’énumération [**eAVEncCommonRateControlMode**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode) .

## <a name="remarks"></a>Notes

Cette propriété est également utilisée avec les [encodeurs de caméra H. 264 UVC 1,5](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5).

[CODECAPI \_ AVEncVideoTemporalLayerCount](/windows/desktop/medfound/codecapi-avencvideotemporallayercount), [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)et CODECAPI \_ AVEncCommonRateControlMode sont des propriétés d’encodeur statiques. Une fois définis, ceux-ci prennent effet uniquement après l’appel d’un type de média défini sur la broche de sortie de la caméra.

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

 

