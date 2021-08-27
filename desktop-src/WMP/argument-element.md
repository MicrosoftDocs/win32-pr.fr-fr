---
title: argument, élément
description: L’élément argument contient une partie d’une chaîne de condition.
ms.assetid: 7e4744ce-e9e2-4a70-a2cc-d33ae1ad2f99
keywords:
- argument, élément Lecteur Windows Media
topic_type:
- apiref
api_name:
- argument Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f5a689b74bd18138361d9377358ddee5cf5979f
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122630190"
---
# <a name="argument-element"></a>argument, élément

L’élément **argument** contient une partie d’une chaîne de condition. Une chaîne de condition comporte généralement une partie condition et une partie valeur. Par exemple, dans la chaîne de condition « artiste est égal à Joe », la partie condition est « égal à » et la partie valeur est « Joe ».

``` syntax
<argument
   name = "string"
>
   string
</argument>
        
```

## <a name="attributes"></a>Attributs

**nom** (obligatoire)

Nom d’une partie de la chaîne de condition.

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                         |
|-----------|----------------------------------|
| Parent    | [échantillon](fragment-element.md) |
| Enfant     | Aucune                             |



 

## <a name="remarks"></a>Remarques

Lorsque l’attribut **Name** d’un élément **fragment** est une caractéristique d’élément multimédia telle que l’artiste de l’album ou le genre, l’élément **fragment** doit contenir deux éléments **argument** : un qui spécifie une condition et un autre qui spécifie une valeur. Le tableau suivant présente deux valeurs possibles pour l’attribut **Name** et la façon dont les éléments **argument** sont utilisés pour spécifier des conditions et des valeurs.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur d'attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Condition</td>
<td>Le contenu de l’élément <strong>argument</strong> est la partie condition d’une chaîne de condition. Par exemple, dans la condition la chaîne &quot; Artist est égale à Jean &quot; , la partie condition est &quot; égale à &quot; . La partie de condition d’une chaîne de condition doit être l’une des suivantes : Equals, n’est pas égal à, contient, ne contient pas, est inférieur à, est supérieur à, est, n’est pas, est antérieur à, est plus récent que, plus récent, en dessous, croissant, décroissant, aléatoire, est au moins égal à.</td>
</tr>
<tr class="even">
<td>Valeur</td>
<td>Le contenu de l’élément <strong>argument</strong> est la partie valeur d’une chaîne de condition. Par exemple, dans la condition chaîne &quot; Artist est égal à Jean &quot; , la partie valeur est &quot; Joe &quot; . Tels<br/>
<pre data-space="preserve"><code><fragment name = &quot;Artist&quot;>
  <argument name = &quot;Condition&quot;>Equals</argument>
  <argument name = &quot;Value&quot;>Joe</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Lorsque l’attribut **Name** d’un élément **fragment** est « limiter la taille totale à » ou « limiter la durée totale à », l’élément **fragment** doit contenir deux éléments **argument** : un qui spécifie un format et un qui spécifie un nombre. Le tableau suivant présente deux valeurs possibles pour l’attribut **Name** et la façon dont les éléments **argument** sont utilisés pour limiter la taille ou la durée d’une sélection.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur d'attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Format</td>
<td>Lorsque l’attribut <strong>Name</strong> de l' <strong>élément fragment</strong> est &quot; limiter la taille totale à &quot; , le contenu de l’élément <strong>argument</strong> doit être l’un des suivants : kilo-octets, mégaoctets ou gigaoctets. lorsque l’attribut <strong>Name</strong> de l’élément <strong>fragment</strong> est limiter la &quot; durée totale à &quot; , le contenu de l’élément <strong>argument</strong> doit être l’un des suivants : secondes, minutes, heures ou jours.<br/></td>
</tr>
<tr class="even">
<td>Number</td>
<td>Le contenu de l’élément <strong>argument</strong> est un nombre qui limite la taille ou la durée de la sélection. Illustre<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Total Size To&quot;>
  <argument name = &quot;Format&quot;>Megabytes</argument>
  <argument name = &quot;Number&quot;>5</argument>
</fragment>

<fragment name = &quot;Limit Total Duration To&quot;>
  <argument name = &quot;Format&quot;>Minutes</argument>
  <argument name = &quot;Number&quot;>20</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

Lorsque l’attribut **Name** d’un élément **fragment** est « Limit Number of items », l’élément **fragment** doit contenir un élément **argument** qui spécifie le nombre d’éléments. Le tableau suivant indique comment utiliser la valeur numérique de l’attribut **Name** .



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Valeur d'attribut</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Number</td>
<td>Le contenu de l’élément <strong>argument</strong> est un nombre qui limite le nombre d’éléments dans une sélection. Tels<br/>
<pre data-space="preserve"><code><fragment name = &quot;Limit Number of Items&quot;>
  <argument name = &quot;Number&quot;>15</argument>
</fragment></code></pre></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|----------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure.<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**fragment, élément**](fragment-element.md)
</dt> <dt>

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





