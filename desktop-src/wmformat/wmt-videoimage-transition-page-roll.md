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
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106520824"
---
# <a name="wmt_videoimage_transition_page_roll"></a>\_rouleau de \_ page de transition VIDEOIMAGE \_ WMT \_

La transition de retour de page transforme l’ancienne image avec un effet de basculement de page, révélant la nouvelle image en dessous.

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
<td>Radius</td>
<td><strong>fEffectPara0</strong></td>
<td>Rayon de la pellicule dans l’effet de rouleau de page.</td>
</tr>
<tr class="even">
<td>Distance</td>
<td><strong>fEffectPara1</strong></td>
<td>Quantité de la nouvelle image qui est révélée par l’effet de rouleau de page, en pixels.</td>
</tr>
<tr class="odd">
<td>Sens</td>
<td><strong>fEffectPara2</strong></td>
<td>Angle ou côté de l’image vidéo, à partir duquel le déroulement de la page est à l’origine. Définissez l’une des valeurs suivantes :<br/>
<ul>
<li>0-côté gauche</li>
<li>1-côté droit</li>
<li>2-bas</li>
<li>3-haut</li>
<li>4-angle inférieur gauche</li>
<li>5-coin inférieur droit</li>
<li>6-coin supérieur gauche</li>
<li>7-coin supérieur droit</li>
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

 

 





