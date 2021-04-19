---
title: LISTBOX. findItem
description: La méthode findItem recherche une chaîne donnée en commençant par l’élément qui suit l’index d’élément spécifié.
ms.assetid: 8d112d99-1866-45e5-b0ef-5d4a3c8b388d
keywords:
- LISTBOX. findItem Windows Media Player
topic_type:
- apiref
api_name:
- LISTBOX.findItem
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 161f4dd8b93fe4fed6a794dffde3e58e840c74e5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530307"
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

## <a name="remarks"></a>Notes

Pour démarrer la recherche à la première ligne du contrôle de zone de liste, utilisez 1 comme *startIndex*. Pour continuer à rechercher du texte après la détection de la première ligne, utilisez l’index de ligne retourné comme *startIndex*, et la recherche commence à la ligne suivante. Cette méthode recherche des sous-chaînes et ne respecte pas la casse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------|
| Version<br/> | Lecteur Windows Media pour Windows XP ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément LISTBOX**](listbox-element.md)
</dt> </dl>

 

 





