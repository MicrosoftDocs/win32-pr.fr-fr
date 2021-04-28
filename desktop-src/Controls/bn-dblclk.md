---
title: BN_DBLCLK le code de notification (winuser. h)
description: Code de notification BN_DBLCLK-envoyé lorsque l’utilisateur double-clique sur un bouton.
ms.assetid: 60cc033f-8b84-4aa5-b625-fdee9deb4757
keywords:
- Contrôles Windows de code de notification BN_DBLCLK
topic_type:
- apiref
api_name:
- BN_DBLCLK
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fdb403f37b8fee9ea36023a7cd2511bbaaa2af81
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096847"
---
# <a name="bn_dblclk-notification-code"></a>\_Code de notification DBLCLKy

Envoyé lorsque l’utilisateur double-clique sur un bouton. Ce code de notification est envoyé automatiquement pour les boutons [**BS \_ UserButton**](button-styles.md), [**BS \_ RadioButton**](button-styles.md)et [**BS \_ OwnerDraw**](button-styles.md) . Les autres types de bouton envoient \_ l’DBLCLK de l’adresse de l’utilisateur uniquement s’ils ont le style [**BS \_ Notify**](button-styles.md) .

La fenêtre parente du bouton reçoit ce code de notification via le message de [**\_ commande WM**](/windows/desktop/menurc/wm-command) .


```C++
BN_DBLCLK

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

L' \_ DBLCLK [de la \_ ](bn-doubleclicked.md) fonction est le même que le code de notification par erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[sur lequel l' \_ utilisateur a cliqué](bn-clicked.md)
</dt> <dt>

[Par le biais du double \_](bn-doubleclicked.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**WM, \_ commande**](/windows/desktop/menurc/wm-command)
</dt> </dl>

 

