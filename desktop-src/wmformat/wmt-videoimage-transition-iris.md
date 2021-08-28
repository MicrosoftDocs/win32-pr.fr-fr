---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl. h)
description: La transition Iris affiche la nouvelle image le long d’un axe x et un axe y. L’effet visuel de cette transition est que la nouvelle image apparaît dans une croix étendue qui atteint tous les côtés du cadre.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_IRIS
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919af0b15ef8a7437c9852df3ff12623553cdabf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472965"
---
# <a name="wmt_videoimage_transition_iris"></a>\_VIDEOIMAGE de \_ transition de BASCULement WMT \_

La transition Iris affiche la nouvelle image le long d’un axe x et un axe y. L’effet visuel de cette transition est que la nouvelle image apparaît dans une croix étendue qui atteint tous les côtés du cadre.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Centrer X | <strong>fEffectPara0</strong> | Coordonnée X, relative à la trame vidéo, du centre de l’effet IRIS. | 
| Centrer Y | <strong>fEffectPara1</strong> | Coordonnée Y, relative à la trame vidéo, du centre de l’effet IRIS. | 
| Largeur | <strong>fEffectPara2</strong> | Largeur de la ligne verticale qui révèle la nouvelle image, en pixels. | 
| Hauteur | <strong>fEffectPara3</strong> | Hauteur de la ligne horizontale qui révèle la nouvelle image, en pixels. | 
| Composition | <strong>fEffectPara4</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





