---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl. h)
description: La transition incrustée révèle la nouvelle image dans un rectangle provenant d’un coin du cadre.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_INSET
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47d53de99d3c6f6144755934989ca3958d28a23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476778"
---
# <a name="wmt_videoimage_transition_inset"></a>inversion de \_ transition VIDEOIMAGE WMT \_ \_

La transition incrustée révèle la nouvelle image dans un rectangle provenant d’un coin du cadre.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Largeur | <strong>fEffectPara0</strong> | Largeur de l’incrustation en pixels. | 
| Hauteur | <strong>fEffectPara1</strong> | Hauteur de l’incrustation en pixels. | 
| Sens | <strong>fEffectPara2</strong> | Angle d’origine de l’encart. Définissez l’une des valeurs suivantes :<br /><ul><li>0-en bas à gauche</li><li>1-en bas à droite</li><li>2-en haut à gauche</li><li>3-en haut à droite</li></ul> | 
| Composition | <strong>fEffectPara3</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





