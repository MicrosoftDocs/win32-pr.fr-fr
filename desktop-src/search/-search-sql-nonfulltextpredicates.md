---
description: Le langage de requête de recherche Microsoft Windows prend en charge six prédicats de recherche de texte non intégral. Les prédicats décrits dans cette section sont répertoriés dans le tableau suivant.
ms.assetid: 74aa6dbc-5c0d-433e-96d9-a8db63907342
title: Prédicats de texte non intégral
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d41076ebc61aa56ed547f13f717ac40bed35959
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106544625"
---
# <a name="non-full-text-predicates"></a><span data-ttu-id="fb14f-104">Prédicats de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="fb14f-104">Non-Full-Text Predicates</span></span>

<span data-ttu-id="fb14f-105">Le langage de requête de recherche Microsoft Windows prend en charge six prédicats de recherche de texte non intégral.</span><span class="sxs-lookup"><span data-stu-id="fb14f-105">The Microsoft Windows Search query language supports six non-full-text search predicates.</span></span> <span data-ttu-id="fb14f-106">Les prédicats décrits dans cette section sont répertoriés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="fb14f-106">The predicates described in this section are listed in the following table.</span></span>



| <span data-ttu-id="fb14f-107">Prédicat de texte non intégral</span><span class="sxs-lookup"><span data-stu-id="fb14f-107">Non-full-text predicate</span></span>                                                    | <span data-ttu-id="fb14f-108">Description</span><span class="sxs-lookup"><span data-stu-id="fb14f-108">Description</span></span>                                                                                                                                                                             |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fb14f-109">Toutes les opérations de bits and au niveau du bit</span><span class="sxs-lookup"><span data-stu-id="fb14f-109">ALL BITWISE and SOME BITWISE</span></span>](all-bitwise.md)                            | <span data-ttu-id="fb14f-110">Est un ensemble de mots clés qui concernent le test des bits dans un type intégral.</span><span class="sxs-lookup"><span data-stu-id="fb14f-110">Is a set of keywords that are about testing the bits in an integral type.</span></span>                                                                                                               |
| [<span data-ttu-id="fb14f-111">DATEADD, fonction</span><span class="sxs-lookup"><span data-stu-id="fb14f-111">DATEADD Function</span></span>](-search-sql-dateadd.md)                                | <span data-ttu-id="fb14f-112">Effectue des calculs de date et d’heure pour les propriétés correspondantes ayant des types de date.</span><span class="sxs-lookup"><span data-stu-id="fb14f-112">Performs time and date calculations for matching properties having date types.</span></span> <span data-ttu-id="fb14f-113">Utilisez la fonction DATEADD pour obtenir des dates et des heures dans un laps de temps spécifié avant le présent.</span><span class="sxs-lookup"><span data-stu-id="fb14f-113">Use the DATEADD function to obtain dates and times in a specified amount of time before the present.</span></span>     |
| [<span data-ttu-id="fb14f-114">Prédicat LIKE</span><span class="sxs-lookup"><span data-stu-id="fb14f-114">LIKE Predicate</span></span>](-search-sql-like.md)                                     | <span data-ttu-id="fb14f-115">Compare les valeurs de colonne à l’aide de critères spéciaux simples avec des caractères génériques.</span><span class="sxs-lookup"><span data-stu-id="fb14f-115">Compares column values using simple pattern matching with wildcard characters.</span></span>                                                                                                          |
| [<span data-ttu-id="fb14f-116">Comparaison de valeurs littérales</span><span class="sxs-lookup"><span data-stu-id="fb14f-116">Literal Value Comparison</span></span>](-search-sql-literalvaluecomparison.md)         | <span data-ttu-id="fb14f-117">Compare les valeurs de colonne à la chaîne, à la date, à l’horodatage, à la valeur numérique et à d’autres valeurs littérales.</span><span class="sxs-lookup"><span data-stu-id="fb14f-117">Compares column values against string, date, time stamp, numeric, and other literal values.</span></span> <span data-ttu-id="fb14f-118">Ce prédicat prend en charge les inégales telles que supérieur à (' > ') et inférieur à (' < ').</span><span class="sxs-lookup"><span data-stu-id="fb14f-118">This predicate supports inequalities such as greater than ('>'), and less than ('<').</span></span> |
| [<span data-ttu-id="fb14f-119">Comparaisons à valeurs multiples (tableau)</span><span class="sxs-lookup"><span data-stu-id="fb14f-119">Multi-Valued (ARRAY) Comparisons</span></span>](-search-sql-multivaluedcomparisons.md) | <span data-ttu-id="fb14f-120">Compare des colonnes à valeurs multiples à un tableau de littéraux à valeurs multiples.</span><span class="sxs-lookup"><span data-stu-id="fb14f-120">Compares multivalued columns against a multivalued array of literals.</span></span>                                                                                                                   |
| [<span data-ttu-id="fb14f-121">Prédicat NULL</span><span class="sxs-lookup"><span data-stu-id="fb14f-121">NULL Predicate</span></span>](-search-sql-null.md)                                     | <span data-ttu-id="fb14f-122">Détecte les valeurs de colonne qui ne sont pas définies pour le document.</span><span class="sxs-lookup"><span data-stu-id="fb14f-122">Detects column values that are undefined for the document.</span></span>                                                                                                                              |



 

> [!IMPORTANT]
> <span data-ttu-id="fb14f-123">Les requêtes de recherche utilisant le prédicat **null** peuvent exiger que la recherche Windows analyse le catalogue entier, ce qui peut ralentir les performances de la requête.</span><span class="sxs-lookup"><span data-stu-id="fb14f-123">Search queries using the **NULL** predicate can require that Windows Search scan the entire catalog, which might slow down the query's performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="fb14f-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fb14f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb14f-125">Prédicats de texte intégral</span><span class="sxs-lookup"><span data-stu-id="fb14f-125">Full-Text Predicates</span></span>](-search-sql-fulltextpredicates.md)
</dt> </dl>

 

 



