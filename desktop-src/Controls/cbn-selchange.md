---
title: CBN_SELCHANGE le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur modifie la sélection actuelle dans la zone de liste d’une zone de liste déroulante.
ms.assetid: 2d0d711c-dfc4-485b-97bb-9ccfa7c5864b
keywords:
- CBN_SELCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- CBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e921b7856780763923a448e42de072476cc02f6b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123822"
---
# <a name="cbn_selchange-notification-code"></a>\_Code de notification CBN selChange

Envoyé lorsque l’utilisateur modifie la sélection actuelle dans la zone de liste d’une zone de liste déroulante. L’utilisateur peut modifier la sélection en cliquant dans la zone de liste ou en utilisant les touches de direction. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification sous la forme d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELCHANGE

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle de la zone de liste déroulante. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la zone de liste déroulante.

</dd> </dl>

## <a name="remarks"></a>Notes

Pour récupérer l’index de la sélection actuelle, envoyez le message [**CB \_ GETCURSEL**](cb-getcursel.md) au contrôle.

Le \_ Code de notification CBN selChange n’est pas envoyé lorsque la sélection actuelle est définie à l’aide du message [**CB \_ SETCURSEL**](cb-setcursel.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[CBN \_ gros plan](cbn-closeup.md)
</dt> <dt>

[CBN \_ DBLCLK](cbn-dblclk.md)
</dt> <dt>

[**\_GETCURSEL CB**](cb-getcursel.md)
</dt> <dt>

[**\_SETCURSEL CB**](cb-setcursel.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

