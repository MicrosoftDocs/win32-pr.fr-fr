---
title: EN_MAXTEXT le code de notification (winuser. h)
description: Envoyé lorsque l’insertion de texte actuelle a dépassé le nombre spécifié de caractères pour le contrôle d’édition.
ms.assetid: b03835d6-d06f-415a-97f2-d2b62b17e175
keywords:
- Contrôles Windows de code de notification EN_MAXTEXT
topic_type:
- apiref
api_name:
- EN_MAXTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 454b48fb232f2225696efacc44d54660d3a83185
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509162"
---
# <a name="en_maxtext-notification-code"></a>\_Code de notification en MAXTEXT

Envoyé lorsque l’insertion de texte actuelle a dépassé le nombre spécifié de caractères pour le contrôle d’édition. L’insertion de texte a été tronquée.

Ce code de notification est également envoyé lorsqu’un contrôle d’édition n’a pas le style [**es \_ AUTOHSCROLL**](edit-control-styles.md) et que le nombre de caractères à insérer dépasse la largeur du contrôle d’édition.

Ce code de notification est également envoyé lorsqu’un contrôle d’édition n’a pas le style [**es \_ AUTOVSCROLL**](edit-control-styles.md) et que le nombre total de lignes résultant d’une insertion de texte dépasse la hauteur du contrôle d’édition.

La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_MAXTEXT

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur du contrôle d’édition. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du contrôle d’édition.

</dd> </dl>

## <a name="remarks"></a>Notes

La fenêtre parente reçoit toujours un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) pour cet événement, elle ne nécessite pas de masque de notification envoyé avec [**em \_ SETEVENTMASK**](em-seteventmask.md).

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

