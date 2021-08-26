---
title: Message UDM_GETRANGE32 (commctrl. h)
description: Récupère la plage 32 bits d’un contrôle up-up.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_GETRANGE32
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72078327b7a580768321f14c1d512e097561ae3441667497a822dc8a8a28b4e2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077099"
---
# <a name="udm_getrange32-message"></a>\_Message GETRANGE32 UDM

Récupère la plage 32 bits d’un contrôle up-up.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers un entier signé qui reçoit la limite inférieure de la plage de contrôles Up-Up. Ce paramètre peut avoir la **valeur null**.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un entier signé qui reçoit la limite supérieure de la plage de contrôles Up-Up. Ce paramètre peut avoir la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de ce message n’est pas utilisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





