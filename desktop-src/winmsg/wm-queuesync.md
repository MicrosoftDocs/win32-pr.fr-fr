---
description: Envoyé par une application de formation basée sur ordinateur (FAO) pour séparer les messages d’entrée utilisateur des autres messages envoyés via la \_ procédure JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Message WM_QUEUESYNC (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06d859f858ab7cf8182282cc20dbf514cfc2d9b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524664"
---
# <a name="wm_queuesync-message"></a>\_Message WM QUEUESYNC

Envoyé par une application de formation basée sur ordinateur (FAO) pour séparer les messages d’entrée utilisateur des autres messages envoyés via la procédure [**\_ JOURNALPLAYBACK**](about-hooks.md) .


```C++
#define WM_QUEUESYNC                    0x0023
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

Une application CBT doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Chaque fois qu’une application CBT utilise la procédure [**\_ JOURNALPLAYBACK**](about-hooks.md) , les premier et dernier messages sont **WM \_ QUEUESYNC**. Cela permet à l’application CBT d’intercepter et d’examiner les messages initiés par l’utilisateur sans le faire pour les événements qu’elle envoie.

Si une application spécifie un handle de fenêtre **null** , le message est publié dans la file d’attente de messages de la fenêtre active.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[*JournalPlaybackProc*](/previous-versions/windows/desktop/legacy/ms644982(v=vs.85))
</dt> <dt>

[**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Hooks](hooks.md)
</dt> </dl>

 

 
