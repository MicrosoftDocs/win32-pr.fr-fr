---
title: Message EM_FINDTEXTEXW (RichEdit. h)
description: Recherche du texte Unicode dans un contrôle RichEdit.
ms.assetid: 7b90ef06-0395-430e-8b5d-b392481a5f70
keywords:
- EM_FINDTEXTEXW les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXTEXW
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf0857e47c6e98f4be6867ca66baef3472766a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942666"
---
# <a name="em_findtextexw-message"></a>\_Message FINDTEXTEXW em

Recherche du texte Unicode dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifie le comportement de l’opération de recherche. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_**</dt> </dl>                               | Microsoft Rich Edit 2,0 et versions ultérieures : si cette valeur est définie, la recherche est effectuée vers l’avant à partir de **FINDTEXTEX. frais. cpMin**; Si la valeur n’est pas définie, la recherche est vers l’arrière à partir de **FINDTEXTEX. frais. cpMin**. <br/> Édition enrichie de Microsoft 1,0 : l' \_ indicateur fr vers le PG. est ignoré. La recherche est toujours Forward.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**le \_ MATCHALEFHAMZA**</dt> </dl> | Si cette valeur est définie, la recherche fait la distinction entre les alefs avec des accents différents. S’il n’est pas défini, les alefs en arabe et en Hébreu avec des accents différents sont tous mis en correspondance par le caractère Alef. <br/>                                                                                           |
| <span id="FR_MATCHCASE"></span><span id="fr_matchcase"></span><dl> <dt>**FR \_ RespecterCasse**</dt> </dl>                | Si cette valeur est définie, l’opération de recherche respecte la casse. Si la valeur n’est pas définie, l’opération de recherche n’est pas sensible à la casse.<br/>                                                                                                                                                                |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Si cette valeur est définie, l’opération de recherche prend en compte les signes diacritiques. S’il n’est pas défini, les marques diacritiques arabe et hébreu sont ignorées. <br/>                                                                                                                                              |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Si cette valeur est définie, l’opération de recherche prend en compte les signes kachidé. Si ce n’est pas le cas, les signes arabe et hébreu sont ignorés. <br/>                                                                                                                                                                |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée. Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.<br/>                                                                                           |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) contenant des informations sur l’opération de recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance. Si la cible est introuvable, la valeur de retour est-1.

## <a name="remarks"></a>Notes

Utilisez ce message pour rechercher des chaînes Unicode. Pour ANSI ;, utilisez [**em \_ FINDTEXTEX**](em-findtextex.md).

Le membre **cpMin** de **FINDTEXTEX.** frais spécifie toujours le point de départ de la recherche, tandis que **cpMax** spécifie le point de terminaison. Lorsque vous effectuez une recherche vers l’arrière, **cpMin** doit être supérieur ou égal à **cpMax**. Lors d’une recherche vers l’avant, la valeur-1 dans **cpMax** étend la plage de recherche à la fin du texte.

Si l’opération de recherche trouve une correspondance, le membre **chrgText** de la structure [**FINDTEXTEX**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) retourne la plage de positions de caractères qui contient le texte correspondant.

**Em \_ FINDTEXTEXW** utilise la structure [**FINDTEXTEXW**](/windows/desktop/api/Richedit/ns-richedit-findtextexa) , tandis que [**em \_ FINDTEXTW**](em-findtextw.md) utilise la structure [**FINDTEXTW**](/windows/win32/api/richedit/ns-richedit-findtexta) . La différence est que **em \_ FINDTEXTEXW** signale la plage de texte qui a été trouvée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FINDTEXTW em**](em-findtextw.md)
</dt> </dl>

 

 





