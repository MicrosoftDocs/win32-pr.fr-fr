---
title: Message EM_SETWORDBREAKPROCEX (RichEdit. h)
description: Définit la procédure de saut de mot étendu pour un contrôle RichEdit.
ms.assetid: 2b45f747-ae15-470b-a786-98d8135289da
keywords:
- EM_SETWORDBREAKPROCEX les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETWORDBREAKPROCEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecc56e147c52d89b929a4e7065d4daafc184406247d60d522ef2bf4317097faf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062839"
---
# <a name="em_setwordbreakprocex-message"></a>\_Message SETWORDBREAKPROCEX em

Définit la procédure de saut de mot étendu pour un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une fonction [*EditWordBreakProcEx*](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex) , ou **null** pour utiliser la procédure par défaut.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne l’adresse de la précédente procédure de coupure de mots étendue.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**EditWordBreakProcEx**](/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex)
</dt> <dt>

[**\_GETWORDBREAKPROCEX em**](em-getwordbreakprocex.md)
</dt> </dl>

 

 





