---
title: Message EM_SETPUNCTUATION (RichEdit. h)
description: Définit les caractères de ponctuation pour un contrôle RichEdit.
ms.assetid: c0c8ad14-63e2-4be8-8fc0-6b8ef9be4522
keywords:
- EM_SETPUNCTUATION les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5e0856c1ee1882695dc5e6d7dfdd6b72ea0f6c4f16ee7396bbfde2b76b49b3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120062899"
---
# <a name="em_setpunctuation-message"></a>\_Message SETPUNCTUATION em

Définit les caractères de ponctuation pour un contrôle RichEdit.

> [!Note]  
> Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0. Elle n’est pas prise en charge dans les versions ultérieures.

 

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le type de ponctuation, qui peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                      | Signification                                      |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**PC \_ leader**</dt> </dl>       | Caractères de ponctuation de début.<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ suivant**</dt> </dl> | Caractères de ponctuation suivants.<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**délimiteur de PC \_**</dt> </dl> | Limite.<br/>                        |
| <span id="PC_OVERFLOW_"></span><span id="pc_overflow_"></span><dl> <dt>**Ordinateur \_ Dépassement de capacité**</dt> </dl> | Non pris en charge.<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**ponctuation**](/windows/desktop/api/Richedit/ns-richedit-punctuation) qui contient les caractères de ponctuation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

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

[**\_GETPUNCTUATION em**](em-getpunctuation.md)
</dt> <dt>

[**PONCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





