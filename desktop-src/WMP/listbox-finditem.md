---
title: LISTBOX. findItem
description: La méthode findItem recherche une chaîne donnée en commençant par l’élément qui suit l’index d’élément spécifié.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX. findItem Lecteur Windows Media
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3625c8d8e9993d09e7b5b41911ead8df857c257a7a2354d71c8d81c1fecc645
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135322"
---
# <a name="listboxfinditem"></a>LISTBOX. findItem

La méthode **FindItem** recherche une chaîne donnée en commençant par l’élément qui suit l’index d’élément spécifié.

``` syntax
        elementID.findItem(startIndex, searchString)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="startIndex"></span><span id="startindex"></span><span id="STARTINDEX"></span>*startIndex*
</dt> <dd>

**Nombre** (**long**) contenant l’index de l’élément à partir duquel commencer la recherche.

</dd> <dt>

<span id="searchString"></span><span id="searchstring"></span><span id="SEARCHSTRING"></span>*searchString*
</dt> <dd>

**Chaîne** contenant le texte à rechercher.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode retourne un **nombre** (**long**) contenant l’index de l’élément qui contient la chaîne.

## <a name="remarks"></a>Remarques

Pour démarrer la recherche à la première ligne du contrôle de zone de liste, utilisez 1 comme *startIndex*. Pour continuer à rechercher du texte après la détection de la première ligne, utilisez l’index de ligne retourné comme *startIndex*, et la recherche commence à la ligne suivante. Cette méthode recherche des sous-chaînes et ne respecte pas la casse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





