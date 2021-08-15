---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: La transition de révélation révèle la nouvelle image le long d’une ligne droite provenant d’un côté du cadre.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_REVEAL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b916a5142f09628852a016754f9fb3ad691882731466d802b8367e03837b9699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083733"
---
# <a name="wmt_videoimage_transition_reveal"></a>\_révélation de \_ transition \_ VIDEOIMAGE WMT

La transition de révélation révèle la nouvelle image le long d’une ligne droite provenant d’un côté du cadre.

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
<td>Quantité de la nouvelle image révélée, en pixels. Cette valeur est relative au côté origine du frame.</td>
</tr>
<tr class="even">
<td>Sens</td>
<td><strong>fEffectPara1</strong></td>
<td>Direction de la révélation. Définissez l’une des valeurs suivantes :<br/>
<ul>
<li>0-révéler à droite ; proviennent du côté gauche du frame.</li>
<li>1-révéler à gauche ; proviennent du côté droit du frame.</li>
<li>2-révéler vers le haut ; proviennent du bas du frame.</li>
<li>3-révéler à la baisse ; proviennent du haut du frame.</li>
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

 

 





