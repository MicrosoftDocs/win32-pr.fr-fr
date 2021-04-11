---
title: TTN_NEEDTEXT le code de notification (commctrl. h)
description: Envoyé par un contrôle ToolTip pour récupérer les informations nécessaires à l’affichage d’une fenêtre d’info-bulle. Ce code de notification est identique à TTN \_ GETDISPINFO. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 5fd82096-cfad-4b58-aa88-101d73116ec9
keywords:
- Contrôles Windows de code de notification TTN_NEEDTEXT
topic_type:
- apiref
api_name:
- TTN_NEEDTEXT
- TTN_NEEDTEXTA
- TTN_NEEDTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31b498f48534d7f6b270027bc1279244c67e26ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104425"
---
# <a name="ttn_needtext-notification-code"></a>\_Code de notification ttn NEEDTEXT

Envoyé par un contrôle ToolTip pour récupérer les informations nécessaires à l’affichage d’une fenêtre d’info-bulle. Ce code de notification est identique à [ttn \_ GETDISPINFO](ttn-getdispinfo.md). Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TTN_NEEDTEXT

    lpnmtdi = (LPNMTTDISPINFO) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) qui identifie l’outil qui a besoin du texte et reçoit les informations demandées.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour de cette notification n’est pas utilisée.

## <a name="remarks"></a>Notes

Remplissez les membres appropriés de la structure pour retourner les informations demandées au contrôle ToolTip. Si votre gestionnaire de messages définit le membre **uFlags** de la structure [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) sur ttf \_ di \_ SETITEM, le contrôle ToolTip stocke les informations et ne les redemande pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **Ttn \_ NEEDTEXTW** (Unicode) et **ttn \_ NEEDTEXTA** (ANSI)<br/>                 |



 

 





