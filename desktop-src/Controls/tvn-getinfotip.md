---
title: TVN_GETINFOTIP le code de notification (commctrl. h)
description: Envoyé par un contrôle Tree-View qui a le style de l’info-bulle du téléviseur \_ . Ce code de notification est envoyé lorsque le contrôle demande des informations de texte supplémentaires à afficher dans une info-bulle. Le code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 20576710-e279-4e61-be6b-bf1d8ea79555
keywords:
- TVN_GETINFOTIP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TVN_GETINFOTIP
- TVN_GETINFOTIPA
- TVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1336571fa2c06e8b22078b1d761d9841217104e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127115514"
---
# <a name="tvn_getinfotip-notification-code"></a>\_Code de notification TVN GETINFOTIP

Envoyé par un contrôle Tree-View qui a le style de l' [**\_ info-bulle du téléviseur**](tree-view-control-window-styles.md) . Ce code de notification est envoyé lorsque le contrôle demande des informations de texte supplémentaires à afficher dans une info-bulle. Le code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TVN_GETINFOTIP

    lpGetInfoTip = (LPNMTVGETINFOTIP)lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtvgetinfotipa) qui contient des informations sur ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Le contrôle ignore la valeur de retour pour ce code de notification.

## <a name="remarks"></a>Notes

Ce code de notification est uniquement envoyé par les contrôles d’arborescence qui ont le style de l' [**\_ info-bulle du téléviseur**](tree-view-control-window-styles.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVN \_ GETINFOTIPW** (Unicode) et **TVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





