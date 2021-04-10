---
title: Message WM_CHANGECBCHAIN (winuser. h)
description: Envoyé à la première fenêtre de la chaîne du presse-papiers lorsqu’une fenêtre est supprimée de la chaîne. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 7be87342-87fa-4cd2-b066-0b36b7ef52f5
keywords:
- WM_CHANGECBCHAIN l’échange de données de message
topic_type:
- apiref
api_name:
- WM_CHANGECBCHAIN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ab91640320e3659d0e9fb130f5c773ccbb7c4e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104089"
---
# <a name="wm_changecbchain-message"></a>\_Message WM CHANGECBCHAIN

Envoyé à la première fenêtre de la chaîne du presse-papiers lorsqu’une fenêtre est supprimée de la chaîne.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_CHANGECBCHAIN                0x030D
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle de la fenêtre en cours de suppression dans la chaîne du presse-papiers.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la fenêtre suivante dans la chaîne après la suppression de la fenêtre. Ce paramètre a la **valeur null** si la fenêtre en cours de suppression est la dernière fenêtre de la chaîne.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Chaque fenêtre de la visionneuse du presse-papiers enregistre le descripteur dans la fenêtre suivante dans la chaîne du presse-papiers. Initialement, ce descripteur est la valeur de retour de la fonction [**SetClipboardViewer**](/windows/desktop/api/Winuser/nf-winuser-setclipboardviewer) .

Quand une fenêtre de la visionneuse du presse-papiers reçoit le message **WM \_ CHANGECBCHAIN** , elle doit appeler la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour transmettre le message à la fenêtre suivante dans la chaîne, sauf si la fenêtre suivante est supprimée. Dans ce cas, la visionneuse du presse-papiers doit enregistrer le handle spécifié par le paramètre *lParam* comme fenêtre suivante dans la chaîne.

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

**Méthodologique**
</dt> <dt>

[Presse-papiers](clipboard.md)
</dt> </dl>

 

