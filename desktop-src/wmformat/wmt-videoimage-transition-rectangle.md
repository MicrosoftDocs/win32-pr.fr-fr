---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl. h)
description: La transition de rectangle révèle la nouvelle image dans un rectangle dans le cadre.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521670"
---
# <a name="wmt_videoimage_transition_rectangle"></a>\_rectangle de \_ transition \_ VIDEOIMAGE WMT

La transition de rectangle révèle la nouvelle image dans un rectangle dans le cadre.

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
<td>Coordonnée X, relative à la trame vidéo, au centre du rectangle.</td>
</tr>
<tr class="even">
<td>Centrer Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordonnée Y, relative à la trame vidéo, au centre du rectangle.</td>
</tr>
<tr class="odd">
<td>Largeur</td>
<td><strong>fEffectPara2</strong></td>
<td>Largeur du rectangle en pixels.</td>
</tr>
<tr class="even">
<td>Hauteur</td>
<td><strong>fEffectPara3</strong></td>
<td>Hauteur du rectangle en pixels.</td>
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

 

 





