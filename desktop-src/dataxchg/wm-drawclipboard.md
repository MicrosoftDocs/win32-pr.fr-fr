---
title: Message WM_DRAWCLIPBOARD (winuser. h)
description: Envoyé à la première fenêtre de la chaîne du presse-papiers lorsque le contenu du presse-papiers change. Cela permet à une fenêtre de la visionneuse du presse-papiers d’afficher le nouveau contenu du presse-papiers. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: ffaadf6f-588b-4a29-b26c-629087e7ce73
keywords:
- WM_DRAWCLIPBOARD l’échange de données de message
topic_type:
- apiref
api_name:
- WM_DRAWCLIPBOARD
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d5ee6f6893375e2604cb39247745fc2758ce8c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513602"
---
# <a name="wm_drawclipboard-message"></a>\_Message WM DRAWCLIPBOARD

Envoyé à la première fenêtre de la chaîne du presse-papiers lorsque le contenu du presse-papiers change. Cela permet à une fenêtre de la visionneuse du presse-papiers d’afficher le nouveau contenu du presse-papiers.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_DRAWCLIPBOARD                0x0308
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="remarks"></a>Notes

Seules les fenêtres de la visionneuse du presse-papiers reçoivent ce message. Il s’agit des fenêtres qui ont été ajoutées à la chaîne du presse-papiers à l’aide de la fonction [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Chaque fenêtre qui reçoit le message **WM \_ DRAWCLIPBOARD** doit appeler la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour transmettre le message à la fenêtre suivante dans la chaîne du presse-papiers. Le handle de la fenêtre suivante dans la chaîne est retourné par [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)et peut changer en réponse à un message [**WM \_ CHANGECBCHAIN**](wm-changecbchain.md) .

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

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer)
</dt> <dt>

[**\_CHANGECBCHAIN WM**](wm-changecbchain.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

