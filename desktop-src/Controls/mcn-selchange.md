---
title: MCN_SELCHANGE le code de notification (commctrl. h)
description: Envoyé par un contrôle Month Calendar lorsque la date ou la plage de dates actuellement sélectionnée change. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 8923524f-d257-409d-bd3e-021684b88856
keywords:
- Contrôles Windows de code de notification MCN_SELCHANGE
topic_type:
- apiref
api_name:
- MCN_SELCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffa328ca0173afd3a577f6cf14e0204cd5c0f7d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032492"
---
# <a name="mcn_selchange-notification-code"></a>\_Code de notification MCN selChange

Envoyé par un contrôle Month Calendar lorsque la date ou la plage de dates actuellement sélectionnée change. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
MCN_SELCHANGE

    lpNMSelChange = (LPNMSELCHANGE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMSELCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmselchange) qui contient des informations sur la plage de dates actuellement sélectionnée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Par exemple, le contrôle envoie MCN \_ selChange lorsque l’utilisateur modifie explicitement la sélection dans le mois en cours ou lorsque la sélection est implicitement modifiée en réponse à la navigation vers le mois suivant/précédent. Ce code de notification est également envoyé par le système à intervalles réguliers afin que le contrôle puisse répondre aux modifications de date.

Ce code de notification est similaire à [MCN \_ Select](mcn-select.md), mais il est envoyé en réponse à toute modification de sélection. MCN \_ Select est envoyé uniquement pour une sélection de date explicite.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





