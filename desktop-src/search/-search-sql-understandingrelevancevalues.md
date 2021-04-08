---
description: Dans une base de données relationnelle, les lignes retournées par une requête de recherche doivent répondre à toutes les conditions appelées par la requête. En revanche, une requête de recherche Windows peut retourner des documents qui remplissent les conditions de recherche à différents degrés.
ms.assetid: 9f37b494-9b7a-45a6-9ee4-6d582742cbd7
title: Compréhension des valeurs de pertinence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a24c71ad523ad869c6ff05b81ff75367031ad38
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862150"
---
# <a name="understanding-relevance-values"></a><span data-ttu-id="1d028-104">Compréhension des valeurs de pertinence</span><span class="sxs-lookup"><span data-stu-id="1d028-104">Understanding Relevance Values</span></span>

<span data-ttu-id="1d028-105">Dans une base de données relationnelle, les lignes retournées par une requête de recherche doivent répondre à toutes les conditions appelées par la requête.</span><span class="sxs-lookup"><span data-stu-id="1d028-105">In a relational database, rows that are returned by a search query must meet all the conditions called for by the query.</span></span> <span data-ttu-id="1d028-106">En revanche, une requête de recherche Windows peut retourner des documents qui remplissent les conditions de recherche à différents degrés.</span><span class="sxs-lookup"><span data-stu-id="1d028-106">In contrast, a Windows Search query can return documents that meet the search conditions to varying degrees.</span></span>

<span data-ttu-id="1d028-107">Par exemple, la recherche du terme « programme » dans une base de données relationnelle produit des enregistrements qui contiennent l’orthographe spécifique du mot.</span><span class="sxs-lookup"><span data-stu-id="1d028-107">For example, a search for the term "program" in a relational database produces records that contain that specific spelling of the word.</span></span> <span data-ttu-id="1d028-108">Si un enregistrement contient une ou 100 instances du mot n’a aucun impact sur les résultats.</span><span class="sxs-lookup"><span data-stu-id="1d028-108">Whether a record contains one or one hundred instances of the word has no impact on the results.</span></span> <span data-ttu-id="1d028-109">En revanche, la recherche Windows retourne une valeur de pertinence associée aux documents correspondants.</span><span class="sxs-lookup"><span data-stu-id="1d028-109">In contrast, Windows Search returns a relevance value associated with the matching documents.</span></span> <span data-ttu-id="1d028-110">La pertinence des documents dont le titre contient « Program » est supérieure à celles qui contiennent le mot uniquement dans le dernier paragraphe.</span><span class="sxs-lookup"><span data-stu-id="1d028-110">The relevance of documents having "program" in the title is higher than those that contain the word only in the last paragraph.</span></span> <span data-ttu-id="1d028-111">De même, les documents contenant des variations du terme de recherche, par exemple « Programs » et « Programming », correspondent également à et sont retournés par la requête.</span><span class="sxs-lookup"><span data-stu-id="1d028-111">Similarly, documents containing variations of the search term, for example "programs" and "programming" also match and are returned by the query.</span></span>

<span data-ttu-id="1d028-112">Les requêtes de recherche Windows retournent des valeurs de pertinence d’entier dans la colonne nommée « rank ».</span><span class="sxs-lookup"><span data-stu-id="1d028-112">Windows Search queries return integer relevance values in the column named "rank".</span></span>

<span data-ttu-id="1d028-113">De plus :</span><span class="sxs-lookup"><span data-stu-id="1d028-113">In addition:</span></span>

-   <span data-ttu-id="1d028-114">Les valeurs de classement retournées par la requête sont des entiers compris entre 0 et 1000.</span><span class="sxs-lookup"><span data-stu-id="1d028-114">Rank values returned by the query are integers ranging from 0 to 1000.</span></span>
-   <span data-ttu-id="1d028-115">Des valeurs de classement plus élevées indiquent des documents qui correspondent mieux aux conditions de recherche.</span><span class="sxs-lookup"><span data-stu-id="1d028-115">Higher rank values indicate documents that better match the search conditions.</span></span>
-   <span data-ttu-id="1d028-116">Les valeurs de classement s’appliquent uniquement à la requête actuelle. elles ne peuvent donc pas être comparées pour les résultats d’une requête à l’autre.</span><span class="sxs-lookup"><span data-stu-id="1d028-116">Rank values apply only to the current query, so they cannot be compared for results across queries.</span></span>
-   <span data-ttu-id="1d028-117">Les valeurs de classement sont relatives aux autres documents correspondant à la requête.</span><span class="sxs-lookup"><span data-stu-id="1d028-117">Rank values are relative to the other documents matching the query.</span></span> <span data-ttu-id="1d028-118">Par conséquent, la valeur de classement d’un document particulier dépend des autres documents qui correspondent également à la requête.</span><span class="sxs-lookup"><span data-stu-id="1d028-118">Therefore, the rank value of a particular document depends on the other documents that also match the query.</span></span>
-   <span data-ttu-id="1d028-119">Les valeurs de classement des éléments correspondant à un prédicat purement relationnel sont 1000.</span><span class="sxs-lookup"><span data-stu-id="1d028-119">Rank values for items matching a purely relational predicate are 1000.</span></span>

<span data-ttu-id="1d028-120">Vous pouvez manipuler les valeurs de classement retournées en utilisant des pondérations de colonnes [dans les prédicats de clause](-search-sql-contains.md) WHERE et [FREETEXT](-search-sql-freetext.md) WHERE, et la clause Rank by.</span><span class="sxs-lookup"><span data-stu-id="1d028-120">You can manipulate the returned rank values by using column weights in the [CONTAINS](-search-sql-contains.md) and [FREETEXT](-search-sql-freetext.md) WHERE clause predicates, and the RANK BY clause.</span></span>

 

 



