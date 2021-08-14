---
description: Diffuser dans chaque fenêtre après un événement de modification de thème. Les exemples d’événements de changement de thème sont l’activation d’un thème, la désactivation d’un thème ou la transition d’un thème à un autre.
ms.assetid: 1a4051ac-cc6e-4520-ab66-d0a41a8a4c73
title: Message WM_THEMECHANGED (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b070cb492fa5db94acb97cd07f3de87455189d542aaaad2a51a3e0ecc6b4268d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118199908"
---
# <a name="wm_themechanged-message"></a>\_Message WM THEMECHANGED

Diffuser dans chaque fenêtre après un événement de modification de thème. Les exemples d’événements de changement de thème sont l’activation d’un thème, la désactivation d’un thème ou la transition d’un thème à un autre.


```C++
#define WM_THEMECHANGED                 0x031A
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre est réservé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre est réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Remarques

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .

> [!Note]  
> Ce message est publié par le système d’exploitation. En général, les applications n’envoient pas ce message.

 

Les thèmes sont des spécifications pour l’apparence des contrôles, afin que l’élément visuel d’un contrôle soit traité séparément de ses fonctionnalités.

Pour libérer un handle de thème existant, appelez [**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata). Pour acquérir un nouveau handle de thème, utilisez [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata).

À la suite de la diffusion **WM \_ THEMECHANGED** , les descripteurs de thème existants ne sont pas valides. Une fenêtre sensible aux thèmes doit libérer et rouvrir l’un de ses descripteurs de thème préexistants lorsqu’elle reçoit le message **WM \_ THEMECHANGED** . Si la fonction [**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata) retourne la **valeur null**, la fenêtre doit être peinte sans thème.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Autres ressources**
</dt> <dt>

[**CloseThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-closethemedata)
</dt> <dt>

[**IsThemeActive**](/windows/win32/api/uxtheme/nf-uxtheme-isthemeactive)
</dt> <dt>

[**OpenThemeData**](/windows/win32/api/uxtheme/nf-uxtheme-openthemedata)
</dt> </dl>

 

 
