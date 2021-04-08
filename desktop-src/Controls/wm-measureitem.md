---
title: Message WM_MEASUREITEM (winuser. h)
description: Envoyé à la fenêtre propriétaire d’une zone de liste déroulante, d’une zone de liste, d’un contrôle de vue de liste ou d’un élément de menu lors de la création du contrôle ou du menu.
ms.assetid: 6947bcd1-fd40-4238-b8f2-d4e06b90c0dc
keywords:
- WM_MEASUREITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_MEASUREITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43e14cc0c39e1d319fb9190f8ad7d51ea25f821c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843877"
---
# <a name="wm_measureitem-message"></a>\_Message WM MEASUREITEM

Envoyé à la fenêtre propriétaire d’une zone de liste déroulante, d’une zone de liste, d’un contrôle de vue de liste ou d’un élément de menu lors de la création du contrôle ou du menu.

Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_MEASUREITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Contient la valeur du membre **CtlID** de la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) vers laquelle pointe le paramètre *lParam* . Cette valeur identifie le contrôle qui a envoyé le message **WM \_ MEASUREITEM** . Si la valeur est égale à zéro, le message a été envoyé par un menu. Si la valeur est différente de zéro, le message a été envoyé par une zone de liste déroulante ou par une zone de liste. Si la valeur est différente de zéro, et que la valeur du membre **ItemId** du **Measureitemstruct,** pointé par *lParam* est (uint) 1, le message a été envoyé par un champ d’édition de liste déroulante.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui contient les dimensions de l’élément de menu ou de contrôle owner-drawn.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la **valeur true**.

## <a name="remarks"></a>Notes

Lorsque la fenêtre propriétaire reçoit le message **WM \_ MEASUREITEM** , le propriétaire remplit la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) désignée par le paramètre *lParam* du message et retourne la valeur, et indique au système les dimensions du contrôle. Si une zone de liste ou une zone de liste déroulante est créée avec le style [**\_ OWNERDRAWVARIABLE**](list-box-styles.md) ou [**CBS \_ OWNERDRAWVARIABLE**](combo-box-styles.md) , ce message est envoyé au propriétaire de chaque élément du contrôle ; sinon, ce message est envoyé une seule fois.

Le système envoie le message **WM \_ MEASUREITEM** à la fenêtre propriétaire des zones de liste modifiable et des zones de liste créées avec le style OWNERDRAWFIXED avant d’envoyer le message [**WM \_ INITDIALOG**](/windows/desktop/dlgbox/wm-initdialog) . Par conséquent, lorsque le propriétaire reçoit ce message, le système n’a pas encore déterminé la hauteur et la largeur de la police utilisée dans le contrôle ; les appels de fonction et les calculs nécessitant ces valeurs doivent se produire dans la fonction principale de l’application ou de la bibliothèque.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**MEASUREITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**\_INITDIALOG WM**](/windows/desktop/dlgbox/wm-initdialog)
</dt> </dl>

 

