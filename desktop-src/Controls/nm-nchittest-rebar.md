---
title: Code de notification NM_NCHITTEST (Rebar) (commctrl. h)
description: Code de notification NM_NCHITTEST (Rebar)-envoyé par un contrôle rebar lorsque le contrôle reçoit un \_ message WM NCHITTEST. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: b345d83e-682d-4067-a783-689d64f9b7bc
keywords:
- Contrôles Windows de code de notification NM_NCHITTEST (Rebar)
topic_type:
- apiref
api_name:
- NM_NCHITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7935f1b3e990db55518c9d22537e8fb6db97962
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112327"
---
# <a name="nm_nchittest-rebar-notification-code"></a>\_Code de notification NCHITTEST nm (Rebar)

Envoyé par un contrôle rebar lorsque le contrôle reçoit un message [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
NM_NCHITTEST

    lpnmmouse = (LPNMMOUSE) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMMOUSE**](/windows/win32/api/commctrl/ns-commctrl-nmmouse) qui contient des informations sur le code de notification. Le membre **dwItemSpec** contient l’index de bande sur lequel le message de test de positionnement s’est produit et le membre **PT** contient les coordonnées de la souris du message de test de positionnement.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retournez zéro pour permettre au Rebar d’effectuer le traitement par défaut du message de test de positionnement, ou retournez l’une des \* valeurs HT documentées sous [**WM \_ NCHITTEST**](/windows/desktop/inputdev/wm-nchittest) pour remplacer le traitement par défaut du test de positionnement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

