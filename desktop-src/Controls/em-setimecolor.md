---
title: Message EM_SETIMECOLOR (RichEdit. h)
description: Définit la couleur de la composition de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit.
ms.assetid: ea5449c9-7d0f-4340-8e3e-1e0b77d443f6
keywords:
- EM_SETIMECOLOR les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETIMECOLOR
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c020bb3af2b1197afc005bd0b6efec82b609b88
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006388"
---
# <a name="em_setimecolor-message"></a>\_Message SETIMECOLOR em

Définit la couleur de la composition de l’éditeur de méthode d’entrée (IME) pour un contrôle RichEdit.

> [!Note]  
> Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0. Elle n’est pas prise en charge dans les versions ultérieures.

 

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor) qui contient la couleur de composition à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_GETIMECOLOR em**](em-getimecolor.md)
</dt> <dt>

[**COMPCOLOR**](/windows/desktop/api/Richedit/ns-richedit-compcolor)
</dt> </dl>

 

 





