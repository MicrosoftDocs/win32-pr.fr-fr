---
title: LISTBOX. insertItem
description: La méthode insertItem insère le texte spécifié à l’index spécifié dans le contrôle de zone de liste.
ms.assetid: c45eb75e-074d-4f3f-bfdd-6c3cbbd71f54
keywords:
- LISTBOX. insertItem Lecteur Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.insertItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0344bbc9fbe4f8f2b680866f70c0fe16398ad08cbf4a916c454223fdff04614e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135302"
---
# <a name="listboxinsertitem"></a>LISTBOX. insertItem

La méthode **InsertItem** insère le texte spécifié à l’index spécifié dans le contrôle de zone de liste.

``` syntax
        elementID.insertItem(index, text)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="index"></span><span id="INDEX"></span>*évaluer*
</dt> <dd>

**Nombre** (**long**) contenant l’index de la ligne à récupérer.

</dd> <dt>

<span id="text"></span><span id="TEXT"></span>*financière*
</dt> <dd>

**Chaîne** contenant le texte à insérer.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lorsqu’une ligne est insérée, les index de ligne des lignes au-dessous de la ligne insérée augmentent d’une unité.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





