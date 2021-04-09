---
description: Le langage SQL de recherche Windows (SQL) est similaire à une requête SQL standard.
ms.assetid: 7d992fa2-4606-46ca-904c-b45056a9bbc2
title: Vue d’ensemble de la syntaxe SQL de Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff6a755312e4358dc2eaa9ea7ae97f22ef783f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104033881"
---
# <a name="overview-of-windows-search-sql-syntax"></a><span data-ttu-id="4dcf0-103">Vue d’ensemble de la syntaxe SQL de Windows Search</span><span class="sxs-lookup"><span data-stu-id="4dcf0-103">Overview of Windows Search SQL Syntax</span></span>

<span data-ttu-id="4dcf0-104">Le langage SQL de recherche Windows (SQL) est similaire à une requête SQL standard.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-104">The Windows Search Structured Query Language (SQL) is similar to a standard SQL query.</span></span> <span data-ttu-id="4dcf0-105">Il est illustré dans les deux syntaxes suivantes :</span><span class="sxs-lookup"><span data-stu-id="4dcf0-105">It is shown in the following two syntaxes:</span></span>


```SQL
SELECT [TOP <positive integer>] <columns>
FROM [machinename.]SystemIndex
[WHERE <conditions>]
[ORDER BY <column>]
```

```SQL
GROUP ON <column> [<ranges>]
[AGGREGATE <aggregate_list>]
[ORDER BY <column> [ASC/DESC]]
OVER (<GROUP ON ...> | <SELECT...>) 
```

<span data-ttu-id="4dcf0-106">Dans l’exemple de requête suivant, les valeurs nombre de pages et date de création sont retournées pour tous les documents contenant plus de 50 pages, triés par ordre croissant de nombre de pages.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-106">In the following query example, the page count and date created values are returned for all documents which have more than 50 pages, sorted is ascending order of page count.</span></span>

```SQL
SELECT System.Document.PageCount, System.DateCreated
FROM SystemIndex
WHERE (System.Document.PageCount > 50)
ORDER BY System.Document.PageCount
```

<span data-ttu-id="4dcf0-107">La syntaxe de requête de recherche Windows prend en charge de nombreuses options, ce qui permet d’obtenir des requêtes plus compliquées.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-107">The Windows Search query syntax supports many options, enabling more complicated queries.</span></span>

<span data-ttu-id="4dcf0-108">Le tableau suivant décrit chaque clause dans les instructions SELECT ou GROUP ON et les fonctionnalités prises en charge.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-108">The following table describes each clause in the SELECT or GROUP ON statements and the features supported.</span></span>

| <span data-ttu-id="4dcf0-109">Clause</span><span class="sxs-lookup"><span data-stu-id="4dcf0-109">Clause</span></span>                                              | <span data-ttu-id="4dcf0-110">Description</span><span class="sxs-lookup"><span data-stu-id="4dcf0-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4dcf0-111">REGROUPER... ...</span><span class="sxs-lookup"><span data-stu-id="4dcf0-111">GROUP ON...OVER...</span></span>](-search-sql-group-on-over.md) | <span data-ttu-id="4dcf0-112">Spécifie comment regrouper les résultats retournés par la requête.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-112">Specifies how to group results returned by the query.</span></span> <span data-ttu-id="4dcf0-113">Vous pouvez spécifier les plages de regroupement et spécifier plusieurs colonnes pour le regroupement.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-113">You can specify the ranges by which to group and specify more than one column for grouping.</span></span> <span data-ttu-id="4dcf0-114">Par exemple, vous pouvez regrouper les résultats sur une plage de tailles de fichier (taille < 100, 100 <= taille < 1000 ; 1000 <= taille) et imbriquer des regroupements.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-114">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size) and nest groupings.</span></span>                                                                                                       |
| [<span data-ttu-id="4dcf0-115">SELECT</span><span class="sxs-lookup"><span data-stu-id="4dcf0-115">SELECT</span></span>](-search-sql-select.md)                    | <span data-ttu-id="4dcf0-116">Spécifie les colonnes retournées par la requête.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-116">Specifies the columns returned by the query.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="4dcf0-117">FROM</span><span class="sxs-lookup"><span data-stu-id="4dcf0-117">FROM</span></span>](-search-sql-from.md)                        | <span data-ttu-id="4dcf0-118">Spécifie l’ordinateur et le catalogue dans lesquels effectuer la recherche.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-118">Specifies the machine and catalog to search.</span></span>                                                                                                                                                                                                                                                                                                                                                         |
| [<span data-ttu-id="4dcf0-119">WHERE</span><span class="sxs-lookup"><span data-stu-id="4dcf0-119">WHERE</span></span>](-search-sql-where.md)                      | <span data-ttu-id="4dcf0-120">Spécifie ce qui constitue un document correspondant.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-120">Specifies what constitutes a matching document.</span></span> <span data-ttu-id="4dcf0-121">Cette clause présente de nombreuses options, permettant ainsi un contrôle riche sur les conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-121">This clause has many options, enabling rich control over the search conditions.</span></span> <span data-ttu-id="4dcf0-122">Par exemple, vous pouvez effectuer une mise en correspondance avec des mots, des expressions, des formes de mots infléchis, des chaînes, des valeurs numériques et de bits, ainsi que des tableaux à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-122">For example, you can match against words, phrases, inflectional word forms, strings, numeric and bitwise values, and multi-valued arrays.</span></span> <span data-ttu-id="4dcf0-123">Vous pouvez également appliquer des pondérations statistiques aux conditions de correspondance et combiner des conditions de correspondance avec des opérateurs booléens.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-123">You can also apply statistical weights to the matching conditions, and combine matching conditions with Boolean operators.</span></span> |
| [<span data-ttu-id="4dcf0-124">ORDER BY</span><span class="sxs-lookup"><span data-stu-id="4dcf0-124">ORDER BY</span></span>](-search-sql-orderby.md)                 | <span data-ttu-id="4dcf0-125">Spécifie l’ordre de tri pour les résultats retournés par la requête.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-125">Specifies the sort order for the results returned by the query.</span></span> <span data-ttu-id="4dcf0-126">Vous pouvez spécifier plusieurs champs sur lesquels les résultats sont triés, et vous pouvez utiliser l’ordre croissant ou décroissant.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-126">You can specify more than one field on which the results are sorted, and you can use ascending or descending ordering.</span></span>                                                                                                                                                                                                               |

### <a name="code-samples"></a><span data-ttu-id="4dcf0-127">Exemples de code</span><span class="sxs-lookup"><span data-stu-id="4dcf0-127">Code samples</span></span>

<span data-ttu-id="4dcf0-128">L’exemple de code WSSQL montre comment communiquer entre Microsoft OLE DB et Windows Search via SQL.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-128">The WSSQL code sample demonstrates how to communicate between Microsoft OLE DB and Windows Search through SQL.</span></span> <span data-ttu-id="4dcf0-129">L’exemple de code WSOleDB illustre Active Template Library (ATL) OLE DB l’accès aux applications Windows Search et deux méthodes supplémentaires pour récupérer les résultats de Windows Search.</span><span class="sxs-lookup"><span data-stu-id="4dcf0-129">The WSOleDB code sample illustrates Active Template Library (ATL) OLE DB access to Windows Search applications, and two additional methods for retrieving results from Windows Search.</span></span> <span data-ttu-id="4dcf0-130">Les deux exemples sont disponibles sur [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span><span class="sxs-lookup"><span data-stu-id="4dcf0-130">Both samples are available on [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch).</span></span>

## <a name="related-topics"></a><span data-ttu-id="4dcf0-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="4dcf0-131">Related topics</span></span>

### <a name="reference"></a><span data-ttu-id="4dcf0-132">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="4dcf0-132">Reference</span></span>

[<span data-ttu-id="4dcf0-133">Littéraux</span><span class="sxs-lookup"><span data-stu-id="4dcf0-133">Literals</span></span>](-search-sql-literals.md)

[<span data-ttu-id="4dcf0-134">Utilisation de recherches localisées</span><span class="sxs-lookup"><span data-stu-id="4dcf0-134">Using Localized Searches</span></span>](-search-sql-usinglocsearches.md)

[<span data-ttu-id="4dcf0-135">Compréhension des valeurs de pertinence</span><span class="sxs-lookup"><span data-stu-id="4dcf0-135">Understanding Relevance Values</span></span>](-search-sql-understandingrelevancevalues.md)

[<span data-ttu-id="4dcf0-136">Mappages de propriétés</span><span class="sxs-lookup"><span data-stu-id="4dcf0-136">Property Mappings</span></span>](-search-3x-wds-propertymappings.md)

[<span data-ttu-id="4dcf0-137">Syntaxe de requête avancée</span><span class="sxs-lookup"><span data-stu-id="4dcf0-137">Advanced Query Syntax</span></span>](-search-3x-advancedquerysyntax.md)

### <a name="conceptual"></a><span data-ttu-id="4dcf0-138">Conceptuel</span><span class="sxs-lookup"><span data-stu-id="4dcf0-138">Conceptual</span></span>

[<span data-ttu-id="4dcf0-139">Extensions SQL dans Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="4dcf0-139">SQL Extensions in Microsoft Windows Search</span></span>](-search-sql-extensions-sps.md)

[<span data-ttu-id="4dcf0-140">Fonctionnalités SQL non disponibles dans Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="4dcf0-140">SQL Features Unavailable in Microsoft Windows Search</span></span>](-search-sql-featuresunavailableinspssearch.md)

[<span data-ttu-id="4dcf0-141">Identificateurs</span><span class="sxs-lookup"><span data-stu-id="4dcf0-141">Identifiers</span></span>](-search-sql-identifiers.md)

[<span data-ttu-id="4dcf0-142">Respect de la casse dans les recherches</span><span class="sxs-lookup"><span data-stu-id="4dcf0-142">Case Sensitivity in Searches</span></span>](-search-sql-casesensitivityinsearches.md)

[<span data-ttu-id="4dcf0-143">Respect des signes diacritiques dans les recherches</span><span class="sxs-lookup"><span data-stu-id="4dcf0-143">Diacritic Sensitivity in Searches</span></span>](-search-sql-accentinsensitivitysearches.md)

[<span data-ttu-id="4dcf0-144">Conversion du type de données d’une colonne</span><span class="sxs-lookup"><span data-stu-id="4dcf0-144">Casting the Data Type of a Column</span></span>](-search-sql-castingdatacolumntype.md)

[<span data-ttu-id="4dcf0-145">Mappages de type de données</span><span class="sxs-lookup"><span data-stu-id="4dcf0-145">Data Type Mappings</span></span>](-search-sql-datatypemappings.md)
