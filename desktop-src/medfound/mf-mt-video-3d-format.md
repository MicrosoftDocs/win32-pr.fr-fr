---
description: Pour un type de média vidéo, spécifie la manière dont les images vidéo 3D sont stockées en mémoire.
ms.assetid: 880DF017-5841-4C0A-82AF-F092DEF5406B
title: Attribut MF_MT_VIDEO_3D_FORMAT (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4100a605ecc7e8fe1c171b02341822972061363e7cd1b322162291dbd75b2c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117692068"
---
# <a name="mf_mt_video_3d_format-attribute"></a>\_Attribut de \_ \_ format vidéo 3D \_ MF MT

Pour un type de média vidéo, spécifie la manière dont les images vidéo 3D sont stockées en mémoire.

## <a name="data-type"></a>Type de données

**MFVideo3DFormat** stocké en tant que **UInt32**

## <a name="remarks"></a>Remarques

La valeur de cet attribut est un membre de l’énumération [**MFVideo3DFormat**](/windows/desktop/api/mfapi/ne-mfapi-mfvideo3dformat) . L’attribut s’applique uniquement si l’attribut [ \_ \_ \_ 3D MF MT Video](mf-mt-video-3d.md) a la **valeur true**.

Cet attribut est requis pour les formats vidéo 3D non compressés. Elle est facultative pour la vidéo 3D compressée. Une source de média qui fournit des frames encodés peut être en mesure de définir l’attribut, en fonction des informations contenues dans le conteneur de fichiers. Dans le cas contraire, l’attribut doit être défini par le décodeur dans le type de média de sortie du décodeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau \| UWP apps\]<br/>                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau \| UWP apps\]<br/>                        |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




