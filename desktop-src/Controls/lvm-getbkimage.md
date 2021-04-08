---
title: Message LVM_GETBKIMAGE (commctrl. h)
description: Obtient l’image d’arrière-plan dans un contrôle d’affichage de liste. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetBkImage.
ms.assetid: db0e8f31-746a-4a16-b689-68da696e3657
keywords:
- LVM_GETBKIMAGE les contrôles de message Windows
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
ms.openlocfilehash: 29e178bae10b9bed880213ca4a4ab2a1b4e07239
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739957"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETBKIMAGEW** (Unicode) et **LVM \_ GETBKIMAGEA** (ANSI)<br/>             |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETBKIMAGE LVM**](lvm-setbkimage.md)
</dt> </dl>

 

 





