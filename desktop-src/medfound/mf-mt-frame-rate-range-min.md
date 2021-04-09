---
description: Fréquence d’images minimale prise en charge par un périphérique de capture vidéo, en images par seconde.
ms.assetid: d3725796-f683-4ca1-a37f-22c40fff0b76
title: Attribut MF_MT_FRAME_RATE_RANGE_MIN (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9692927242eea7ec65b86572db455e610e30c711
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867546"
---
# <a name="mf_mt_frame_rate_range_min-attribute"></a>\_ \_ \_ \_ \_ Attribut min de la plage de fréquence d’images MF

Fréquence d’images minimale prise en charge par un périphérique de capture vidéo, en images par seconde.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Pour définir cet attribut, appelez [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Notes

La fréquence d’images est exprimée sous la forme d’un rapport. Les 32 bits supérieurs de la valeur d’attribut contiennent le numérateur, et les 32 de bits inférieurs contiennent le dénominateur. Par exemple, si la fréquence d’images est de 30 images par seconde (FPS), le ratio est de 30/1.

Si l’appareil de capture signale une fréquence d’images minimale, la source du média définit cet attribut sur le type de média. La fréquence d’images maximale est donnée dans l’attribut [ \_ \_ \_ \_ \_ Max MT](mf-mt-frame-rate-range-max.md) cadence de la plage de fréquences d’images. Il n’est pas garanti que l’appareil prenne en charge chaque incrément dans cette plage.

Pour définir la fréquence d’images de l’appareil, commencez par modifier la valeur de l’attribut de [**\_ \_ \_ fréquence d’images MF MF**](mf-mt-frame-rate-attribute.md) sur le type de média. Définissez ensuite le type de média sur la source du média.

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 7 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2008 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Comment définir la fréquence d’images de capture vidéo](how-to-set-the-video-capture-frame-rate.md)
</dt> <dt>

[Attributs du type de média](media-type-attributes.md)
</dt> <dt>

[Capture vidéo](video-capture.md)
</dt> <dt>

[\_plage de \_ fréquence d’images MF MT \_ \_ \_ Max](mf-mt-frame-rate-range-max.md)
</dt> </dl>

 

 




