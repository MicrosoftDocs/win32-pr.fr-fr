---
title: EN_SETFOCUS le code de notification (winuser. h)
description: Envoyé lorsqu’un contrôle d’édition reçoit le focus clavier. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message de commande WM.
ms.assetid: 482d2afa-4e21-4f3f-bdf4-6966b34cc3c4
keywords:
- Contrôles Windows de code de notification EN_SETFOCUS
topic_type:
- apiref
api_name:
- EN_SETFOCUS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5cb96482f0e42669658dde3a39637e3c2311619
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743036"
---
# <a name="en_setfocus-notification-code"></a>\_Code de notification en SetFocus

Envoyé lorsqu’un contrôle d’édition reçoit le focus clavier. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_SETFOCUS

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

**Référence**
</dt> <dt>

[en \_ KILLFOCUS](en-killfocus.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

