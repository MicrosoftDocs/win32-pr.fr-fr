---
title: Message WM_MENUGETOBJECT (winuser. h)
description: Envoyé au propriétaire d’un menu glisser-déplacer lorsque le curseur de la souris entre dans un élément de menu ou se déplace du centre de l’élément vers le haut ou le bas de l’élément.
ms.assetid: 08348e43-3d21-4543-b624-5504575efced
keywords:
- WM_MENUGETOBJECT des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_MENUGETOBJECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08e124c7f2757a0d6d1d2ac0904052b6d3c255ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519202"
---
# <a name="wm_menugetobject-message"></a>\_Message WM MENUGETOBJECT

Envoyé au propriétaire d’un menu glisser-déplacer lorsque le curseur de la souris entre dans un élément de menu ou se déplace du centre de l’élément vers le haut ou le bas de l’élément.


```C++
#define WM_MENUGETOBJECT                0x0124
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

L’application doit retourner l’une des valeurs suivantes.



| Code/valeur de retour                                                                                                                                                | Description                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**MNGO \_ Noerreur**</dt> <dt>0x00000001</dt> </dl>     | Un pointeur d’interface a été retourné dans le membre **pvObj** de [**MENUGETOBJECTINFO**](/windows/win32/api/winuser/ns-winuser-menugetobjectinfo)<br/> |
| <dl> <dt>**MNGO \_ Nointerface**</dt> <dt>0x00000000</dt> </dl> | L’interface n’est pas prise en charge.<br/>                                                                             |



 

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

 

 





