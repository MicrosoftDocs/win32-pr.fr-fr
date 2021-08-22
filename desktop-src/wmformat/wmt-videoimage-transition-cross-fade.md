---
title: WMT_VIDEOIMAGE_TRANSITION_CROSS_FADE (Wmsdkidl. h)
description: La transition de fondu croisé n’a aucun effet spécial ; les caractéristiques du fondu (dissolution) sont déterminées par les membres fPrevBlendCoef et fCurrBlendCoef de la \_ \_ structure SAMPLE2 WMT VIDEOIMAGE.
ms.assetid: 254c4552-ce49-4f44-86e3-ee7d30c83000
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_CROSS_FADE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_CROSS_FADE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb7e08b1b59899c25445373ba07d72ea9851ad4269365270b3b2ebdcd4223ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083763"
---
# <a name="wmt_videoimage_transition_cross_fade"></a>\_ \_ fondu croisé de transition VIDEOIMAGE \_ WMT \_

La transition de fondu croisé n’a aucun effet spécial ; les caractéristiques du fondu (dissolution) sont déterminées par les membres **fPrevBlendCoef** et **fCurrBlendCoef** de la structure [**\_ \_ SAMPLE2 WMT VIDEOIMAGE**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) .

## <a name="parameters"></a>Paramètres

Cette transition n’accepte aucun paramètre.

## <a name="remarks"></a>Remarques

La définition de cette transition revient à affecter la valeur 0 au membre **dwEffectType** de la structure **\_ \_ SAMPLE2 WMT VIDEOIMAGE** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





