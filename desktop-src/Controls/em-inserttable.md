---
title: Message EM_INSERTTABLE (RichEdit. h)
description: Insère une ou plusieurs lignes de table identiques avec des cellules vides.
ms.assetid: 7F9B2F28-1035-44AA-9DF6-57BC62886A4E
keywords:
- EM_INSERTTABLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_INSERTTABLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea5de278df98e412f219d246164221cfea75255
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464534"
---
# <a name="em_inserttable-message"></a>\_Message INSERTTABLE em

Insère une ou plusieurs lignes de table identiques avec des cellules vides.


```C++
#define EM_INSERTTABLE       (WM_USER + 232)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Pointeur vers une structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) .

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne S \_ OK si la table est insérée ou un code d’erreur dans le cas contraire.

## <a name="remarks"></a>Notes

Si le membre **cpStartRow** du [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) est 1, ce message supprime le texte sélectionné (le cas échéant), puis insère les lignes de table vides avec les paramètres de ligne et de cellule donnés par *wParam* et *lParam*. Elle laisse la sélection pointant vers le début de la première cellule de la première ligne. Le client peut ensuite remplir les cellules de la table en pointant la sélection (ou un [**ITextRange**](/windows/desktop/api/Tom/nn-tom-itextrange)) sur les différentes marques de fin de cellule et en insérant et en mettant en forme le texte souhaité. Ce type de texte peut inclure des lignes de table imbriquée. Sinon, si le membre **cpStartRow** du **TABLEROWPARMS** est supérieur ou égal à 0, les lignes de la table sont insérées à la position de caractère donnée par **cpStartRow**. Cela modifie uniquement la sélection actuelle si la table est insérée à l’intérieur du texte sélectionné.

Une table RichEdit Microsoft se compose d’une séquence de lignes de table qui, à leur tour, est composée de séquences de paragraphes. Une ligne de table commence par le point de délimiteur de deux caractères spécial U + FFF9 U + 000D et se termine par le point d’arrêt à deux caractères U + FFFB U + 000D. Chaque cellule se termine par la marque de cellule U + 0007, qui est traitée comme une marque de fin de paragraphe dure exactement comme U + 000D (CR) est. Les paramètres de ligne de table et de cellule sont traités comme une mise en forme spéciale des paragraphes des séparateurs de lignes de table. La mise en forme contient les informations dans la structure [**TABLEROWPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablerowparms) . Les paramètres de cellule fournis par la structure [**TABLECELLPARMS**](/windows/desktop/api/Richedit/ns-richedit-tablecellparms) sont stockés dans une version développée du tableau Tabs. Ce format permet d’imbriquer des tables dans d’autres tables, jusqu’à quinze niveaux de profondeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_INSERTIMAGE em**](em-insertimage.md)
</dt> </dl>

 

 





