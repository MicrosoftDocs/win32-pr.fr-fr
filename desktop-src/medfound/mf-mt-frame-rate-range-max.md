---
description: Fréquence d’images maximale prise en charge par un périphérique de capture vidéo, en images par seconde.
ms.assetid: 8e0c4996-9f78-424e-b012-502228b6a27a
title: Attribut MF_MT_FRAME_RATE_RANGE_MAX (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62399445cd31c7820ea9de7082fce71febbf3ba2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951535"
---
# <a name="mf_mt_frame_rate_range_max-attribute"></a>\_ \_ \_ \_ \_ Attribut max de la plage de fréquence d’images MF MT

Fréquence d’images maximale prise en charge par un périphérique de capture vidéo, en images par seconde.

## <a name="data-type"></a>Type de données

**UINT64**

## <a name="getset"></a>Obtenir/définir

Pour récupérer cet attribut, appelez [**MFGetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributeratio).

Pour définir cet attribut, appelez [**MFSetAttributeRatio**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributeratio).

## <a name="remarks"></a>Notes

La fréquence d’images est exprimée sous la forme d’un rapport. Les 32 bits supérieurs de la valeur d’attribut contiennent le numérateur, et les 32 de bits inférieurs contiennent le dénominateur. Par exemple, si la fréquence d’images est de 30 images par seconde (FPS), le ratio est de 30/1.

Si l’appareil de capture signale une fréquence d’images maximale, la source du média définit cet attribut sur le type de média. La fréquence d’images minimale est indiquée dans l’attribut min Mt de la plage de fréquences d' [ \_ \_ images \_ \_ \_ MT](mf-mt-frame-rate-range-min.md) . Il n’est pas garanti que l’appareil prenne en charge chaque incrément dans cette plage.

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

[plage de fréquence d’images MF- \_ \_ \_ \_ \_ min](mf-mt-frame-rate-range-min.md)
</dt> </dl>

 

 




