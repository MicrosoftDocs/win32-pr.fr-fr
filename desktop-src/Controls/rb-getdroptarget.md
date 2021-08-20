---
title: Message RB_GETDROPTARGET (commctrl. h)
description: Récupère le pointeur d’interface IDropTarget d’un contrôle rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET les contrôles de Windows de message
topic_type:
- apiref
api_name:
- RB_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5793d2192ef65f193ff27d40cc14660c90d067034d8c1304e1bde1a354a4f493
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118169609"
---
# <a name="rb_getdroptarget-message"></a>\_Message GETDROPTARGET RB

Récupère le pointeur d’interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) d’un contrôle rebar.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Doit être zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un pointeur [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) qui reçoit le pointeur d’interface. Il incombe à l’appelant d’appeler [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) sur ce pointeur lorsqu’il n’est plus nécessaire.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

