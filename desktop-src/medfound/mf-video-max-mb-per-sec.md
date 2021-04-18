---
description: Spécifie, sur IMFTransform, la vitesse de traitement maximale bloc macro, en blocs macros par seconde, qui est prise en charge par l’encodeur matériel.
ms.assetid: 1AA41DE3-C37C-41BA-9549-5F12373DDB3B
title: Attribut MF_VIDEO_MAX_MB_PER_SEC (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbee009b50daee074241c11750e9d25240cda153
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542908"
---
# <a name="mf_video_max_mb_per_sec-attribute"></a>\_ \_ Attribut nombre maximal de \_ Mo \_ par \_ seconde de la vidéo MF

Spécifie, sur [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform), la vitesse de traitement maximale bloc macro, en blocs macros par seconde, qui est prise en charge par l’encodeur matériel.

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

Ceci est un attribut de lecture seule.

**Encodeurs H. 264/AVC :**

Cet attribut est affecté par les propriétés suivantes :

-   [MF \_ \_ \_ Niveau vidéo MT](mf-mt-video-level.md) (qui est un alias du [ \_ niveau de \_ MPEG2 \_ MT MPEG2](mf-mt-mpeg2-level-attribute.md))
-   [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

Si l’attribut de [ \_ \_ \_ niveau vidéo MF MT](mf-mt-video-level.md) est présent, l’encodeur doit retourner la vitesse de traitement pour le débit binaire et la résolution les plus élevés pris en charge au niveau spécifié. Si l' \_ \_ \_ attribut de niveau vidéo MF MT n’est pas présent, il doit utiliser un niveau par défaut de 4.

Si la propriété [CODECAPI \_ AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md) ICodecAPI a été définie, l’encodeur doit retourner la vitesse de traitement correspondant à la valeur définie pour cette propriété. Si l' \_ attribut CODECAPI AVEncCommonQualityVsSpeed n’est pas présent, il doit utiliser la valeur par défaut 0, qui doit être le mode de traitement le plus rapide.

Si la propriété [CODECAPI \_ AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md) ICodecAPI a été définie sur une valeur valide et prise en charge, l’encodeur doit retourner la vitesse de traitement correspondant à la valeur définie pour cette propriété. Si l' \_ attribut CODECAPI AVEncMPVDefaultBPictureCount n’est pas une avance, t, il doit utiliser une valeur par défaut de 0 B frames.

Seuls les 28 bits inférieurs doivent être utilisés par une application. Le 4bits supérieur est réservé à une utilisation ultérieure. Les applications doivent ignorer les 4 bits supérieurs et MFTs doit définir les 4 bits supérieurs à 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | \[Applications Windows 8.1 Desktop Apps \| UWP\]<br/>                                |
| Serveur minimal pris en charge<br/> | Applications Windows Server 2012 R2 \[ Desktop Apps \| UWP\]<br/>                     |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
