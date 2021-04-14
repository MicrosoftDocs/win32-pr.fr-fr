---
title: Message WM_MENUCOMMAND (winuser. h)
description: Envoyé lorsque l’utilisateur effectue une sélection à partir d’un menu.
ms.assetid: 1ed702ef-8d32-4d4c-a68a-ffd199112ced
keywords:
- WM_MENUCOMMAND des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUCOMMAND
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13288c49327b536db6ebef8a41526facd3fb2d51
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385279"
---
# <a name="wm_menucommand-message"></a>\_Message WM MENUCOMMAND

Envoyé lorsque l’utilisateur effectue une sélection à partir d’un menu.


```C++
#define WM_MENUCOMMAND                  0x0126
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément sélectionné.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers le menu de l’élément sélectionné.

</dd> </dl>

## <a name="remarks"></a>Notes

Le message **WM \_ MENUCOMMAND** vous donne un handle au menu qui vous permet d’accéder aux données de menu dans la structure [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) et vous donne également l’index de l’élément sélectionné, ce qui est généralement ce dont les applications ont besoin. En revanche, le message de [**\_ commande WM**](wm-command.md) vous donne l’identificateur d’élément de menu.

Le **message WM \_ MENUCOMMAND** est envoyé uniquement pour les menus définis avec l’indicateur **MNS \_ NOTIFYBYPOS** défini dans le membre **dwStyle** de la structure [**MENUINFO**](/windows/win32/api/winuser/ns-winuser-menuinfo) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble des menus](menus.md)
</dt> </dl>

 

 





