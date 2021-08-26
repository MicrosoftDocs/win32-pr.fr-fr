---
title: Message EM_SETWORDWRAPMODE (RichEdit. h)
description: Définit les options de retour automatique à la disposition et de césure des mots pour un contrôle RichEdit.
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a0b5c750bb83f4f3fb0c1acfc82b67677c36094df461d10787186177fc891df2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047979"
---
# <a name="em_setwordwrapmode-message"></a>\_Message SETWORDWRAPMODE em

Définit les options de retour automatique à la disposition et de césure des mots pour un contrôle RichEdit.

> [!Note]  
> Ce message est pris en charge uniquement dans les versions asiatiques de Microsoft Rich Edit 1,0. Elle n’est pas prise en charge dans les versions ultérieures.

 

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                         | Signification                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF \_ WORDWRAP**</dt> </dl>    | Active les opérations de retour automatique à la ligne, telles que l’Kinsoku en japonais. <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF \_ WordBreak**</dt> </dl> | Active les opérations de césure en anglais en japonais et en chinois. Active l’opération de césure de mots hangeul.<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**\_dépassement WBF**</dt> </dl>    | Reconnaît la ponctuation de dépassement. (Non pris en charge actuellement.)<br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF \_ niveau1**</dt> </dl>          | Définit la table de ponctuation de niveau 1 comme valeur par défaut.<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF- \_ d’isolement2**</dt> </dl>          | Définit la table de ponctuation de niveau 2 comme valeur par défaut.<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ personnalisé**</dt> </dl>          | Définit la table de ponctuation définie par l’application.<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message retourne les options de retour automatique à la casse et de césure en cours.

## <a name="remarks"></a>Remarques

Ce message ne doit pas être envoyé par la procédure de césure des mots définie par l’application.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



 

 





