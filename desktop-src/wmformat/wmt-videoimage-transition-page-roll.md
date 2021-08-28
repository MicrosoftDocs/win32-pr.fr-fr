---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: La transition de retour de page transforme l’ancienne image avec un effet de basculement de page, révélant la nouvelle image en dessous.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfa69988f5b5414eac3e27b3371bca0e0a28810
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474975"
---
# <a name="wmt_videoimage_transition_page_roll"></a>\_rouleau de \_ page de transition VIDEOIMAGE \_ WMT \_

La transition de retour de page transforme l’ancienne image avec un effet de basculement de page, révélant la nouvelle image en dessous.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Radius | <strong>fEffectPara0</strong> | Rayon de la pellicule dans l’effet de rouleau de page. | 
| Distance | <strong>fEffectPara1</strong> | Quantité de la nouvelle image qui est révélée par l’effet de rouleau de page, en pixels. | 
| Sens | <strong>fEffectPara2</strong> | Angle ou côté de l’image vidéo, à partir duquel le déroulement de la page est à l’origine. Définissez l’une des valeurs suivantes :<br /><ul><li>0-côté gauche</li><li>1-côté droit</li><li>2-bas</li><li>3-haut</li><li>4-angle inférieur gauche</li><li>5-coin inférieur droit</li><li>6-coin supérieur gauche</li><li>7-coin supérieur droit</li></ul> | 
| Composition | <strong>fEffectPara3</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





