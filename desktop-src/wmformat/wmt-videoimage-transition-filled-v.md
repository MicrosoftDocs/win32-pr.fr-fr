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
ms.openlocfilehash: cfe229657dfd29d3cb9d83a8a4853e2e89a7a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542449"
---
# <a name="wmt_videoimage_transition_filled_v"></a>VIDEOIMAGE de transition à la \_ \_ transition WMT \_ \_

La transition de V remplie révèle la nouvelle image dans un triangle provenant d’un côté du frame.

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
<td>Largeur</td>
<td><strong>fEffectPara0</strong></td>
<td>Largeur du V rempli en pixels.</td>
</tr>
<tr class="even">
<td>Hauteur</td>
<td><strong>fEffectPara1</strong></td>
<td>Hauteur du V rempli en pixels.</td>
</tr>
<tr class="odd">
<td>Sens</td>
<td><strong>fEffectPara2</strong></td>
<td>Direction d’origine du V rempli. Définissez l’une des valeurs suivantes :<br/>
<ul>
<li>0-entre le côté gauche du cadre.</li>
<li>1 : entre le côté droit du cadre.</li>
<li>2-entre le bas du cadre.</li>
<li>3-entre le haut du cadre.</li>
</ul></td>
</tr>
<tr class="even">
<td>Composition</td>
<td><strong>fEffectPara3</strong></td>
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

 

 





