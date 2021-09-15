---
title: LVN_MARQUEEBEGIN le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle d’affichage de liste qu’une sélection de cadre englobant (texte défilant) a commencé. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: e9daa264-1861-4791-9a12-cf95d86a688e
keywords:
- LVN_MARQUEEBEGIN les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LVN_MARQUEEBEGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d46d399b8355bea0ddb2054340d52db59c3ad27
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127312549"
---
# <a name="lvn_marqueebegin-notification-code"></a>\_Code de notification LVN MARQUEEBEGIN

Avertit une fenêtre parente d’un contrôle d’affichage de liste qu’une sélection de cadre englobant (texte défilant) a commencé. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
LVN_MARQUEEBEGIN

    pnmv = (LPNMLISTVIEW) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) .

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pour accepter le code de notification, retournez zéro. Pour quitter la sélection de rectangle englobant, retournez une valeur différente de zéro.

## <a name="remarks"></a>Remarques

Une *sélection de cadre englobant* est le processus qui consiste à cliquer sur la zone cliente de la fenêtre d’affichage de liste et à faire glisser pour sélectionner plusieurs éléments simultanément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





