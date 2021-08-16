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
ms.openlocfilehash: 2f815e0bb1fc7e8e1cba277f68b7950af2b20395092b69b2c07ebb7ac51367da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843788"
---
# <a name="wmt_videoimage_transition_inset"></a>inversion de \_ transition VIDEOIMAGE WMT \_ \_

La transition incrustée révèle la nouvelle image dans un rectangle provenant d’un coin du cadre.

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
<td>Largeur de l’incrustation en pixels.</td>
</tr>
<tr class="even">
<td>Hauteur</td>
<td><strong>fEffectPara1</strong></td>
<td>Hauteur de l’incrustation en pixels.</td>
</tr>
<tr class="odd">
<td>Sens</td>
<td><strong>fEffectPara2</strong></td>
<td>Angle d’origine de l’encart. Définissez l’une des valeurs suivantes :<br/>
<ul>
<li>0-en bas à gauche</li>
<li>1-en bas à droite</li>
<li>2-en haut à gauche</li>
<li>3-en haut à droite</li>
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

 

 





