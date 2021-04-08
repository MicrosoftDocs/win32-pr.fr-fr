---
description: Le prédicat FREETEXT fait partie de la clause WHERE et prend en charge la recherche de mots et d’expressions dans des colonnes de texte.
ms.assetid: 8afc95d1-25cd-4448-8bee-d132c2da22b3
title: Prédicat FREETEXT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc78be4d5ac75f892c82c6dad390e4583876856f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750388"
---
# <a name="freetext-predicate"></a>Prédicat FREETEXT

Le prédicat FREETEXT fait partie de la clause [Where](-search-sql-where.md) et prend en charge la recherche de mots et d’expressions dans des colonnes de texte. Utilisez le prédicat FREETEXT pour rechercher des documents contenant des combinaisons de mots recherchés répartis dans le contenu ou les colonnes spécifiés. Pour obtenir la valeur de classement, incluez System. Search. Rank, qui est un classement de pertinence, en tant que colonne dans l’instruction SELECT.

Le prédicat FREETEXT a la syntaxe suivante :


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



La référence de colonne de texte intégral est facultative. Avec elle, vous pouvez spécifier une colonne unique ou un [alias de regroupement de colonnes](-search-sql-with-as.md) sur lequel le prédicat FREETEXT est testé. Lorsque la colonne de texte intégral est spécifiée comme « ALL » ou « \* », toutes les propriétés de texte indexées sont recherchées. Bien qu’il ne soit pas nécessaire que la colonne soit une propriété de texte, les résultats peuvent être incompréhensibles si la colonne est d’un autre type de données. Le nom de colonne peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité, et vous devez le séparer de la condition par une virgule. Si aucune condition de texte intégral n’est fournie, la colonne contents, qui est le corps du document, est utilisée.

Vous pouvez spécifier des paramètres régionaux de recherche pour identifier l’analyseur lexical et les formes fléchies appropriées pour la requête de recherche. Les valeurs de paramètres régionaux valides sont un identificateur de code (LCID) de langue Windows standard. Par exemple, 1033 est le LCID de États-Unis-anglais. Placez le LCID en tant que dernier élément à l’intérieur des parenthèses de la clause FREETEXT. Pour obtenir des informations importantes sur la recherche et les langages, consultez [utilisation des recherches localisées](-search-sql-usinglocsearches.md).

> [!Note]  
> Les paramètres régionaux de recherche par défaut sont les paramètres régionaux par défaut du système.

 

Vous devez placer la partie de la condition FREETEXT entre guillemets simples, et elle doit comporter un ou plusieurs termes de recherche. Le prédicat FREETEXT ne prend pas en charge les opérations logiques. Pour rechercher une expression comme s’il s’agissait d’un mot unique, placez l’expression entre guillemets doubles.

Lorsque vous utilisez le prédicat FREETEXT, les résultats de la requête de recherche retournent des documents contenant tous les termes recherchés. Les termes n’ont pas besoin d’apparaître dans un ordre particulier. Les documents qui contiennent davantage de termes de recherche ont des valeurs de colonne de classement plus élevées.

## <a name="examples"></a>Exemples

L’exemple suivant recherche des documents contenant « Computer », « Software », « Hardware » ou des combinaisons de ces mots :


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> Vous ne pouvez pas utiliser les correspondances de mots simples et d’expressions dans le même prédicat FREETEXT.

 

Lors de l’exécution de requêtes avec des contractions, vous devez placer les guillemets dans une séquence d’échappement dans la contraction lors de l’utilisation de FREETEXT, mais pas lors de l’utilisation de CONTAINs.

Par exemple, la syntaxe suivante échoue :


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



La syntaxe correcte comprend deux guillemets simples, et non un guillemet double.

La syntaxe suivante est réussie :


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Informations de référence**
</dt> <dt>

[CONTAINs, prédicat](-search-sql-contains.md)
</dt> <dt>

[Clause WHERE](-search-sql-where.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



