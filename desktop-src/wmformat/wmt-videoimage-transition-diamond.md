---
title: WMT_VIDEOIMAGE_TRANSITION_DIAMOND (Wmsdkidl. h)
description: La transition Diamond révèle la nouvelle image dans un losange.
ms.assetid: ff36a64d-62f7-424d-acc9-a7902926a90c
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_DIAMOND
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAMOND
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af271c220fc48924905a067336a438baec1ef0ac4b2dca1b266d3ea77d665f71
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117653280"
---
# <a name="wmt_videoimage_transition_diamond"></a>\_transition VIDEOIMAGE WMT- \_ \_ losange

La transition Diamond révèle la nouvelle image dans un losange.

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
<td>Coordonnée X, relative à la trame vidéo, au centre du losange.</td>
</tr>
<tr class="even">
<td>Centrer Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordonnée Y, relative à la trame vidéo, au centre du losange.</td>
</tr>
<tr class="odd">
<td>Largeur</td>
<td><strong>fEffectPara2</strong></td>
<td>Largeur du losange en pixels.</td>
</tr>
<tr class="even">
<td>Hauteur</td>
<td><strong>fEffectPara3</strong></td>
<td>Hauteur du losange en pixels.</td>
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

 

 





