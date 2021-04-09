---
title: Message UDM_SETACCEL (commctrl. h)
description: Définit l’accélération pour un contrôle up-up.
ms.assetid: af1d0a34-13ba-4bda-82f5-d7afab6bb1ed
keywords:
- UDM_SETACCEL les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033257"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETACCEL UDM**](udm-getaccel.md)
</dt> </dl>

 

 





