---
description: Le terme proche est utilisé pour spécifier que deux termes de recherche de contenu doivent être relativement proches les uns des autres pour être reconnus comme correspondant au prédicat CONTAINs.
ms.assetid: cbc449b1-9f1d-42a2-b39e-d5cd69c052df
title: À court terme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4676ec8af80f674ca0b8124d8b4f941d0d6f4936
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318158"
---
# <a name="near-term"></a><span data-ttu-id="9ca1e-103">À court terme</span><span class="sxs-lookup"><span data-stu-id="9ca1e-103">NEAR Term</span></span>

<span data-ttu-id="9ca1e-104">Le terme proche est utilisé pour spécifier que deux termes de recherche de contenu doivent être relativement proches les uns des autres pour être reconnus comme correspondant au prédicat [Contains](-search-sql-contains.md) .</span><span class="sxs-lookup"><span data-stu-id="9ca1e-104">The NEAR term is used to specify that two content search terms must be relatively close to one another to be recognized as matching for the [CONTAINS](-search-sql-contains.md) predicate.</span></span>

<span data-ttu-id="9ca1e-105">La syntaxe du terme proche est la suivante :</span><span class="sxs-lookup"><span data-stu-id="9ca1e-105">The syntax for the NEAR term is:</span></span>


```
<content_search_term> NEAR | ~ <content_search_term>
```



<span data-ttu-id="9ca1e-106">Le terme proche peut être représenté par le mot clé « NEAR » ou par un tilde (~).</span><span class="sxs-lookup"><span data-stu-id="9ca1e-106">The NEAR term can be represented by the keyword "NEAR" or by a tilde (~).</span></span>

<span data-ttu-id="9ca1e-107">Lorsque les mots joints à proximité dans la requête se trouvent dans environ 50 mots l’un de l’autre à l’intérieur de la colonne dans laquelle la recherche est effectuée, le terme proche retourne une correspondance.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-107">When the words joined by NEAR in the query are found within approximately 50 words of each other inside the column being searched, the NEAR term returns a match.</span></span> <span data-ttu-id="9ca1e-108">Plus les deux mots sont proches, plus le classement calculé est élevé pour le terme proche.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-108">The closer together the two words are, the higher the calculated rank for the NEAR term.</span></span> <span data-ttu-id="9ca1e-109">Plus les deux mots sont éloignés, plus le rang est bas.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-109">The farther apart the two words are, the lower the rank.</span></span>

> [!Note]  
> <span data-ttu-id="9ca1e-110">Le nombre de mots entre les termes de recherche trouvés est approximatif et dépend de l’apparence des mots parasites, tels que « a » ou « The », et de la manière dont séparateurs le texte.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-110">The number of words between found search terms is approximate and depends on the appearance of noise words, like "a" or "the", and how wordbreakers tokenize text.</span></span> <span data-ttu-id="9ca1e-111">Il peut être inférieur à 50.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-111">It may be less than 50.</span></span>

 


<span data-ttu-id="9ca1e-112">Le tableau suivant décrit les types de terme de recherche de contenu qui peuvent être utilisés avec un terme proche dans un prédicat CONTAINs.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-112">The following table describes content search term types that can be used with a NEAR term in a CONTAINS predicate.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9ca1e-113">Type</span><span class="sxs-lookup"><span data-stu-id="9ca1e-113">Type</span></span></th>
<th><span data-ttu-id="9ca1e-114">Description</span><span class="sxs-lookup"><span data-stu-id="9ca1e-114">Description</span></span></th>
<th><span data-ttu-id="9ca1e-115">Exemples</span><span class="sxs-lookup"><span data-stu-id="9ca1e-115">Examples</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9ca1e-116">Word</span><span class="sxs-lookup"><span data-stu-id="9ca1e-116">Word</span></span></td>
<td><span data-ttu-id="9ca1e-117">Mot unique sans espaces ni autres signes de ponctuation.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-117">A single word without spaces or other punctuation.</span></span> <span data-ttu-id="9ca1e-118">Les guillemets doubles ne sont pas nécessaires.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-118">Double quotation marks are not necessary.</span></span></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;computer NEAR software)&#39;)</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="9ca1e-119">Expression</span><span class="sxs-lookup"><span data-stu-id="9ca1e-119">Phrase</span></span></td>
<td><span data-ttu-id="9ca1e-120">Plusieurs mots ou espaces inclus.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-120">Multiple words or included spaces.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;computer software&quot; NEAR hardware)&#39;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9ca1e-121">Caractère générique</span><span class="sxs-lookup"><span data-stu-id="9ca1e-121">Wildcard</span></span></td>
<td><span data-ttu-id="9ca1e-122">Mots ou expressions avec l’astérisque (\*) ajouté à la fin.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-122">Words or phrases with the asterisk (\*) added to the end.</span></span> <span data-ttu-id="9ca1e-123">Pour plus d’informations, consultez <a href="-search-sql-wildcards.md">utilisation de caractères génériques dans le PRÉDICAT Contains</a>.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-123">For more information, see <a href="-search-sql-wildcards.md">Using Wildcards in the CONTAINS Predicate</a>.</span></span></td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>...WHERE CONTAINS(&#39;&quot;compu*&quot; NEAR &quot;soft*&quot;&#39;)</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>

> [!Note]  
> <span data-ttu-id="9ca1e-124">Si les mots de correspondance spécifiés avec le terme proche se trouvent tous deux dans la colonne recherchée, mais qu’ils sont plus éloignés de 50 mots, le résultat est toujours retourné, mais a un [rang](-search-sql-understandingrelevancevalues.md) égal à 0.</span><span class="sxs-lookup"><span data-stu-id="9ca1e-124">If the match words specified with the NEAR term are both found in the column being searched, but are farther apart than 50 words, the result is still returned, but has a [rank](-search-sql-understandingrelevancevalues.md) of 0.</span></span>

 

### <a name="example"></a><span data-ttu-id="9ca1e-125">Exemple</span><span class="sxs-lookup"><span data-stu-id="9ca1e-125">Example</span></span>

<span data-ttu-id="9ca1e-126">L’exemple suivant illustre le chaînage de près des termes, à l’aide des formes courtes et longues du terme :</span><span class="sxs-lookup"><span data-stu-id="9ca1e-126">The following example shows chaining of NEAR terms, using both the short and long forms of the term:</span></span>


```
...WHERE CONTAINS('computer NEAR software ~ "setup application"')
```



## <a name="related-topics"></a><span data-ttu-id="9ca1e-127">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="9ca1e-127">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="9ca1e-128">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="9ca1e-128">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9ca1e-129">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="9ca1e-129">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="9ca1e-130">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="9ca1e-130">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="9ca1e-131">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="9ca1e-131">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="9ca1e-132">Utilisation de caractères génériques dans le prédicat CONTAINs</span><span class="sxs-lookup"><span data-stu-id="9ca1e-132">Using Wildcards in the CONTAINS Predicate</span></span>](-search-sql-wildcards.md)
</dt> </dl>

 

 



