---
title: Message EM_SETEXTENDEDSTYLE (commctrl. h)
description: Informe le contrôle d’édition de la définition de styles étendus. Envoyez ce message ou utilisez la macro Edit \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETEXTENDEDSTYLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 10/19/2018
ms.openlocfilehash: 560b675927b4497810b8d492fd89b5765aa5a2c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105571"
---
# <a name="em_setextendedstyle-message"></a>\_Message SETEXTENDEDSTYLE em

Informe le contrôle d’édition de la définition de styles étendus. Envoyez ce message ou utilisez la macro [**Edit \_ SetExtendedStyle**](/windows/desktop/api/Commctrl/nf-commctrl-edit_setextendedstyle).

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Masque utilisé pour sélectionner les styles à définir.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur qui indique le style étendu. Pour plus d’informations sur les styles, consultez [modifier les styles étendus de contrôle](edit-control-window-extended-styles.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si ce message est correctement exécuté, il renvoie la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Les styles étendus pour un contrôle d’édition n’ont rien à faire avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1809 \[ uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2019 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

