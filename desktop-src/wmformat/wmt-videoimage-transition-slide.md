---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl. h)
description: La transition de la diapositive révèle la nouvelle image en faisant glisser l’ancienne image hors du cadre.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_SLIDE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523993"
---
# <a name="wmt_videoimage_transition_slide"></a>\_diapositive de \_ transition \_ VIDEOIMAGE WMT

La transition de la diapositive révèle la nouvelle image en faisant glisser l’ancienne image hors du cadre.

## <a name="parameters"></a>Paramètres

Le tableau suivant décrit les paramètres utilisés par cette transition et répertorie les membres de la structure [**\_ \_ SAMPLE2 VIDEOIMAGE WMT**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à laquelle ils sont assignés.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Paramètre</th>
<th>Membre de structure</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Distance</td>
<td><strong>fEffectPara0</strong></td>
<td>Distance, en pixels, à partir de laquelle l’ancienne image s’éloigne du cadre.</td>
</tr>
<tr class="even">
<td>Sens</td>
<td><strong>fEffectPara1</strong></td>
<td>Sens dans lequel l’ancienne image diapositives. Définissez l’une des valeurs suivantes :<br/>
<ul>
<li>0-glissement vers la droite.</li>
<li>1-déplacer vers la gauche.</li>
<li>2-glissez vers le haut.</li>
<li>3-déplacer vers le bas.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composition</td>
<td><strong>fEffectPara2</strong></td>
<td>Définissez l’une des valeurs suivantes :
<ul>
<li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li>
<li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





