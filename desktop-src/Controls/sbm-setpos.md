---
title: Message SBM_SETPOS (winuser. h)
description: Le \_ message SBM SetPos est envoyé pour définir la position de la case de défilement (Thumb) et, le cas échéant, redessine la barre de défilement pour refléter la nouvelle position de la case de défilement.
ms.assetid: 6b3c16ba-1cdf-41ff-8546-ba98477af334
keywords:
- SBM_SETPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SBM_SETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7a7dc99da5f4b3dbb301f15ddd722f1d664932f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117025"
---
# <a name="sbm_setpos-message"></a>\_Message SBM SetPos

Le message **SBM \_ SetPos** est envoyé pour définir la position de la case de défilement (Thumb) et, le cas échéant, redessine la barre de défilement pour refléter la nouvelle position de la case de défilement.

Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**SetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-setscrollpos) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **SetScrollPos** fonctionne correctement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie la nouvelle position de la case de défilement. Elle doit être comprise dans la plage de défilement. Si ce paramètre est en dehors de la plage de défilement, la valeur est arrondie à la valeur la plus proche valide.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie si la barre de défilement doit être redessinée pour refléter la nouvelle position de la case de défilement. Si ce paramètre a la **valeur true**, la barre de défilement est redessinée. Si la **valeur est false**, la barre de défilement n’est pas redessinée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

**ComCtl32.dll version 5,0**: si la position de la case de défilement a changé, la valeur de retour est la position précédente de la case de défilement ; dans le cas contraire, il est égal à zéro.

**ComCtl32.dll version 6,0**: position actuelle de la case de défilement, qu’elle ait été modifiée ou non.

## <a name="remarks"></a>Notes

Si le contrôle de barre de défilement est redessiné par un appel ultérieur à une autre fonction, l’affectation de la **valeur false** au paramètre *lParam* est utile.

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

[**\_GETPOS SBM**](sbm-getpos.md)
</dt> <dt>

[**\_GETRANGE SBM**](sbm-getrange.md)
</dt> <dt>

[**\_DÉtrange SBM**](sbm-setrange.md)
</dt> <dt>

[**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)
</dt> </dl>

 

