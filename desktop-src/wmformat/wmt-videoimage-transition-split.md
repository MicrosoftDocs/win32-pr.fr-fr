---
title: WMT_VIDEOIMAGE_TRANSITION_SPLIT (Wmsdkidl. h)
description: La transition de fractionnement révèle la nouvelle image en fractionnant l’ancienne image. Le fractionnement s’affiche sur une ligne horizontale ou verticale droite à partir du cadre.
ms.assetid: ad777bfb-29a7-441f-8399-e462639450eb
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_SPLIT
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SPLIT
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aa478220064fb896150301112ef5afea0078659789f7fc617608cdb1eec323
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089599"
---
# <a name="wmt_videoimage_transition_split"></a>\_ \_ fractionnement de transition VIDEOIMAGE WMT \_

La transition de fractionnement révèle la nouvelle image en fractionnant l’ancienne image. Le fractionnement s’affiche sur une ligne horizontale ou verticale droite à partir du cadre.

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
<td>Centrer X</td>
<td><strong>fEffectPara0</strong></td>
<td>Coordonnée X, relative à la trame vidéo, de la ligne d’origine de la Division.</td>
</tr>
<tr class="even">
<td>Centrer Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordonnée Y, relative à la trame vidéo, de la ligne d’origine de la Division.</td>
</tr>
<tr class="odd">
<td>Distance</td>
<td><strong>fEffectPara2</strong></td>
<td>Largeur du fractionnement en pixels.</td>
</tr>
<tr class="even">
<td>Sens</td>
<td><strong>fEffectPara3</strong></td>
<td>Orientation du fractionnement. Définissez l’une des valeurs suivantes :<br/>
<ul>
<li>0-fractionne le long d’une ligne horizontale.</li>
<li>1-fractionne le long d’une ligne verticale.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composition</td>
<td><strong>fEffectPara4</strong></td>
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

 

 





