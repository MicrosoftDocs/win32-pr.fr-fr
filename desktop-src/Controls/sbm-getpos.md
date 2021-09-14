---
title: Message SBM_GETPOS (winuser. h)
description: Le \_ message SBM GETPOS est envoyé pour récupérer la position actuelle de la case de défilement d’un contrôle de barre de défilement.
ms.assetid: 00344d93-f205-4cda-aa25-6dd065f41b6e
keywords:
- SBM_GETPOS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SBM_GETPOS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d088fc790985e57928f1ab56cd42254b1a087dc
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117037"
---
# <a name="sbm_getpos-message"></a>\_Message SBM GETPOS

Le message **SBM \_ GETPOS** est envoyé pour récupérer la position actuelle de la case de défilement d’un contrôle de barre de défilement. La position actuelle est une valeur relative qui dépend de la plage de défilement actuelle. Par exemple, si la plage de défilement est comprise entre 0 et 100 et que la case de défilement se trouve au milieu de la barre, la position actuelle est 50.

Les applications ne doivent pas envoyer ce message directement. Au lieu de cela, ils doivent utiliser la fonction [**GetScrollPos**](/windows/desktop/api/Winuser/nf-winuser-getscrollpos) . Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Les applications qui implémentent un contrôle de barre de défilement personnalisé doivent répondre à ces messages pour que la fonction **GetScrollPos** fonctionne correctement.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour correspond à la position actuelle de la case de défilement dans la barre de défilement.

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

[**\_GETRANGE SBM**](sbm-getrange.md)
</dt> <dt>

[**\_SetPos SBM**](sbm-setpos.md)
</dt> <dt>

[**\_DÉtrange SBM**](sbm-setrange.md)
</dt> <dt>

[**\_SETRANGEREDRAW SBM**](sbm-setrangeredraw.md)
</dt> </dl>

 

