---
description: Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo. Il s’agit d’un alias \_ du \_ niveau de MPEG2 MT MPEG2 \_ .
ms.assetid: 23786FC8-ACA4-4F6A-98BA-57A8C76BD4C6
title: Attribut MF_MT_VIDEO_LEVEL (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca2c5eb00390df1b5c18cab7e04a5f7449f84fc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521393"
---
# <a name="mf_mt_video_level-attribute"></a>\_Attribut de \_ niveau vidéo MF MT \_

Spécifie le niveau MPEG-2 ou H. 264 dans un type de média vidéo. Il s’agit d’un alias du [ \_ niveau de \_ MPEG2 MT MPEG2 \_ ](mf-mt-mpeg2-level-attribute.md).

## <a name="data-type"></a>Type de données

**UINT32**

## <a name="remarks"></a>Notes

**Encodeurs H. 264 :**

Les niveaux pris en charge sont étendus pour inclure le [**eAVEncH264VLevel5 \_ 2**](/windows/desktop/api/codecapi/ne-codecapi-eavench264vlevel).

Par défaut : la valeur par défaut recommandée consiste à sélectionner le niveau minimal pour correspondre à la configuration de l’encodage vidéo, y compris la résolution, la fréquence d’images, etc.

Valeur par défaut recommandée : sélectionnez le niveau minimum pour correspondre à la configuration de l’encodage vidéo, y compris la résolution, la fréquence d’images, etc.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                       |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 R2 \[ uniquement\]<br/>                            |
| En-tête<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Liste alphabétique des attributs Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




