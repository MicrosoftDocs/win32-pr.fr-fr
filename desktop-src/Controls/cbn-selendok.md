---
title: CBN_SELENDOK le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur sélectionne un élément de liste, ou sélectionne un élément, puis ferme la liste. Elle indique que la sélection de l’utilisateur doit être traitée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le \_ message de commande WM.
ms.assetid: ef0ac46f-2db9-40d6-ba82-7e90d71fdd37
keywords:
- Contrôles Windows de code de notification CBN_SELENDOK
topic_type:
- apiref
api_name:
- CBN_SELENDOK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a0b04fcce0ec2b3f6a2bf5b5e04fa4110ad6ceb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510325"
---
# <a name="cbn_selendok-notification-code"></a>\_Code de notification CBN SELENDOK

Envoyé lorsque l’utilisateur sélectionne un élément de liste, ou sélectionne un élément, puis ferme la liste. Elle indique que la sélection de l’utilisateur doit être traitée. La fenêtre parente de la zone de liste déroulante reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
CBN_SELENDOK

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

Dans une zone de liste modifiable avec le style [**CBS \_ simple**](combo-box-styles.md) , le \_ Code de notification CBN SELENDOK est envoyé immédiatement avant chaque code de notification [CBN \_ selChange](cbn-selchange.md) .

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

[CBN \_ selChange](cbn-selchange.md)
</dt> <dt>

[CBN \_ SELENDCANCEL](cbn-selendcancel.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

