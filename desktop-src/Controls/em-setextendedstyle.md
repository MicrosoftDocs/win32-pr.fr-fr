---
title: Message EM_SETEXTENDEDSTYLE (commctrl. h)
description: Informe le contrôle d’édition de la définition de styles étendus. Envoyez ce message ou utilisez la macro Edit \_ SetExtendedStyle.
ms.assetid: 4ca010c3-2c70-41e5-ade4-11e1895fda26
keywords:
- EM_SETEXTENDEDSTYLE les contrôles de Windows de message
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006403"
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

## <a name="return-value"></a>Valeur de retour

Si ce message est correctement exécuté, il renvoie la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Les styles étendus pour un contrôle d’édition n’ont rien à faire avec les styles étendus utilisés avec la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) ou la fonction [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, version 1809 \[ applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows Serveur 2019 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

