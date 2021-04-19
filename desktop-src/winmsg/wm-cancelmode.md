---
description: Envoyé pour annuler certains modes, tels que la capture de la souris.
ms.assetid: c801233a-c4d8-4fd9-aaf0-3d4503bbce26
title: Message WM_CANCELMODE (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c23b842dfdfde7dc550d8ec6d942bcc83ea25f3d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530100"
---
# <a name="wm_cancelmode-message"></a>\_Message WM CANCELMODE

Envoyé pour annuler certains modes, tels que la capture de la souris. Par exemple, le système envoie ce message à la fenêtre active lorsqu’une boîte de dialogue ou une boîte de message s’affiche. Certaines fonctions envoient également ce message explicitement à la fenêtre spécifiée, qu’il s’agisse de la fenêtre active ou non. Par exemple, la fonction [**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow) envoie ce message lors de la désactivation de la fenêtre spécifiée.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CANCELMODE                   0x001F
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

Type : **LRESULT**

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Lorsque le message **WM \_ CANCELMODE** est envoyé, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) annule le traitement interne de l’entrée de la barre de défilement standard, annule le traitement du menu interne et libère la capture de la souris.

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

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**EnableWindow**](/windows/win32/api/winuser/nf-winuser-enablewindow)
</dt> <dt>

[**ReleaseCapture**](/windows/win32/api/winuser/nf-winuser-releasecapture)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
