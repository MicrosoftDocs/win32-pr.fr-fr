---
title: Message EM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère le style étendu d’un contrôle d’édition. Envoyez ce message explicitement ou à l’aide de la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 77aa5827cc256c040d34ca24574dfa0b12816accaff9e5c0e92b4400195cae2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019667"
---
# <a name="em_getextendedstyle-message-commctrlh"></a>Message EM_GETEXTENDEDSTYLE (commctrl. h)

Récupère le style étendu pour un contrôle Tree-View. Envoyez ce message explicitement ou à l’aide de la macro [**Edit \_ GetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_getextendedstyle) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la valeur du style étendu. Pour plus d’informations sur les styles, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).

## <a name="remarks"></a>Remarques

Les styles étendus pour un contrôle d’édition n’ont rien à faire avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 \[ applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

