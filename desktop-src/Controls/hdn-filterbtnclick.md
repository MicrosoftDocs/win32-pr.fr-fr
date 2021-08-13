---
title: HDN_FILTERBTNCLICK le code de notification (commctrl. h)
description: Notifie la fenêtre parente du contrôle header lorsque l’utilisateur clique sur le bouton de filtre ou en réponse à un \_ message HDM SETITEM. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 36b85cdc-1022-4568-8891-0c919c850fd4
keywords:
- HDN_FILTERBTNCLICK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- HDN_FILTERBTNCLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 01ba216c9946854ccfc6a651db90ab1dd5ed106dfca6ddf568d485c33dae70ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435509"
---
# <a name="hdn_filterbtnclick-notification-code"></a>\_Code de notification HDN FILTERBTNCLICK

Notifie la fenêtre parente du contrôle header lorsque l’utilisateur clique sur le bouton de filtre ou en réponse à un message [**HDM \_ SETITEM**](hdm-setitem.md) . Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
HDN_FILTERBTNCLICK

    pNMHDFilterBtnClk = (LPNMHDFILTERBTNCLICK) lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick) qui contient des informations sur le contrôle header et le bouton de filtre d’en-tête.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si vous renvoyez la **valeur true**, un code de notification [HDN \_ FILTERCHANGE](hdn-filterchange.md) sera envoyé à la fenêtre parente du contrôle d’en-tête. Ce code de notification donne à la fenêtre parente la possibilité de synchroniser ses éléments d’interface utilisateur. Retourne la **valeur false** si vous ne souhaitez pas envoyer la notification.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**NMHDFILTERBTNCLICK**](/windows/win32/api/commctrl/ns-commctrl-nmhdfilterbtnclick)
</dt> </dl>

 

 





