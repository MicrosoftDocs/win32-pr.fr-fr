---
title: Message UDM_SETACCEL (commctrl. h)
description: Définit l’accélération pour un contrôle up-up.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL les contrôles de Windows de message
topic_type:
- apiref
api_name:
- UDM_SETACCEL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b43ed290ce1668ffcaa9fb086a99ad52e5129ad6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115441"
---
# <a name="udm_setaccel-message"></a>\_Message SETACCEL UDM

Définit l’accélération pour un contrôle up-up.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de structures [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) spécifiées par *aAccels*.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau de structures [**UDACCEL**](/windows/desktop/api/Commctrl/ns-commctrl-udaccel) qui contiennent des informations d’accélération. Les éléments doivent être triés dans l’ordre croissant en fonction du membre **nSec** .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETACCEL UDM**](udm-getaccel.md)
</dt> </dl>

 

 





