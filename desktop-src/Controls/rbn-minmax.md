---
title: RBN_MINMAX le code de notification (commctrl. h)
description: Envoyé par un contrôle rebar avant d’agrandir ou de réduire une bande. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 75619cb0-ef0b-44fa-83b2-15a5e5e92c60
keywords:
- Contrôles Windows de code de notification RBN_MINMAX
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
ms.openlocfilehash: b3569a28d0c0a610ccccf42d11ff4b2e5b4b0007
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512399"
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
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





