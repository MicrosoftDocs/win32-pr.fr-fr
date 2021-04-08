---
title: Message MCM_SETTODAY (commctrl. h)
description: Définit le \ 0034 ; Today \ 0034 ; sélection pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetToday.
ms.assetid: fcd4d33d-e661-4e02-8d19-666d80e1a070
keywords:
- MCM_SETTODAY les contrôles de message Windows
topic_type:
- apiref
api_name:
- MCM_SETTODAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b725e5f61e3c08170a323b063616434acb857e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743813"
---
# <a name="mcm_settoday-message"></a>\_Message SETTODAY MCM

Définit la sélection « aujourd’hui » pour un contrôle Month Calendar. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetToday**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_settoday) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contient la date à définir comme sélection « aujourd’hui » pour le contrôle. Si ce paramètre a la valeur **null**, le contrôle retourne au paramètre par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="remarks"></a>Notes

Si la sélection « aujourd’hui » est définie sur une autre date que la valeur par défaut, les conditions suivantes s’appliquent :

-   Le contrôle ne met pas à jour automatiquement la sélection « aujourd’hui » lorsque l’heure passe à minuit pour le jour actuel.
-   Le contrôle ne met pas automatiquement à jour son affichage en fonction des modifications de paramètres régionaux.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Heures dans le contrôle Month Calendar](month-calendar-controls.md)
</dt> </dl>

 

