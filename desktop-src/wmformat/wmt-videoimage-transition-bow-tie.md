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
ms.openlocfilehash: 6f77cd2782bad6e4f83b5a4d1e719b0c21d704fefd2d4cccacfc0690a4fb0fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843950"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>\_liaison d' \_ étrave de transition VIDEOIMAGE \_ WMT \_

La transition de liaison papillone révèle la nouvelle image dans un ensemble de triangles sur les côtés opposés du cadre.

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
<td>Largeur de chaque côté triangulaire de l’égalité d’étrave.</td>
</tr>
<tr class="even">
<td>Hauteur</td>
<td><strong>fEffectPara1</strong></td>
<td>Hauteur de chaque côté triangulaire de l’égalité d’étrave.</td>
</tr>
<tr class="odd">
<td>Sens</td>
<td><strong>fEffectPara2</strong></td>
<td>Définissez l’une des valeurs suivantes :
<ul>
<li>0-spécifie l’effet de lien d’étrave horizontal, dans lequel les triangles entrent à partir des côtés droit et gauche du cadre.</li>
<li>1-spécifie l’effet de lien d’inclinaison vertical, dans lequel les triangles entrent en haut et en bas du cadre.</li>
</ul></td>
</tr>
<tr class="even">
<td>Composition</td>
<td><strong>fEffectPara3</strong></td>
<td>Définissez l’une des valeurs suivantes :
<ul>
<li>0-spécifie une composition normale dans laquelle l’image précédente est l’arrière-plan et l’image actuelle est le premier plan.</li>
<li>1-spécifie la composition inversée, dans laquelle l’image actuelle est l’image d’arrière-plan, et l’image précédente est le premier plan.</li>
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

 

 





