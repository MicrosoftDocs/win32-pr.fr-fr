---
title: Message EM_GETPARAFORMAT (RichEdit. h)
description: Récupère la mise en forme de paragraphe de la sélection actuelle dans un contrôle RichEdit.
ms.assetid: 79a7d34f-5da1-452d-b31f-b2eec913f5cb
keywords:
- EM_GETPARAFORMAT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda99d1fefc0e2a13cc989726c86588103b7f94d7042b98393709cf4a2cd5f29
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048849"
---
# <a name="em_getparaformat-message"></a>\_Message GETPARAFORMAT em

Récupère la mise en forme de paragraphe de la sélection actuelle dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) qui reçoit les attributs de mise en forme de paragraphe de la sélection actuelle.

Si plusieurs paragraphes sont sélectionnés, la structure reçoit les attributs du premier paragraphe et le membre **dwMask** spécifie les attributs qui sont cohérents dans toute la sélection.

Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , qui est une extension de la structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) . Avant d’envoyer le message **\_ GETPARAFORMAT em** , définissez le membre **cbSize** de la structure pour indiquer la version de la structure.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne la valeur du membre **dwMask** de la structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) .

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





