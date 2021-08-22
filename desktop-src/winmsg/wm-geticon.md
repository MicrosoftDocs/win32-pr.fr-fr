---
description: Envoyé à une fenêtre pour récupérer un handle vers la grande ou la petite icône associée à une fenêtre. Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: Message WM_GETICON (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df8922fa09cf425594a07768f0d7c9ae0ac09222647f181f45331c2b0d47fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587419"
---
# <a name="wm_geticon-message"></a>\_Message WM GETICON

Envoyé à une fenêtre pour récupérer un handle vers la grande ou la petite icône associée à une fenêtre. Le système affiche la grande icône dans la boîte de dialogue ALT + TAB et la petite icône dans le titre de la fenêtre.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Type d’icône récupéré. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                          | Signification                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**Icône \_ BIG**</dt> <dt>1</dt> </dl>          | Récupérez la grande icône pour la fenêtre.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**Icône \_ PETIT**</dt> <dt>0</dt> </dl>    | Récupérez la petite icône pour la fenêtre.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**Icône \_ SMALL2**</dt> <dt>2</dt> </dl> | Récupère la petite icône fournie par l’application. Si l’application n’en fournit pas, le système utilise l’icône générée par le système pour cette fenêtre.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

PPP de l’icône en cours de récupération. Cela peut être utilisé pour fournir des icônes différentes en fonction de la taille de l’icône.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HICON**

La valeur de retour est un handle vers la grande ou la petite icône, en fonction de la valeur de *wParam*. Lorsqu’une application reçoit ce message, elle peut renvoyer un descripteur à une grande ou petite icône, ou passer le message à la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

## <a name="remarks"></a>Remarques

Lorsqu’une application reçoit ce message, elle peut renvoyer un descripteur à une grande ou petite icône, ou transmettre le message à [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne un handle vers la grande ou la petite icône associée à la fenêtre, en fonction de la valeur de *wParam*.

Une fenêtre qui n’a pas d’icône définie explicitement (avec **WM \_ SETICON**) utilise l’icône de la classe de fenêtre inscrite. dans ce cas, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne 0 pour un message **WM \_ GETICON** . Si l’envoi d’un message **WM \_ GETICON** à une fenêtre retourne 0, essayez ensuite d’appeler la fonction [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) pour la fenêtre. Si la valeur renvoyée est 0, essayez la fonction [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona) .

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

[**\_SETICON WM**](wm-seticon.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
