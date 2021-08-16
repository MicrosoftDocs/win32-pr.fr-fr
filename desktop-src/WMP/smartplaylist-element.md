---
title: Élément smartPlaylist
description: L’élément smartPlaylist contient la partie définie dynamiquement d’une sélection.
ms.assetid: 05912849-7475-4eb9-a7bd-00f20b80b1cf
keywords:
- élément smartPlaylist Lecteur Windows Media
topic_type:
- apiref
api_name:
- smartPlaylist Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a21d685759e9e8b27c881ceaec6595535b3c4b799eb28ecd94dd96a3a571ec99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763469"
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



 

## <a name="remarks"></a>Remarques

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

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





