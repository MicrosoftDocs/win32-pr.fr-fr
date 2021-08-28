---
title: EN_HSCROLL le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur clique sur la barre de défilement horizontale d’un contrôle d’édition. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un \_ message de commande WM. La fenêtre parente est avertie avant la mise à jour de l’écran.
ms.assetid: beaaa80c-4108-4a8e-aed8-04c9a3a08f3e
keywords:
- EN_HSCROLL les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_HSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4e5b0f42d08977f7a1be68a5010aa7403b10fc2e5a126aa542bb25a644a7b70
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119436769"
---
# <a name="en_hscroll-notification-code"></a>\_Code de notification en HSCROLL

Envoyé lorsque l’utilisateur clique sur la barre de défilement horizontale d’un contrôle d’édition. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . La fenêtre parente est avertie avant la mise à jour de l’écran.


```C++
EN_HSCROLL

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

Ce code de notification est envoyé pour les événements de souris suivants sur la barre de défilement horizontale : cliquez sur le bouton fléché ou cliquez entre le bouton fléché et le curseur. Toutefois, le code de notification n’est pas envoyé quand vous cliquez sur le curseur de la barre de défilement. Le code de notification est également envoyé lorsqu’un événement de clavier provoque une modification dans la zone d’affichage du contrôle d’édition, par exemple en appuyant sur origine, fin, flèche gauche ou flèche droite.

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour recevoir les codes de notification en **\_ HSCROLL** , spécifiez [**ENM \_ faites défiler**](rich-edit-control-event-mask-flags.md) le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) . Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

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

[en \_ VSCROLL](en-vscroll.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

