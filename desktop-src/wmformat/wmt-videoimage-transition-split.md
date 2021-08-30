---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl. h)
description: La transition de fractionnement révèle la nouvelle image en fractionnant l’ancienne image. Le fractionnement s’affiche sur une ligne horizontale ou verticale droite à partir du cadre.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_SPLIT
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a8ae4e805d61ea83f2e5e6cb80d1424547be6a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474695"
---
# <a name="wmt_videoimage_transition_split"></a>\_ \_ fractionnement de transition VIDEOIMAGE WMT \_

La transition de fractionnement révèle la nouvelle image en fractionnant l’ancienne image. Le fractionnement s’affiche sur une ligne horizontale ou verticale droite à partir du cadre.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Centrer X | <strong>fEffectPara0</strong> | Coordonnée X, relative à la trame vidéo, de la ligne d’origine de la Division. | 
| Centrer Y | <strong>fEffectPara1</strong> | Coordonnée Y, relative à la trame vidéo, de la ligne d’origine de la Division. | 
| Distance | <strong>fEffectPara2</strong> | Largeur du fractionnement en pixels. | 
| Sens | <strong>fEffectPara3</strong> | Orientation du fractionnement. Définissez l’une des valeurs suivantes :<br /><ul><li>0-fractionne le long d’une ligne horizontale.</li><li>1-fractionne le long d’une ligne verticale.</li></ul> | 
| Composition | <strong>fEffectPara4</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





