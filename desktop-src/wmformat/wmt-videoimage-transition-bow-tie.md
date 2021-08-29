---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl. h)
description: La transition de liaison papillone révèle la nouvelle image dans un ensemble de triangles sur les côtés opposés du cadre.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45b61314709f6b0000281ac54e10f8aa702a9b24
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471515"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>\_liaison d' \_ étrave de transition VIDEOIMAGE \_ WMT \_

La transition de liaison papillone révèle la nouvelle image dans un ensemble de triangles sur les côtés opposés du cadre.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.




| Paramètre | Membre de structure | Description | 
|-----------|------------------|-------------|
| Largeur | <strong>fEffectPara0</strong> | Largeur de chaque côté triangulaire de l’égalité d’étrave. | 
| Hauteur | <strong>fEffectPara1</strong> | Hauteur de chaque côté triangulaire de l’égalité d’étrave. | 
| Sens | <strong>fEffectPara2</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie l’effet de lien d’étrave horizontal, dans lequel les triangles entrent à partir des côtés droit et gauche du cadre.</li><li>1-spécifie l’effet de lien d’inclinaison vertical, dans lequel les triangles entrent en haut et en bas du cadre.</li></ul> | 
| Composition | <strong>fEffectPara3</strong> | Définissez l’une des valeurs suivantes :<ul><li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li><li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan.</li></ul> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





