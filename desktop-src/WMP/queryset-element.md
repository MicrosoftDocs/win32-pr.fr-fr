---
title: Élément querySet
description: L’élément querySet contient des éléments qui définissent les éléments multimédias qui seront sélectionnés dans la bibliothèque.
ms.assetid: 18b5a509-a56b-4fd1-812f-60b8efd5136b
keywords:
- élément querySet Lecteur Windows Media
topic_type:
- apiref
api_name:
- querySet Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb157bb30c2e728b7840fe7021a2a4fcacc317b10eb6778b5702d7d2277c4a92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570612"
---
# <a name="queryset-element"></a>Élément querySet

L’élément **querySet** contient des éléments qui définissent les éléments multimédias qui seront sélectionnés dans la bibliothèque.

``` syntax
<querySet>
</querySet>
```

## <a name="attributes"></a>Attributs

Cet élément n’a pas d’attributs.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                                   |
|-----------|--------------------------------------------|
| Parent    | [smartPlaylist](smartplaylist-element.md) |
| Enfant     | [sourceFilter](sourcefilter-element.md)   |



 

## <a name="remarks"></a>Notes

L’élément **querySet** spécifie les éléments multimédias à sélectionner à partir de la bibliothèque, sans tenir compte de la taille du jeu de résultats. L’élément **Filter** , en revanche, limite la taille du jeu de résultats.

## <a name="examples"></a>Exemples


```
<querySet>
    <sourceFilter 
        type = "smartFilterObject" 
        id = "{4202947A-A563-4B05-A754-A1B4B5989849}"
        name = "Windows Media Local Music Library Filter">
            <fragment name = "Genre">
                <argument name = "Condition">Equals</argument>
                <argument name = "Value">Rock</argument>
            </fragment>
            <fragment name = "Artist">
                <argument name = "Condition">Does Not Equal</argument>
                <argument name = "Value">Brenda Diaz</argument>
            </fragment>
    </sourceFilter>
</querySet>
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**argument, élément**](argument-element.md)
</dt> <dt>

[**Élément Filter**](filter-element.md)
</dt> <dt>

[**fragment, élément**](fragment-element.md)
</dt> <dt>

[**Élément smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Élément sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





