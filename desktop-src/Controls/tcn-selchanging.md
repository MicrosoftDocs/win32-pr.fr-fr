---
title: TCN_SELCHANGING le code de notification (commctrl. h)
description: Avertit une fenêtre parente d’un contrôle onglet que l’onglet actuellement sélectionné va être modifié. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: ec7b1bd3-8932-4418-9eed-ecb7c748e4dd
keywords:
- TCN_SELCHANGING les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TCN_SELCHANGING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75fbf92139a43b19d41fce0fd607932531fef7e23556330b9bda376945a21080
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104669"
---
# <a name="tcn_selchanging-notification-code"></a>\_Code de notification TCN SELCHANGING

Avertit une fenêtre parente d’un contrôle onglet que l’onglet actuellement sélectionné va être modifié. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TCN_SELCHANGING 

    lpnmhdr = (LPNMHDR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) qui contient des informations supplémentaires sur cette notification.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** pour empêcher la modification de la sélection ou **false** pour permettre la modification de la sélection.

## <a name="remarks"></a>Remarques

Pour déterminer l’onglet actuellement sélectionné, utilisez la macro [**TabCtrl \_ GetCurSel**](/windows/desktop/api/Commctrl/nf-commctrl-tabctrl_getcursel) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[TCN \_ selChange](tcn-selchange.md)
</dt> </dl>

 

 





