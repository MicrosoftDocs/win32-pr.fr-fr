---
title: Code de notification NM_DBLCLK (mode liste) (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur double-clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- Contrôles Windows de code de notification NM_DBLCLK (mode liste)
topic_type:
- apiref
api_name:
- NM_DBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: add6af24b4272631be7c2be387a7ffda899469b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843081"
---
# <a name="nm_dblclk-list-view-notification-code"></a>\_DBLCLK nm (mode liste) Code de notification

Envoyé par un contrôle List-View lorsque l’utilisateur double-clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_DBLCLK
        
    lpnmitem = (LPNMITEMACTIVATE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

[Version 4,71](common-control-versions.md). Pointeur vers une structure [**NMITEMACTIVATE**](/windows/win32/api/commctrl/ns-commctrl-nmitemactivate) qui contient des informations supplémentaires sur cette notification. Les membres **iItem**, **iSubItem** et **ptAction** de cette structure contiennent des informations sur l’élément.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="remarks"></a>Notes

Le membre **iItem** de *lParam* est uniquement valide si l’utilisateur clique sur l’étiquette de la première colonne ou sur l’icône. Pour déterminer l’élément sélectionné lorsqu’un clic est effectué ailleurs dans une ligne, envoyez un message [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





