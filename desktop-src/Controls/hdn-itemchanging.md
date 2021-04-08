---
title: HDN_ITEMCHANGING le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête sont sur le point d’être modifiés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: c3361f88-69d4-425f-b548-0ad3b2a00af4
keywords:
- Contrôles Windows de code de notification HDN_ITEMCHANGING
topic_type:
- apiref
api_name:
- HDN_ITEMCHANGING
- HDN_ITEMCHANGINGA
- HDN_ITEMCHANGINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c803f9bde466b524b2ca1cb89062f5fc89d6865f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843149"
---
# <a name="hdn_itemchanging-notification-code"></a>\_Code de notification HDN ITEMCHANGING

Avertit la fenêtre parente d’un contrôle header que les attributs d’un élément d’en-tête sont sur le point d’être modifiés. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_ITEMCHANGING

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément d’en-tête, y compris les attributs qui sont sur le point d’être modifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **false** pour autoriser les modifications, ou **true** pour les empêcher.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ ITEMCHANGINGW** (Unicode) et **HDN \_ ITEMCHANGINGA** (ANSI)<br/>         |



 

 





