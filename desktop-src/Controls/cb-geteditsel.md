---
title: Message CB_GETEDITSEL (winuser. h)
description: Obtient les positions des caractères de début et de fin de la sélection actuelle dans le contrôle d’édition d’une zone de liste déroulante.
ms.assetid: 72b64135-e35a-4f72-9fc7-e6bedf495f23
keywords:
- CB_GETEDITSEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETEDITSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 220750e96e08455eb36e6b6d698fb99056ad3dca6dfbb51054c6cd7cc33fd7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171604"
---
# <a name="cb_geteditsel-message"></a>\_Message GETEDITSEL CB

Obtient les positions des caractères de début et de fin de la sélection actuelle dans le contrôle d’édition d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la position de départ de la sélection. Ce paramètre peut être **NULL**.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une valeur **DWORD** qui reçoit la position de fin de la sélection. Ce paramètre peut être **NULL**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est une valeur **DWORD** de base zéro avec la position de départ de la sélection dans le [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et avec la position de fin du premier caractère après le dernier caractère sélectionné dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="examples"></a>Exemples

L’exemple de code suivant montre deux façons de récupérer la plage de sélection actuelle.


```C++
DWORD start, end;

// Get the range from [out] parameters.
// hwnd is the handle of the combo box control.
SendMessage(hwnd, CB_GETEDITSEL, (WPARAM)&start, (LPARAM)&end;

// Get the range from the return value.
DWORD range = SendMessage(hwnd, CB_GETEDITSEL, NULL, NULL);
start = LOWORD(range);
end = HIWORD(range);
```



## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETEDITSEL CB**](cb-seteditsel.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> </dl>

 

