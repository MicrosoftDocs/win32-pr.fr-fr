---
description: Le groupe sur...
ms.assetid: 37f027c1-c2af-4d62-8b5f-918499fc2d7c
title: REGROUPER... ... Gestion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df21bb53babd25ae3e407032c6cf9d3774323e85
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122882020"
---
# <a name="group-on--over--statement"></a>REGROUPER... ... Gestion

Le groupe sur... ... l’instruction retourne un ensemble de lignes hiérarchique dans lequel les résultats de la recherche sont divisés en groupes basés sur une colonne spécifiée et des plages de regroupement facultatives. Si vous regroupez sur la colonne [System. Kind](../properties/props-system-kind.md) , le jeu de résultats est divisé en plusieurs groupes : l’un pour les documents, l’autre pour les communications, et ainsi de suite. Si vous regroupez sur [System. Size](../properties/props-system-size.md) et la plage de groupes 100 Ko, le jeu de résultats est divisé en trois groupes : les éléments de taille < 100 Ko, les éléments de taille >= 100 Ko et les éléments sans valeur de taille. Vous pouvez également agréger des regroupements avec des fonctions.

Cette rubrique aborde les sujets suivants :

-   [Syntaxe](#syntax)
-   [Plages de groupes](#group-ranges)
-   [Étiquetage des groupes](#labeling-groups)
-   [Classement des groupes](#ordering-groups)
-   [Imbrication de groupes](#nesting-groups)
-   [Regroupement sur les propriétés de vecteur](#grouping-on-vector-properties)
-   [Autres exemples](#more-examples)
-   [Rubriques connexes](#related-topics)

## <a name="syntax"></a>Syntaxe

Le groupe sur... ... la syntaxe de l’instruction est la suivante :


```
GROUP ON <column> ['['<group ranges>']']] 
[AGGREGATE <aggregate_function>] 
[ORDER BY <column> [<direction>]] | [ORDER IN GROUP '<group name>' BY <column> [<direction>]]
    OVER (GROUP ON... | SELECT... ] )
```



où les plages de regroupement sont définies comme suit :


```
<group ranges> := <range limit> [/'<label>'] | <range limit> [/'<label>'], <group ranges>
<range limit> := (<number> | <date> | '<string>' | BEFORE('<string>') | AFTER('<string>')) 
```



La colonne GROUP &lt; on &gt; peut être un [identificateur](-search-sql-identifiers.md) standard ou délimité pour une propriété dans la Banque de propriétés.

Le facultatif <group ranges> est une liste d’une ou plusieurs valeurs (nombre, date ou chaîne) utilisées pour diviser les résultats en groupes. <range limit>Identifie un point de division dans le jeu de résultats retourné, et <label> identifie une étiquette conviviale pour un groupe. Vous pouvez diviser le jeu de résultats en autant de groupes que nécessaire.

Le premier groupe de résultats inclut les éléments dont la valeur minimale possible pour la propriété spécifiée est inférieure à la limite de la première plage. Ce groupe peut être référencé à l’aide du mot clé MINVALUE. Le deuxième groupe peut être référencé avec le spécificateur de limite de plage lui-même et comprend les éléments dont la valeur de la propriété spécifiée est supérieure ou égale à la limite de la plage. Tous les éléments qui n’ont pas de valeur pour la propriété spécifiée sont retournés en dernier et peuvent être référencés à l’aide du mot clé **null** .

Par exemple, une limite de plage de « 2006-01-01 » pour la propriété [System. DateCreated](../properties/props-system-datecreated.md) divise le jeu de résultats en éléments dont les dates sont antérieures à 2006-01-01 (groupe MinValue), les éléments dont la date est identique ou postérieure à 2006-01-01 (groupe 2006-01-01) et les éléments sans date (groupe **null** ).

Dans chaque groupe, les résultats sont triés en fonction des valeurs de la colonne regrouper sur par défaut. La clause [order by](-search-sql-orderby.md) facultative peut contenir un spécificateur de direction de ASC pour l’ordre croissant (de faible à élevé) ou DESC pour l’ordre décroissant (de haut en bas), et l' [ordre dans la clause Group by](-search-sql-orderingroup.md) peut ordonner chaque groupe à l’aide de différentes règles. Pour plus d’informations, consultez la section [classement des groupes](#ordering-groups) ci-dessous.

## <a name="group-ranges"></a>Plages de groupes

Le tableau suivant montre comment les résultats sont divisés en groupes en fonction des limites de plage :



| Exemple ( &lt; plages de groupes de colonnes &gt; \[ \] )        | Résultats                                                                                                                                                                                                                                                                         |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| System. size \[ 1000, 5000\]                       | Les résultats sont regroupés en quatre compartiments : **MinValue**: taille < 1000<br/> **1000 :** 1000 <= taille < 5000<br/> **5000 :** Taille >= 5000<br/> **Null :** Aucune valeur pour la taille<br/>                                                                      |
| System. Author \[ Before ('m'), après ('r')\]         | Les résultats sont regroupés en quatre compartiments : **MinValue :** Author < caractère avant « m »<br/> **m :** caractère avant "m" <= auteur < caractère après "r"<br/> **r :** caractère après « r » <= auteur<br/> **Null :** Aucune valeur pour Author<br/>      |
| System. Author \[ MinValue/'a to l', "m"/m to z'\] | Les résultats sont regroupés en trois compartiments : **a à l :** auteur < « m »<br/> **de m à z :** "m" <= auteur <br/> **Null :** Aucune valeur pour Author<br/>                                                                                                               |
| System. DateCreated \[ « 2005-1-01 », « 2006-6-01 »\]   | Les résultats sont regroupés en quatre compartiments :<br/> **MinValue :** DateCreated < 2005-1-01<br/> **2005-1-01 :** 2005-1-01 <= DateCreated < 2006-6-01<br/> **2006-1-01 :** DateCreated >= 2006-6-01<br/> **Null :** Aucune valeur pour DateCreated<br/> |



 

 

> [!IMPORTANT]
>
> Correcte `GROUP ON System.Author['m','z','a']`
>
> Correctrices `GROUP ON System.Author['a','m','z']`

 

 

## <a name="labeling-groups"></a>Étiquetage des groupes

Pour améliorer la lisibilité, vous pouvez étiqueter des groupes à l’aide de la syntaxe suivante :


```
GROUP ON <column> [<range limit>/'<label>',<range limit>/'<label>']
```



L’étiquette est séparée de la limite de plage par une barre oblique et est placée entre guillemets simples. Si vous ne spécifiez pas d’étiquette, le nom de groupe est la chaîne de limite de plage.

Voici un exemple de groupes d’étiquetage :


```
GROUP ON System.Size [(MINVALUE/'Small','100')/'Medium','50000'/'Large']
    OVER (SELECT System.Size FROM SystemIndex)
```



dans Windows 7 ou version ultérieure, vous pouvez également utiliser une \[ autre \] étiquette générique pour combiner plusieurs plages de regroupement. Les résultats de tous les groupes identifiés avec cette étiquette sont combinés dans un groupe avec cette étiquette. Ce groupe de résultats est retourné après tous les autres groupes, à l’exception du groupe **null** . Le groupe **null** contient des résultats pour les éléments qui n’ont pas de valeur pour la propriété spécifiée. avant le Windows 7 \[ , l’autre \] étiquette est traitée comme toute autre étiquette de groupe.

le code suivant est un exemple d’utilisation de l' \[ autre \] étiquette pour les groupes qui seraient créés dans Windows 7 ou version ultérieure :


```
GROUP ON System.Author ['0', 'A'/'[OTHER]', 'I', 'Q', 'W'/'[OTHER]', 'Y']
    OVER (SELECT System.DateCreated FROM SystemIndex)
```



le tableau suivant montre les groupes qui seraient créés par le code de regroupement précédent dans Windows 7 ou version ultérieure.



| Groupe     | System.Author | System. FileName |
|-----------|---------------|-----------------|
| 0         | 1Bill         | Lorem.docx      |
| Q         | Dame         | Ipsum.docx      |
|           | Robin         | dolor.docx      |
| O         | Zara          | amet.docx       |
| \[AUTRES\] | Abner         | nonummy.docx    |
|           | Bob           | laoreet.docx    |
|           | Xaria         | magna.docx      |
| **NULL**  |               | aliquam.docx    |



 

## <a name="ordering-groups"></a>Classement des groupes

Il existe trois façons de commander des éléments dans des groupes :

-   Classement par défaut : Si vous ne spécifiez pas le cas contraire, les résultats sont classés en fonction des valeurs de la colonne regrouper sur, dans l’ordre croissant.
-   Trier par : vous pouvez spécifier l’ordre décroissant dans une clause ORDER BY. Vous devez classer les résultats en fonction de la colonne regrouper sur.
-   ORDRE dans regrouper par : vous pouvez spécifier un ordre différent pour chaque groupe. si vous regroupez sur [system. genre](../properties/props-system-kind.md), vous pouvez commander des documents par system [. Author](../properties/props-system-author.md) et music par [system. Musique. Artiste](../properties/props-system-music-artist.md).

Pour plus d’informations sur la façon de trier les résultats, consultez les pages de référence des clauses Order [by](-search-sql-orderby.md) et [Order in Group](-search-sql-orderingroup.md) .

## <a name="nesting-groups"></a>Imbrication de groupes

Vous pouvez imbriquer des groupes avec plusieurs clauses GROUP ON. L’ordre spécifié dans la requête est directement reflété dans la hiérarchie des groupes de sortie, comme indiqué dans l’exemple suivant.


```
GROUP ON <System.Kind> 
      OVER (GROUP ON <System.Author> 
                  OVER (SELECT <System.DateCreated>))
```





| System. Kind    | System.Author | System. DateCreated |
|----------------|---------------|--------------------|
| dans des documents      | Willa         | 2006-01-02         |
|                |               | 2006-01-05         |
|                | Zara          | 2007-06-02         |
|                |               | 2007-09-10         |
| communications | Abner         | 2006-04-16         |
|                | Jean          | 2007-02-20         |
|                | Willa         | 2006-10-15         |
|                | Zara          | 2008-01-02         |



 

 

## <a name="grouping-on-vector-properties"></a>Regroupement sur les propriétés de vecteur

Le regroupement sur les propriétés vectorielles, les propriétés qui peuvent contenir une ou plusieurs valeurs simultanément, compare les valeurs de vecteur individuellement par défaut. Par exemple, s’il existe un document, Lorem.docx avec la propriété System. Author comme «Theresa ; Zara» et un autre document, Ipsum.docx avec la propriété System. Author comme « Zara », la requête retourne le jeu de résultats dans deux groupes comme indiqué ici :


```
GROUP ON <System.Author> 
      OVER (SELECT <System.FileName>)
```





| System.Author | System. FileName |
|---------------|-----------------|
| Theresa       | Lorem.docx      |
| Zara          | Lorem.docx      |
|               | Ipsum.docx      |



 

Comme vous pouvez le voir, le regroupement sur des propriétés vectorielles retourne des lignes en double. Lorem.docx apparaît deux fois parce qu’il a deux auteurs.

 

## <a name="more-examples"></a>Plus d'exemples


```
GROUP ON System.Photo.ISOSpeed [0,10,100] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.DateCreated['2005/01/01 00:00:00', '2005/12/30 23:00:00'] 
      OVER (SELECT System.ItemName, System.Size, System.ItemUrl FROM SystemIndex)
            
GROUP ON System.Author ORDER BY System.Author DESC 
      OVER (GROUP ON System.DateCreated ORDER BY System.DateCreated ASC 
                  OVER (SELECT System.FileName, System.DateCreated, System.Size FROM SystemIndex 
                        WHERE CONTAINS(*, 'text')))

GROUP ON System.ItemName [before('a'), 'a', before ('c'), 'd', after('d')] 
      OVER (SELECT System.ItemName, System.ItemUrl FROM SystemIndex ORDER BY System.ItemName)                        
                        
GROUP ON System.ItemNameDisplay ['a' / 'col_a','c' / 'col_c'] 
      OVER (SELECT System.ItemNameDisplay FROM SystemIndex 
            ORDER BY System.ItemNameDisplay)

GROUP ON System.Size[1,2] 
      OVER (GROUP ON System.Author['a','f','mc','x'] 
                  OVER (GROUP ON System.DateCreated['2005/07/25 07:00:00', '2005/08/25 07:00:00']
                        ORDER BY System.DateCreated DESC 
                              OVER (SELECT System.FileName FROM SystemIndex 
                                    WHERE CONTAINS('text'))))   
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctions d’agrégation](-search-sql-aggregates.md)
</dt> <dt>

[Clause ORDER BY](-search-sql-orderby.md)
</dt> <dt>

[COMMANDE dans la clause GROUP](-search-sql-orderingroup.md)
</dt> </dl>

 

 
