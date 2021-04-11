---
title: HDN_ITEMCHANGED le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête ont changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ab707010-8ed2-4575-8233-8a1f5656e498
keywords:
- Contrôles Windows de code de notification HDN_ITEMCHANGED
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGED
- HDN_ITEMCHANGEDA
- HDN_ITEMCHANGEDW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d67157ff7f775c124236b7a77a1051b7644758c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032432"
---
# <a name="hdn_itemchanged-notification-code"></a>\_Code de notification HDN ITEMCHANGED

Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête ont changé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ITEMCHANGED

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header, y compris les attributs qui ont été modifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ ITEMCHANGEDW** (Unicode) et **HDN \_ ITEMCHANGEDA** (ANSI)<br/>           |



 

 





