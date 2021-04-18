---
title: Message EM_SETPARAFORMAT (RichEdit. h)
description: Définit la mise en forme de paragraphe pour la sélection actuelle dans un contrôle RichEdit.
ms.assetid: 2d612e1b-1489-4055-929b-e0b2719f6ec2
keywords:
- EM_SETPARAFORMAT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETPARAFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8780ed79650a90a8d85ee8025dbe97e9af36aa1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465055"
---
# <a name="em_setparaformat-message"></a>\_Message SETPARAFORMAT em

Définit la mise en forme de paragraphe pour la sélection actuelle dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) spécifiant les nouveaux attributs de mise en forme de paragraphe. Seuls les attributs spécifiés par le membre **dwMask** sont modifiés.

Microsoft Rich Edit 2,0 et versions ultérieures : ce paramètre peut être un pointeur vers une structure [**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2) , qui est une extension de la structure [**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat) . Avant d’envoyer le message **\_ SETPARAFORMAT em** , définissez le membre **cbSize** de la structure pour indiquer la version de la structure.

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

[**PARAFORMAT**](/windows/desktop/api/Richedit/ns-richedit-paraformat)
</dt> <dt>

[**PARAFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-paraformat2)
</dt> </dl>

 

 





