---
title: LBN_DBLCLK le code de notification (winuser. h)
description: Indique à l’application que l’utilisateur a double-cliqué sur un élément dans une zone de liste. La fenêtre parente de la zone de liste reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 487282cb-833a-4123-987e-6a417fbd09d4
keywords:
- LBN_DBLCLK les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LBN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 132e1b68527aca9227702caeea40ffd8deb46e375ffdd87bcf1288dfb01584e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085309"
---
# <a name="lbn_dblclk-notification-code"></a>\_Code de notification LBN DBLCLK

Indique à l’application que l’utilisateur a double-cliqué sur un élément dans une zone de liste. La fenêtre parente de la zone de liste reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
LBN_DBLCLK

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de la zone de liste. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers la zone de liste.

</dd> </dl>

## <a name="remarks"></a>Remarques

Ce code de notification est envoyé uniquement par une zone de liste dont le style de notification est L [**BS \_**](button-styles.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[LBN \_ selChange](lbn-selchange.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

