---
title: EN_CHANGE le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur a effectué une action qui peut avoir modifié du texte dans un contrôle d’édition.
ms.assetid: 8a04e6fb-ae9d-4d94-8047-6de96df899f5
keywords:
- EN_CHANGE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_CHANGE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b86dbfb90376a85df09cad854882fa2616e6b7cb247cab4106850608a4b96ad4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437049"
---
# <a name="en_change-notification-code"></a>\_Code de notification de modification

Envoyé lorsque l’utilisateur a effectué une action qui peut avoir modifié du texte dans un contrôle d’édition. Contrairement au code de notification en [ \_ mise à jour](en-update.md) , ce code de notification est envoyé une fois que le système a mis à jour l’écran. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
EN_CHANGE

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

## <a name="remarks"></a>Remarques

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour recevoir les \_ codes de notification de modification, spécifiez [**ENM \_ change**](rich-edit-control-event-mask-flags.md) dans le masque envoyé avec le message [**em \_ SETEVENTMASK**](em-seteventmask.md) . Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

Le \_ Code de notification de modification n’est pas envoyé lorsque le style de [**\_ multiligne es**](edit-control-styles.md) est utilisé et que le texte est envoyé par le biais de [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext).

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

[en cours de \_ mise à jour](en-update.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

