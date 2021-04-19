---
title: Styles de contrôle de barre de progression (CommCtrl. h)
description: Les styles de contrôle suivants sont pris en charge par les contrôles de barre de progression
ms.assetid: bd89aa74-c15e-4745-8b2b-7cbd8b28c1c8
topic_type:
- apiref
api_name:
- PBS_MARQUEE
- PBS_SMOOTH
- PBS_SMOOTHREVERSE
- PBS_VERTICAL
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d55ec928fb1ee2715576f3131dde0f661a91fcf8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523603"
---
# <a name="progress-bar-control-styles"></a>Styles de contrôle de barre de progression

Les styles de contrôle suivants sont pris en charge par les contrôles de [barre de progression](progress-bar-control.md) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Constante</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_MARQUEE"></span><span id="pbs_marquee"></span><dl> <dt><strong>PBS_MARQUEE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,0</a> ou ultérieure. La taille de l’indicateur de progression n’augmente pas, mais se déplace à plusieurs reprises le long de la longueur de la barre, ce qui indique l’activité sans spécifier quelle proportion de la progression est terminée. <br/>
<blockquote>
[!Note]<br />
Comctl32.dll version 6 n’est pas redistribuable, mais elle est incluse dans Windows ou version ultérieure. Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_SMOOTH"></span><span id="pbs_smooth"></span><dl> <dt><strong>PBS_SMOOTH</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 4,70</a> ou ultérieure. La barre de progression affiche l’état de progression dans une barre de défilement lisse au lieu de la barre segmentée par défaut. <br/>
<blockquote>
[!Note]<br />
Ce style est pris en charge uniquement dans le thème Windows classique. Tous les autres thèmes remplacent ce style.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="PBS_SMOOTHREVERSE"></span><span id="pbs_smoothreverse"></span><dl> <dt><strong>PBS_SMOOTHREVERSE</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 6,0</a> ou ultérieure et <strong>Windows Vista.</strong> Détermine le comportement d’animation que la barre de progression doit utiliser lors du déplacement vers l’arrière (d’une valeur supérieure à une valeur inférieure). Si cette valeur est définie, une &quot; &quot; transition en douceur aura lieu, sinon le contrôle &quot; passera &quot; à la valeur inférieure.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="PBS_VERTICAL"></span><span id="pbs_vertical"></span><dl> <dt><strong>PBS_VERTICAL</strong></dt> </dl></td>
<td style="text-align: left;"><a href="common-control-versions.md">Version 4,70</a> ou ultérieure. La barre de progression affiche l’état de progression verticalement, de bas en haut.<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Notes

Vous pouvez définir des styles de barre de progression, de la même façon que d’autres contrôles communs, avec [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa), [**GetWindowLong**](/windows/desktop/api/winuser/nf-winuser-getwindowlonga)ou [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

