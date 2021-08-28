---
title: LBN_SELCHANGE le code de notification (winuser. h)
description: Indique à l’application que la sélection dans une zone de liste a été modifiée suite à une entrée de l’utilisateur. La fenêtre parente de la zone de liste reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- LBN_SELCHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- LBN_SELCHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef87aebcf2ce804a10b4682bfaf2cba900bd227a06671959d11babce5f46774
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085179"
---
# <a name="lbn_selchange-notification-code"></a>\_Code de notification LBN selChange

Indique à l’application que la sélection dans une zone de liste a été modifiée suite à une entrée de l’utilisateur. La fenêtre parente de la zone de liste reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
LBN_SELCHANGE

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

Ce code de notification est envoyé uniquement par une zone de liste dont le style de [**\_ notification est lbs**](list-box-styles.md) .

Ce code de notification n’est pas envoyé si le message [**lb \_ SETSEL**](lb-setsel.md), [**lb \_ SETCURSEL**](lb-setcursel.md), [**lb \_ SELECTSTRING**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) ou [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) modifie la sélection.

Pour une zone de liste à sélection multiple, le \_ Code de notification LBN selChange est envoyé chaque fois que l’utilisateur appuie sur une touche de direction, même si la sélection ne change pas.

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

[**\_SETCURSEL lb**](lb-setcursel.md)
</dt> <dt>

[LBN \_ DBLCLK](lbn-dblclk.md)
</dt> <dt>

[LBN \_ SELCANCEL](lbn-selcancel.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

