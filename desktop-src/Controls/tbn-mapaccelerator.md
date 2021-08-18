---
title: TBN_MAPACCELERATOR le code de notification (commctrl. h)
description: Demande l’index du bouton dans la barre d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 488c78ff00b75c42f6646e314c75d63445c7400eb9130464b126e75bcf2df942
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434189"
---
# <a name="tbn_mapaccelerator-notification-code"></a>\_Code de notification TBN MAPACCELERATOR

Demande l’index du bouton dans la barre d’outils correspondant au caractère d’accélérateur spécifié. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) qui contient le caractère de touche accélérateur et qui reçoit l’index du bouton correspondant. Le champ **dwItemNext** a la valeur-1 si l’accélérateur ne correspond pas à une commande.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

TRUE si **NMCHAR. dwItemNext** est défini sur une valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





