---
title: Message RB_GETDROPTARGET (commctrl. h)
description: Récupère le pointeur d’interface IDropTarget d’un contrôle rebar.
ms.assetid: f429c5d1-406b-47f0-a654-47cabccc1d0e
keywords:
- RB_GETDROPTARGET les contrôles de message Windows
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
ms.openlocfilehash: 55b7960cc13230a2715348bc55e5e65de6f72e5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466078"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

