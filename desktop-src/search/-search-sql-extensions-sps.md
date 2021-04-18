---
description: La recherche Microsoft Windows, basée sur les normes SQL-92 et SQL-99, améliore les recherches basées sur les documents en texte intégral dans les applications de gestion de documents ou de gestion des connaissances.
ms.assetid: 136af1ea-452a-491b-bec7-8c45fa01f87f
title: Extensions SQL dans Microsoft Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340766d5db99a749e8f508e2dc0bec6a549adfc4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525491"
---
# <a name="sql-extensions-in-microsoft-windows-search"></a><span data-ttu-id="a19fe-103">Extensions SQL dans Microsoft Windows Search</span><span class="sxs-lookup"><span data-stu-id="a19fe-103">SQL Extensions in Microsoft Windows Search</span></span>

<span data-ttu-id="a19fe-104">La recherche Microsoft Windows, basée sur les normes SQL-92 et SQL-99, améliore les recherches basées sur les documents en texte intégral dans les applications de gestion de documents ou de gestion des connaissances.</span><span class="sxs-lookup"><span data-stu-id="a19fe-104">Microsoft Windows Search, based on the SQL-92 and SQL-99 standards, improves full-text document-based searches in document-management or knowledge-management applications.</span></span> <span data-ttu-id="a19fe-105">Les améliorations de Windows Search sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="a19fe-105">Windows Search improvements include the following:</span></span>

## <a name="128-character-identifier-names"></a><span data-ttu-id="a19fe-106">128-noms d’identificateurs de caractères</span><span class="sxs-lookup"><span data-stu-id="a19fe-106">128-Character Identifier Names</span></span>

<span data-ttu-id="a19fe-107">Alors que SQL-92 et SQL-99 restreignent la colonne et d’autres identificateurs à 18 caractères, Windows Search prend en charge les noms de colonnes de 128 caractères.</span><span class="sxs-lookup"><span data-stu-id="a19fe-107">While SQL-92 and SQL-99 restrict column and other identifiers to 18 characters, Windows Search supports 128-character column names.</span></span> <span data-ttu-id="a19fe-108">Pour plus d’informations, consultez [Identificateurs](-search-sql-identifiers.md).</span><span class="sxs-lookup"><span data-stu-id="a19fe-108">For more information, see [Identifiers](-search-sql-identifiers.md).</span></span>

## <a name="grouping-results-by-columns"></a><span data-ttu-id="a19fe-109">Regroupement des résultats par colonnes</span><span class="sxs-lookup"><span data-stu-id="a19fe-109">Grouping Results by Columns</span></span>

<span data-ttu-id="a19fe-110">Les requêtes peuvent spécifier la façon dont les résultats doivent être regroupés.</span><span class="sxs-lookup"><span data-stu-id="a19fe-110">Queries can specify how to group results.</span></span> <span data-ttu-id="a19fe-111">Vous pouvez spécifier les plages selon lesquelles effectuer un regroupement, et vous pouvez spécifier plusieurs colonnes pour le regroupement.</span><span class="sxs-lookup"><span data-stu-id="a19fe-111">You can specify the ranges by which to group, and you can specify more than one column for grouping.</span></span> <span data-ttu-id="a19fe-112">Par exemple, vous pouvez regrouper les résultats sur une plage de tailles de fichier (taille < 100, 100 <= taille < 1000 ; 1000 <= taille) et vous pouvez imbriquer des regroupements.</span><span class="sxs-lookup"><span data-stu-id="a19fe-112">For example, you can group results over a range of file sizes (size < 100, 100 <= size < 1000; 1000 <= size), and you can nest groupings.</span></span> <span data-ttu-id="a19fe-113">Pour plus d’informations, consultez [regrouper sur... ... Instruction](-search-sql-group-on-over.md).</span><span class="sxs-lookup"><span data-stu-id="a19fe-113">For more information, see [GROUP ON ... OVER... Statement](-search-sql-group-on-over.md).</span></span>

## <a name="diacritic-insensitive-searching"></a><span data-ttu-id="a19fe-114">Recherche Diacritic-Insensitive</span><span class="sxs-lookup"><span data-stu-id="a19fe-114">Diacritic-Insensitive Searching</span></span>

<span data-ttu-id="a19fe-115">En plus de la recherche qui ne respecte pas la casse, la recherche Windows prend en charge la recherche qui ne respecte pas les signes diacritiques (accents).</span><span class="sxs-lookup"><span data-stu-id="a19fe-115">In addition to searching that is not case-sensitive, Windows Search supports searching that is not sensitive to diacritics (accent marks).</span></span> <span data-ttu-id="a19fe-116">Pour plus d’informations, consultez [sensibilité des signes diacritiques dans les recherches](-search-sql-accentinsensitivitysearches.md).</span><span class="sxs-lookup"><span data-stu-id="a19fe-116">For more information, see [Diacritic Sensitivity in Searches](-search-sql-accentinsensitivitysearches.md).</span></span>

## <a name="column-weighting"></a><span data-ttu-id="a19fe-117">Pondération de colonne</span><span class="sxs-lookup"><span data-stu-id="a19fe-117">Column Weighting</span></span>

<span data-ttu-id="a19fe-118">Les requêtes qui recherchent plusieurs colonnes peuvent spécifier l’importance de chaque colonne.</span><span class="sxs-lookup"><span data-stu-id="a19fe-118">Queries that search more than one column can specify the importance of each column.</span></span> <span data-ttu-id="a19fe-119">Les prédicats [Contains](-search-sql-contains.md) et [FREETEXT](-search-sql-freetext.md) prennent en charge la pondération de colonne.</span><span class="sxs-lookup"><span data-stu-id="a19fe-119">The [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) predicates both support column weighting.</span></span>

## <a name="null-predicate"></a><span data-ttu-id="a19fe-120">Prédicat NULL</span><span class="sxs-lookup"><span data-stu-id="a19fe-120">NULL Predicate</span></span>

<span data-ttu-id="a19fe-121">Bien que l’indexation du contenu de texte intégral n’ait aucun ensemble de colonnes défini, les requêtes peuvent exiger que les membres du jeu de résultats n’aient pas de colonnes spécifiées.</span><span class="sxs-lookup"><span data-stu-id="a19fe-121">Although full-text content indexing has no defined set of columns, queries can require that members of the result set do or do not have specified columns.</span></span> <span data-ttu-id="a19fe-122">Il n’est pas possible de faire la différence entre un document a une propriété spécifiée avec la valeur définie sur **null** et un document qui n’a pas de propriété.</span><span class="sxs-lookup"><span data-stu-id="a19fe-122">It is not possible to differentiate between a document has a specified property with the value set to **NULL**, and a document that does not have the property at all.</span></span>

## <a name="rank-modification"></a><span data-ttu-id="a19fe-123">Modification de classement</span><span class="sxs-lookup"><span data-stu-id="a19fe-123">Rank Modification</span></span>

<span data-ttu-id="a19fe-124">Vous pouvez manipuler le classement des résultats de recherche à l’aide de [pondérations](-search-sql-understandingrelevancevalues.md) sur les propriétés et sur des groupes de propriétés avec alias.</span><span class="sxs-lookup"><span data-stu-id="a19fe-124">You can manipulate the search results ranking by using [weights](-search-sql-understandingrelevancevalues.md) on properties and on aliased groups of properties.</span></span> <span data-ttu-id="a19fe-125">La contrainte de classement prend en charge la manipulation directe du classement de pertinence en fonction des critères que vous spécifiez.</span><span class="sxs-lookup"><span data-stu-id="a19fe-125">Rank coercion supports direct manipulation of the relevance ranking based on the criteria you specify.</span></span>

 

 



