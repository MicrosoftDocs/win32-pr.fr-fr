---
title: Message WM_UNINITMENUPOPUP (winuser. h)
description: Envoyé lorsqu’un menu ou sous-menu déroulant a été détruit.
ms.assetid: 06129d88-6cf9-4d55-b8eb-6f78994bc87a
keywords:
- WM_UNINITMENUPOPUP des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_UNINITMENUPOPUP
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7356c0aa4aa62521d2ab998773d07b8aa1a107c92b541c556756a567d31a09a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971788"
---
# <a name="wm_uninitmenupopup-message"></a>\_Message WM UNINITMENUPOPUP

Envoyé lorsqu’un menu ou sous-menu déroulant a été détruit.


```C++
#define WM_UNINITMENUPOPUP              0x0125
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle du menu

</dd> <dt>

*lParam* 
</dt> <dd>

Le mot de poids fort identifie le menu qui a été détruit. Actuellement, ce paramètre peut uniquement être **MF \_ SYSMENU** (menu fenêtre).

</dd> </dl>

## <a name="remarks"></a>Remarques

Si une application reçoit un message [**WM \_ INITMENUPOPUP**](wm-initmenupopup.md) , elle recevra un message **WM \_ UNINITMENUPOPUP** .

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

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

