---
title: Message WM_INITMENU (winuser. h)
description: Envoyé lorsqu’un menu va devenir actif.
ms.assetid: d0fcc6d8-f57c-4d04-b9e7-4cfab6add173
keywords:
- WM_INITMENU des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_INITMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94626b99a5016efaa9427d1ae8b3b3122e599965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106543633"
---
# <a name="wm_initmenu-message"></a>\_Message WM INITMENU

Envoyé lorsqu’un menu va devenir actif. Il se produit lorsque l’utilisateur clique sur un élément dans la barre de menus ou appuie sur une touche de menu. Cela permet à l’application de modifier le menu avant qu’il ne soit affiché.

Une fenêtre reçoit ce message par le biais de sa fonction [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_INITMENU                     0x0116
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du menu à initialiser.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

## <a name="remarks"></a>Notes

Un message **WM \_ INITMENU** est envoyé uniquement lors d’un premier accès à un menu ; un seul message **WM \_ INITMENU** est généré pour chaque accès. Par exemple, le déplacement de la souris sur plusieurs éléments de menu tout en maintenant le bouton enfoncé ne génère pas de nouveaux messages. **WM \_ INITMENU** ne fournit pas d’informations sur les éléments de menu.

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

[**\_INITMENUPOPUP WM**](wm-initmenupopup.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

 

