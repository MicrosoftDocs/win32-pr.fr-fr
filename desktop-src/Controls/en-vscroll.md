---
title: EN_VSCROLL le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur clique sur la barre de défilement verticale d’un contrôle d’édition ou lorsque l’utilisateur fait défiler la roulette de la souris au-dessus du contrôle d’édition.
ms.assetid: 46307dee-3c5c-4020-9c2b-ec4638a0cea5
keywords:
- EN_VSCROLL les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- EN_VSCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de1f99b9ea05d037b5c00562a24bda1e434ce08d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006305"
---
# <a name="en_vscroll-notification-code"></a>\_Code de notification en VSCROLL

Envoyé lorsque l’utilisateur clique sur la barre de défilement verticale d’un contrôle d’édition ou lorsque l’utilisateur fait défiler la roulette de la souris au-dessus du contrôle d’édition. La fenêtre parente du contrôle d’édition reçoit ce code de notification par le biais d’un message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) . La fenêtre parente est avertie avant la mise à jour de l’écran.


```C++
EN_VSCROLL

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

Ce message est envoyé pour les événements de souris suivants sur la barre de défilement verticale : cliquez sur le bouton fléché ou cliquez entre le bouton fléché et le curseur. Toutefois, le message n’est pas envoyé quand vous cliquez sur la souris de la barre de défilement. Le message est également envoyé lorsqu’un événement de clavier provoque une modification dans la zone d’affichage du contrôle d’édition, par exemple en appuyant sur origine, fin, PAGE précédente, PAGE suivante, flèche haut ou flèche bas.

La roulette de la souris est une souris dotée d’une roulette centrale qui défile. Pour plus d’informations, consultez « la roulette de la souris » dans [à propos de l’entrée de la souris](/windows/desktop/inputdev/about-mouse-input).

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Pour recevoir \_ les codes de notification en VSCROLL, spécifiez [**ENM \_ faites défiler**](rich-edit-control-event-mask-flags.md) le masque envoyé avec le message de [**em \_ SETEVENTMASK**](em-seteventmask.md) . Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[en \_ HSCROLL](en-hscroll.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Utilisation des contrôles d’édition](using-edit-controls.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

