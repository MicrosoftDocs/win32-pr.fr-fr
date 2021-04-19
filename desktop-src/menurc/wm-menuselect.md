---
title: Message WM_MENUSELECT (winuser. h)
description: Envoyé à la fenêtre propriétaire d’un menu lorsque l’utilisateur sélectionne un élément de menu.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106514259"
---
# <a name="wm_menuselect-message"></a>\_Message WM MENUSELECT

Envoyé à la fenêtre propriétaire d’un menu lorsque l’utilisateur sélectionne un élément de menu.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le mot de poids faible spécifie l’index de l’élément de menu ou du sous-menu. Si l’élément sélectionné est un élément de commande, ce paramètre contient l’identificateur de l’élément de menu. Si l’élément sélectionné ouvre un menu déroulant ou un sous-menu, ce paramètre contient l’index du menu déroulant ou du sous-menu du menu principal, et le paramètre *lParam* contient le handle du menu principal (clic). Utilisez la fonction [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) pour récupérer la poignée de menu du menu déroulant ou du sous-menu.

Le mot de poids fort spécifie un ou plusieurs indicateurs de menu. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                                                                             | Signification                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_**</dt> <dt>0x00000004L</dt> bitmap </dl>                | Item affiche une bitmap.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_**</dt> <dt>0x00000008L</dt> activé </dl>             | L’élément est activé.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_ Désactivation**</dt> de <dt>0x00000002L</dt> </dl>          | L'élément est désactivé.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_ 0x00000001L GRISés**</dt> <dt></dt> </dl>                | L’élément est grisé.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt> </dl>                | L’élément est mis en surbrillance.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt> </dl> | L’élément est sélectionné avec la souris.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_ OWNERDRAW**</dt> <dt>0x00000100L</dt> </dl>       | L’élément est un élément owner-drawn.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_**</dt> <dt>0x00000010L</dt> Popup </dl>                   | Élément ouvre un menu déroulant ou un sous-menu.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl>             | L’élément est contenu dans le menu fenêtre. Le paramètre *lParam* contient un handle vers le menu associé au message.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers le menu sur lequel l’utilisateur a cliqué.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Si le mot de poids fort de *wParam* contient 0xFFFF et que le paramètre *lParam* contient la **valeur null**, le système a fermé le menu.

N’utilisez pas la valeur 1 pour le mot de poids fort de *wParam*, car cette valeur est spécifiée sous la forme (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*). Si la valeur est 0xFFFF, elle est interprétée comme 0x0000FFFF, et non pas par 1, en raison de la conversion en **uint**.

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

[**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

 

