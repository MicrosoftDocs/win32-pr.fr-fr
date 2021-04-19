---
description: Une fois qu’un résultat est retourné à partir d’une requête, vous pouvez accéder à plusieurs propriétés de l’ensemble de lignes.
ms.assetid: 71aa0ad6-ef34-47ee-945f-04bda20bf8a4
title: Propriétés du rowset
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e498c701224a879c09653d6f265151297d2ee1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515212"
---
# <a name="rowset-properties"></a><span data-ttu-id="3b53c-103">Propriétés du rowset</span><span class="sxs-lookup"><span data-stu-id="3b53c-103">Rowset Properties</span></span>

<span data-ttu-id="3b53c-104">Une fois qu’un résultat est retourné à partir d’une requête, vous pouvez accéder à plusieurs propriétés de l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="3b53c-104">After a result is returned from a query, you can access several properties for the rowset.</span></span>

<span data-ttu-id="3b53c-105">En plus des propriétés de l’ensemble de lignes OLE-DB standard, Windows Search SQL offre les quatre propriétés personnalisées suivantes.</span><span class="sxs-lookup"><span data-stu-id="3b53c-105">In addition to the standard OLE-DB rowset properties, Windows Search SQL offers the following four custom properties.</span></span> <span data-ttu-id="3b53c-106">Le GUID de ce jeu de propriétés est {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span><span class="sxs-lookup"><span data-stu-id="3b53c-106">The GUID for this property set is {AA6EE6B0E828-11D0-B23E-00AA0047FC01}.</span></span>

<span data-ttu-id="3b53c-107">Windows Search prend en charge la propriété OLE-DB standard DBPROP \_ COMMANDTIMEOUT du jeu de propriétés d' [ensemble de \_ lignes DBPROPSET](/previous-versions//ms691738(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="3b53c-107">Windows Search supports the standard OLE-DB property DBPROP\_COMMANDTIMEOUT of the [DBPROPSET\_ROWSET](/previous-versions//ms691738(v=vs.85)) property set.</span></span>



| <span data-ttu-id="3b53c-108">Nom de la propriété</span><span class="sxs-lookup"><span data-stu-id="3b53c-108">Property name</span></span>                  | <span data-ttu-id="3b53c-109">PROPID/type</span><span class="sxs-lookup"><span data-stu-id="3b53c-109">PROPID/type</span></span> | <span data-ttu-id="3b53c-110">Description</span><span class="sxs-lookup"><span data-stu-id="3b53c-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b53c-111">DONOTCOMPUTEEXPENSIVEPROPS</span><span class="sxs-lookup"><span data-stu-id="3b53c-111">DONOTCOMPUTEEXPENSIVEPROPS</span></span>     | <span data-ttu-id="3b53c-112">booléen 15/VT \_</span><span class="sxs-lookup"><span data-stu-id="3b53c-112">15/VT\_BOOL</span></span> | <span data-ttu-id="3b53c-113">L’affectation de la valeur true empêche le calcul des propriétés coûteuses telles que les résultats trouvés et le classement maximal qui nécessitent l’évaluation de l’ensemble de la requête lorsqu’une propriété d’ensemble de lignes est accédée.</span><span class="sxs-lookup"><span data-stu-id="3b53c-113">Setting this to true prevents computing expensive properties like Results Found and Max Rank that require evaluating the whole query when any rowset property is accessed.</span></span>                                                                                                                                                                         |
| <span data-ttu-id="3b53c-114">Rang maximal (rang MAX. \_ )</span><span class="sxs-lookup"><span data-stu-id="3b53c-114">Maximum Rank (MAX\_RANK)</span></span>       | <span data-ttu-id="3b53c-115">6/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3b53c-115">6/VT\_I4</span></span>    | <span data-ttu-id="3b53c-116">Classement le plus élevé calculé pour tous les résultats.</span><span class="sxs-lookup"><span data-stu-id="3b53c-116">The highest rank computed for any result.</span></span>                                                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="3b53c-117">Résultats trouvés (résultats \_ trouvés)</span><span class="sxs-lookup"><span data-stu-id="3b53c-117">Results Found (RESULTS\_FOUND)</span></span> | <span data-ttu-id="3b53c-118">7/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3b53c-118">7/VT\_I4</span></span>    | <span data-ttu-id="3b53c-119">Nombre total d’éléments uniques pour cette requête.</span><span class="sxs-lookup"><span data-stu-id="3b53c-119">The total number of unique items for this query.</span></span> <span data-ttu-id="3b53c-120">Pour une requête SELECT, il s’agit du nombre d’éléments dans l’ensemble de lignes.</span><span class="sxs-lookup"><span data-stu-id="3b53c-120">For a SELECT query, this is the number of items in the rowset.</span></span> <span data-ttu-id="3b53c-121">Pour un groupe sur une requête, il s’agit du nombre d’éléments feuille uniques.</span><span class="sxs-lookup"><span data-stu-id="3b53c-121">For a GROUP ON query, this is the number of unique leaf items.</span></span> <span data-ttu-id="3b53c-122">Cette propriété n’identifie pas le nombre de lignes dans l’ensemble de lignes de niveau supérieur (le nombre de groupes de niveau supérieur).</span><span class="sxs-lookup"><span data-stu-id="3b53c-122">This property does not identify the number of rows in the top-level rowset (the number of top-level groups).</span></span>                                                        |
| <span data-ttu-id="3b53c-123">Où ID (WHEREID)</span><span class="sxs-lookup"><span data-stu-id="3b53c-123">Where ID (WHEREID)</span></span>             | <span data-ttu-id="3b53c-124">8/VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="3b53c-124">8/VT\_I4</span></span>    | <span data-ttu-id="3b53c-125">Identificateur des restrictions utilisées pour une requête.</span><span class="sxs-lookup"><span data-stu-id="3b53c-125">The identifier for the restrictions used for a query.</span></span> <span data-ttu-id="3b53c-126">Si un ensemble de lignes est ouvert lors de l’exécution d’une nouvelle requête, la nouvelle requête peut réutiliser les restrictions de l’ancienne requête, tirant ainsi parti du travail déjà effectué.</span><span class="sxs-lookup"><span data-stu-id="3b53c-126">If a rowset is open when a new query is executed, the new query can reuse the restrictions from the older query, thereby taking advantage of the work already completed.</span></span> <span data-ttu-id="3b53c-127">Pour plus d’informations sur la réutilisation des restrictions WHERE, référez-vous à la [fonction ReuseWhere](-search-sql-reusewhere.md).</span><span class="sxs-lookup"><span data-stu-id="3b53c-127">For more information on reusing WHERE restrictions, refer to the [ReuseWhere function](-search-sql-reusewhere.md).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="3b53c-128">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3b53c-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b53c-129">Indexation des événements d’ensemble de priorités et d’ensembles de lignes dans Windows 7</span><span class="sxs-lookup"><span data-stu-id="3b53c-129">Indexing Prioritization and Rowset Events in Windows 7</span></span>](indexing-prioritization-and-rowset-events.md)
</dt> </dl>

 

 
