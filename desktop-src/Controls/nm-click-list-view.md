---
title: Code de notification NM_CLICK (mode liste) (commctrl. h)
description: Envoyé par un contrôle List-View lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 7921bc27-54ca-4bb2-ac88-8267776661ab
keywords:
- NM_CLICK (mode liste) code de notification Windows les contrôles
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e9189861db0ec956b549145584202e3b88978478a9dd8de4386785d46e0d160
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120061759"
---
# <a name="nm_click-list-view-notification-code"></a>NM- \_ cliquer (mode liste) Code de notification

Envoyé par un contrôle List-View lorsque l’utilisateur clique sur un élément avec le bouton gauche de la souris. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_CLICK

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



 

 





