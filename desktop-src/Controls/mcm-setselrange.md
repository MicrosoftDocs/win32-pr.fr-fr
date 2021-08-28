---
title: Message MCM_SETSELRANGE (commctrl. h)
description: Définit la sélection d’un contrôle Month Calendar sur une plage de dates donnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro calendrier monthcal SetSelRange.
ms.assetid: 750b0c83-6baa-4caa-a738-feae8751a70e
keywords:
- MCM_SETSELRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_SETSELRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdf6708aa382abfa92562aa55943c06180d0231cff568b74de380416e48731a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018977"
---
# <a name="mcm_setselrange-message"></a>\_Message SETSELRANGE MCM

Définit la sélection d’un contrôle Month Calendar sur une plage de dates donnée. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**calendrier monthcal \_ SetSelRange**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setselrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contiennent des informations de date représentant les limites de sélection. La première date sélectionnée doit être spécifiée dans *lpSysTimeArray* \[ 0 \] et la dernière date sélectionnée doit être spécifiée dans *lpSysTimeArray* \[ 1 \] .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire. Ce message échouera s’il est appliqué à un contrôle Month Calendar qui n’utilise pas le style [**MCS \_ MultiSelect**](month-calendar-control-styles.md) .

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

 

