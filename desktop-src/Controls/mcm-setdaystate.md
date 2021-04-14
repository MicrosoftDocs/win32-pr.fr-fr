---
title: Message MCM_SETDAYSTATE (commctrl. h)
description: Définit les États du jour pour tous les mois actuellement visibles dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetDayState.
ms.assetid: 518cb2a9-ea82-40b4-88ca-f901b6f9f8c4
keywords:
- MCM_SETDAYSTATE les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETDAYSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6174cc7d8d97d424d599671740530dd8014cc998
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466802"
---
# <a name="mcm_setdaystate-message"></a>\_Message SETDAYSTATE MCM

Définit les États du jour pour tous les mois actuellement visibles dans un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetDayState**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setdaystate) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeur indiquant le nombre d’éléments dans le tableau vers lequel *lParam* pointe.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau de valeurs [**MONTHDAYSTATE**](monthdaystate.md) qui définissent la façon dont le contrôle Month Calendar dessine chaque jour dans son affichage.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Notes

Une application peut définir explicitement des informations d’état de jour en envoyant ce message, mais l’État ne sera pas conservé lorsqu’une autre partie du calendrier défilera vers l’affichage. Les informations d’État du jour sont généralement définies en réponse au code de notification [MCN \_ GETDAYSTATE](mcn-getdaystate.md) , qui est envoyé chaque fois que le contrôle doit être actualisé.

Le tableau au niveau de *lParam* doit contenir autant d’éléments que la valeur retournée par la macro suivante :

`MonthCal_GetMonthRange(hwndMC, GMR_DAYSTATE, NULL);`

Gardez à l’esprit que le tableau au niveau de *lParam* doit contenir des valeurs [**MONTHDAYSTATE**](monthdaystate.md) qui correspondent à tous les mois actuellement dans l’affichage du contrôle, dans l’ordre chronologique. Cela comprend les deux mois qui peuvent être partiellement affichés avant le premier mois et après le mois précédent.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Utilisation des contrôles Month Calendar](using-month-calendar-controls.md)
</dt> </dl>

 

 





