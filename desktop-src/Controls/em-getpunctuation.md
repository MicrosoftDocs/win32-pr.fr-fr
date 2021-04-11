---
title: Message EM_GETPUNCTUATION (RichEdit. h)
description: Obtient les caractères de ponctuation actuels pour le contrôle RichEdit.
ms.assetid: 1c04967b-d75e-4f54-b35b-cd50bac9cdfa
keywords:
- EM_GETPUNCTUATION les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETPUNCTUATION
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 158c26deca3328d9cdbed7ffe7cf885b0582d1a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105298"
---
# <a name="em_getpunctuation-message"></a>\_Message GETPUNCTUATION em

Obtient les caractères de ponctuation actuels pour le contrôle RichEdit.

> [!Note]  
> Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0. Elle n’est pas prise en charge dans les versions ultérieures de la modification enrichie.

 

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le type de ponctuation peut être l’une des valeurs suivantes.



| Valeur                                                                                                                                                      | Signification                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PC_LEADING"></span><span id="pc_leading"></span><dl> <dt>**PC \_ leader**</dt> </dl>       | Caractères de ponctuation de début<br/>   |
| <span id="PC_FOLLOWING"></span><span id="pc_following"></span><dl> <dt>**PC \_ suivant**</dt> </dl> | Caractères de ponctuation suivants<br/> |
| <span id="PC_DELIMITER"></span><span id="pc_delimiter"></span><dl> <dt>**délimiteur de PC \_**</dt> </dl> | Délimiteur<br/>                        |
| <span id="PC_OVERFLOW"></span><span id="pc_overflow"></span><dl> <dt>**dépassement du PC \_**</dt> </dl>    | Non pris en charge<br/>                    |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**ponctuation**](/windows/desktop/api/Richedit/ns-richedit-punctuation) qui reçoit les caractères de ponctuation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est une valeur différente de zéro.

Si l’opération échoue, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETPUNCTUATION em**](em-setpunctuation.md)
</dt> <dt>

[**PONCTUATION**](/windows/desktop/api/Richedit/ns-richedit-punctuation)
</dt> </dl>

 

 





