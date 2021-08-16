---
description: Envoyé à la fenêtre propriétaire d’un contrôle ou d’un élément de menu lors de la création du contrôle ou du menu.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Message DFM_WM_MEASUREITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e7ad0d39a56f598a8ef4773c70f4f438388e91a2154b3083fdf85a1ebebec22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860897"
---
# <a name="dfm_wm_measureitem-message"></a>\_Message DFM WM \_ MEASUREITEM

Envoyé à la fenêtre propriétaire d’un contrôle ou d’un élément de menu lors de la création du contrôle ou du menu.


```C++
DFM_WM_MEASUREITEM 

    wParam = (WPARAM);

    lParam = (LPARAM)(LPMEASUREITEMSTRUCT) lpMeasureItem;

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Valeur du membre **CtlID** de la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) vers laquelle pointe le paramètre *lpMeasureItem* . Cette valeur identifie le contrôle qui a envoyé le message **DFM \_ WM \_ MEASUREITEM** .

</dd> <dt>

*lpMeasureItem* \[ à\]
</dt> <dd>

Pointeur vers une structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) qui contient les dimensions de l’élément de menu ou de contrôle owner-drawn.

</dd> </dl>

## <a name="remarks"></a>Remarques

Lorsque la fenêtre propriétaire reçoit le message **DFM \_ WM \_ MEASUREITEM** , le propriétaire remplit la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) pointée par le paramètre *lpMeasureItem* du message et retourne. cela indique au système les dimensions du contrôle.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
