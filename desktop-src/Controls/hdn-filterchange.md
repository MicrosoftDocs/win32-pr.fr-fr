---
title: HDN_FILTERCHANGE le code de notification (commctrl. h)
description: Notifie la fenêtre parente du contrôle d’en-tête que les attributs d’un filtre de contrôle d’en-tête sont modifiés ou modifiés. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 0a46af14-569a-4119-881f-549a130f9b0d
keywords:
- HDN_FILTERCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- HDN_FILTERCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3d5d31b792e909cd79cdc6aa966bfdce450787b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999924"
---
# <a name="hdn_filterchange-notification-code"></a>\_Code de notification HDN FILTERCHANGE

Notifie la fenêtre parente du contrôle d’en-tête que les attributs d’un filtre de contrôle d’en-tête sont modifiés ou modifiés. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_FILTERCHANGE

    pNMHeader =  (LPNMHEADER) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHEADER**](/windows/win32/api/commctrl/ns-commctrl-nmheadera) qui contient des informations sur le contrôle header et l’élément d’en-tête, y compris les attributs qui sont sur le point d’être modifiés.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**HDM \_ SETFILTERCHANGETIMEOUT**](hdm-setfilterchangetimeout.md)
</dt> </dl>

 

 





