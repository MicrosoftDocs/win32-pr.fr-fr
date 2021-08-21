---
title: Code de notification NM_RDBLCLK (mode liste) (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur double-clique sur un élément avec le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ebbb127f-07bd-48e0-bf38-7bbda5802f70
keywords:
- NM_RDBLCLK (mode liste) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_RDBLCLK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c0197659f89392d352e2500d37cbda9dadee5487c5ee180123f502d127925a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957988"
---
# <a name="nm_rdblclk-list-view-notification-code"></a>\_RDBLCLK nm (mode liste) Code de notification

Envoyé par un contrôle List-View lorsque l’utilisateur double-clique sur un élément avec le bouton droit de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_RDBLCLK

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

Le membre **iItem** de *lParam* n’est valide que si l’utilisateur clique sur l’étiquette de la première colonne ou sur l’icône. Pour déterminer l’élément sélectionné lorsqu’un clic est effectué ailleurs dans une ligne, envoyez un message [**\_ SUBITEMHITTEST LVM**](lvm-subitemhittest.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





