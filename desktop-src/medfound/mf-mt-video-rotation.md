---
description: Spécifie la rotation d’une image vidéo dans le sens des aiguilles d’une montre.
ms.assetid: 7C0911A6-6D7C-4510-891F-A6F56CE1EC2B
title: Attribut MF_MT_VIDEO_ROTATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f46a67c9861b8094e909e5c6fd7bc82e46166dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868937"
---
# <a name="mf_mt_video_rotation-attribute"></a>Attribut de rotation de la \_ vidéo MF MT \_ \_

Spécifie la rotation d’une image vidéo dans le sens des aiguilles d’une montre.

## <a name="data-type"></a>Type de données

**MFVideoRotationFormat** stocké en tant que **UInt32**

## <a name="remarks"></a>Notes

La vidéo à partir d’un périphérique de poche, tel qu’un téléphone mobile, est souvent pivotée par 90, 180 ou 270 degrés. Si l’appareil photo stocke l’orientation en tant que métadonnées dans le fichier vidéo, l’image peut être ajustée au moment de la lecture.

Si cet attribut a la valeur **MFVideoRotationFormat \_ 90**, cela signifie que le contenu a été pivoté de 90 degrés dans le sens inverse des aiguilles d’une montre. Si le contenu a pivoté de 90 degrés dans le sens des aiguilles d’une montre, la valeur de l’attribut serait **MFVideoRotationFormat \_ 270**.

Les valeurs prises en charge pour cet attribut sont énumérées dans [**MFVideoRotationFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideorotationformat).

La constante GUID de cet attribut est exportée à partir de mfuuid. lib.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Types de médias](media-types.md)
</dt> </dl>

 

 




