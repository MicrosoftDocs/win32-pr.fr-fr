---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl. h)
description: La transition de V remplie révèle la nouvelle image dans un triangle provenant d’un côté du frame.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_FILLED_V
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbf032700959dd21a560b879357de2800ac657b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466156"
---
# <a name="wmt_videoimage_transition_filled_v"></a>VIDEOIMAGE de transition à la \_ \_ transition WMT \_ \_

La transition de V remplie révèle la nouvelle image dans un triangle provenant d’un côté du frame.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Largeur | <strong>fEffectPara0</strong> | Largeur du V rempli en pixels. | 
| Hauteur | <strong>fEffectPara1</strong> | Hauteur du V rempli en pixels. | 
| Sens | <strong>fEffectPara2</strong> | Direction d’origine du V rempli. Définissez l’une des valeurs suivantes :<br /><ul><li>0-entre le côté gauche du cadre.</li><li>1 : entre le côté droit du cadre.</li><li>2-entre le bas du cadre.</li><li>3-entre le haut du cadre.</li></ul> | 
| Composition | <strong>fEffectPara3</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





