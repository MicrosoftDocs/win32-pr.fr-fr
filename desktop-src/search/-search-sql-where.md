---
description: Les conditions qui déterminent si un document est inclus dans les résultats retournés par la requête sont spécifiées par la clause WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: Clause where (recherche Windows)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e711219ff8eea81e8c4f8fd8145baccc35f49389d412f0e4ac088aa06666643
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118462401"
---
# <a name="where-clause-windows-search"></a>Clause where (recherche Windows)

Les conditions qui déterminent si un document est inclus dans les résultats retournés par la requête sont spécifiées par la clause WHERE. Au niveau le plus élevé, la syntaxe de la clause WHERE comporte deux parties :


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



L’alias de groupe <facultatif \_> partie de la clause simplifie les requêtes complexes en affectant un alias à un groupe d’une ou de plusieurs colonnes. Cela peut améliorer la lisibilité des requêtes complexes qui recherchent les mêmes informations sur plusieurs colonnes spécifiées par des URL. Pour plus d’informations sur les alias de groupe, consultez [with--As Group alias Predicate](-search-sql-with-as.md).

La <search condition> partie de la clause WHERE est un ou plusieurs prédicats de recherche qui spécifient des critères de correspondance pour la recherche. Les prédicats de recherche sont des expressions qui déclarent des faits sur une valeur.

Le résultat d’une condition de recherche est une valeur booléenne, soit **true** si le document remplit les conditions de recherche spécifiées, soit **false** dans le cas contraire. Si le résultat est **true**, le document est retourné. Si le résultat est **false**, le document n’est pas retourné. les valeurs de classement des Documents renvoyés dans une requête de recherche Microsoft Windows sont attribuées en fonction de leur correspondance avec les conditions de recherche. Chacune des conditions de recherche de requête peut inclure une clause [RANKBY](-search-sql-rankby.md) qui prend en charge la modification des valeurs de classement retournées.

La [fonction ReuseWhere](-search-sql-reusewhere.md) rend plus efficace plusieurs requêtes qui utilisent certaines des mêmes conditions de recherche. La clause WHERE d’une requête spécifie l’ensemble des éléments qui correspondent dans une requête. Les requêtes suivantes peuvent partager le travail effectué pour le évaluation précédent à l’aide de la fonction ReuseWhere dans la nouvelle clause WHERE de la requête.

## <a name="search-predicates"></a>Prédicats de recherche

Une condition de recherche se compose d’un ou de plusieurs prédicats ou conditions de recherche qui décrivent ce que l’utilisateur recherche (par exemple, où System. DateCreated > ' 2006-04-19 '). Les prédicats de recherche peuvent être combinés à l’aide des opérateurs logiques **and**, **or** ou **not**. L’opérateur unaire facultatif **ne peut pas** être utilisé avec **et** et uniquement pour nier la valeur logique d’un prédicat ou d’une condition de recherche. Vous pouvez utiliser des parenthèses pour regrouper et imbriquer des termes logiques.

Le tableau suivant indique l’ordre de priorité des opérateurs logiques.



| Ordre (priorité) | Opérateur logique |
|--------------------|------------------|
| Premier (le plus élevé)    | **NOT**          |
| Second             | **AND**          |
| Troisième (le plus bas)     | **OR**           |



 

Les opérateurs logiques du même type sont associatifs et il n’y a pas d’ordre de calcul spécifié. Par exemple, les points (A **et** b) **et** (C **et** d) peuvent être calculés (a **et** d) **et** (B **et** c) sans aucune modification dans le résultat logique.

> [!IMPORTANT]
>
> Incorrect : où **ne contient pas** ('Computer')
>
> Correct : WHERE CONTAINs ('Software') **et not** Contains ('Computer')

 

Dans les requêtes complexes, vous souhaiterez peut-être mettre l’accent sur les correspondances dans certaines colonnes que dans d’autres. Par exemple, lors de la recherche de documents qui traitent de la « conception de logiciels », Rechercher le terme de recherche dans le titre du document est plus susceptible d’être une correspondance correcte que de trouver les mots individuels dans le texte du document. pour influencer le classement des documents de cette manière, le langage de requête de recherche Microsoft Windows prend en charge la pondération des conditions de recherche. Pour plus d’informations sur la pondération des colonnes, consultez [Contains Predicate](-search-sql-contains.md) et [FREETEXT Predicate](-search-sql-freetext.md).

il existe trois groupes de prédicats de recherche dans Windows recherche : recherches en texte intégral, non en texte intégral et profondeur de dossier. Les prédicats de recherche en texte intégral correspondent généralement à la signification du contenu, du titre et d’autres colonnes, et prennent en charge la mise en correspondance linguistique (par exemple, les autres formes de mots, expressions et recherches de proximité). En revanche, les prédicats de recherche de texte non intégral correspondent à la valeur des colonnes spécifiées et n’incluent pas de traitement linguistique spécial, mais dans plusieurs cas, elles offrent des critères spéciaux basés sur des caractères. Les prédicats de profondeur de dossier limitent l’étendue de recherche à un chemin d’accès spécifié.

> [!Note]  
> Si la requête retourne un document parce qu’un prédicat de texte non intégral prend la valeur **true** pour ce document, la valeur de classement est calculée comme 1000. L’utilisation de la [fonction de forçage de rang](-search-sql-rankby.md) peut modifier la valeur de classement.

 

Les tableaux suivants décrivent les prédicats de recherche en texte intégral, non en texte intégral et profondeur de dossier.



| Prédicat de texte intégral                  | Description                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CONTAINS](-search-sql-contains.md) | Prend en charge les recherches complexes de termes dans les colonnes de texte de document (par exemple, titre, contenu). Peut rechercher les formes fléchies des termes recherchés, tester la proximité des termes et effectuer des comparaisons logiques. Les termes de recherche peuvent inclure des caractères génériques. |
| [FREETEXT](-search-sql-freetext.md) | Recherche des documents qui correspondent à la signification de l’expression de recherche. Les mots connexes et les expressions similaires correspondent, avec la colonne de classement calculée en fonction de la précision du document par rapport à l’expression de recherche. Les termes de recherche ne peuvent pas contenir de caractères génériques.  |



 



| Prédicat de texte non intégral                                                    | Description                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [LIKE](-search-sql-like.md)                                               | Les valeurs de colonne sont comparées à l’aide de critères spéciaux simples avec des caractères génériques.                                                                                                    |
| [Comparaison de valeurs littérales](-search-sql-literalvaluecomparison.md)         | Les valeurs de colonne sont comparées aux valeurs de chaîne, de date, d’horodatage, numériques et d’autres valeurs littérales. Ce prédicat prend en charge l’égalité et les inégales telles que supérieur à et inférieur à. |
| [Comparaisons à valeurs multiples (tableau)](-search-sql-multivaluedcomparisons.md) | Les colonnes à valeurs multiples sont comparées à un tableau de littéraux à valeurs multiples.                                                                                                             |
| [NULL](-search-sql-null.md)                                               | Les valeurs de colonne qui ne sont pas définies pour le document peuvent être détectées à l’aide du prédicat **null** .                                                                                    |



 



| Profondeur du dossier                             | Description                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [ÉTENDUE](-search-sql-folderdepth.md)     | Effectue une traversée profonde du chemin d’accès spécifié, y compris le dossier spécifique et tous les sous-dossiers. |
| [DIRECTORY](-search-sql-folderdepth.md) | Effectue un parcours superficiel du chemin d’accès spécifié, en recherchant uniquement le dossier spécifique.            |



 

## <a name="examples"></a>Exemples

Pour obtenir des exemples de la clause WHERE, consultez les rubriques de prédicat individuelles liées dans le tableau précédent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[ReuseWhere fonction)](-search-sql-reusewhere.md)
</dt> <dt>

[Propriétés du rowset](-search-sql-rowset-properties.md)
</dt> <dt>

[FROM, clause](-search-sql-from.md)
</dt> <dt>

[vue d’ensemble de la syntaxe de SQL de recherche](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[Prédicat WITH--AS Group alias](-search-sql-with-as.md)
</dt> <dt>

[Prédicats d’étendue et de répertoire](-search-sql-folderdepth.md)
</dt> <dt>

[RANK BY, clause](-search-sql-rankby.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



