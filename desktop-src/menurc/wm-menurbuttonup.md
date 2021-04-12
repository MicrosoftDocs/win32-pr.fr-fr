---
title: Message WM_MENURBUTTONUP (winuser. h)
description: Envoyé lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve sur un élément de menu.
ms.assetid: e061cba0-6aea-4df4-a39a-7e55f0db45c0
keywords:
- WM_MENURBUTTONUP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENURBUTTONUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7206fc79f6f990611c81ad0e844ae26af3764c6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317517"
---
# <a name="wm_menurbuttonup-message"></a>\_Message WM MENURBUTTONUP

Envoyé lorsque l’utilisateur relâche le bouton droit de la souris alors que le curseur se trouve sur un élément de menu.


```C++
#define WM_MENURBUTTONUP                0x0122
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de l’élément de menu sur lequel le bouton droit de la souris a été relâché.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du menu contenant l’élément.

</dd> </dl>

## <a name="remarks"></a>Notes

Le message **WM \_ MENURBUTTONUP** permet aux applications de fournir un menu contextuel également appelé menu contextuel pour l’élément de menu spécifié dans ce message. Pour afficher un menu contextuel pour un élément de menu, appelez la fonction [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) avec le **module TPM \_ recurse**.

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

 

 





