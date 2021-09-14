---
title: Élément Filter
description: L’élément Filter contient des éléments qui limitent la taille d’une sélection, la durée d’une sélection ou le nombre d’éléments multimédias dans une sélection.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- élément de filtre Lecteur Windows Media
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127192264"
---
# <a name="filter-element"></a>Élément Filter

L’élément **Filter** contient des éléments qui limitent la taille d’une sélection, la durée d’une sélection ou le nombre d’éléments multimédias dans une sélection.

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**entrer**
</dt> <dd>

Type de l’objet Filter. Il n’existe pas de valeurs prédéfinies pour cet attribut.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (obligatoire) 
</dt> <dd>

GUID qui identifie de façon unique un objet filtre. Les méthodes de l’objet de filtre sont appelées pour interpréter les éléments de **fragment** contenus dans l’élément de **filtre** .



| Valeur                                  | Description                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | ID du filtre « filtre de sélection automatique Microsoft--limite les sélections automatiques par nombre, taille ou durée ». |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nom** (obligatoire) 
</dt> <dd>

Nom de l’objet de filtre.



| Valeur                                                                              | Description                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filtre de sélection automatique Microsoft--limite les sélections automatiques par nombre, taille ou durée | Limite les sélections automatiques par nombre, taille ou durée. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                                   |
|-----------|--------------------------------------------|
| Parent    | [smartPlaylist](smartplaylist-element.md) |
| Enfant     | [échantillon](fragment-element.md)           |



 

## <a name="remarks"></a>Notes

L’élément **Filter** n’ajoute pas d’éléments multimédias à une sélection ; Il supprime simplement ou filtre le contenu qui a été sélectionné par l’élément **sourceFilter** .

## <a name="examples"></a>Exemples


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**argument, élément**](argument-element.md)
</dt> <dt>

[**fragment, élément**](fragment-element.md)
</dt> <dt>

[**Élément smartPlaylist**](smartplaylist-element.md)
</dt> <dt>

[**Élément sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





