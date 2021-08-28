---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: La transition de révélation révèle la nouvelle image le long d’une ligne droite provenant d’un côté du cadre.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_REVEAL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140271d365d9673c948c4ff6f540e9bef33e8006
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469316"
---
# <a name="wmt_videoimage_transition_reveal"></a>\_révélation de \_ transition \_ VIDEOIMAGE WMT

La transition de révélation révèle la nouvelle image le long d’une ligne droite provenant d’un côté du cadre.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Distance | <strong>fEffectPara0</strong> | Quantité de la nouvelle image révélée, en pixels. Cette valeur est relative au côté origine du frame. | 
| Sens | <strong>fEffectPara1</strong> | Direction de la révélation. Définissez l’une des valeurs suivantes :<br /><ul><li>0-révéler à droite ; proviennent du côté gauche du frame.</li><li>1-révéler à gauche ; proviennent du côté droit du frame.</li><li>2-révéler vers le haut ; proviennent du bas du frame.</li><li>3-révéler à la baisse ; proviennent du haut du frame.</li></ul> | 
| Composition | <strong>fEffectPara2</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





