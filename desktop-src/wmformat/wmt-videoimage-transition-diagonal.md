---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl. h)
description: La transition diagonale révèle la nouvelle image le long d’une ligne diagonale, en partant d’un coin du cadre.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106527295"
---
# <a name="wmt_videoimage_transition_diagonal"></a>\_transition de \_ transition VIDEOIMAGE en \_ diagonale

La transition diagonale révèle la nouvelle image le long d’une ligne diagonale, en partant d’un coin du cadre.

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
<td>Largeur de la section diagonale en pixels.</td>
</tr>
<tr class="even">
<td>Hauteur</td>
<td><strong>fEffectPara1</strong></td>
<td>Hauteur de la section diagonale en pixels.</td>
</tr>
<tr class="odd">
<td>Sens</td>
<td><strong>fEffectPara2</strong></td>
<td>Détermine l’angle d’origine de la transition. Définissez sur l’un des éléments suivants :<br/>
<ul>
<li>0-en haut à droite</li>
<li>1-en haut à gauche</li>
<li>2-en bas à droite</li>
<li>3-en bas à gauche</li>
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

 

 





