---
title: Message EM_SETBIDIOPTIONS (RichEdit. h)
description: Le \_ message em SETBIDIOPTIONS définit l’état actuel des options bidirectionnelles dans le contrôle Rich Edit.
ms.assetid: b518e423-317a-4654-9d9f-c501028e2a0a
keywords:
- EM_SETBIDIOPTIONS les contrôles de Windows de message
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
ms.openlocfilehash: f22d03e1738fc688d34f55a6823f7ae95c2dfc41724e827cd31a184ac7cbdfce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119545019"
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

## <a name="remarks"></a>Remarques

Le contrôle RichEdit doit être en mode texte brut ou **em \_ SETBIDIOPTIONS** ne fera rien.

Dans les contrôles de texte brut, **em \_ SETBIDIOPTIONS** détermine automatiquement l’orientation et/ou l’alignement des paragraphes en fonction des règles de contexte. Ces règles indique que la direction et/ou l’alignement sont dérivés du premier caractère fort dans le contrôle. Un caractère fort est un caractère à partir duquel la direction du texte peut être déterminée (consultez Unicode standard version 2,0). La direction du paragraphe et/ou l’alignement sont appliqués au format par défaut.

**Em \_ SETBIDIOPTIONS** fait uniquement passer le format de paragraphe par défaut à RTL (de droite à gauche) s’il trouve un caractère RTL,

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
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

 

 





