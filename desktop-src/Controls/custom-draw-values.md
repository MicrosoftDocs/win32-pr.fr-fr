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
ms.openlocfilehash: cb714df7c91819a7d459c4c9fbed1fbc1e0d4fd2455f52891030d95991fa6497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117831690"
---
# <a name="custom-draw-values"></a>Valeurs de dessin personnalisées

Cette section répertorie les valeurs utilisées pour identifier les parties d’un contrôle TrackBar.



| Constante                                                                                                                                                   | Description                                                                                                     |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| <span id="TBCD_CHANNEL"></span><span id="tbcd_channel"></span><dl> <dt>**\_canal TBCD**</dt> </dl> | Identifie le canal que le marqueur de curseur de défilement du contrôle TrackBar délimite.<br/>                        |
| <span id="TBCD_THUMB"></span><span id="tbcd_thumb"></span><dl> <dt>**\_Thumb TBCD**</dt> </dl>       | Identifie le marqueur de curseur de défilement du contrôle TrackBar. Il s’agit de la partie du contrôle que l’utilisateur déplace.<br/> |
| <span id="TBCD_TICS"></span><span id="tbcd_tics"></span><dl> <dt>**TBCD \_ tics**</dt> </dl>          | Identifie les graduations affichées le long du bord du contrôle TrackBar.<br/>                      |



## <a name="remarks"></a>Remarques

Les valeurs de dessin personnalisées, par exemple, sont spécifiées dans le membre **dwItemSpec** de la structure [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

 





