---
title: HDN_BEGINTRACK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur a commencé à faire glisser un séparateur dans le contrôle (autrement dit, l’utilisateur a appuyé sur le bouton gauche de la souris pendant que le curseur de la souris se trouve sur un séparateur dans le contrôle header).
ms.assetid: 363b14bc-2b7e-4c37-9caf-7671fcc3cfa5
keywords:
- HDN_BEGINTRACK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- HDN_BEGINTRACK
- HDN_BEGINTRACKA
- HDN_BEGINTRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6da4ae2c360b13077a612b92ab19a739a58a07e3
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999940"
---
# <a name="hdn_begintrack-notification-code"></a>\_Code de notification HDN BEGINTRACK

Avertit la fenêtre parente d’un contrôle header que l’utilisateur a commencé à faire glisser un séparateur dans le contrôle (autrement dit, l’utilisateur a appuyé sur le bouton gauche de la souris pendant que le curseur de la souris se trouve sur un séparateur dans le contrôle header). Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_BEGINTRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément dont le séparateur doit être glissé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne **false** pour autoriser le suivi du séparateur, ou **true** pour empêcher le suivi.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ BEGINTRACKW** (Unicode) et **HDN \_ BEGINTRACKA** (ANSI)<br/>             |



 

 





