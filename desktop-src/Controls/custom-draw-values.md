---
title: Valeurs de dessin personnalisées (CommCtrl. h)
description: Cette section répertorie les valeurs utilisées pour identifier les parties d’un contrôle TrackBar.
ms.assetid: 154321c7-99f8-4ed5-a5ff-fb96126b43c7
topic_type:
- apiref
api_name:
- TBCD_CHANNEL
- TBCD_THUMB
- TBCD_TICS
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccf05ab951fdc83ec5be414688be56d710ba0d98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537471"
---
# <a name="custom-draw-values"></a>Valeurs de dessin personnalisées

Cette section répertorie les valeurs utilisées pour identifier les parties d’un contrôle TrackBar.



| Constante                                                                                                                                                   | Description                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canal TBCD**</dt> </dl> | Identifie le canal que le marqueur de curseur de défilement du contrôle TrackBar délimite.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**\_Thumb TBCD**</dt> </dl>       | Identifie le marqueur de curseur de défilement du contrôle TrackBar. Il s’agit de la partie du contrôle que l’utilisateur déplace.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ tics**</dt> </dl>          | Identifie les graduations affichées le long du bord du contrôle TrackBar.<br/>                      |



## <a name="remarks"></a>Notes

Les valeurs de dessin personnalisées, par exemple, sont spécifiées dans le membre **dwItemSpec** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





