---
title: BN_PUSHED le code de notification (winuser. h)
description: Envoyé lorsque l’état de transmission d’un bouton est défini sur Push.
ms.assetid: 34000def-189c-4a37-bcef-4ca09a67df00
keywords:
- BN_PUSHED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- BN_PUSHED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d18a27599c770eb55d889a21956312512ca804cc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006521"
---
# <a name="bn_pushed-notification-code"></a>\_Code de notification push de la pousse

Envoyé lorsque l’état de transmission d’un bouton est défini sur Push.

> [!Note]  
> ce code de notification est fourni uniquement pour la compatibilité avec les versions 16 bits de Windows antérieures à la version 3,0. Les applications doivent utiliser le style de bouton [**BS \_ OwnerDraw**](button-styles.md) et la structure [**drawitemstruct,**](/windows/win32/api/winuser/ns-winuser-drawitemstruct) pour cette tâche.

 

La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_PUSHED

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

## <a name="remarks"></a>Notes

L’envoi d' \_ un push est le même que le code de notification [ \_ HiLite](bn-hilite.md) .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**aucune \_ transmission de type push**](bn-unpushed.md)
</dt> </dl>

 

