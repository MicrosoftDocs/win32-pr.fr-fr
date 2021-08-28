---
title: Message MCM_SETRANGE (commctrl. h)
description: Définit les dates minimale et maximale autorisées pour un contrôle Month Calendar. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la \_ macro SetRange calendrier monthcal.
ms.assetid: dab9ebb0-f397-4e71-b060-ef8d7d89a6bc
keywords:
- MCM_SETRANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- MCM_SETRANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c66e9cca17aabd93bfba896d361da6b90eab0c5c21fc4d50ec3c81a9eba5ccd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119319249"
---
# <a name="mcm_setrange-message"></a>\_Message de SEtrange MCM

Définit les dates minimale et maximale autorisées pour un contrôle Month Calendar. Vous pouvez envoyer ce message de manière explicite ou à l’aide de la macro [**\_ SetRange calendrier monthcal**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_setrange) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Valeurs d’indicateur qui spécifient quelles limites de date sont définies. Cette valeur doit être l’une des valeurs suivantes, ou les deux :



| Valeur                                                                                                                                          | Signification                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GDTR_MAX"></span><span id="gdtr_max"></span><dl> <dt>**GDTR \_ Max**</dt> </dl> | La date maximale autorisée est définie. La structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) à *lpSysTimeArray* \[ 1 \] doit contenir des informations de date. <br/> |
| <span id="GDTR_MIN"></span><span id="gdtr_min"></span><dl> <dt>**GDTR \_ min.**</dt> </dl> | La date minimale autorisée est définie. La structure [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) à *lpSysTimeArray* \[ 0 \] doit contenir des informations de date. <br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau à deux éléments de structures [**SystemTime**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime) qui contiennent les limites de date. La limite maximale doit être comprise dans *lpSysTimeArray* \[ 1 \] si GDTR \_ Max est spécifié, et *lpSysTimeArray* \[ 0 \] doit contenir la limite minimale si GDTR \_ min est spécifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

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

 

