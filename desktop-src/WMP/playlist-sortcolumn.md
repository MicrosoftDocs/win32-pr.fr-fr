---
title: PLAYLIST. sortColumn
description: La méthode sortColumn trie les données dans la colonne spécifiée.
ms.assetid: 1563fee8-044a-4cb4-a9c2-11d4533536da
keywords:
- PLAYLIST. sortColumn Lecteur Windows Media
topic_type:
- apiref
api_name:
- PLAYLIST.sortColumn
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f21f0032ee4db4c7af46b5dda814bb11db551330
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520949"
---
# <a name="playlistsortcolumn"></a>PLAYLIST. sortColumn

La méthode **SortColumn** trie les données dans la colonne spécifiée.

``` syntax
        elementID.sortColumn(column)
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*chronique*
</dt> <dd>

**Nombre** (**long**) indiquant l’index de la colonne à trier.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode trie la colonne spécifiée de la même façon que les boutons d’en-tête de colonne dans l’élément **playlist** . Si la colonne n’a pas encore été triée, elle est triée dans l’ordre alphanumérique. S’il a été trié, son ordre est inversé.

Pour que cette méthode fonctionne, l’attribut **allowColumnSorting** doit avoir la valeur true.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





