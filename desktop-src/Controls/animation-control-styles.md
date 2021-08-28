---
title: Styles de contrôle d’animation (CommCtrl. h)
description: Cette section répertorie les styles de fenêtre utilisés avec les contrôles d’animation.
ms.assetid: ad4fc4fd-166d-4871-9f60-5133a48681aa
topic_type:
- apiref
api_name:
- ACS_AUTOPLAY
- ACS_CENTER
- ACS_TIMER
- ACS_TRANSPARENT
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 314a7cd6aebb4a3535d7a0b7c7f20adc35a567c99ec428bc0446d70a197bd131
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020047"
---
# <a name="animation-control-styles"></a>Styles de contrôle d’animation

Cette section répertorie les styles de fenêtre utilisés avec les contrôles d’animation.



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
<td style="text-align: left;"><span id="ACS_AUTOPLAY"></span><span id="acs_autoplay"></span><dl> <dt><strong>ACS_AUTOPLAY</strong></dt> </dl></td>
<td style="text-align: left;">Démarre la diffusion de l’animation dès l’ouverture du clip AVI. <br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_CENTER"></span><span id="acs_center"></span><dl> <dt><strong>ACS_CENTER</strong></dt> </dl></td>
<td style="text-align: left;">Centre l’animation dans la fenêtre du contrôle d’animation. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="ACS_TIMER"></span><span id="acs_timer"></span><dl> <dt><strong>ACS_TIMER</strong></dt> </dl></td>
<td style="text-align: left;">Par défaut, le contrôle crée un thread pour lire le clip AVI. Si vous définissez cet indicateur, le contrôle lit le clip sans créer de thread. en interne, le contrôle utilise un minuteur Win32 pour synchroniser la lecture. <br/> <strong>Comctl32.dll version 6 et versions ultérieures :</strong> Ce style n’est pas pris en charge. Par défaut, le contrôle lit le clip AVI sans créer de thread.<br/>
<blockquote>
[!Note]<br />
Comctl32.dll version 6 n’est pas redistribuable. Pour utiliser Comctl32.dll version 6, spécifiez-la dans un manifeste. Pour plus d’informations sur les manifestes, consultez <a href="cookbook-overview.md">activation des styles visuels</a>.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="ACS_TRANSPARENT"></span><span id="acs_transparent"></span><dl> <dt><strong>ACS_TRANSPARENT</strong></dt> </dl></td>
<td style="text-align: left;">Vous permet de faire correspondre la couleur d’arrière-plan d’une animation à celle de la fenêtre sous-jacente, en créant un &quot; &quot; arrière-plan transparent. Le parent du contrôle d’animation ne doit pas avoir le style WS_CLIPCHILDREN (consultez <a href="/windows/desktop/winmsg/window-styles">styles de fenêtre</a>). Le contrôle envoie un message <a href="wm-ctlcolorstatic.md"><strong>WM_CTLCOLORSTATIC</strong></a> à son parent. Utilisez <a href="/windows/desktop/api/wingdi/nf-wingdi-setbkcolor"><strong>SetBkColor</strong></a> pour définir la couleur d’arrière-plan du contexte de périphérique sur une valeur appropriée. Le contrôle interprète le pixel supérieur gauche de la première image comme la couleur d’arrière-plan par défaut de l’animation. Il remappera tous les pixels avec cette couleur à la valeur que vous avez fournie en réponse à WM_CTLCOLORSTATIC. <br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



