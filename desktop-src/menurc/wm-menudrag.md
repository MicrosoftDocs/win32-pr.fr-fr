---
title: Message WM_MENUDRAG (winuser. h)
description: Envoyé au propriétaire d’un menu glisser-déplacer lorsque l’utilisateur fait glisser un élément de menu.
ms.assetid: 99e8f490-ef1e-4964-a3a1-47030a88f10c
keywords:
- WM_MENUDRAG des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUDRAG
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22792c7606bb001b72b7c4751d14129bca02c5b4a5b337e0349a9a9a2120b62a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971798"
---
# <a name="wm_menudrag-message"></a>\_Message WM MENUDRAG

Envoyé au propriétaire d’un menu glisser-déplacer lorsque l’utilisateur fait glisser un élément de menu.


```C++
#define WM_MENUDRAG                     0x0123
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Position de l’élément où l’opération glisser a commencé.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du menu contenant l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application doit retourner l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                   | Description                                                                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <dl> <dt>**MND \_ CONTINUER**</dt> <dt>0</dt> </dl> | Le menu doit rester actif. Si la souris est relâchée, elle doit être ignorée.<br/> |
| <dl> <dt>**MND \_ ENDMENU**</dt> <dt>1</dt> </dl>  | Le menu doit être terminé.<br/>                                                      |



 

## <a name="remarks"></a>Remarques

L’application peut appeler la fonction [**DoDragDrop**](/windows/win32/api/ole2/nf-ole2-dodragdrop) en réponse à ce message.

Pour créer un menu glisser-déplacer, appelez [**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo) avec **MNS \_ DRAGDROP**.

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

[**SetMenuInfo**](/windows/desktop/api/Winuser/nf-winuser-setmenuinfo)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

