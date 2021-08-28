---
description: Publié dans la file d’attente de messages du thread d’installation lors de l’expiration d’un minuteur. Le message est publié par la fonction GetMessage ou PeekMessage.
ms.assetid: 419e3f05-35ec-4e48-b24d-ab98df687b20
title: Message WM_TIMER (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d770d640b801849eeebe1c4ec86df8c41642c6149b89e00d82261f4e090f56f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710029"
---
# <a name="wm_timer-message"></a>\_Message du minuteur WM

Publié dans la file d’attente de messages du thread d’installation lors de l’expiration d’un minuteur. Le message est publié par la fonction [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) ou [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) .


```C++
#define WM_TIMER                        0x0113
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Identificateur de la minuterie.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une fonction de rappel définie par l’application qui a été passée à la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) lors de l’installation du minuteur.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **LRESULT**

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

Vous pouvez traiter le message en fournissant un cas de **\_ minuterie WM** dans la procédure de fenêtre. Sinon, [**DispatchMessage**](/windows/win32/api/winuser/nf-winuser-dispatchmessage) appellera la fonction de rappel [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc) spécifiée dans l’appel à la fonction [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer) utilisée pour installer la minuterie.

Le message du **\_ minuteur WM** est un message de priorité basse. Les fonctions [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) et [**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea) publient ce message uniquement lorsqu’aucun autre message de priorité plus élevée ne se trouve dans la file d’attente de messages du thread.

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

[**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage)
</dt> <dt>

[**PeekMessage**](/windows/win32/api/winuser/nf-winuser-peekmessagea)
</dt> <dt>

[**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)
</dt> <dt>

[**TimerProc**](/windows/win32/api/winuser/nc-winuser-timerproc)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Minuteurs](timers.md)
</dt> </dl>

 

 
