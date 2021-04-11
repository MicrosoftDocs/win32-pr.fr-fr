---
title: Message EM_SETBIDIOPTIONS (RichEdit. h)
description: Le \_ message em SETBIDIOPTIONS définit l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETBIDIOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84dc4b92f7a989ab5ef283b36708094a143475de
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105592"
---
# <a name="em_setbidioptions-message"></a>\_Message SETBIDIOPTIONS em

Le message **em \_ SETBIDIOPTIONS** définit l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions) qui indique comment définir l’état des options bidirectionnelles dans le contrôle Rich Edit.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le contrôle RichEdit doit être en mode texte brut ou **em \_ SETBIDIOPTIONS** ne fera rien.

Dans les contrôles de texte brut, **em \_ SETBIDIOPTIONS** détermine automatiquement l’orientation et/ou l’alignement des paragraphes en fonction des règles de contexte. Ces règles indique que la direction et/ou l’alignement sont dérivés du premier caractère fort dans le contrôle. Un caractère fort est un caractère à partir duquel la direction du texte peut être déterminée (consultez Unicode standard version 2,0). La direction du paragraphe et/ou l’alignement sont appliqués au format par défaut.

**Em \_ SETBIDIOPTIONS** fait uniquement passer le format de paragraphe par défaut à RTL (de droite à gauche) s’il trouve un caractère RTL,

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**BIDIOPTIONS**](/windows/desktop/api/Richedit/ns-richedit-bidioptions)
</dt> <dt>

[**\_GETBIDIOPTIONS em**](em-getbidioptions.md)
</dt> </dl>

 

 





