---
title: Message WM_INITMENUPOPUP (winuser. h)
description: WM_INITMENUPOPUP message-envoyé quand un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.
ms.assetid: 08ae1a78-5e68-488c-9b77-ee42044ca3ab
keywords:
- WM_INITMENUPOPUP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_INITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ba23607dcb8da7fb282e380e87fe6a2cbb9a26a50850845a5877d036983665f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117869598"
---
# <a name="wm_initmenupopup-message"></a>\_Message WM INITMENUPOPUP

Envoyé lorsqu’un menu déroulant ou un sous-menu est sur le paragraphe actif. Cela permet à une application de modifier le menu avant qu’il ne soit affiché, sans modifier le menu entier.


```C++
#define WM_INITMENUPOPUP                0x0117
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers le menu ou le sous-menu déroulant.

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids faible spécifie la position relative de base zéro de l’élément de menu qui ouvre le menu déroulant ou le sous-menu.

Le mot de poids fort indique si le menu déroulant est le menu fenêtre. Si le menu est le menu fenêtre, ce paramètre a la **valeur true**; Sinon, la **valeur est false**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si une application traite ce message, elle doit retourner la valeur zéro.

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

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

[**\_INITMENU WM**](wm-initmenu.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Raccourcis clavier](keyboard-accelerators.md)
</dt> </dl>

 

