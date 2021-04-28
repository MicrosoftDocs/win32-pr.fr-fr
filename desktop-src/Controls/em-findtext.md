---
title: Message EM_FINDTEXT (RichEdit. h)
description: EM_FINDTEXT message-recherche du texte dans un contrôle RichEdit.
ms.assetid: f19e19a0-d8dd-4d31-b76d-f1f09577dd2d
keywords:
- EM_FINDTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_FINDTEXT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 452d4e2534fb05cbbbf4c02ac4146f2f8914c9bb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109847"
---
# <a name="em_findtext-message"></a>\_Message du TEXTECHERCHÉ em

Recherche du texte dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Spécifiez les paramètres de l’opération de recherche. Ce paramètre peut être une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                                     | Signification                                                                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FR_DOWN"></span><span id="fr_down"></span><dl> <dt>**FR \_**</dt> </dl>                               | Microsoft Rich Edit 2,0 et versions ultérieures : si cette option est définie, la recherche se fait à partir de la fin de la sélection actuelle jusqu’à la fin du document. S’il n’est pas défini, la recherche commence à la fin de la sélection actuelle jusqu’au début du document. <br/> Édition enrichie de Microsoft 1,0 : l' \_ indicateur fr vers le PG. est ignoré. La recherche est toujours à la fin de la sélection actuelle jusqu’à la fin du document.<br/> |
| <span id="FR_MATCHALEFHAMZA"></span><span id="fr_matchalefhamza"></span><dl> <dt>**le \_ MATCHALEFHAMZA**</dt> </dl> | Microsoft Rich Edit 3,0 et versions ultérieures : si cette valeur est définie, la recherche fait la distinction entre les alefs arabes avec des accents différents. S’il n’est pas défini, tous les alefs sont mis en correspondance par le caractère Alef seul. <br/>                                                                                                                                                                                                      |
| <span id="FR_MATCHDIAC"></span><span id="fr_matchdiac"></span><dl> <dt>**\_MATCHDIAC fr**</dt> </dl>                | Édition enrichie de Microsoft 3,0 et versions ultérieures : si elle est définie, l’opération de recherche prend en compte les marques diacritiques arabe et hébreu. S’il n’est pas défini, les signes diacritiques sont ignorés. <br/>                                                                                                                                                                                                                             |
| <span id="FR_MATCHKASHIDA"></span><span id="fr_matchkashida"></span><dl> <dt>**FR \_ MATCHKASHIDA**</dt> </dl>       | Rich Edit 3,0 et versions ultérieures de Microsoft : si cette valeur est définie, l’opération de recherche prend en compte les kachidés arabes. Si la valeur n’est pas définie, les signes kachidé sont ignorés. <br/>                                                                                                                                                                                                                                                          |
| <span id="FR_MATCHWIDTH"></span><span id="fr_matchwidth"></span><dl> <dt>**\_MATCHWIDTH fr**</dt> </dl>             | Windows 8 : si cette valeur est définie, les versions sur un octet et sur deux octets du même caractère sont considérées comme différentes.<br/>                                                                                                                                                                                                                                                                          |
| <span id="FR_WHOLEWORD"></span><span id="fr_wholeword"></span><dl> <dt>**\_WHOLEWORD fr**</dt> </dl>                | Si elle est définie, l’opération recherche uniquement les mots entiers qui correspondent à la chaîne recherchée. Si la valeur n’est pas définie, l’opération recherche également des fragments de mot qui correspondent à la chaîne recherchée.<br/>                                                                                                                                                                                                             |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Structure [**TexteCherché**](/windows/win32/api/richedit/ns-richedit-findtexta) contenant des informations sur l’opération de recherche.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Si la chaîne cible est trouvée, la valeur de retour est la position de base zéro du premier caractère de la correspondance. Si la cible est introuvable, la valeur de retour est-1.

## <a name="remarks"></a>Notes 

Le membre **cpMin** de **FINDTEXT.** frais spécifie toujours le point de départ de la recherche, tandis que **cpMax** spécifie le point de terminaison. Lorsque vous effectuez une recherche vers l’arrière, **cpMin** doit être supérieur ou égal à **cpMax**. Lors d’une recherche vers l’avant, la valeur-1 dans **cpMax** étend la plage de recherche à la fin du texte.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**FINDTEXT**](/windows/win32/api/richedit/ns-richedit-findtexta)
</dt> </dl>

 

 





