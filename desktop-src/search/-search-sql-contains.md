---
description: Le prédicat CONTAINs fait partie de la clause WHERE et prend en charge la recherche de mots et d’expressions dans des colonnes de texte.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: CONTAINs, prédicat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2885187d0dd25f38e6bbf40b3259164f0aa91e05
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122625285"
---
# <a name="contains-predicate"></a>CONTAINs, prédicat

Le prédicat CONTAINs fait partie de la clause WHERE et prend en charge la recherche de mots et d’expressions dans des colonnes de texte. Le prédicat CONTAINs possède des fonctionnalités pour la correspondance des mots, la correspondance des formes fléchies de mots, la recherche à l’aide de caractères génériques et la recherche à l’aide de la proximité. Vous pouvez également appliquer des pondérations dans un prédicat CONTAINs pour définir l’importance des colonnes où le terme recherché est trouvé. Le prédicat CONTAINs est mieux adapté pour les correspondances exactes, contrairement au prédicat [FREETEXT](-search-sql-freetext.md) , qui est mieux adapté à la recherche de documents contenant des combinaisons de mots recherchés répartis dans l’ensemble de la colonne. Les recherches ne tiennent pas compte des majuscules.

Voici la syntaxe de base du prédicat CONTAINs :

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

La référence de colonne de texte intégral \_ est facultative. Avec elle, vous pouvez limiter la recherche à une seule colonne ou à un groupe de colonnes sur lequel le prédicat CONTAINs est testé. Lorsque la colonne de texte intégral est spécifiée comme « ALL » ou « \* », toutes les propriétés de texte indexées sont recherchées. Bien qu’il ne soit pas nécessaire que la colonne soit une propriété de texte, les résultats peuvent être incompréhensibles si la colonne est d’un autre type de données. Le nom de colonne peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité, et vous devez le séparer de la condition par une virgule. Si aucune colonne de texte intégral n’est spécifiée, la colonne System. Search. Contents, qui est le corps du document, est utilisée.

La partie LCID du prédicat spécifie les paramètres régionaux de la recherche. Cela indique au moteur de recherche d’utiliser l’analyseur lexical et les formes fléchies appropriées pour la requête de recherche. pour spécifier les paramètres régionaux, indiquez le Windows identificateur du code de langue standard (LCID). Par exemple, 1033 est le LCID de États-Unis-anglais. Placez le LCID en tant que dernier élément à l’intérieur des parenthèses de la clause CONTAINs. Pour obtenir des informations importantes sur la recherche et les langages, consultez [utilisation des recherches localisées](-search-sql-usinglocsearches.md).

> [!NOTE]  
> Les paramètres régionaux de recherche par défaut sont les paramètres régionaux par défaut du système.

La partie de condition Contains \_ doit être placée entre des guillemets simples pour les mots simples ou des guillemets doubles pour les expressions, et se compose d’un ou plusieurs termes de recherche de contenu combinés à l’aide des opérateurs logiques **et** ou. Vous pouvez utiliser l’opérateur unaire facultatif **non** après un opérateur **and** pour nier la valeur logique d’un terme de recherche de contenu.

> [!NOTE]  
> L’opérateur **not** ne peut se produire qu’après **et**. Vous ne pouvez pas utiliser l’opérateur **not** s’il n’existe qu’une seule condition de correspondance, ou après l’opérateur **or** .

Vous pouvez utiliser des parenthèses pour regrouper et imbriquer des termes de recherche de contenu. Le tableau suivant décrit l’ordre de priorité des opérateurs logiques.

| Ordre (priorité) | Opérateur logique |
|--------------------|------------------|
| Premier (le plus élevé)    | **NOT**          |
| Second             | **AND**          |
| Troisième (le plus bas)     | **OR**           |

Les opérateurs logiques du même type sont associatifs et il n’y a pas d’ordre de calcul spécifié. Par exemple, les points (A **et** b) **et** (C **et** d) peuvent être calculés (B **et** c) **et** (a **et** d) sans aucune modification dans le résultat logique.

Le tableau suivant décrit les types de termes de recherche de contenu.

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Type</th>
<th>Description</th>
<th>Exemples</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Word</td>
<td>Mot unique sans espaces ni autres signes de ponctuation. Les guillemets doubles ne sont pas nécessaires.</td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (&#39;computer&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Phrase</td>
<td>Plusieurs mots ou espaces inclus.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer software&quot;&#39;)

Or, to use a double quote mark:

... WHERE CONTAINS
(&#39;&quot;computer &quot;&quot;science&quot;&quot; &quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Caractère générique</td>
<td>Mots ou expressions avec l’astérisque (*) ajouté à la fin. Pour plus d’informations, consultez <a href="-search-sql-wildcards.md">utilisation de caractères génériques dans le PRÉDICAT Contains</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;compu*&quot;&#39;)

Matches &quot;computer&quot;, &quot;computers&quot;,
&quot;computation&quot;, and &quot;compulsory&quot;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Colonne de texte intégral</td>
<td>Nom de colonne de propriété par rapport auquel correspondre à la requête restante.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS (System.Author,&#39;&quot;James&quot; OR &quot;Juan&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Booléen</td>
<td>Mots, expressions et chaînes de caractères génériques combinés à l’aide des opérateurs booléens <strong>and</strong>, <strong>or</strong>ou <strong>not</strong>. Mettez les termes booléens entre guillemets doubles.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer monitor&quot; AND
  &quot;software program&quot; AND
  &quot;install component&quot;&#39;)

...WHERE CONTAINS
 (&#39; &quot;computer&quot; AND
  &quot;software&quot; AND
  &quot;install&quot; &#39; )

...WHERE CONTAINS
(&#39;&quot;computer software install&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>Rapproché</td>
<td>Mots, expressions ou caractères génériques séparés par la fonction NEAR. Pour plus d’informations, consultez à <a href="-search-sql-near.md">court terme</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;&quot;computer&quot; NEAR &quot;software&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>FormsOf</td>
<td>Correspond à un mot et aux versions fléchies de ce mot. Pour plus d’informations, consultez <a href="-search-sql-formsof.md">terme FORMSOF</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;FORMSOF
 (INFLECTIONAL, &quot;happy&quot;))

Matches &quot;happy&quot;, &quot;happier&quot;,
&quot;happiest&quot;, &quot;happily&quot;, and so on.</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td>IsAbout</td>
<td>Combine les résultats de correspondance sur plusieurs termes de recherche de mots, d’expressions ou de caractères génériques. Chaque terme de recherche peut éventuellement être pondéré. Vous pouvez éventuellement spécifier la méthode de calcul Rank, qui combine les pondérations et le nombre d’éléments correspondants dans le document. Pour plus d’informations, consultez <a href="-search-sql-isabout.md">terme ISABOUT</a>.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS
(&#39;ISABOUT ( &quot;computer&quot; WEIGHT (0.75) ,
    &quot;software&quot; WEIGHT (0.25) ,
    &quot;development&quot; WEIGHT (0.255)
 ) RANKMETHOD INNER PRODUCT
&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

Cette section comprend les rubriques suivantes :

- [Utilisation de caractères génériques dans le prédicat CONTAINs](-search-sql-wildcards.md)
- [Terme FORMSOF](-search-sql-formsof.md)
- [Terme ISABOUT](-search-sql-isabout.md)
- [À court terme](-search-sql-near.md)

## <a name="related-topics"></a>Rubriques connexes

### <a name="reference"></a>Référence

[Clause WHERE](-search-sql-where.md)

### <a name="conceptual"></a>Conceptuel

[Prédicats de texte intégral](-search-sql-fulltextpredicates.md)

[Prédicats de texte non intégral](-search-sql-nonfulltextpredicates.md)
