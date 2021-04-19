---
description: Publié dans une application lorsqu’un utilisateur annule les activités de journalisation de l’application. Le message est publié avec un handle de fenêtre NULL.
ms.assetid: 7515acb5-4526-40f7-abb7-822a073ac7dc
title: Message WM_CANCELJOURNAL (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a5676472d12c8cef2a03e508eca6bb742596a36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530624"
---
# <a name="wm_canceljournal-message"></a>\_Message WM CANCELJOURNAL

Publié dans une application lorsqu’un utilisateur annule les activités de journalisation de l’application. Le message est publié avec un handle de fenêtre **null** .


```C++
#define WM_CANCELJOURNAL                0x004B
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **void**

Ce message ne retourne pas de valeur. Il est destiné à être traité à partir de la boucle principale d’une application ou d’une procédure de hook [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) , et non à partir d’une procédure de fenêtre.

## <a name="remarks"></a>Notes

L’enregistrement de journal et les modes de lecture sont des modes imposés sur le système qui permettent à une application d’enregistrer ou de lire des entrées d’utilisateur de manière séquentielle. Le système passe à ces modes lorsqu’une application installe une procédure de hook [*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85)) ou [*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85)) . Lorsque le système se trouve dans l’un de ces modes de journalisation, les applications doivent mettre en lecture les entrées de la file d’attente d’entrée. Si une application cesse de lire l’entrée alors que le système est en mode de journalisation, les autres applications sont forcées à attendre.

Pour garantir un système robuste, qui ne peut pas être rendu non réactif par une application, le système annule automatiquement les activités de journalisation lorsqu’un utilisateur appuie sur CTRL + ECHAP ou CTRL + ALT + SUPPR. Le système décroche ensuite les procédures de hook de journalisation et publie un message **WM \_ CANCELJOURNAL** , avec un handle de fenêtre **null** , à l’application qui définit le hook de journalisation.

Le message **WM \_ CANCELJOURNAL** a un handle de fenêtre **null** , il ne peut donc pas être distribué à une procédure de fenêtre. Il existe deux façons pour une application de voir un **message WM \_ CANCELJOURNAL** : si l’application s’exécute dans sa propre boucle principale, elle doit intercepter le message entre son appel à [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) et son appel à [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage). Si l’application ne s’exécute pas dans sa propre boucle principale, elle doit définir une procédure de hook [*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85)) (à l’aide d’un appel à [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) en spécifiant le type de hook **BL \_ GETMESSAGE** ) qui surveille le message.

Lorsqu’une application voit un message **WM \_ CANCELJOURNAL** , elle peut supposer deux choses : l’utilisateur a annulé intentionnellement l’enregistrement du journal ou le mode de lecture, et le système a déjà décroché un enregistrement de journal ou des procédures de hook de lecture.

Notez que les combinaisons de touches mentionnées ci-dessus (CTRL + ESC ou CTRL + ALT + SUPPR) provoquent l’annulation de la journalisation par le système. Si une application ne répond pas, elle donne à l’utilisateur un moyen de récupération. Le code de la touche virtuelle [**VK \_ Cancel**](../inputdev/virtual-key-codes.md) (généralement implémentée en tant que combinaison de touches CTRL + ATTN) est ce qu’une application qui est en mode d’enregistrement journal doit surveiller comme signal indiquant que l’utilisateur souhaite annuler l’activité de journalisation. La différence réside dans le fait que la surveillance de **VK \_ Cancel** est un comportement suggéré pour la journalisation des applications, tandis que CTRL + ESC ou Ctrl + Alt + Suppr oblige le système à annuler la journalisation quel que soit le comportement de l’application de journalisation.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[*JournalRecordProc*](/previous-versions/windows/desktop/legacy/ms644983(v=vs.85))
</dt> <dt>

[*GetMsgProc*](/previous-versions/windows/desktop/legacy/ms644981(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Hooks](hooks.md)
</dt> </dl>

 

 
