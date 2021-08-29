---
description: Envoyé par une application de formation basée sur ordinateur (FAO) pour séparer les messages d’entrée utilisateur des autres messages envoyés via la \_ procédure JOURNALPLAYBACK.
ms.assetid: 9ac265be-1fcc-476f-9dee-3e961340b5a1
title: Message WM_QUEUESYNC (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6db37a9e7eedc4d12c6750b150f31be1f77ad33da189c8333a4a2c788f45099d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710069"
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

## <a name="remarks"></a>Remarques

Chaque fois qu’une application CBT utilise la procédure [**\_ JOURNALPLAYBACK**](about-hooks.md) , les premier et dernier messages sont **WM \_ QUEUESYNC**. Cela permet à l’application CBT d’intercepter et d’examiner les messages initiés par l’utilisateur sans le faire pour les événements qu’elle envoie.

Si une application spécifie un handle de fenêtre **null** , le message est publié dans la file d’attente de messages de la fenêtre active.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                                              |
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

 

 
