---
title: Message WM_NEXTDLGCTL (winuser. h)
description: Envoyé à une procédure de boîte de dialogue pour définir le focus clavier sur un autre contrôle dans la boîte de dialogue.
ms.assetid: 63d9fac2-3057-4bfa-9960-911fd18877d4
keywords:
- Boîtes de dialogue de WM_NEXTDLGCTL message
topic_type:
- apiref
api_name:
- WM_NEXTDLGCTL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc6b70dbaf010b839a0069513f97de8fdab1c0a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508953"
---
# <a name="wm_nextdlgctl-message"></a>\_Message WM NEXTDLGCTL

Envoyé à une procédure de boîte de dialogue pour définir le focus clavier sur un autre contrôle dans la boîte de dialogue.


```C++
#define WM_NEXTDLGCTL                   0x0028
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Si *lParam* a la **valeur true**, ce paramètre identifie le contrôle qui reçoit le focus. Si *lParam* a la **valeur false**, ce paramètre indique si le contrôle suivant ou précédent avec le style **WS \_ TABSTOP** reçoit le focus. Si *wParam* est égal à zéro, le contrôle suivant reçoit le focus ; Sinon, le contrôle précédent avec le style **WS \_ TABSTOP** reçoit le focus.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible indique comment le système utilise *wParam*. Si le mot de poids faible est **true**, *wParam* est un handle associé au contrôle qui reçoit le focus. Sinon, *wParam* est un indicateur qui indique si le contrôle suivant ou précédent avec le style **WS \_ TABSTOP** reçoit le focus.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Notes

Ce message effectue des opérations de gestion de boîte de dialogue supplémentaires au-delà de celles effectuées par la fonction [**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus) **WM \_ NEXTDLGCTL** met à jour la bordure du bouton de commande par défaut, définit l’identificateur de contrôle par défaut et sélectionne automatiquement le texte d’un contrôle d’édition (si la fenêtre cible est un contrôle d’édition).

N’utilisez pas la fonction [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour envoyer un message **WM \_ NEXTDLGCTL** si votre application traite de façon simultanée d’autres messages qui définissent le focus. Utilisez à la place la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

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

[**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea)
</dt> <dt>

[**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage)
</dt> <dt>

[**SetFocus**](/windows/desktop/api/winuser/nf-winuser-setfocus)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Boîtes de dialogue](dialog-boxes.md)
</dt> </dl>

 

