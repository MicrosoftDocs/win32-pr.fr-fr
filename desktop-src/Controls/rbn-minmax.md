---
title: RBN_MINMAX le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar avant d’agrandir ou de réduire une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- RBN_MINMAX les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- RBN_MINMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18fea875af376b3ec9b311d2aad09597f0ce6ea264963e9e466cc87ce4fe4b6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984989"
---
# <a name="rbn_minmax-notification-code"></a>\_Code de notification RBN MinMax

Envoyé par un contrôle rebar avant d’agrandir ou de réduire une bande. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
RBN_MINMAX
```



## <a name="parameters"></a>Paramètres

Ce code de notification n’a pas de paramètres.

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro pour empêcher l’opération de se produire, zéro pour l’autoriser à continuer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





