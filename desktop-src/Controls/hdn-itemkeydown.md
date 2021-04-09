---
title: HDN_ITEMKEYDOWN le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header qu’une touche a été enfoncée avec un élément sélectionné. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ab6922ab-907d-44fc-8606-28f395118405
keywords:
- Contrôles Windows de code de notification HDN_ITEMKEYDOWN
topic_type:
- apiref
api_name:
- HDN_ITEMKEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c4415eb5a026bf96d53884fe2735f3a3fa2e494
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104033245"
---
# <a name="hdn_itemkeydown-notification-code"></a>\_Code de notification HDN ITEMKEYDOWN

Avertit la fenêtre parente d’un contrôle header qu’une touche a été enfoncée avec un élément sélectionné. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ITEMKEYDOWN

   pNMHeader = (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations supplémentaires sur la touche qui est enfoncée.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





