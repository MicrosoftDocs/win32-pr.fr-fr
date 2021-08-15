---
description: Spécifie les modes de contrôle de fréquence pris en charge pour un flux vidéo H. 264.
ms.assetid: DAA62ECD-AFA2-40C2-9B52-F2D581F4D894
title: Attribut MF_MT_H264_SUPPORTED_RATE_CONTROL_MODES (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9665fd99635749e2400437e77cb89e74d2cb8675689f6f4b867a20ac82fadaec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692281"
---
# <a name="mf_mt_h264_supported_rate_control_modes-attribute"></a>\_Attribut de \_ \_ mode de \_ contrôle de taux pris en charge \_ \_ pour MF MT H264 –

Spécifie les modes de contrôle de fréquence pris en charge pour un flux vidéo H. 264.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**IMFAttributes :: GetUInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Pour définir cet attribut, appelez [**IMFAttributes :: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>S’applique à

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>Remarques

Cet attribut s’applique aux types de média pour les flux H. 264 transmis sur USB. La valeur correspond au champ **bmSupportedRateControlModes** dans le descripteur de format vidéo 1,5 UVC H. 264.

Cet attribut est également utilisé avec les [encodeurs de caméra H. 264 UVC 1,5](camera-encoder-h264-uvc-1-5.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> </dl>

 

 




