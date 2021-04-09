---
title: Message WM_NEXTMENU (winuser. h)
description: Envoyé à une application lorsque la touche de direction droite ou gauche est utilisée pour basculer entre la barre de menus et le menu système.
ms.assetid: 3fa50fd3-47a6-4dae-9ceb-2abb6626e0a6
keywords:
- WM_NEXTMENU des menus de message et d’autres ressources
topic_type:
- apiref
api_name:
- WM_NEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ecb8efe8c80a3355a30ab0abf28019f87b33963
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942878"
---
# <a name="wm_nextmenu-message"></a>\_Message WM NEXTMENU

Envoyé à une application lorsque la touche de direction droite ou gauche est utilisée pour basculer entre la barre de menus et le menu système.


```C++
#define WM_NEXTMENU                     0x0213
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Code de la clé virtuelle de la clé. Consultez [**codes de clé virtuelle**](/windows/desktop/inputdev/virtual-key-codes).

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) qui contient des informations sur le menu à activer.

</dd> </dl>

## <a name="remarks"></a>Notes

En répondant à ce message, l’application peut spécifier le menu vers lequel basculer dans le membre **hmenuNext** de [**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu) et la fenêtre pour recevoir les messages de notification de menu dans le membre **hwndNext** de la structure **MDINEXTMENU** . Vous devez définir les deux membres pour que les modifications prennent effet (elles ont initialement la **valeur null**).

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

[**MDINEXTMENU**](/windows/win32/api/winuser/ns-winuser-mdinextmenu)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Menus](menus.md)
</dt> </dl>

 

