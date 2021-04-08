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
# <a name="freetext-predicate"></a><span data-ttu-id="826ae-103">Prédicat FREETEXT</span><span class="sxs-lookup"><span data-stu-id="826ae-103">FREETEXT Predicate</span></span>

<span data-ttu-id="826ae-104">Le prédicat FREETEXT fait partie de la clause [Where](-search-sql-where.md) et prend en charge la recherche de mots et d’expressions dans des colonnes de texte.</span><span class="sxs-lookup"><span data-stu-id="826ae-104">The FREETEXT predicate is part of the [WHERE](-search-sql-where.md) clause and supports searching for words and phrases in text columns.</span></span> <span data-ttu-id="826ae-105">Utilisez le prédicat FREETEXT pour rechercher des documents contenant des combinaisons de mots recherchés répartis dans le contenu ou les colonnes spécifiés.</span><span class="sxs-lookup"><span data-stu-id="826ae-105">Use the FREETEXT predicate to find documents containing combinations of the search words spread throughout the content or columns specified.</span></span> <span data-ttu-id="826ae-106">Pour obtenir la valeur de classement, incluez System. Search. Rank, qui est un classement de pertinence, en tant que colonne dans l’instruction SELECT.</span><span class="sxs-lookup"><span data-stu-id="826ae-106">To get the rank value, include System.Search.Rank, which is a ranking of relevence, as a column in the SELECT statment.</span></span>

<span data-ttu-id="826ae-107">Le prédicat FREETEXT a la syntaxe suivante :</span><span class="sxs-lookup"><span data-stu-id="826ae-107">The FREETEXT predicate has the following syntax:</span></span>


```
FREETEXT
(["<fulltext_column>",]'<freetext_condition>'[,<LCID>])...
```



<span data-ttu-id="826ae-108">La référence de colonne de texte intégral est facultative.</span><span class="sxs-lookup"><span data-stu-id="826ae-108">The fulltext column reference is optional.</span></span> <span data-ttu-id="826ae-109">Avec elle, vous pouvez spécifier une colonne unique ou un [alias de regroupement de colonnes](-search-sql-with-as.md) sur lequel le prédicat FREETEXT est testé.</span><span class="sxs-lookup"><span data-stu-id="826ae-109">With it, you can specify a single column, or a [column grouping alias](-search-sql-with-as.md) against which the FREETEXT predicate is tested.</span></span> <span data-ttu-id="826ae-110">Lorsque la colonne de texte intégral est spécifiée comme « ALL » ou « \* », toutes les propriétés de texte indexées sont recherchées.</span><span class="sxs-lookup"><span data-stu-id="826ae-110">When the fulltext column is specified as "ALL" or "\*", all indexed text properties are searched.</span></span> <span data-ttu-id="826ae-111">Bien qu’il ne soit pas nécessaire que la colonne soit une propriété de texte, les résultats peuvent être incompréhensibles si la colonne est d’un autre type de données.</span><span class="sxs-lookup"><span data-stu-id="826ae-111">Although the column is not required to be a text property, the results might be meaningless if the column is some other data type.</span></span> <span data-ttu-id="826ae-112">Le nom de colonne peut être un [identificateur](-search-sql-identifiers.md)standard ou délimité, et vous devez le séparer de la condition par une virgule.</span><span class="sxs-lookup"><span data-stu-id="826ae-112">The column name can be either a regular or delimited [identifier](-search-sql-identifiers.md), and you must separate it from the condition by a comma.</span></span> <span data-ttu-id="826ae-113">Si aucune condition de texte intégral n’est fournie, la colonne contents, qui est le corps du document, est utilisée.</span><span class="sxs-lookup"><span data-stu-id="826ae-113">If no fulltext condition is supplied, the Contents column, which is the body of the document, is used.</span></span>

<span data-ttu-id="826ae-114">Vous pouvez spécifier des paramètres régionaux de recherche pour identifier l’analyseur lexical et les formes fléchies appropriées pour la requête de recherche.</span><span class="sxs-lookup"><span data-stu-id="826ae-114">You can specify a search locale to identify the appropriate word breaker and inflectional forms for the search query.</span></span> <span data-ttu-id="826ae-115">Les valeurs de paramètres régionaux valides sont un identificateur de code (LCID) de langue Windows standard.</span><span class="sxs-lookup"><span data-stu-id="826ae-115">Valid locale values are a Windows standard language code identifier (LCID).</span></span> <span data-ttu-id="826ae-116">Par exemple, 1033 est le LCID de États-Unis-anglais.</span><span class="sxs-lookup"><span data-stu-id="826ae-116">For example, 1033 is the LCID for United States-English.</span></span> <span data-ttu-id="826ae-117">Placez le LCID en tant que dernier élément à l’intérieur des parenthèses de la clause FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="826ae-117">Place the LCID as the last item inside the parentheses of the FREETEXT clause.</span></span> <span data-ttu-id="826ae-118">Pour obtenir des informations importantes sur la recherche et les langages, consultez [utilisation des recherches localisées](-search-sql-usinglocsearches.md).</span><span class="sxs-lookup"><span data-stu-id="826ae-118">For important information about searching and languages, see [Using Localized Searches](-search-sql-usinglocsearches.md).</span></span>

> [!Note]  
> <span data-ttu-id="826ae-119">Les paramètres régionaux de recherche par défaut sont les paramètres régionaux par défaut du système.</span><span class="sxs-lookup"><span data-stu-id="826ae-119">The default search locale is the system default locale.</span></span>

 

<span data-ttu-id="826ae-120">Vous devez placer la partie de la condition FREETEXT entre guillemets simples, et elle doit comporter un ou plusieurs termes de recherche.</span><span class="sxs-lookup"><span data-stu-id="826ae-120">You must enclose the freetext condition portion in single quotation marks, and it must consist of one or more search terms.</span></span> <span data-ttu-id="826ae-121">Le prédicat FREETEXT ne prend pas en charge les opérations logiques.</span><span class="sxs-lookup"><span data-stu-id="826ae-121">The FREETEXT predicate does not support logical operations.</span></span> <span data-ttu-id="826ae-122">Pour rechercher une expression comme s’il s’agissait d’un mot unique, placez l’expression entre guillemets doubles.</span><span class="sxs-lookup"><span data-stu-id="826ae-122">To search for a phrase as if it were a single word, enclose the phrase in double quotation marks.</span></span>

<span data-ttu-id="826ae-123">Lorsque vous utilisez le prédicat FREETEXT, les résultats de la requête de recherche retournent des documents contenant tous les termes recherchés.</span><span class="sxs-lookup"><span data-stu-id="826ae-123">When you use the FREETEXT predicate, the search query results return documents containing all of the search terms.</span></span> <span data-ttu-id="826ae-124">Les termes n’ont pas besoin d’apparaître dans un ordre particulier.</span><span class="sxs-lookup"><span data-stu-id="826ae-124">The terms do not need to appear in any particular order.</span></span> <span data-ttu-id="826ae-125">Les documents qui contiennent davantage de termes de recherche ont des valeurs de colonne de classement plus élevées.</span><span class="sxs-lookup"><span data-stu-id="826ae-125">Documents that contain more of the search terms have higher rank column values.</span></span>

## <a name="examples"></a><span data-ttu-id="826ae-126">Exemples</span><span class="sxs-lookup"><span data-stu-id="826ae-126">Examples</span></span>

<span data-ttu-id="826ae-127">L’exemple suivant recherche des documents contenant « Computer », « Software », « Hardware » ou des combinaisons de ces mots :</span><span class="sxs-lookup"><span data-stu-id="826ae-127">The following example searches for documents containing "computer", "software", "hardware", or combinations of those words:</span></span>


```
WHERE FREETEXT('computer software hardware')
```



> [!Note]  
> <span data-ttu-id="826ae-128">Vous ne pouvez pas utiliser les correspondances de mots simples et d’expressions dans le même prédicat FREETEXT.</span><span class="sxs-lookup"><span data-stu-id="826ae-128">You cannot use both single-word matching and phrase matching in the same FREETEXT predicate.</span></span>

 

<span data-ttu-id="826ae-129">Lors de l’exécution de requêtes avec des contractions, vous devez placer les guillemets dans une séquence d’échappement dans la contraction lors de l’utilisation de FREETEXT, mais pas lors de l’utilisation de CONTAINs.</span><span class="sxs-lookup"><span data-stu-id="826ae-129">When performing queries with contractions, you must escape the quotation mark in the contraction when using FREETEXT, but not when using CONTAINS.</span></span>

<span data-ttu-id="826ae-130">Par exemple, la syntaxe suivante échoue :</span><span class="sxs-lookup"><span data-stu-id="826ae-130">For example, the following syntax fails:</span></span>


```
WHERE FREETEXT(*,'"We'll meet next week"')
```



<span data-ttu-id="826ae-131">La syntaxe correcte comprend deux guillemets simples, et non un guillemet double.</span><span class="sxs-lookup"><span data-stu-id="826ae-131">The correct syntax includes two single quotation marks, not a double quotation mark.</span></span>

<span data-ttu-id="826ae-132">La syntaxe suivante est réussie :</span><span class="sxs-lookup"><span data-stu-id="826ae-132">The following syntax succeeds:</span></span>


```
WHERE FREETEXT(*,'"We''ll meet next week"')
```



## <a name="related-topics"></a><span data-ttu-id="826ae-133">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="826ae-133">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="826ae-134">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="826ae-134">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="826ae-135">CONTAINs, prédicat</span><span class="sxs-lookup"><span data-stu-id="826ae-135">CONTAINS Predicate</span></span>](-search-sql-contains.md)
</dt> <dt>

[<span data-ttu-id="826ae-136">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="826ae-136">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

<span data-ttu-id="826ae-137">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="826ae-137">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="826ae-138">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="826ae-138">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



