---
title: Message LVM_GETBKIMAGE (commctrl. h)
description: Obtient l’image d’arrière-plan dans un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetBkImage.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETBKIMAGE
- LVM_GETBKIMAGEA
- LVM_GETBKIMAGEW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3393c226c250de2821d7fab930f950ff5a223218a77a1b9c4bc20b51b527a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062639"
---
# <a name="lvm_getbkimage-message"></a>\_Message GETBKIMAGE LVM

Obtient l’image d’arrière-plan dans un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetBkImage**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getbkimage) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**LVBKIMAGE**](/windows/win32/api/commctrl/ns-commctrl-lvbkimagea) qui recevra les informations sur l’image d’arrière-plan.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETBKIMAGEW** (Unicode) et **LVM \_ GETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETBKIMAGE LVM**](lvm-setbkimage.md)
</dt> </dl>

 

 





