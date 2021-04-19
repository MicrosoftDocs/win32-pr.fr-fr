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
ms.openlocfilehash: 725691dd39b271894558567fb4f86511f75e2589
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541271"
---
# <a name="wmt_videoimage_transition_cross_fade"></a>\_ \_ fondu croisé de transition VIDEOIMAGE \_ WMT \_

La transition de fondu croisé n’a aucun effet spécial ; les caractéristiques du fondu (dissolution) sont déterminées par les membres **fPrevBlendCoef** et **fCurrBlendCoef** de la structure [**\_ \_ SAMPLE2 WMT VIDEOIMAGE**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) .

## <a name="parameters"></a>Paramètres

Cette transition n’accepte aucun paramètre.

## <a name="remarks"></a>Notes

La définition de cette transition revient à affecter la valeur 0 au membre **dwEffectType** de la structure **\_ \_ SAMPLE2 WMT VIDEOIMAGE** .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





