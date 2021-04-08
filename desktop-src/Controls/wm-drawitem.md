---
title: Message WM_DRAWITEM (winuser. h)
description: Envoyé à la fenêtre parente d’un bouton owner-drawn, d’une zone de liste modifiable, d’une zone de liste ou d’un menu lorsqu’un aspect visuel du bouton, zone de liste déroulante, zone de liste ou menu a changé.
ms.assetid: e54bae5e-10d6-43b0-a766-1b270c8873a9
keywords:
- WM_DRAWITEM les contrôles de message Windows
topic_type:
- apiref
api_name:
- WM_DRAWITEM
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5bd6465a560a0590ed9f5b483afae4c0d72d637
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741364"
---
# <a name="wm_drawitem-message"></a>\_Message WM DRAWITEM

Envoyé à la fenêtre parente d’un bouton owner-drawn, d’une zone de liste modifiable, d’une zone de liste ou d’un menu lorsqu’un aspect visuel du bouton, zone de liste déroulante, zone de liste ou menu a changé.

Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
WM_DRAWITEM

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie l’identificateur du contrôle qui a envoyé le message **WM \_ DRAWITEM** . Si le message a été envoyé par un menu, ce paramètre est égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) contenant des informations sur l’élément à dessiner et le type de dessin requis.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la **valeur true**.

## <a name="remarks"></a>Notes

Par défaut, la fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dessine le rectangle de focus pour un élément de zone de liste owner-drawn.

Le membre *itemAction* de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) spécifie l’opération de dessin qu’une application doit effectuer.

Avant de revenir au traitement de ce message, une application doit s’assurer que le contexte de périphérique identifié par le membre *HDC* de la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) est dans l’État par défaut.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DRAWITEMSTRUCT,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

