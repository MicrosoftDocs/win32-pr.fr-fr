---
description: Le \_ message WM DEVMODECHANGE est envoyé à toutes les fenêtres de niveau supérieur chaque fois que l’utilisateur modifie les paramètres du mode de l’appareil.
ms.assetid: 06b625a8-7584-4a98-b8e7-f1de668c274e
title: Message WM_DEVMODECHANGE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 068e74264a7492bbb1e685fe6de110e909698374
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973518"
---
# <a name="wm_devmodechange-message"></a>\_Message WM DEVMODECHANGE

Le message **WM \_ DEVMODECHANGE** est envoyé à toutes les fenêtres de niveau supérieur chaque fois que l’utilisateur modifie les paramètres du mode de l’appareil.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND hwnd, 
  UINT  uMsg, 
  WPARAM wParam, 
  LPARAM lParam     
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle d'une fenêtre.

</dd> <dt>

*uMsg* 
</dt> <dd>

\_DEVMODECHANGE WM

</dd> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne qui spécifie le nom de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Ce message ne peut pas être envoyé directement à une fenêtre. Pour envoyer le message **WM \_ DEVMODECHANGE** à toutes les fenêtres de niveau supérieur, utilisez la fonction [**SendMessageTimeout**](/windows/win32/api/winuser/nf-winuser-sendmessagetimeouta) avec le paramètre *HWND* défini sur \_ Broadcast HWND.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des contextes de périphérique](device-contexts.md)
</dt> <dt>

[Messages de contexte de périphérique](device-context-messages.md)
</dt> </dl>

 

 
