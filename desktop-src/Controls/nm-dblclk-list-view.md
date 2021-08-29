---
title: Code de notification NM_DBLCLK (mode liste) (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur double-clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 28455109-177e-4932-88c5-500a3a91c13a
keywords:
- NM_DBLCLK (mode liste) code de notification Windows les contrôles
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
ms.openlocfilehash: c3590b417954f67c454b6cece979bdd6eac4706fa5dfc97b7dda30be6dde183c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919699"
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

## <a name="remarks"></a>Remarques

Le membre **iItem** de *lParam* est uniquement valide si l’utilisateur clique sur l’étiquette de la première colonne ou sur l’icône. Pour déterminer l’élément sélectionné lorsqu’un clic est effectué ailleurs dans une ligne, envoyez un message [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





