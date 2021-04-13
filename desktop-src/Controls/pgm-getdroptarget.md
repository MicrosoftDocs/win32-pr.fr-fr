---
title: Message PGM_GETDROPTARGET (commctrl. h)
description: Récupère le pointeur d’interface IDropTarget d’un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de radiomessagerie \_ GetDropTarget.
ms.assetid: 6b548c30-2d32-4372-90e4-346a27dda218
keywords:
- PGM_GETDROPTARGET les contrôles de message Windows
topic_type:
- apiref
api_name:
- PGM_GETDROPTARGET
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b90f7f9667dd30a79b9345eec211a6ebfcd7a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466095"
---
# <a name="pgm_getdroptarget-message"></a>\_Message GETDROPTARGET PGM

Récupère le pointeur d’interface [**IDropTarget**](/windows/desktop/api/oleidl/nn-oleidl-idroptarget) d’un contrôle de pagineur. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro de [**radiomessagerie \_ GetDropTarget**](/windows/desktop/api/Commctrl/nf-commctrl-pager_getdroptarget) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

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



 

