---
title: BN_HILITE le code de notification (winuser. h)
description: Envoyé lorsque l’utilisateur sélectionne un bouton.
ms.assetid: f20ba77e-257c-44ec-a2dd-dbf23cd78d07
keywords:
- BN_HILITE les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- BN_HILITE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e864fff01fcce9c7856ab040f66d12e08524c731b43d343a2e878e15e41e801f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119827619"
---
# <a name="bn_hilite-notification-code"></a>\_Code de notification HILITEy

Envoyé lorsque l’utilisateur sélectionne un bouton.

> [!Note]  
> ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0. Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.

 

La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_HILITE

    WPARAM wParam;
    LPARAM lParam;
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) contient l’identificateur de contrôle du bouton. [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) spécifie le code de notification.

</dd> <dt>

*lParam* 
</dt> <dd>

Handle du bouton.

</dd> </dl>

## <a name="remarks"></a>Remarques

L' \_ HiLite de l’erreur est le même que le code de notification [ \_ Push](bn-pushed.md) de la fonction.

## <a name="requirements"></a>Configuration requise



| Condition requise | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

