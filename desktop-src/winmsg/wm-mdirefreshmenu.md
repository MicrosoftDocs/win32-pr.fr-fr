---
description: Une application envoie le \_ message WM MDIREFRESHMENU à une fenêtre cliente d’interface multidocument (MDI) pour actualiser le menu fenêtre de la fenêtre frame MDI.
ms.assetid: 6450d84a-a0b9-45d0-9e0c-757d26502059
title: Message WM_MDIREFRESHMENU (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 707059d3cc51703819968f929f9692dbb2422ee3f9fa77e2edb697f12257faf9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118200065"
---
# <a name="wm_mdirefreshmenu-message"></a>\_Message WM MDIREFRESHMENU

Une application envoie le message **WM \_ MDIREFRESHMENU** à une fenêtre cliente d’interface multidocument (MDI) pour actualiser le menu fenêtre de la fenêtre frame MDI.


```C++
#define WM_MDIREFRESHMENU               0x0234
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé et doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **HMENU**

Si le message est correctement exécuté, la valeur de retour est le handle du menu de la fenêtre frame.

Si le message échoue, la valeur de retour est **null**.

## <a name="remarks"></a>Remarques

Après l’envoi de ce message, une application doit appeler la fonction [**DrawMenuBar**](/windows/win32/api/winuser/nf-winuser-drawmenubar) pour mettre à jour la barre de menus.

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

[**\_MDISETMENU WM**](wm-mdisetmenu.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Interface multidocument](multiple-document-interface.md)
</dt> </dl>

 

 
