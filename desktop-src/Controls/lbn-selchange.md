---
title: LBN_SELCHANGE le code de notification (winuser. h)
description: Indique à l’application que la sélection dans une zone de liste a été modifiée suite à une entrée de l’utilisateur. La fenêtre parente de la zone de liste reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: 126d2c47-816e-4179-a870-f5c5a34c5513
keywords:
- Contrôles Windows de code de notification LBN_SELCHANGE
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
ms.openlocfilehash: e029d1753a0fa74f39a59a459d6ede45811a40fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741572"
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

## <a name="remarks"></a>Notes

Ce code de notification est envoyé uniquement par une zone de liste dont le style de [**\_ notification est lbs**](list-box-styles.md) .

Ce code de notification n’est pas envoyé si le message [**lb \_ SETSEL**](lb-setsel.md), [**lb \_ SETCURSEL**](lb-setcursel.md), [**lb \_ SELECTSTRING**](lb-selectstring.md), [**lb \_ SELITEMRANGE**](lb-selitemrange.md) ou [**lb \_ SELITEMRANGEEX**](lb-selitemrangeex.md) modifie la sélection.

Pour une zone de liste à sélection multiple, le \_ Code de notification LBN selChange est envoyé chaque fois que l’utilisateur appuie sur une touche de direction, même si la sélection ne change pas.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
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

 

