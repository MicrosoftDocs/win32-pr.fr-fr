---
description: Une application envoie le \_ message WM MDISETMENU à une fenêtre cliente d’interface multidocument (MDI) pour remplacer le menu entier d’une fenêtre frame MDI, pour remplacer le menu fenêtre de la fenêtre frame, ou les deux.
ms.assetid: 5cc85032-5378-44a0-abd4-d583deaa3294
title: Message WM_MDISETMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5fe87682691c5f113034c20c68cefd81ca3a7018bd44eb868c4f18551cacacd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119772069"
---
# <a name="wm_mdisetmenu-message"></a>\_Message WM MDISETMENU

Une application envoie le message **WM \_ MDISETMENU** à une fenêtre cliente d’interface multidocument (MDI) pour remplacer le menu entier d’une fenêtre frame MDI, pour remplacer le menu fenêtre de la fenêtre frame, ou les deux.


```C++
#define WM_MDISETMENU                   0x0230
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le menu de la nouvelle fenêtre frame. Si ce paramètre a la **valeur null**, le menu de la fenêtre frame n’est pas modifié.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle vers le nouveau menu fenêtre. Si ce paramètre a la **valeur null**, le menu fenêtre n’est pas modifié.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HMENU**

Si le message est correctement exécuté, la valeur de retour est le handle du menu de la fenêtre frame précédente.

Si le message échoue, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Après l’envoi de ce message, une application doit appeler la fonction [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) pour mettre à jour la barre de menus.

Si ce message remplace le menu fenêtre, les éléments de menu de la fenêtre enfant MDI sont supprimés du menu fenêtre précédente et ajoutés au menu nouvelle fenêtre.

Si une fenêtre enfant MDI est agrandie et que ce message remplace le menu fenêtre frame MDI, l’icône de menu fenêtre et l’icône de restauration sont supprimées du menu de la fenêtre frame précédente et ajoutées au menu nouvelle fenêtre frame.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar)
</dt> <dt>

[**\_MDIREFRESHMENU WM**](wm-mdirefreshmenu.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 
