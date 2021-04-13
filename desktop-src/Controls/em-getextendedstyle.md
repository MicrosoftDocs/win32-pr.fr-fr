---
title: Message EM_GETEXTENDEDSTYLE (commctrl. h)
description: Récupère le style étendu d’un contrôle d’édition. Envoyez ce message explicitement ou à l’aide de la \_ macro Edit GetExtendedStyle.
ms.assetid: 557f796e-c9d1-4ea1-b8a6-44ae0bed5ffc
keywords:
- EM_GETEXTENDEDSTYLE les contrôles de message Windows
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
ms.openlocfilehash: 37dc117bccd57b51098a7ca8c19e8b178037bef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466111"
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

## <a name="remarks"></a>Notes

Les styles étendus pour un contrôle d’édition n’ont rien à faire avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1809 \[ uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2019 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

