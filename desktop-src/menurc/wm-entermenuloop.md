---
title: Message WM_ENTERMENULOOP (winuser. h)
description: Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été entrée.
ms.assetid: 0a018b6f-fe4b-4e90-bbb6-9b5719253dc1
keywords:
- WM_ENTERMENULOOP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_ENTERMENULOOP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5851109e44100d558603fb268a4668c1f138fff97e5e87db50a28445e70adb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939609"
---
# <a name="wm_entermenuloop-message"></a>\_Message WM ENTERMENULOOP

Notifie la procédure de fenêtre principale d’une application qu’une boucle modale de menu a été entrée.


```C++
#define WM_ENTERMENULOOP                0x0211
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie si le menu fenêtre a été entré à l’aide de la fonction [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) . Ce paramètre a la valeur **true** si le menu fenêtre a été entré à l’aide de **TrackPopupMenu**, et **false** dans le cas contraire.

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

[**\_EXITMENULOOP WM**](wm-exitmenuloop.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

