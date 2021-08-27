---
title: Message CB_GETCOMBOBOXINFO (winuser. h)
description: Obtient des informations sur la zone de liste déroulante spécifiée.
ms.assetid: 3239dfa8-7301-48e3-ba8e-29c5d5f43b39
keywords:
- CB_GETCOMBOBOXINFO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- CB_GETCOMBOBOXINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ce6227df0031c01b15892daa14eea9cc8d25bd2c7eede68af275063d7201505
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089289"
---
# <a name="cb_getcomboboxinfo-message"></a>\_Message GETCOMBOBOXINFO CB

Obtient des informations sur la zone de liste déroulante spécifiée.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* \[ à\]
</dt> <dd>

Pointeur vers une structure [**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo) qui reçoit les informations.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est différente de zéro.

Si la fonction échoue, la valeur de retour est égale à zéro. Pour obtenir des informations détaillées sur l’erreur, appelez [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).

## <a name="remarks"></a>Remarques

Ce message est équivalent à [**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**COMBOBOXINFO**](/windows/win32/api/winuser/ns-winuser-comboboxinfo)
</dt> <dt>

[**GetComboBoxInfo**](/windows/desktop/api/Winuser/nf-winuser-getcomboboxinfo)
</dt> </dl>

 

