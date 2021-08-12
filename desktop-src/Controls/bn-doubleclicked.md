---
title: BN_DOUBLECLICKED le code de notification (winuser. h)
description: Code de notification BN_DOUBLECLICKED-envoyé lorsque l’utilisateur double-clique sur un bouton.
ms.assetid: 2fd7363a-5a02-453c-bfab-df5cbf8e42a5
keywords:
- BN_DOUBLECLICKED les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- BN_DOUBLECLICKED
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ce43cebee93516f929f9a763c14dd51d9d486470eeb93818b9605c3f23a1914
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118674123"
---
# <a name="bn_doubleclicked-notification-code"></a>Code de notification de la \_

Envoyé lorsque l’utilisateur double-clique sur un bouton. Ce code de notification est envoyé automatiquement pour les boutons [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)et [**BS \_ OwnerDraw**](button-styles.md) . Les autres types de boutons envoient un type d' \_ utilisateur avec le style de [**\_ notification BS**](button-styles.md) .

La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DOUBLECLICKED

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

L’erreur de l’un des fautes \_ est le même que le code de notification [ \_ DBLCLK](bn-dblclk.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



 

