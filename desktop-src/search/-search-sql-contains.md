---
description: Le prédicat CONTAINs fait partie de la clause WHERE et prend en charge la recherche de mots et d’expressions dans des colonnes de texte.
ms.assetid: 53083966-54cc-4a16-a161-caa663bea7ea
title: CONTAINs, prédicat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 908f4c67d5c1d5bcf00c60bd8cb271928682a907
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862154"
---
# <a name="contains-predicate"></a><span data-ttu-id="08e5d-103">CONTAINs, prédicat</span><span class="sxs-lookup"><span data-stu-id="08e5d-103">CONTAINS Predicate</span></span>

<span data-ttu-id="08e5d-104">Le prédicat CONTAINs fait partie de la clause WHERE et prend en charge la recherche de mots et d’expressions dans des colonnes de texte.</span><span class="sxs-lookup"><span data-stu-id="08e5d-104">The CONTAINS predicate is part of the WHERE clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="08e5d-105">Le prédicat CONTAINs possède des fonctionnalités pour la correspondance des mots, la correspondance des formes fléchies de mots, la recherche à l’aide de caractères génériques et la recherche à l’aide de la proximité.</span><span class="sxs-lookup"><span data-stu-id="08e5d-105">The CONTAINS predicate has features for matching words, matching inflectional forms of words, searching using wildcard characters, and searching using proximity.</span></span> <span data-ttu-id="08e5d-106">Vous pouvez également appliquer des pondérations dans un prédicat CONTAINs pour définir l’importance des colonnes où le terme recherché est trouvé.</span><span class="sxs-lookup"><span data-stu-id="08e5d-106">You can also apply weights in a CONTAINS predicate to set the importance of the columns where the search term is found.</span></span> <span data-ttu-id="08e5d-107">Le prédicat CONTAINs est mieux adapté pour les correspondances exactes, contrairement au prédicat [FREETEXT](-search-sql-freetext.md) , qui est mieux adapté à la recherche de documents contenant des combinaisons de mots recherchés répartis dans l’ensemble de la colonne.</span><span class="sxs-lookup"><span data-stu-id="08e5d-107">The CONTAINS predicate is better suited for exact matches, in contrast to the [FREETEXT](-search-sql-freetext.md) predicate, which is better suited to finding documents containing combinations of the search words spread throughout the column.</span></span> <span data-ttu-id="08e5d-108">Les recherches ne tiennent pas compte des majuscules.</span><span class="sxs-lookup"><span data-stu-id="08e5d-108">Searches are not case-sensitive.</span></span>

<span data-ttu-id="08e5d-109">Voici la syntaxe de base du prédicat CONTAINs :</span><span class="sxs-lookup"><span data-stu-id="08e5d-109">The following is the basic syntax of the CONTAINS predicate:</span></span>

```SQL
...CONTAINS(["<fulltext_column>",]'<contains_condition>'[,<LCID>])...
```

<span data-ttu-id="08e5d-110">La référence de colonne de texte intégral \_ est facultative.</span><span class="sxs-lookup"><span data-stu-id="08e5d-110">The fulltext\_column reference is optional.</span></span> <span data-ttu-id="08e5d-111">Avec elle, vous pouvez limiter la recherche à une seule colonne ou à un groupe de colonnes sur lequel le prédicat CONTAINs est testé.</span><span class="sxs-lookup"><span data-stu-id="08e5d-111">With it, you can limit the search to a single column or a column group against which the CONTAINS predicate is tested.</span></span> <span data-ttu-id="08e5d-112">Lorsque la colonne de texte intégral est spécifiée comme « ALL » ou « \* », toutes les propriétés de texte indexées sont recherchées.</span><span class="sxs-lookup"><span data-stu-id="08e5d-112">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="08e5d-113">Bien qu’il ne soit pas nécessaire que la colonne soit une propriété de texte, les résultats peuvent être incompréhensibles si la colonne est d’un autre type de données.</span><span class="sxs-lookup"><span data-stu-id="08e5d-113">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="08e5d-114">Le nom de colonne peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité, et vous devez le séparer de la condition par une virgule.</span><span class="sxs-lookup"><span data-stu-id="08e5d-114">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="08e5d-115">Si aucune colonne de texte intégral n’est spécifiée, la colonne System. Search. Contents, qui est le corps du document, est utilisée.</span><span class="sxs-lookup"><span data-stu-id="08e5d-115">If no fulltext column is specified, the System.Search.Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="08e5d-116">La partie LCID du prédicat spécifie les paramètres régionaux de la recherche.</span><span class="sxs-lookup"><span data-stu-id="08e5d-116">The LCID portion of the predicate specifies the search locale.</span></span> <span data-ttu-id="08e5d-117">Cela indique au moteur de recherche d’utiliser l’analyseur lexical et les formes fléchies appropriées pour la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="08e5d-117">This instructs the search engine to use the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="08e5d-118">Pour spécifier les paramètres régionaux, indiquez l’identificateur de code (LCID) de la langue Windows standard.</span><span class="sxs-lookup"><span data-stu-id="08e5d-118">To specify the locale, provide the Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="08e5d-119">Par exemple, 1033 est le LCID de États-Unis-anglais.</span><span class="sxs-lookup"><span data-stu-id="08e5d-119">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="08e5d-120">Placez le LCID en tant que dernier élément à l’intérieur des parenthèses de la clause CONTAINs.</span><span class="sxs-lookup"><span data-stu-id="08e5d-120">Place the LCID as the last item inside the parentheses of the CONTAINS clause.</span></span> <span data-ttu-id="08e5d-121">Pour obtenir des informations importantes sur la recherche et les langages, consultez [utilisation des recherches localisées](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="08e5d-121">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!NOTE]  
> <span data-ttu-id="08e5d-122">Les paramètres régionaux de recherche par défaut sont les paramètres régionaux par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="08e5d-122">The default search locale is the system default locale.</span></span>

<span data-ttu-id="08e5d-123">La partie de condition Contains \_ doit être placée entre des guillemets simples pour les mots simples ou des guillemets doubles pour les expressions, et se compose d’un ou plusieurs termes de recherche de contenu combinés à l’aide des opérateurs logiques **et** ou.</span><span class="sxs-lookup"><span data-stu-id="08e5d-123">The contains\_condition portion must be enclosed in single quotation marks for single words or double quotation marks for phrases, and consists of one or more content search terms that are combined using the logical operators **AND** or **OR**.</span></span> <span data-ttu-id="08e5d-124">Vous pouvez utiliser l’opérateur unaire facultatif **non** après un opérateur **and** pour nier la valeur logique d’un terme de recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="08e5d-124">You can use the optional unary operator **NOT** after an **AND** operator to negate the logical value of a content search term.</span></span>

> [!NOTE]  
> <span data-ttu-id="08e5d-125">L’opérateur **not** ne peut se produire qu’après **et**.</span><span class="sxs-lookup"><span data-stu-id="08e5d-125">The **NOT** operator can occur only after **AND**.</span></span> <span data-ttu-id="08e5d-126">Vous ne pouvez pas utiliser l’opérateur **not** s’il n’existe qu’une seule condition de correspondance, ou après l’opérateur **or** .</span><span class="sxs-lookup"><span data-stu-id="08e5d-126">You cannot use the **NOT** operator if there is only one match condition, or after the **OR** operator.</span></span>

<span data-ttu-id="08e5d-127">Vous pouvez utiliser des parenthèses pour regrouper et imbriquer des termes de recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="08e5d-127">You can use parentheses to group and nest content search terms.</span></span> <span data-ttu-id="08e5d-128">Le tableau suivant décrit l’ordre de priorité des opérateurs logiques.</span><span class="sxs-lookup"><span data-stu-id="08e5d-128">The following table describes the order of precedence for the logical operators.</span></span>

| <span data-ttu-id="08e5d-129">Ordre (priorité)</span><span class="sxs-lookup"><span data-stu-id="08e5d-129">Order (precedence)</span></span> | <span data-ttu-id="08e5d-130">Opérateur logique</span><span class="sxs-lookup"><span data-stu-id="08e5d-130">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="08e5d-131">Premier (le plus élevé)</span><span class="sxs-lookup"><span data-stu-id="08e5d-131">First (highest)</span></span>    | <span data-ttu-id="08e5d-132">**NOT**</span><span class="sxs-lookup"><span data-stu-id="08e5d-132">**NOT**</span></span>          |
| <span data-ttu-id="08e5d-133">Seconde</span><span class="sxs-lookup"><span data-stu-id="08e5d-133">Second</span></span>             | <span data-ttu-id="08e5d-134">**AND**</span><span class="sxs-lookup"><span data-stu-id="08e5d-134">**AND**</span></span>          |
| <span data-ttu-id="08e5d-135">Troisième (le plus bas)</span><span class="sxs-lookup"><span data-stu-id="08e5d-135">Third (lowest)</span></span>     | <span data-ttu-id="08e5d-136">**OR**</span><span class="sxs-lookup"><span data-stu-id="08e5d-136">**OR**</span></span>           |

<span data-ttu-id="08e5d-137">Les opérateurs logiques du même type sont associatifs et il n’y a pas d’ordre de calcul spécifié.</span><span class="sxs-lookup"><span data-stu-id="08e5d-137">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="08e5d-138">Par exemple, les points (A **et** b) **et** (C **et** d) peuvent être calculés (B **et** c) **et** (a **et** d) sans aucune modification dans le résultat logique.</span><span class="sxs-lookup"><span data-stu-id="08e5d-138">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (B **AND** C) **AND** (A **AND** D) with no change in the logical result.</span></span>

<span data-ttu-id="08e5d-139">Le tableau suivant décrit les types de termes de recherche de contenu.</span><span class="sxs-lookup"><span data-stu-id="08e5d-139">The following table describes the types of content search terms.</span></span>

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="08e5d-140">Type</span><span class="sxs-lookup"><span data-stu-id="08e5d-140">Type</span></span></th>
<th><span data-ttu-id="08e5d-141">Description</span><span class="sxs-lookup"><span data-stu-id="08e5d-141">Description</span></span></th>
<th><span data-ttu-id="08e5d-142">Exemples</span><span class="sxs-lookup"><span data-stu-id="08e5d-142">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="08e5d-143">Word</span><span class="sxs-lookup"><span data-stu-id="08e5d-143">Word</span></span></td>
<td><span data-ttu-id="08e5d-144">Mot unique sans espaces ni autres signes de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="08e5d-144">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="08e5d-145">Les guillemets doubles ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="08e5d-145">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><span data-ttu-id="08e5d-146">Expression</span><span class="sxs-lookup"><span data-stu-id="08e5d-146">Phrase</span></span></td>
<td><span data-ttu-id="08e5d-147">Plusieurs mots ou espaces inclus.</span><span class="sxs-lookup"><span data-stu-id="08e5d-147">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><span data-ttu-id="08e5d-148">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="08e5d-148">Wildcard</span></span></td>
<td><span data-ttu-id="08e5d-149">Mots ou expressions avec l’astérisque (\*) ajouté à la fin.</span><span class="sxs-lookup"><span data-stu-id="08e5d-149">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="08e5d-150">Pour plus d’informations, consultez <a href="-search-sql-wildcards.md">utilisation de caractères génériques dans le PRÉDICAT Contains</a>.</span><span class="sxs-lookup"><span data-stu-id="08e5d-150">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><span data-ttu-id="08e5d-151">Colonne de texte intégral</span><span class="sxs-lookup"><span data-stu-id="08e5d-151">Full-text Column</span></span></td>
<td><span data-ttu-id="08e5d-152">Nom de colonne de propriété par rapport auquel correspondre à la requête restante.</span><span class="sxs-lookup"><span data-stu-id="08e5d-152">A property column name against which to match the remaining query.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><span data-ttu-id="08e5d-153">Boolean</span><span class="sxs-lookup"><span data-stu-id="08e5d-153">Boolean</span></span></td>
<td><span data-ttu-id="08e5d-154">Mots, expressions et chaînes de caractères génériques combinés à l’aide des opérateurs booléens <strong>and</strong>, <strong>or</strong>ou <strong>not</strong>.</span><span class="sxs-lookup"><span data-stu-id="08e5d-154">Words, phrases, and wildcard strings combined by using the Boolean operators <strong>AND</strong>, <strong>OR</strong>, or <strong>NOT</strong>.</span></span> <span data-ttu-id="08e5d-155">Mettez les termes booléens entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="08e5d-155">Enclose the Boolean terms in double quotation marks.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><span data-ttu-id="08e5d-156">Rapproché</span><span class="sxs-lookup"><span data-stu-id="08e5d-156">Near</span></span></td>
<td><span data-ttu-id="08e5d-157">Mots, expressions ou caractères génériques séparés par la fonction NEAR.</span><span class="sxs-lookup"><span data-stu-id="08e5d-157">Words, phrases, or wildcards separated by the function NEAR.</span></span> <span data-ttu-id="08e5d-158">Pour plus d’informations, consultez à <a href="-search-sql-near.md">court terme</a>.</span><span class="sxs-lookup"><span data-stu-id="08e5d-158">For more information, see <a href="-search-sql-near.md">NEAR Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><span data-ttu-id="08e5d-159">FormsOf</span><span class="sxs-lookup"><span data-stu-id="08e5d-159">FormsOf</span></span></td>
<td><span data-ttu-id="08e5d-160">Correspond à un mot et aux versions fléchies de ce mot.</span><span class="sxs-lookup"><span data-stu-id="08e5d-160">Matches a word and the inflectional versions of that word.</span></span> <span data-ttu-id="08e5d-161">Pour plus d’informations, consultez <a href="-search-sql-formsof.md">terme FORMSOF</a>.</span><span class="sxs-lookup"><span data-stu-id="08e5d-161">For more information, see <a href="-search-sql-formsof.md">FORMSOF Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td><span data-ttu-id="08e5d-162">IsAbout</span><span class="sxs-lookup"><span data-stu-id="08e5d-162">IsAbout</span></span></td>
<td><span data-ttu-id="08e5d-163">Combine les résultats de correspondance sur plusieurs termes de recherche de mots, d’expressions ou de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="08e5d-163">Combines matching results over multiple word, phrase, or wildcard search terms.</span></span> <span data-ttu-id="08e5d-164">Chaque terme de recherche peut éventuellement être pondéré.</span><span class="sxs-lookup"><span data-stu-id="08e5d-164">Each search term can optionally be weighted.</span></span> <span data-ttu-id="08e5d-165">Vous pouvez éventuellement spécifier la méthode de calcul Rank, qui combine les pondérations et le nombre d’éléments correspondants dans le document.</span><span class="sxs-lookup"><span data-stu-id="08e5d-165">You can optionally specify the rank calculation method, which combines the weights and how many of the items the document matches.</span></span> <span data-ttu-id="08e5d-166">Pour plus d’informations, consultez <a href="-search-sql-isabout.md">terme ISABOUT</a>.</span><span class="sxs-lookup"><span data-stu-id="08e5d-166">For more information, see <a href="-search-sql-isabout.md">ISABOUT Term</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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

<span data-ttu-id="08e5d-167">Cette section comprend les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="08e5d-167">This section includes the following topics:</span></span>

- [<span data-ttu-id="08e5d-168">Utilisation de caractères génériques dans le prédicat CONTAINs</span><span class="sxs-lookup"><span data-stu-id="08e5d-168">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
- [<span data-ttu-id="08e5d-169">Terme FORMSOF</span><span class="sxs-lookup"><span data-stu-id="08e5d-169">FORMSOF Term</span></span>](-search-sql-formsof.md)
- [<span data-ttu-id="08e5d-170">Terme ISABOUT</span><span class="sxs-lookup"><span data-stu-id="08e5d-170">ISABOUT Term</span></span>](-search-sql-isabout.md)
- [<span data-ttu-id="08e5d-171">À court terme</span><span class="sxs-lookup"><span data-stu-id="08e5d-171">NEAR Term</span></span>](-search-sql-near.md)

## <a name="related-topics"></a><span data-ttu-id="08e5d-172">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="08e5d-172">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="08e5d-173">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="08e5d-173">Reference</span></span>

[<span data-ttu-id="08e5d-174">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="08e5d-174">WHERE Clause</span></span>](-search-sql-where.md)

### <a name="conceptual"></a><span data-ttu-id="08e5d-175">Conceptuel</span><span class="sxs-lookup"><span data-stu-id="08e5d-175">Conceptual</span></span>

[<span data-ttu-id="08e5d-176">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="08e5d-176">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)

[<span data-ttu-id="08e5d-177">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="08e5d-177">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
