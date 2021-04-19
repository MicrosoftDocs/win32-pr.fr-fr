---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl. h)
description: La transition de la roue révèle la nouvelle image en tournant quatre lignes autour d’un point pivot commun, comme les rayons d’une roue.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- Format Windows Media WMT_VIDEOIMAGE_TRANSITION_WHEEL
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541791"
---
# <a name="wmt_videoimage_transition_wheel"></a>\_volant de \_ transition \_ VIDEOIMAGE WMT

La transition de la roue révèle la nouvelle image en tournant quatre lignes autour d’un point pivot commun, comme les rayons d’une roue.

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
<td>Coordonnée X, relative à la trame vidéo, du centre de l’effet de roulette.</td>
</tr>
<tr class="even">
<td>Centrer Y</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordonnée Y, relative à la trame vidéo, du centre de l’effet de roulette.</td>
</tr>
<tr class="odd">
<td>Angle</td>
<td><strong>fEffectPara2</strong></td>
<td>Angle de rotation, en degrés, des rayons de l’effet de roulette. La valeur 0,0 indique l’ancienne image sans que la nouvelle image soit révélée. Une valeur de 90,0 indique que la nouvelle image est entièrement dévoilée. Le mouvement de 0,0 à 90,0 apparaît sous forme de rotation des rayons dans le sens des aiguilles d’une montre.<br/></td>
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

 

 





