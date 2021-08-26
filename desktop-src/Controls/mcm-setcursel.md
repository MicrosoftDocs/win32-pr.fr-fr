---
title: Message MCM_SETCURSEL (commctrl. h)
description: Définit la date actuellement sélectionnée pour un contrôle Month Calendar. Si la date spécifiée n’est pas affichée, le contrôle met à jour l’affichage pour l’afficher. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetCurSel.
ms.assetid: 2a9f82a1-66d9-44dd-b60f-b588b4688316
keywords:
- MCM_SETCURSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_SETCURSEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e63238f11f93e56c18e1897fcdd3cb96977f23fe16bde19123b5c063f99c0ff0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061889"
---
# <a name="mcm_setcursel-message"></a>\_Message SETCURSEL MCM

Définit la date actuellement sélectionnée pour un contrôle Month Calendar. Si la date spécifiée n’est pas affichée, le contrôle met à jour l’affichage pour l’afficher. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setcursel) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contient la date à définir comme sélection actuelle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire. Ce message échouera s’il est appliqué à un contrôle Month Calendar qui utilise le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Heures dans le contrôle Month Calendar](month-calendar-controls.md)
</dt> </dl>

 

