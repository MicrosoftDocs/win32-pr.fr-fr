---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl. h)
description: La transition en étoile révèle la nouvelle image dans une étoile à cinq branches dans le cadre.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_STAR
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7524e51908f7d941aa04b138cc67ba6c4ab6a2a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479495"
---
# <a name="wmt_videoimage_transition_star"></a>\_étoile de \_ transition \_ VIDEOIMAGE WMT

La transition en étoile révèle la nouvelle image dans une étoile à cinq branches dans le cadre.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Centrer X | <strong>fEffectPara0</strong> | Coordonnée X, relative à la trame vidéo, au centre de l’étoile. | 
| Centrer Y | <strong>fEffectPara1</strong> | Coordonnée Y, relative à la trame vidéo, au centre de l’étoile. | 
| Radius | <strong>fEffectPara2</strong> | Rayon, en pixels, du cercle défini par les points de l’étoile. | 
| Composition | <strong>fEffectPara3</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan.</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





