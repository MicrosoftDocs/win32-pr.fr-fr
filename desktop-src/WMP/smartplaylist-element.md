---
title: Élément smartPlaylist
description: L’élément smartPlaylist contient la partie définie dynamiquement d’une sélection.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- Élément smartPlaylist lecteur Windows Media
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 511294af2de4343cb7f63db4312d530aadf57da6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106544111"
---
# <a name="smartplaylist-element"></a>Élément smartPlaylist

L’élément **smartPlaylist** contient la partie définie dynamiquement d’une sélection.

``` syntax
<smartPlaylist
    version = "number"
>
</smartPlaylist>
```

## <a name="attributes"></a>Attributs



| Terme                                                                                                                                   | Description                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span id="version__required______________"></span><span id="VERSION__REQUIRED______________"></span>**version** (obligatoire) <br/> | Nombre décimal représentant le numéro de version du schéma de la sélection intelligente. Défini sur 1.0.0.0.<br/> |



 

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                                                       |
|-----------|----------------------------------------------------------------|
| Parent    | [séquentiel](seq-element.md)                                         |
| Enfant     | [querySet](queryset-element.md), [filtre](filter-element.md) |



 

## <a name="remarks"></a>Notes

Un élément **smartPlaylist** contient généralement un élément **querySet** et peut également contenir un élément **Filter** .

## <a name="examples"></a>Exemples


```
<smartPlaylist version = "1.0.0.0">
    <querySet>
        <sourceFilter 
            type = "smartFilterObject"
            id = "12345678-1234-3333-abCD-123ABCdefGHI"
            name = "Music in my library">
                <fragment name = "Genre">
                    <argument name = "condition">Is</argument>
                    <argument name = "value">Rock</argument>
                </fragment>
                <fragment name = "Album Artist">
                    <argument name = "condition">Is Not</argument>
                    <argument name = "value">Brenda Diaz</argument>
                </fragment>
        </sourceFilter>
    </querySet>
    <filter>
    </filter>
</smartPlaylist>
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

[**Élément querySet**](queryset-element.md)
</dt> <dt>

[**Seq, élément**](seq-element.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





