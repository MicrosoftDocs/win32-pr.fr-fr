---
title: LVN_GETINFOTIP le code de notification (commctrl. h)
description: Envoyé par une grande icône Afficher le contrôle List-View avec le \_ \_ style étendu LVS ex info-bulle.
ms.assetid: 62be5087-7e49-4722-a63a-1768e030af48
keywords:
- LVN_GETINFOTIP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_GETINFOTIP
- LVN_GETINFOTIPA
- LVN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f7477230913ec5efd0827bc48e1a6021619aa4cdbbad252426d1af364b5b36b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117830440"
---
# <a name="lvn_getinfotip-notification-code"></a>\_Code de notification LVN GETINFOTIP

Envoyé par une grande icône Afficher le contrôle List-View avec le style étendu [**LVS \_ ex \_ info-bulle**](extended-list-view-styles.md) . Ce code de notification est envoyé lorsque le contrôle List-View demande des informations de texte supplémentaires à afficher dans une info-bulle. Il est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_GETINFOTIP

    pGetInfoTip = (LPNMLVGETINFOTIP) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) qui contient des informations sur ce code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="remarks"></a>Remarques

Ce code de notification est uniquement envoyé par les contrôles List-View qui ont le style étendu [**LVS \_ ex \_ info-bulle**](extended-list-view-styles.md) . Le \_ Code de notification LVN GETINFOTIP est envoyé uniquement pour le sous-élément 0.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVN \_ GETINFOTIPW** (Unicode) et **LVN \_ GETINFOTIPA** (ANSI)<br/>             |



 

 





