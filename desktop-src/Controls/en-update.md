---
title: EN_UPDATE le code de notification (winuser. h)
description: Envoyé lorsqu’un contrôle d’édition va se redessiner lui-même.
ms.assetid: 59138736-6cc9-4a3f-95f3-ada9cbf253cb
keywords:
- Contrôles Windows de code de notification EN_UPDATE
topic_type:
- apiref
api_name:
- EN_UPDATE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b045efcfb5d50cb2a85c9ae230e215263aa2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105550"
---
# <a name="en_update-notification-code"></a>Code de notification en cours de \_ mise à jour

Envoyé lorsqu’un contrôle d’édition va se redessiner lui-même. Ce code de notification est envoyé une fois que le contrôle a mis en forme le texte, mais avant d’afficher le texte. Vous pouvez ainsi redimensionner la fenêtre de contrôle d’édition, si nécessaire. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_UPDATE

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

**Édition enrichie 1,0 :** Pour recevoir des \_ codes de notification en mise à jour, spécifiez la [**\_ mise à jour ENM**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .

**Édition enrichie 2,0 et versions ultérieures :** L’indicateur de [**\_ mise à jour ENM**](rich-edit-control-event-mask-flags.md) est ignoré. Le \_ Code de notification en mise à jour est toujours reçu. Toutefois, lorsque Microsoft Rich Edit 3,0 émule Microsoft Rich Edit 1,0, pour recevoir \_ les codes de notification de mise à jour, vous devez spécifier **ENM \_ Update** dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) .

Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[en \_ modification](en-change.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

