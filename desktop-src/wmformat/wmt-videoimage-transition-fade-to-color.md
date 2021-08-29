---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: La transition de fondu à couleur est comprise entre l’image et une image de couleur unie.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 315a0d190a65c8f756eabaff6b86dd2efb6d4dbe97e5b5de8e7a3dfe782c880a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109939"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>\_ \_ transition \_ en fondu VIDEOIMAGE WMT \_ vers la \_ couleur

La transition de fondu à couleur est comprise entre l’image et une image de couleur unie.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.



| Paramètre         | Membre de structure | Description                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Rouge               | **fEffectPara0** | Valeur rouge de la couleur d’arrière-plan. Défini sur un nombre compris entre 0 et 255.                                                                                                                                                     |
| Vert             | **fEffectPara1** | Valeur verte de la couleur d’arrière-plan. Défini sur un nombre compris entre 0 et 255.                                                                                                                                                   |
| Bleu              | **fEffectPara2** | Valeur bleue de la couleur d’arrière-plan. Défini sur un nombre compris entre 0 et 255.                                                                                                                                                    |
| Poids de l’arrière-plan | **fEffectPara3** | Poids de la couleur d’arrière-plan. Ce paramètre exprime le pourcentage de la couleur d’arrière-plan dans la combinaison en tant que valeur décimale. Par exemple, pour mélanger la couleur d’arrière-plan à 30%, en faisant de l’image 70% de la combinaison, définissez sur 0,30. |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





