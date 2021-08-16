---
title: Message PGN_HOTITEMCHANGE (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle de pagineur que l’élément réactif (en surbrillance) a changé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0f59677c-0251-49f4-b909-6fac6d93f354
keywords:
- PGN_HOTITEMCHANGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- PGN_HOTITEMCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6510eeb648ad883d04ccc0baf916223bb5209d110c2237ef3bf618d241c2ede
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830133"
---
# <a name="pgn_hotitemchange-message"></a>\_Message PGN HOTITEMCHANGE

Avertit la fenêtre parente d’un contrôle de pagineur que l’élément réactif (en surbrillance) a changé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
PGN_HOTITEMCHANGE

    pnmPGHotItem = (LPNMPGHOTITEM) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMPGHOTITEM**](/windows/win32/api/commctrl/ns-commctrl-nmpghotitem) qui contient des informations sur ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retournez zéro pour mettre en surbrillance l’élément ou une valeur différente de zéro pour empêcher la mise en surbrillance.

## <a name="remarks"></a>Remarques

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





