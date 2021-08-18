---
title: Message WM_CTLCOLORDLG (winuser. h)
description: Envoyé à une boîte de dialogue avant que le système ne dessine la boîte de dialogue. En répondant à ce message, la boîte de dialogue peut définir ses couleurs de texte et d’arrière-plan à l’aide du handle de contexte de périphérique d’affichage spécifié.
ms.assetid: 5b90ab3f-b751-486f-a0fa-33f791c31a26
keywords:
- Boîtes de dialogue de WM_CTLCOLORDLG message
topic_type:
- apiref
api_name:
- WM_CTLCOLORDLG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5b7ab11bbb2cfd402888f930d5bcf2afa08b7ba83f74252fb3e443fd9e9309a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118503412"
---
# <a name="wm_ctlcolordlg-message"></a>\_Message WM CTLCOLORDLG

Envoyé à une boîte de dialogue avant que le système ne dessine la boîte de dialogue. En répondant à ce message, la boîte de dialogue peut définir ses couleurs de texte et d’arrière-plan à l’aide du handle de contexte de périphérique d’affichage spécifié.


```C++
#define WM_CTLCOLORDLG                  0x0136
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du contexte de périphérique pour la boîte de dialogue.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle de la boîte de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner un handle à un pinceau. Le système utilise le pinceau pour peindre l’arrière-plan de la boîte de dialogue.

## <a name="remarks"></a>Remarques

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) sélectionne les couleurs système par défaut de la boîte de dialogue.

Le système ne détruit pas automatiquement le pinceau retourné. Il incombe à l’application de détruire le pinceau lorsqu’il n’est plus nécessaire.

Le message **WM \_ CTLCOLORDLG** n’est jamais envoyé entre les threads. Elle est envoyée uniquement au sein d’un thread.

Notez que le message **WM \_ CTLCOLORDLG** est envoyé à la boîte de dialogue elle-même ; tous les autres messages **WM \_ CTLCOLOR \*** sont envoyés au propriétaire du contrôle.

Si une procédure de boîte de dialogue gère ce message, elle doit effectuer un cast de la valeur de retour souhaitée en **\_ ptr int** et retourner la valeur directement. Si la procédure de boîte de dialogue retourne la **valeur false**, la gestion des messages par défaut est effectuée. La valeur **DWL \_ MSGRESULT** définie par la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) est ignorée.

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

[**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**RealizePalette**](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[**SelectPalette**](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> </dl>

 

