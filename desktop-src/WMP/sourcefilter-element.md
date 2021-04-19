---
title: Élément sourceFilter
description: L’élément sourceFilter contient des éléments qui sélectionnent des éléments dans une bibliothèque.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Élément sourceFilter lecteur Windows Media
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525606"
---
# <a name="sourcefilter-element"></a>Élément sourceFilter

L’élément **sourceFilter** contient des éléments qui sélectionnent des éléments dans une bibliothèque.

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**entrer**
</dt> <dd>

Type de l’objet Filter. Il n’existe pas de valeurs prédéfinies pour cet attribut.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatoire) 
</dt> <dd>

GUID qui identifie de façon unique l’objet de filtre source. Les méthodes de l’objet de filtre source sont appelées pour interpréter les éléments de **fragment** contenus dans l’élément **sourceFilter** .



| Valeur                                  | Description                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | GUID du filtre source « musique dans ma bibliothèque ».    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | GUID du filtre source « vidéo dans ma bibliothèque ».    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | GUID du filtre source « images dans ma bibliothèque ». |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | GUID du filtre source « émissions TV dans ma bibliothèque ». |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nom** (obligatoire) 
</dt> <dd>

Nom de l’objet de filtre.



| Valeur                  | Description                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Musique dans ma bibliothèque    | Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments musicaux dans la bibliothèque de l’utilisateur. |
| Vidéo dans ma bibliothèque    | Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments vidéo dans la bibliothèque de l’utilisateur. |
| Images dans ma bibliothèque | Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments de photo dans la bibliothèque de l’utilisateur. |
| Émissions TV dans ma bibliothèque | Objet de filtre qui sélectionne des éléments spécifiés à partir de l’ensemble d’éléments TV dans la bibliothèque de l’utilisateur.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                         |
|-----------|----------------------------------|
| Parent    | [querySet](queryset-element.md) |
| Enfant     | [échantillon](fragment-element.md) |



 

## <a name="remarks"></a>Notes

L’élément **sourceFilter** sélectionne des éléments de la bibliothèque sans tenir compte de la taille du jeu de résultats. L’élément **Filter** , en revanche, limite la taille du jeu de résultats.

## <a name="examples"></a>Exemples


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
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
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Élément Filter**](filter-element.md)
</dt> <dt>

[**fragment, élément**](fragment-element.md)
</dt> <dt>

[**Élément querySet**](queryset-element.md)
</dt> <dt>

[**Informations de référence sur les éléments de sélection Windows Media**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





