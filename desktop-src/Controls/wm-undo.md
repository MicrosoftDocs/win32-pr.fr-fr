---
title: Message WM_UNDO (winuser. h)
description: Une application envoie un \_ message WM Undo à un contrôle d’édition pour annuler la dernière opération. Lorsque ce message est envoyé à un contrôle d’édition, le texte supprimé précédemment est restauré ou le texte ajouté précédemment est supprimé.
ms.assetid: bb5a3425-bf99-4a08-8747-82c24c5889ad
keywords:
- WM_UNDO les contrôles de Windows de message
topic_type:
- apiref
api_name:
- WM_UNDO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b6e4bd0715b7eeb5f99f34f5142ac3198c5c1eae53cf4486c3efce9dace19a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119311339"
---
# <a name="wm_undo-message"></a>\_Message d’annulation WM

Une application envoie un message **WM \_ Undo** à un contrôle d’édition pour annuler la dernière opération. Lorsque ce message est envoyé à un contrôle d’édition, le texte supprimé précédemment est restauré ou le texte ajouté précédemment est supprimé.

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

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est **true**.

Si le message échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Remarques

**Modification riche :** Il est recommandé d’utiliser l' [**\_ annulation em**](em-undo.md) à la place de l' **\_ annulation de WM**.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Autres ressources**
</dt> <dt>

[**WM- \_ Clear**](/windows/desktop/dataxchg/wm-clear)
</dt> <dt>

[**\_copie WM**](/windows/desktop/dataxchg/wm-copy)
</dt> <dt>

[**découpe WM \_**](/windows/desktop/dataxchg/wm-cut)
</dt> <dt>

[**\_coller WM**](/windows/desktop/dataxchg/wm-paste)
</dt> </dl>

 

