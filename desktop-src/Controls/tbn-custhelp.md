---
title: TBN_CUSTHELP le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a choisi le bouton aide dans la boîte de dialogue Personnaliser la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e889764b-abbd-42a6-8c13-ace6ee052039
keywords:
- TBN_CUSTHELP les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_CUSTHELP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89754deaef2ec4ceb020bd1572c5a419315299e0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116337"
---
# <a name="tbn_custhelp-notification-code"></a>\_Code de notification TBN CUSTHELP

Avertit la fenêtre parente d’une barre d’outils que l’utilisateur a choisi le bouton aide dans la boîte de dialogue Personnaliser la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_CUSTHELP 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations sur le code de notification.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





