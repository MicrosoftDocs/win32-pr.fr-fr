---
title: Message UDM_GETACCEL (commctrl. h)
description: Récupère les informations d’accélération pour un contrôle up-up.
ms.assetid: 794538d6-ca01-4f05-82d1-ce7bc0f76f64
keywords:
- UDM_GETACCEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_GETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86a9740e59631b737453763a10ccb9820056d95
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115474"
---
# <a name="udm_getaccel-message"></a>\_Message GETACCEL UDM

Récupère les informations d’accélération pour un contrôle up-up.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre d’éléments dans le tableau spécifié par *lParam*.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau de structures [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) qui reçoivent des informations d’accélération.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est le nombre d’accélérateurs actuellement définis pour le contrôle.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETACCEL UDM**](udm-setaccel.md)
</dt> </dl>

 

 





