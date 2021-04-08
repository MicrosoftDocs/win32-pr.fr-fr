---
title: DTN_DATETIMECHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle de sélecteur de date et heure (PAO) chaque fois qu’une modification se produit. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 65cdd8fb-1f07-4447-b503-d40fdfa37202
keywords:
- Contrôles Windows de code de notification DTN_DATETIMECHANGE
topic_type:
- apiref
api_name:
- DTN_DATETIMECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a40072a54732a0a3575e3153ddb901ca1df291b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843938"
---
# <a name="dtn_datetimechange-notification-code"></a>\_Code de notification DTN DATETIMECHANGE

Envoyé par un contrôle de sélecteur de date et heure (PAO) chaque fois qu’une modification se produit. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
DTN_DATETIMECHANGE

    lpChange = (LPNMDATETIMECHANGE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMDATETIMECHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmdatetimechange) contenant des informations sur la modification qui a eu lieu dans le contrôle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le propriétaire du contrôle doit retourner zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





