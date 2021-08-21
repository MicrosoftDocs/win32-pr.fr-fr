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
ms.openlocfilehash: 34dfce7306ceb39d64665538a21dbaef965ea799141a2756c2fea5bbe23ea9cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335655"
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

## <a name="remarks"></a>Remarques

Cette méthode trie la colonne spécifiée de la même façon que les boutons d’en-tête de colonne dans l’élément **playlist** . Si la colonne n’a pas encore été triée, elle est triée dans l’ordre alphanumérique. S’il a été trié, son ordre est inversé.

Pour que cette méthode fonctionne, l’attribut **allowColumnSorting** doit avoir la valeur true.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------|
| Version<br/> | Lecteur Windows Media version 7,0 ou ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément PLAYLIST**](playlist-element.md)
</dt> <dt>

[**PLAYLIST. allowColumnSorting**](playlist-allowcolumnsorting.md)
</dt> </dl>

 

 





