---
title: Message UDM_GETRANGE32 (commctrl. h)
description: Récupère la plage 32 bits d’un contrôle up-up.
ms.assetid: a94b50c9-cd2f-430d-875f-720e51f544f1
keywords:
- UDM_GETRANGE32 les contrôles de message Windows
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
ms.openlocfilehash: ca418cd08dc4c81b3ff734d74f3ca9deeef7d848
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465023"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





