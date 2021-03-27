---
description: Envoyé à la fenêtre propriétaire d’un contrôle ou d’un élément de menu lors de la création du contrôle ou du menu.
ms.assetid: 4584a3da-6c92-4ecd-8cf2-e4afc1b8321d
title: Message DFM_WM_MEASUREITEM (shlobj. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c4ad79acf221ecaabf9060940ad2514422bef1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393436"
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

## <a name="remarks"></a>Notes

Lorsque la fenêtre propriétaire reçoit le message **DFM \_ WM \_ MEASUREITEM** , le propriétaire remplit la structure [**measureitemstruct,**](/windows/win32/api/winuser/ns-winuser-measureitemstruct) pointée par le paramètre *lpMeasureItem* du message et retourne. cela indique au système les dimensions du contrôle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 
