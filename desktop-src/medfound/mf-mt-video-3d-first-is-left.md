---
description: Pour un format vidéo 3D, spécifie la vue de gauche.
ms.assetid: 4F33BF2D-EB32-46B6-B071-F9130D404201
title: Attribut MF_MT_VIDEO_3D_FIRST_IS_LEFT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 027d91509d772a9200cdfc0ac64cce15514aa5a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393788"
---
# <a name="mf_mt_video_3d_first_is_left-attribute"></a>La \_ \_ vidéo 3D MF MT \_ \_ First est l' \_ \_ attribut Left

Pour un format vidéo 3D, spécifie la vue de gauche.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Pour la vidéo 3D, chaque exemple de vidéo contient deux vues, qui sont désignées en *premier* et en *deuxième vue*. La disposition exacte des vues en mémoire est indiquée par l’attribut [de \_ \_ format vidéo \_ 3D \_ MF MT](mf-mt-video-3d-format.md) .



| Format               | Premier affichage              | Deuxième vue               |
|----------------------|-------------------------|---------------------------|
| Compressé côte à côte  | Moitié gauche de la mémoire tampon | Moitié droite de la mémoire tampon  |
| Condensé de haut en bas | Moitié supérieure de la mémoire tampon  | Moitié inférieure de la mémoire tampon |
| Multivue            | Index de mémoire tampon 0          | Index de mémoire tampon 1            |
| Vue de base            | Frame entier            | Non présent               |



 

Par défaut, la première vue est la vue de gauche, tandis que la deuxième vue est la vue de droite. Si les affichages de gauche et de droite sont permutés, affectez \_ à l’attribut MF MT \_ Video \_ 3D First la \_ \_ \_ **valeur false** dans le type de média.

> [!Note]  
> Dans le format de *vue de base* (**MFVideo3DSampleFormat \_ BaseView**), seule la vue de base est conservée. cet attribut ne s’applique donc pas.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications Windows 8 \[ Desktop Apps \| UWP\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ \| apps UWP\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




