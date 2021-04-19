---
description: Pour un format vidéo 3D, spécifie la vue qui est la vue de base.
ms.assetid: 11555BA0-D9BE-4239-A857-C9EEE86A8520
title: Attribut MF_MT_VIDEO_3D_LEFT_IS_BASE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8f5ece66db7de19cd77d7e686d9665ad239c6d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536565"
---
# <a name="mf_mt_video_3d_left_is_base-attribute"></a>MF \_ MT \_ Video \_ 3D \_ Left \_ est l' \_ attribut de base

Pour un format vidéo 3D, spécifie la vue qui est la vue de base.

## <a name="data-type"></a>Type de données

**Bool** stocké comme **UInt32**

## <a name="remarks"></a>Notes

Par défaut, la vue de gauche d’une séquence vidéo 3D est la vue de base. Si la vue de droite est la vue de base, affectez la valeur **false** à cet attribut.

Pour convertir une vidéo stéréoscopique en 2D, conservez la vue de base et débarrassez-vous de l’autre vue.

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

 

 




