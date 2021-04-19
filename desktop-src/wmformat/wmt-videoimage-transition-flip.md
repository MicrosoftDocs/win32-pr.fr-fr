---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl. h)
description: La transition de retournement fait pivoter l’ancienne image sur un axe y à travers le centre du cadre. La nouvelle image est révélée à l’arrière de l’ancienne image.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_FLIP
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc92ad1dfffd945b89293dd9207289aa47645d4f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537702"
---
# <a name="wmt_videoimage_transition_flip"></a>\_ \_ basculement de transition VIDEOIMAGE WMT \_

La transition de retournement fait pivoter l’ancienne image sur un axe y à travers le centre du cadre. La nouvelle image est révélée à l’arrière de l’ancienne image.

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
<td>Angle</td>
<td><strong>fEffectPara0</strong></td>
<td>Angle de rotation, de 0,0 à 180,0 degrés.</td>
</tr>
<tr class="even">
<td>Composition</td>
<td><strong>fEffectPara1</strong></td>
<td>Définissez l’une des valeurs suivantes :
<ul>
<li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li>
<li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Vous pouvez visualiser l’effet de cette transition comme si les deux images étaient des photographies physiques collées en arrière-plan. La transition a le même effet que le maintien de deux photographies de ce type au centre du bord inférieur et les faire pivoter de 180 degrés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Transitions d’images vidéo**](video-image-transitions.md)
</dt> </dl>

 

 





