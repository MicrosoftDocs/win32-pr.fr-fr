---
title: Message EM_FINDTEXTW (RichEdit. h)
description: 'EM_FINDTEXTW message : recherche le texte Unicode dans un contrôle RichEdit.'
ms.assetid: 0c1579f5-3b37-4e28-86a2-f4e03e195f38
keywords:
- EM_FINDTEXTW les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 325ff948c4c8f03e8051248f15928d8e8c56e52f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109797"
---
# <a name="em_findtextw-message"></a>\_Message FINDTEXTW em

Recherche du texte Unicode dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie les paramètres de l’opération de recherche. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_**</dt> </dl>                               | Si cette option est définie, l’opération recherche à partir de la fin de la sélection actuelle jusqu’à la fin du document. Si la valeur n’est pas définie, l’opération recherche à partir de la fin de la sélection actuelle jusqu’au début du document.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**le \_ MATCHALEFHAMZA**</dt> </dl> | Par défaut, les alefs arabe et hébreu avec des accents différents sont tous mis en correspondance par le caractère Alef. Définissez cet indicateur si vous souhaitez que la recherche fasse la distinction entre les alefs et les accents différents.<br/>               |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ RespecterCasse**</dt> </dl>                | Si cette valeur est définie, l’opération de recherche respecte la casse. Si la valeur n’est pas définie, l’opération de recherche n’est pas sensible à la casse.<br/>                                                                                                       |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Par défaut, les marques diacritiques arabe et hébreu sont ignorées. Définissez cet indicateur si vous souhaitez que l’opération de recherche examine les signes diacritiques.<br/>                                                                  |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Par défaut, les kachidés arabe et hébreu sont ignorés. Définissez cet indicateur si vous souhaitez que l’opération de recherche examine les signes kachidé.<br/>                                                                                    |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée. Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.<br/>                                  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) contenant des informations sur l’opération de recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance. Si la cible est introuvable, la valeur de retour est-1.

## <a name="remarks"></a>Notes 

**Em \_ FINDTEXTW** utilise la structure [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) , tandis que [**em \_ FINDTEXTEXW**](em-findtextexw.md) utilise la structure [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) . La différence est que **FINDTEXTEXW** renvoie la plage de texte qui a été trouvée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FINDTEXTEXW em**](em-findtextexw.md)
</dt> </dl>

 

 





