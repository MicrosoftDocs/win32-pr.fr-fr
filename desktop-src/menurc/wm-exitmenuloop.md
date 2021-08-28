---
title: Message WM_EXITMENULOOP (winuser. h)
description: Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été quittée.
ms.assetid: b2a9d537-af7c-4c8a-932a-95e45eb8deb5
keywords:
- WM_EXITMENULOOP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_EXITMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec6d2cfb8457a748b7bb7bbdda481a0a1f73e5331891d45bd1bf1cabdfe0c5c0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886379"
---
# <a name="wm_exitmenuloop-message"></a>\_Message WM EXITMENULOOP

Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été quittée.


```C++
#define WM_EXITMENULOOP                 0x0212
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie si le menu est un menu contextuel. Ce paramètre a la valeur **true** s’il s’agit d’un menu contextuel, **false** dans le cas contraire.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Une application doit retourner zéro si elle traite ce message.

## <a name="remarks"></a>Remarques

La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retourne la valeur zéro.

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

[**\_ENTERMENULOOP WM**](wm-entermenuloop.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

