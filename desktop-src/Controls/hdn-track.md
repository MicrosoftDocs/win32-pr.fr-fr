---
title: HDN_TRACK le code de notification (commctrl. h)
description: Avertit la fenêtre parente d’un contrôle header que l’utilisateur fait glisser un séparateur dans le contrôle header. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 26660ae1-0d6e-4ee7-8b6a-d621abef352d
keywords:
- HDN_TRACK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- HDN_TRACK
- HDN_TRACKA
- HDN_TRACKW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fb32a553c85c8fb1bc8321dae5e85b3e7832cf90e4a6652ad163511ad4420d7
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435219"
---
# <a name="hdn_track-notification-code"></a>\_Code de notification HDN Track

Avertit la fenêtre parente d’un contrôle header que l’utilisateur fait glisser un séparateur dans le contrôle header. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_TRACK

    pNMHeader = (LPNMHEADER) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément dont le séparateur est glissé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne **false** pour poursuivre le suivi du séparateur, ou **true** pour terminer le suivi.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **HDN \_ TRACKW** (Unicode) et **HDN \_ tracka** (ANSI)<br/>                       |



 

 





