---
title: Message EM_FINDTEXTEX (RichEdit. h)
description: EM_FINDTEXTEX message-recherche du texte dans un contrôle RichEdit.
ms.assetid: f1bf925b-2776-40b8-9d05-8484daf8d989
keywords:
- EM_FINDTEXTEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2158dabf9ea17d1bd4cac48454bdbb4056765752
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109837"
---
# <a name="em_findtextex-message"></a>\_Message FINDTEXTEX em

Recherche du texte dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le comportement de l’opération de recherche. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_**</dt> </dl>                               | Microsoft Rich Edit 2,0 et versions ultérieures : si cette valeur est définie, la recherche est effectuée vers l’avant à partir de **FINDTEXTEX. frais. cpMin**; Si la valeur n’est pas définie, la recherche est vers l’arrière à partir de **FINDTEXTEX. frais. cpMin**. <br/> Édition enrichie de Microsoft 1,0 : l' \_ indicateur fr vers le PG. est ignoré. La recherche est toujours Forward.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**le \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3,0 et versions ultérieures : si cette valeur est définie, la recherche fait la distinction entre les alefs arabe et hébreu avec des accents différents. S’il n’est pas défini, tous les alefs sont mis en correspondance par le caractère Alef seul. <br/>                                                                         |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ RespecterCasse**</dt> </dl>                | Si cette valeur est définie, l’opération de recherche respecte la casse. Si la valeur n’est pas définie, l’opération de recherche n’est pas sensible à la casse. <br/>                                                                                                                                                               |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Édition enrichie de Microsoft 3,0 et versions ultérieures : si elle est définie, l’opération de recherche prend en compte les marques diacritiques arabe et hébreu. S’il n’est pas défini, les signes diacritiques sont ignorés. <br/>                                                                                                           |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Édition enrichie de Microsoft 3,0 et versions ultérieures : si elle est définie, l’opération de recherche prend en compte les kachidés arabes et Hébreux. Si la valeur n’est pas définie, les signes kachidé sont ignorés. <br/>                                                                                                                             |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée. Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) contenant des informations sur l’opération de recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance. Si la cible est introuvable, la valeur de retour est-1.

## <a name="remarks"></a>Notes 

Utilisez ce message pour rechercher des chaînes ANSI. Pour Unicode, utilisez [**em \_ FINDTEXTEXW**](em-findtextexw.md).

Le membre **cpMin** de **FINDTEXTEX.** frais spécifie toujours le point de départ de la recherche, tandis que **cpMax** spécifie le point de terminaison. Lorsque vous effectuez une recherche vers l’arrière, **cpMin** doit être supérieur ou égal à **cpMax**. Lors d’une recherche vers l’avant, la valeur-1 dans **cpMax** étend la plage de recherche à la fin du texte.

Si l’opération de recherche trouve une correspondance, le membre **chrgText** de la structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retourne la plage de positions de caractères qui contient le texte correspondant.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TEXTECHERCHÉ em**](em-findtext.md)
</dt> </dl>

 

 





