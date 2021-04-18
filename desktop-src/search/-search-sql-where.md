---
description: Les conditions qui déterminent si un document est inclus dans les résultats retournés par la requête sont spécifiées par la clause WHERE.
ms.assetid: e3b5ee92-e817-49b8-aa8b-5d68254bb819
title: WHERE, clause (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45a37334d656b0a321abdcdd4a5d045eb9d4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515983"
---
# <a name="where-clause-windows-search"></a><span data-ttu-id="17031-103">WHERE, clause (Windows Search)</span><span class="sxs-lookup"><span data-stu-id="17031-103">WHERE Clause (Windows Search)</span></span>

<span data-ttu-id="17031-104">Les conditions qui déterminent si un document est inclus dans les résultats retournés par la requête sont spécifiées par la clause WHERE.</span><span class="sxs-lookup"><span data-stu-id="17031-104">The conditions that determine whether a document is included in the results returned by the query are specified by the WHERE clause.</span></span> <span data-ttu-id="17031-105">Au niveau le plus élevé, la syntaxe de la clause WHERE comporte deux parties :</span><span class="sxs-lookup"><span data-stu-id="17031-105">At the highest level, there are two parts to the WHERE clause syntax:</span></span>


```
...WHERE [<group_aliases>] <search_condition>
...WHERE ReuseWhere(<WHEREID>)
```



<span data-ttu-id="17031-106">L’alias de groupe <facultatif \_> partie de la clause simplifie les requêtes complexes en affectant un alias à un groupe d’une ou de plusieurs colonnes.</span><span class="sxs-lookup"><span data-stu-id="17031-106">The optional <group\_alias> portion of the clause simplifies complex queries by assigning an alias to a group of one or more columns.</span></span> <span data-ttu-id="17031-107">Cela peut améliorer la lisibilité des requêtes complexes qui recherchent les mêmes informations sur plusieurs colonnes spécifiées par des URL.</span><span class="sxs-lookup"><span data-stu-id="17031-107">This can improve the readability of complex queries that search for the same information across multiple columns specified by URLs.</span></span> <span data-ttu-id="17031-108">Pour plus d’informations sur les alias de groupe, consultez [with--As Group alias Predicate](-search-sql-with-as.md).</span><span class="sxs-lookup"><span data-stu-id="17031-108">For more information about group aliases, see [WITH -- AS Group Alias Predicate](-search-sql-with-as.md).</span></span>

<span data-ttu-id="17031-109">La <search condition> partie de la clause WHERE est un ou plusieurs prédicats de recherche qui spécifient des critères de correspondance pour la recherche.</span><span class="sxs-lookup"><span data-stu-id="17031-109">The <search condition> portion of the WHERE clause is one or more search predicates that specify matching criteria for the search.</span></span> <span data-ttu-id="17031-110">Les prédicats de recherche sont des expressions qui déclarent des faits sur une valeur.</span><span class="sxs-lookup"><span data-stu-id="17031-110">Search predicates are expressions that assert some fact about some value.</span></span>

<span data-ttu-id="17031-111">Le résultat d’une condition de recherche est une valeur booléenne, soit **true** si le document remplit les conditions de recherche spécifiées, soit **false** dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="17031-111">The result of a search condition is a Boolean value, either **TRUE** if the document meets the specified search conditions, or **FALSE** if it does not.</span></span> <span data-ttu-id="17031-112">Si le résultat est **true**, le document est retourné.</span><span class="sxs-lookup"><span data-stu-id="17031-112">If the result is **TRUE**, the document is returned.</span></span> <span data-ttu-id="17031-113">Si le résultat est **false**, le document n’est pas retourné.</span><span class="sxs-lookup"><span data-stu-id="17031-113">If the result is **FALSE**, the document is not returned.</span></span> <span data-ttu-id="17031-114">Les valeurs de classement des documents renvoyés dans une requête de recherche Microsoft Windows sont attribuées en fonction de leur correspondance avec les conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="17031-114">Documents returned in a Microsoft Windows Search query are assigned rank values according to how well they match the search conditions.</span></span> <span data-ttu-id="17031-115">Chacune des conditions de recherche de requête peut inclure une clause [RANKBY](-search-sql-rankby.md) qui prend en charge la modification des valeurs de classement retournées.</span><span class="sxs-lookup"><span data-stu-id="17031-115">Each of the query search conditions can include a [RANKBY](-search-sql-rankby.md) clause that supports modifying the returned rank values.</span></span>

<span data-ttu-id="17031-116">La [fonction ReuseWhere](-search-sql-reusewhere.md) rend plus efficace plusieurs requêtes qui utilisent certaines des mêmes conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="17031-116">The [ReuseWhere function](-search-sql-reusewhere.md) makes multiple queries that use the some of the same search conditions more efficient.</span></span> <span data-ttu-id="17031-117">La clause WHERE d’une requête spécifie l’ensemble des éléments qui correspondent dans une requête.</span><span class="sxs-lookup"><span data-stu-id="17031-117">The WHERE clause in a query specifies the set of items that match in a query.</span></span> <span data-ttu-id="17031-118">Les requêtes suivantes peuvent partager le travail effectué pour le évaluation précédent à l’aide de la fonction ReuseWhere dans la nouvelle clause WHERE de la requête.</span><span class="sxs-lookup"><span data-stu-id="17031-118">Subsequent queries can share the work performed for the previous evalution by using the ReuseWhere function in the new query WHERE clause.</span></span>

## <a name="search-predicates"></a><span data-ttu-id="17031-119">Prédicats de recherche</span><span class="sxs-lookup"><span data-stu-id="17031-119">Search Predicates</span></span>

<span data-ttu-id="17031-120">Une condition de recherche se compose d’un ou de plusieurs prédicats ou conditions de recherche qui décrivent ce que l’utilisateur recherche (par exemple, où System. DateCreated > ' 2006-04-19 ').</span><span class="sxs-lookup"><span data-stu-id="17031-120">A search condition consists of one or more predicates or search conditions that describe what the user is searching for (for example, WHERE System.DateCreated >'2006-04-19').</span></span> <span data-ttu-id="17031-121">Les prédicats de recherche peuvent être combinés à l’aide des opérateurs logiques **and**, **or** ou **not**.</span><span class="sxs-lookup"><span data-stu-id="17031-121">Search predicates can be combined using the logical operators **AND**, **OR**, or **NOT**.</span></span> <span data-ttu-id="17031-122">L’opérateur unaire facultatif **ne peut pas** être utilisé avec **et** et uniquement pour nier la valeur logique d’un prédicat ou d’une condition de recherche.</span><span class="sxs-lookup"><span data-stu-id="17031-122">The optional unary operator **NOT** can be used only with **AND** and only to negate the logical value of a predicate or search condition.</span></span> <span data-ttu-id="17031-123">Vous pouvez utiliser des parenthèses pour regrouper et imbriquer des termes logiques.</span><span class="sxs-lookup"><span data-stu-id="17031-123">You can use parentheses to group and nest logical terms.</span></span>

<span data-ttu-id="17031-124">Le tableau suivant indique l’ordre de priorité des opérateurs logiques.</span><span class="sxs-lookup"><span data-stu-id="17031-124">The following table shows the order of precedence for the logical operators.</span></span>



| <span data-ttu-id="17031-125">Ordre (priorité)</span><span class="sxs-lookup"><span data-stu-id="17031-125">Order (precedence)</span></span> | <span data-ttu-id="17031-126">Opérateur logique</span><span class="sxs-lookup"><span data-stu-id="17031-126">Logical operator</span></span> |
|--------------------|------------------|
| <span data-ttu-id="17031-127">Premier (le plus élevé)</span><span class="sxs-lookup"><span data-stu-id="17031-127">First (highest)</span></span>    | <span data-ttu-id="17031-128">**NOT**</span><span class="sxs-lookup"><span data-stu-id="17031-128">**NOT**</span></span>          |
| <span data-ttu-id="17031-129">Seconde</span><span class="sxs-lookup"><span data-stu-id="17031-129">Second</span></span>             | <span data-ttu-id="17031-130">**AND**</span><span class="sxs-lookup"><span data-stu-id="17031-130">**AND**</span></span>          |
| <span data-ttu-id="17031-131">Troisième (le plus bas)</span><span class="sxs-lookup"><span data-stu-id="17031-131">Third (lowest)</span></span>     | <span data-ttu-id="17031-132">**OR**</span><span class="sxs-lookup"><span data-stu-id="17031-132">**OR**</span></span>           |



 

<span data-ttu-id="17031-133">Les opérateurs logiques du même type sont associatifs et il n’y a pas d’ordre de calcul spécifié.</span><span class="sxs-lookup"><span data-stu-id="17031-133">Logical operators of the same type are associative, and there is no specified calculation order.</span></span> <span data-ttu-id="17031-134">Par exemple, les points (A **et** b) **et** (C **et** d) peuvent être calculés (a **et** d) **et** (B **et** c) sans aucune modification dans le résultat logique.</span><span class="sxs-lookup"><span data-stu-id="17031-134">For example, (A **AND** B) **AND** (C **AND** D) can be calculated (A **AND** D) **AND** (B **AND** C) with no change in the logical result.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="17031-135">Incorrect : où **ne contient pas** ('Computer')</span><span class="sxs-lookup"><span data-stu-id="17031-135">Incorrect: WHERE **NOT** CONTAINS ('computer')</span></span>
>
> <span data-ttu-id="17031-136">Correct : WHERE CONTAINs ('Software') **et not** Contains ('Computer')</span><span class="sxs-lookup"><span data-stu-id="17031-136">Correct: WHERE CONTAINS ('software') **AND NOT** CONTAINS ('computer')</span></span>

 

<span data-ttu-id="17031-137">Dans les requêtes complexes, vous souhaiterez peut-être mettre l’accent sur les correspondances dans certaines colonnes que dans d’autres.</span><span class="sxs-lookup"><span data-stu-id="17031-137">In complex queries, you might want to place more emphasis on matches in some columns than in others.</span></span> <span data-ttu-id="17031-138">Par exemple, lors de la recherche de documents qui traitent de la « conception de logiciels », Rechercher le terme de recherche dans le titre du document est plus susceptible d’être une correspondance correcte que de trouver les mots individuels dans le texte du document.</span><span class="sxs-lookup"><span data-stu-id="17031-138">For example, when searching for documents that discuss "software design", finding the search term in the document title is more likely to be a good match than finding the individual words in the text of the document.</span></span> <span data-ttu-id="17031-139">Pour influencer le classement des documents de cette manière, le langage de requête de recherche Microsoft Windows prend en charge la pondération des conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="17031-139">To influence the ranking of documents in this manner, the Microsoft Windows Search query language supports weighting the search conditions.</span></span> <span data-ttu-id="17031-140">Pour plus d’informations sur la pondération des colonnes, consultez [Contains Predicate](-search-sql-contains.md) et [FREETEXT Predicate](-search-sql-freetext.md).</span><span class="sxs-lookup"><span data-stu-id="17031-140">For more information about column weighting, see [CONTAINS Predicate](-search-sql-contains.md) and [FREETEXT Predicate](-search-sql-freetext.md).</span></span>

<span data-ttu-id="17031-141">Il existe trois groupes de prédicats de recherche dans Windows Search : recherches en texte intégral, non en texte intégral et profondeur de dossier.</span><span class="sxs-lookup"><span data-stu-id="17031-141">There are three groups of search predicates in Windows Search: full-text, non-full-text, and folder depth searches.</span></span> <span data-ttu-id="17031-142">Les prédicats de recherche en texte intégral correspondent généralement à la signification du contenu, du titre et d’autres colonnes, et prennent en charge la mise en correspondance linguistique (par exemple, les autres formes de mots, expressions et recherches de proximité).</span><span class="sxs-lookup"><span data-stu-id="17031-142">Full-text search predicates typically match the meaning of the content, title, and other columns, and support linguistic matching (for example, alternative word forms, phrases, and proximity searching).</span></span> <span data-ttu-id="17031-143">En revanche, les prédicats de recherche de texte non intégral correspondent à la valeur des colonnes spécifiées et n’incluent pas de traitement linguistique spécial, mais dans plusieurs cas, elles offrent des critères spéciaux basés sur des caractères.</span><span class="sxs-lookup"><span data-stu-id="17031-143">In contrast, non-full-text search predicates match the value of the specified columns and do not include any special linguistic processing, but in several cases offer character-based pattern matching.</span></span> <span data-ttu-id="17031-144">Les prédicats de profondeur de dossier limitent l’étendue de recherche à un chemin d’accès spécifié.</span><span class="sxs-lookup"><span data-stu-id="17031-144">Folder depth predicates restrict the search scope to a specified path.</span></span>

> [!Note]  
> <span data-ttu-id="17031-145">Si la requête retourne un document parce qu’un prédicat de texte non intégral prend la valeur **true** pour ce document, la valeur de classement est calculée comme 1000.</span><span class="sxs-lookup"><span data-stu-id="17031-145">If the query returns a document because a non-full-text predicate evaluates to **TRUE** for that document, the rank value is calculated as 1000.</span></span> <span data-ttu-id="17031-146">L’utilisation de la [fonction de forçage de rang](-search-sql-rankby.md) peut modifier la valeur de classement.</span><span class="sxs-lookup"><span data-stu-id="17031-146">Using the [rank coercion function](-search-sql-rankby.md) can modify the rank value.</span></span>

 

<span data-ttu-id="17031-147">Les tableaux suivants décrivent les prédicats de recherche en texte intégral, non en texte intégral et profondeur de dossier.</span><span class="sxs-lookup"><span data-stu-id="17031-147">The following tables describe the full-text, non-full-text, and folder depth search predicates.</span></span>



| <span data-ttu-id="17031-148">Prédicat de texte intégral</span><span class="sxs-lookup"><span data-stu-id="17031-148">Full-text predicate</span></span>                  | <span data-ttu-id="17031-149">Description</span><span class="sxs-lookup"><span data-stu-id="17031-149">Description</span></span>                                                                                                                                                                                                                                                      |
|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17031-150">CONTAINS</span><span class="sxs-lookup"><span data-stu-id="17031-150">CONTAINS</span></span>](-search-sql-contains.md) | <span data-ttu-id="17031-151">Prend en charge les recherches complexes de termes dans les colonnes de texte de document (par exemple, titre, contenu).</span><span class="sxs-lookup"><span data-stu-id="17031-151">Supports complex searches for terms in document text columns (for example, title, contents).</span></span> <span data-ttu-id="17031-152">Peut rechercher les formes fléchies des termes recherchés, tester la proximité des termes et effectuer des comparaisons logiques.</span><span class="sxs-lookup"><span data-stu-id="17031-152">Can search for inflected forms of the search terms, test for proximity of the terms, and perform logical comparisons.</span></span> <span data-ttu-id="17031-153">Les termes de recherche peuvent inclure des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="17031-153">Search terms can include wildcard characters.</span></span> |
| [<span data-ttu-id="17031-154">FREETEXT</span><span class="sxs-lookup"><span data-stu-id="17031-154">FREETEXT</span></span>](-search-sql-freetext.md) | <span data-ttu-id="17031-155">Recherche des documents qui correspondent à la signification de l’expression de recherche.</span><span class="sxs-lookup"><span data-stu-id="17031-155">Searches for documents that match the meaning of the search phrase.</span></span> <span data-ttu-id="17031-156">Les mots connexes et les expressions similaires correspondent, avec la colonne de classement calculée en fonction de la précision du document par rapport à l’expression de recherche.</span><span class="sxs-lookup"><span data-stu-id="17031-156">Related words and similar phrases will match, with the rank column calculated based on how closely the document matches the search phrase.</span></span> <span data-ttu-id="17031-157">Les termes de recherche ne peuvent pas contenir de caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="17031-157">Search terms cannot include wildcard characters.</span></span>  |



 



| <span data-ttu-id="17031-158">Prédicat de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="17031-158">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="17031-159">Description</span><span class="sxs-lookup"><span data-stu-id="17031-159">Description</span></span>                                                                                                                                                                           |
|----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17031-160">LIKE</span><span class="sxs-lookup"><span data-stu-id="17031-160">LIKE</span></span>](-search-sql-like.md)                                               | <span data-ttu-id="17031-161">Les valeurs de colonne sont comparées à l’aide de critères spéciaux simples avec des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="17031-161">Column values are compared using simple pattern matching with wildcard characters.</span></span>                                                                                                    |
| [<span data-ttu-id="17031-162">Comparaison de valeurs littérales</span><span class="sxs-lookup"><span data-stu-id="17031-162">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="17031-163">Les valeurs de colonne sont comparées aux valeurs de chaîne, de date, d’horodatage, numériques et d’autres valeurs littérales.</span><span class="sxs-lookup"><span data-stu-id="17031-163">Column values are compared against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="17031-164">Ce prédicat prend en charge l’égalité et les inégales telles que supérieur à et inférieur à.</span><span class="sxs-lookup"><span data-stu-id="17031-164">This predicate supports equality and inequalities such as greater than and less than.</span></span> |
| [<span data-ttu-id="17031-165">Comparaisons à valeurs multiples (tableau)</span><span class="sxs-lookup"><span data-stu-id="17031-165">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="17031-166">Les colonnes à valeurs multiples sont comparées à un tableau de littéraux à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="17031-166">Multivalued columns are compared against a multivalued array of literals.</span></span>                                                                                                             |
| [<span data-ttu-id="17031-167">NULL</span><span class="sxs-lookup"><span data-stu-id="17031-167">NULL</span></span>](-search-sql-null.md)                                               | <span data-ttu-id="17031-168">Les valeurs de colonne qui ne sont pas définies pour le document peuvent être détectées à l’aide du prédicat **null** .</span><span class="sxs-lookup"><span data-stu-id="17031-168">Column values that are undefined for the document can be detected by using the **NULL** predicate.</span></span>                                                                                    |



 



| <span data-ttu-id="17031-169">Profondeur du dossier</span><span class="sxs-lookup"><span data-stu-id="17031-169">Folder Depth</span></span>                             | <span data-ttu-id="17031-170">Description</span><span class="sxs-lookup"><span data-stu-id="17031-170">Description</span></span>                                                                                        |
|------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="17031-171">ÉTENDUE</span><span class="sxs-lookup"><span data-stu-id="17031-171">SCOPE</span></span>](-search-sql-folderdepth.md)     | <span data-ttu-id="17031-172">Effectue une traversée profonde du chemin d’accès spécifié, y compris le dossier spécifique et tous les sous-dossiers.</span><span class="sxs-lookup"><span data-stu-id="17031-172">Performs a deep traversal of the specified path, including the specific folder and all subfolders.</span></span> |
| [<span data-ttu-id="17031-173">DIRECTORY</span><span class="sxs-lookup"><span data-stu-id="17031-173">DIRECTORY</span></span>](-search-sql-folderdepth.md) | <span data-ttu-id="17031-174">Effectue un parcours superficiel du chemin d’accès spécifié, en recherchant uniquement le dossier spécifique.</span><span class="sxs-lookup"><span data-stu-id="17031-174">Performs a shallow traversal of the specified path, searching only the specific folder.</span></span>            |



 

## <a name="examples"></a><span data-ttu-id="17031-175">Exemples</span><span class="sxs-lookup"><span data-stu-id="17031-175">Examples</span></span>

<span data-ttu-id="17031-176">Pour obtenir des exemples de la clause WHERE, consultez les rubriques de prédicat individuelles liées dans le tableau précédent.</span><span class="sxs-lookup"><span data-stu-id="17031-176">For examples of the WHERE clause, see the individual predicate topics linked in the preceding table.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17031-177">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17031-177">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="17031-178">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="17031-178">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="17031-179">ReuseWhere fonction)</span><span class="sxs-lookup"><span data-stu-id="17031-179">ReuseWhere function</span></span>](-search-sql-reusewhere.md)
</dt> <dt>

[<span data-ttu-id="17031-180">Propriétés du rowset</span><span class="sxs-lookup"><span data-stu-id="17031-180">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> <dt>

[<span data-ttu-id="17031-181">FROM, clause</span><span class="sxs-lookup"><span data-stu-id="17031-181">FROM Clause</span></span>](-search-sql-from.md)
</dt> <dt>

[<span data-ttu-id="17031-182">Vue d’ensemble de la syntaxe de recherche SQL</span><span class="sxs-lookup"><span data-stu-id="17031-182">Overview of the Search SQL Syntax</span></span>](-search-sql-ovwofsearchquery.md)
</dt> <dt>

[<span data-ttu-id="17031-183">Prédicat WITH--AS Group alias</span><span class="sxs-lookup"><span data-stu-id="17031-183">WITH -- AS Group Alias Predicate</span></span>](-search-sql-with-as.md)
</dt> <dt>

[<span data-ttu-id="17031-184">Prédicats d’étendue et de répertoire</span><span class="sxs-lookup"><span data-stu-id="17031-184">SCOPE and DIRECTORY Predicates</span></span>](-search-sql-folderdepth.md)
</dt> <dt>

[<span data-ttu-id="17031-185">RANK BY, clause</span><span class="sxs-lookup"><span data-stu-id="17031-185">RANK BY Clause</span></span>](-search-sql-rankby.md)
</dt> <dt>

<span data-ttu-id="17031-186">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="17031-186">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="17031-187">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="17031-187">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> <dt>

[<span data-ttu-id="17031-188">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="17031-188">Non-Full-Text Predicates</span></span>](-search-sql-nonfulltextpredicates.md)
</dt> </dl>

 

 



