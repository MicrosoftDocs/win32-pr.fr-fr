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
ms.openlocfilehash: 573f3dd93a6e4b0b3db6682d36804416d6f6f1e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117614"
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

## <a name="return-value"></a>Valeur de retour

Retournez zéro pour mettre en surbrillance l’élément ou une valeur différente de zéro pour empêcher la mise en surbrillance.

## <a name="remarks"></a>Notes

> [!Note]  
> Pour utiliser ce code de notification, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





