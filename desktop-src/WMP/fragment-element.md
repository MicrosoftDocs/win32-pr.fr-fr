---
title: fragment, élément
description: L’élément fragment spécifie une condition de la requête qui sélectionne des éléments de la bibliothèque. Les conditions sont spécifiées par les chaînes de condition. Une chaîne de condition a généralement une partie nom, une partie condition et une partie valeur.
ms.assetid: 1575318f-8527-42ba-9c2f-9993a60987d7
keywords:
- fragment, élément Lecteur Windows Media
topic_type:
- apiref
api_name:
- fragment Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: da4cd18c6286cf2439e310b4e797f6978f3b2395
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127122709"
---
# <a name="fragment-element"></a>fragment, élément

L’élément **fragment** spécifie une condition de la requête qui sélectionne des éléments de la bibliothèque. Les conditions sont spécifiées par les chaînes de condition. Une chaîne de condition a généralement une partie nom, une partie condition et une partie valeur.

``` syntax
<fragment
    name = "string"
>
</fragment>
```

## <a name="attributes"></a>Attributs

<dl> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**nom** (obligatoire) 
</dt> <dd>

Partie d’une chaîne de condition. Consultez la section Notes.

</dd> </dl>

## <a name="parentchild-elements"></a>Éléments parent/enfant



| Hierarchy | Éléments                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [filtre](filter-element.md), [sourceFilter](sourcefilter-element.md) |
| Enfant     | [argument](argument-element.md)                                       |



 

## <a name="remarks"></a>Notes

Certaines chaînes de condition ont une partie des attributs de métadonnées, une partie de condition et une partie valeur. Par exemple, dans la chaîne de condition « l’artiste de l’album est Joe », la partie de l’attribut Metadata est « Artist Artist », la partie condition est « is » et la partie valeur est « Joe ».

Exemple :


```XML
<fragment name = "Album Artist">
    <argument name = "condition">Is</argument>
    <argument name = "value">Joe</argument>
</fragment>
```



Pour les chaînes de condition de ce type, le tableau suivant indique les attributs de métadonnées possibles, les conditions possibles et les valeurs possibles :



| Attribut de métadonnées                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             | Conditions possibles                                                                                             | Valeurs possibles                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Artiste ActorAlbum<br/> Titre de l’album<br/> Auteur<br/> Caption<br/> Canal<br/> Composer<br/> Conducteur<br/> Fournisseur de contenu<br/> Genre du fournisseur de contenu<br/> Artiste contributeur<br/> Texte de Copyright<br/> Directeur<br/> Épisode<br/> Type de fichier<br/> Genre<br/> Clé<br/> Mots clés<br/> Langage<br/> Humeur<br/> Classification parentale<br/> Période<br/> Producer<br/> Fournisseur<br/> Publisher<br/> Série<br/> nom de la station<br/> Sous-genre<br/> Sous-titre<br/> Intitulé<br/> Writer<br/> | EqualsDoes non égal<br/> Est<br/> N’est pas<br/> Contient<br/> Ne contient pas<br/> | Valeur de chaîne quelconque                                                                                                                                                                                                                                                                                                  |
| Vitesse de transmission (en kilo-octets par seconde).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            | EqualsDoes non égal<br/> Est<br/> N’est pas<br/> Contient<br/> Ne contient pas<br/> | 4864<br/> 96<br/> 128<br/> 160<br/> 192<br/> 256<br/> 300<br/> 500<br/> 750<br/> 1 000<br/> 1500<br/> 3000<br/> 4500<br/> 6000<br/> 7500<br/>                                                                            |
| Type de support secondaire                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           | EqualsDoes non égal<br/> Est<br/> N’est pas<br/> Contient<br/> Ne contient pas<br/> | Audio : NewsAudio : parler Show<br/> Audio : livres audio<br/> Audio : mot parlé audio<br/> Vidéo : Actualités<br/> Vidéo : parler Show<br/> Vidéo : vidéo de démarrage<br/> Vidéo : film/film<br/> Vidéo : émission TV<br/> Vidéo : vidéo d’entreprise<br/> vidéo : Musique vidéo<br/> |
| Taille du fichier (en Ko) hauteur de l’image<br/> Largeur de l’image<br/> Nombre de jeux : totaux de l’après-midi<br/> Nombre de jeux : total des soirs<br/> Nombre de jeux : total des matins<br/> Nombre de jeux : totaux de nuit<br/> Nombre de jeux : total global<br/> Nombre de lectures : jour de la semaine total<br/> Nombre de jeux : week-end total<br/>                                                                                                                                                                                                                                                                                                                  | Est inférieur à, est supérieur à<br/> Est<br/> N’est pas<br/>                                          | Nombre quelconque                                                                                                                                                                                                                                                                                                        |
| Expiration de la diffusion encodée<br/> Date d’enregistrement<br/> Date de prise<br/> Année de sortie<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Est avant<br/> Est<br/> N’est pas<br/>                                                    | YesterdayLast semaine<br/> Le mois dernier<br/> 6 mois<br/> 1 an<br/> 2 ans<br/> 5 ans<br/> 2000s<br/> années 1990<br/> années<br/> 1970<br/> 1960<br/> 1950s<br/> 1940s<br/>                                                            |
| Date Added                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Est avant<br/> Est<br/> N’est pas<br/>                                                    | YesterdayLast semaine<br/> Le mois dernier<br/> 6 mois<br/> 1 an<br/> 2 ans<br/> 5 ans<br/>                                                                                                                                                                                   |
| Date de la dernière lecture                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               | ThanMore plus ancien que<br/> Est<br/> N’est pas<br/>                                           | YesterdayLast semaine<br/> Le mois dernier<br/> 6 mois<br/> 1 an<br/> 2 ans<br/> 5 ans<br/>                                                                                                                                                                                   |
| Mois pris                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Est antérieur à plus récent que<br/> Est<br/> N’est pas<br/>                                         | 12<br/> 3<br/> 4<br/> 5<br/> 6<br/> 7<br/> 8<br/> 9<br/> 10<br/> 11<br/> 12<br/> 13<br/>                                                                                                                                                  |
| Année de prise                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Est antérieur à plus récent que<br/> Est<br/> N’est pas<br/>                                         | Toute année                                                                                                                                                                                                                                                                                                          |
| Évaluation automatique de RatingMy<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                | Est supérieur ou égal à<br/> Est<br/> N’est pas<br/>                                           | Étoile Unrated1<br/> 2 étoiles<br/> 3 étoiles<br/> 4 étoiles<br/> 5 étoiles<br/>                                                                                                                                                                                                              |
| Champ \# 1Custom champ personnalisé \# 2<br/> Nom de fichier<br/> Champs clés<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | ContainsDoes ne contient pas<br/>                                                                             | Toute chaîne                                                                                                                                                                                                                                                                                                        |



 

Certaines chaînes de condition ont une partie limite, une partie nombre et une partie format. Par exemple, dans la chaîne de condition « limiter la taille totale à 3 mégaoctets », la partie de limite est « limiter la taille totale à », la partie du nombre est « 3 » et la partie du format est « mégaoctets ».

Exemple :


```XML
<fragment name = "Limit Total Size To">
  <argument name = "number">3</argument>
  <argument name = "format">Megabytes</argument>
</fragment>
```



Pour les chaînes de condition de ce type, le tableau suivant répertorie les limites et les formats possibles.



| Limiteur                 | Nombres possibles | Formats possibles                |
|-------------------------|------------------|---------------------------------|
| Limiter la taille totale à     | Nombre quelconque       | Kilo-octets, mégaoctets, gigaoctets |
| Limiter la durée totale à | Nombre quelconque       | Secondes, minutes, heures, jours   |



 

Certaines chaînes de condition comportent une partie limite et une partie nombre. Par exemple, dans la chaîne de condition « limiter le nombre d’éléments à 25 », la partie de limite est « limiter le nombre d’éléments » et la partie du nombre est « 25 ».

Exemple :


```XML
<fragment name = "Limit Number of Items">
    <argument name = "number">25</argument>
</fragment>
```



Pour les chaînes de condition de ce type, le tableau suivant affiche le seul limiteur possible.



| Limiteur               | Nombres possibles |
|-----------------------|------------------|
| Limiter le nombre d’éléments | Nombre quelconque       |



 

Certaines chaînes de condition comportent une partie protection et une partie condition. Par exemple, dans la chaîne de condition « protection présente », la partie protection est « protection » et la partie condition est « est ».

Exemple :


```XML
<fragment name = "Protection">
    <argument name = "condition">Is</argument>
</fragment>
```



Pour les chaînes de condition de ce type, le tableau suivant indique les conditions possibles.



| Partie protection | Conditions possibles             |
|--------------------|---------------------------------|
| Protection         | Est<br/> N’est pas<br/> |



 

Il existe un type d’élément **fragment** qui ne contient pas de chaîne de condition. Si l’attribut Name d’un élément **fragment** est « randomiser l’ordre de lecture », l’élément de **fragment** ne contient aucun élément **argument** . Cet élément **fragment** indique au joueur de lire la liste dans un ordre aléatoire.

Exemple :


```XML
<fragment name = "Randomize Playback Order">
</fragment>
```



Certaines chaînes de condition ont une partie de tri, une partie valeur et une partie condition. Par exemple, dans la chaîne de condition « Trier par titre dans l’ordre croissant », la partie de tri est « Trier par », la partie valeur est « titre » et la partie condition est « croissant ». Notez que dans ce cas, la partie valeur est un attribut de métadonnées.

Exemple :


```XML
<fragment name = "Sort By">
    <argument name = "value">Title</argument>
    <argument name = "condition">Ascending</argument>
</fragment>
```



Pour les chaînes de condition de ce type, le tableau suivant indique les valeurs possibles et les conditions.



| Partie de tri | Valeurs possibles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | Conditions possibles                              |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| Trier par      | GenreTitle<br/> Date Added<br/> Classement automatique<br/> Mon évaluation<br/> Nombre de jeux : total global<br/> Nombre de jeux : total des matins<br/> Nombre de jeux : totaux de l’après-midi<br/> Nombre de jeux : total des soirs<br/> Nombre de jeux : totaux de nuit<br/> Nombre de lectures : jour de la semaine total<br/> Nombre de jeux : week-end total<br/> Acteur<br/> Sous-titre<br/> nom de la station<br/> Canal<br/> Heure de la diffusion<br/> Directeur<br/> Année de sortie<br/> Writer<br/> Producer<br/> Date d’enregistrement<br/> Date encodée<br/> Vitesse de transmission<br/> Protection<br/> | AscendingDescending<br/> Aléatoire<br/> |



 

Lorsque vous utilisez un élément fragment pour trier une sélection, vous devez effectuer un tri sur un attribut de métadonnées qui s’applique au type d’éléments multimédias que vous triez. Par exemple, si vous triez des éléments musicaux, vous ne pouvez pas effectuer de tri sur l’acteur. Le tableau suivant indique les attributs de métadonnées que vous pouvez utiliser pour trier les types de médias.



| Type de support  | Attributs de métadonnées possibles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Musique       | GenreTitle<br/> Date Added<br/> Classement automatique<br/> Mon évaluation<br/> Nombre de jeux : total global<br/> Nombre de jeux : total des matins<br/> Nombre de jeux : totaux de l’après-midi<br/> Nombre de jeux : total des soirs<br/> Nombre de jeux : totaux de nuit<br/> Nombre de lectures : jour de la semaine total<br/> Nombre de jeux : week-end total<br/>                                                                                                                                                                                                                                                                                            |
| Vidéo ou TV | GenreActor<br/> Sous-titre<br/> Intitulé<br/> Date Added<br/> Classement automatique<br/> nom de la station<br/> Canal<br/> Heure de la diffusion<br/> Directeur<br/> Année de sortie<br/> Writer<br/> Producer<br/> Date d’enregistrement<br/> Date encodée<br/> Vitesse de transmission<br/> Mon évaluation<br/> Protection<br/> Nombre de jeux : total global<br/> Nombre de jeux : total des matins<br/> Nombre de jeux : totaux de l’après-midi<br/> Nombre de jeux : total des soirs<br/> Nombre de jeux : totaux de nuit<br/> Nombre de lectures : jour de la semaine total<br/> Nombre de jeux : week-end total<br/> |
| Case d’option       | TitleDate ajouté<br/> Vitesse de transmission<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Photo       | Intitulé                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Autres       | GenreTitle<br/> Date Added<br/> Classement automatique<br/> Mon évaluation<br/> Vitesse de transmission<br/> Nombre de jeux : total global<br/> Nombre de jeux : total des matins<br/> Nombre de jeux : totaux de l’après-midi<br/> Nombre de jeux : total des soirs<br/> Nombre de jeux : totaux de nuit<br/> Nombre de lectures : jour de la semaine total<br/> Nombre de jeux : week-end total<br/>                                                                                                                                                                                                                                                                    |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|--------------------|---------------------------------------------------|
| Version<br/> | Lecteur Windows Media série 9 ou version ultérieure<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**argument, élément**](argument-element.md)
</dt> <dt>

[**Élément Filter**](filter-element.md)
</dt> <dt>

[**Élément sourceFilter**](sourcefilter-element.md)
</dt> <dt>

[**Windows Référence des éléments de sélection de média**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





