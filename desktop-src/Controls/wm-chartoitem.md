---
title: Message WM_CHARTOITEM (winuser. h)
description: Envoyé par une zone de liste avec le \_ style WANTKEYBOARDINPUT lbs à son propriétaire en réponse à un \_ message WM char.
ms.assetid: f941c00b-b836-4f1b-b8cf-8ac2b0704af3
keywords:
- WM_CHARTOITEM les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_CHARTOITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3809ae800cfc753925e7c27d87f970ce56c10d90ace7c23e87b46f3e0067fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957528"
---
# <a name="wm_chartoitem-message"></a>\_Message WM CHARTOITEM

Envoyé par une zone de liste avec le style [**\_ WANTKEYBOARDINPUT lbs**](list-box-styles.md) à son propriétaire en réponse à un message [**WM \_ char**](/windows/desktop/inputdev/wm-char) .


```C++
WM_CHARTOITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) spécifie le code de caractère de la touche sur laquelle l’utilisateur a appuyé. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie la position actuelle du signe insertion.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la zone de liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour spécifie l’action exécutée par l’application en réponse au message. Une valeur de retour de-1 ou-2 indique que l’application a géré tous les aspects de la sélection de l’élément et ne nécessite aucune action supplémentaire de la zone de liste. Une valeur de retour supérieure ou égale à 0 spécifie l’index de base zéro d’un élément dans la zone de liste et indique que la zone de liste doit exécuter l’action par défaut pour la frappe sur l’élément spécifié.

## <a name="remarks"></a>Remarques

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne-1.

Seules les zones de liste owner-drawn ne disposant pas du style de [**\_ HASSTRINGS lbs**](list-box-styles.md) peuvent recevoir ce message.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en valeur **booléenne** et retourner la valeur directement. La valeur *DWL \_ MSGRESULT* définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

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

[**\_VKEYTOITEM WM**](wm-vkeytoitem.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_caractère WM**](/windows/desktop/inputdev/wm-char)
</dt> </dl>

 

