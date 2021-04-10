---
title: HDN_ITEMDBLCLICK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur le contrôle. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify. Seuls les contrôles d’en-tête définis sur le \_ style des boutons HDS envoient ce code de notification.
ms.assetid: 72bb00b9-226f-4409-b788-b623868f78b6
keywords:
- Contrôles Windows de code de notification HDN_ITEMDBLCLICK
topic_type:
- apiref
api_name:
- HDN_ITEMDBLCLICK
- HDN_ITEMDBLCLICKA
- HDN_ITEMDBLCLICKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e61117303ecc478a998da8799867988dbc1ca08
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104200579"
---
# <a name="hdn_itemdblclick-notification-code"></a>\_Code de notification HDN ITEMDBLCLICK

Avertit la fenêtre parente d’un contrôle header que l’utilisateur a double-cliqué sur le contrôle. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) . Seuls les contrôles d’en-tête définis sur le style des [**\_ boutons HDS**](header-control-styles.md) envoient ce code de notification.


```C++
HDN_ITEMDBLCLICK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ ITEMDBLCLICKW** (Unicode) et **HDN \_ ITEMDBLCLICKA** (ANSI)<br/>         |



 

 





