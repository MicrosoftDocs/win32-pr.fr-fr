---
title: TCN_KEYDOWN le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet qu’une touche a été enfoncée. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- TCN_KEYDOWN les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116121"
---
# <a name="tcn_keydown-notification-code"></a>Code de notification KeyOut TCN \_

Avertit une fenêtre parente d’un contrôle onglet qu’une touche a été enfoncée. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





