---
description: La clause WHERE d’une requête spécifie un ensemble d’éléments pour lesquels faire correspondre les résultats.
ms.assetid: ed51edd5-6edc-4fcd-a69b-cb48c399ba7c
title: ReuseWhere fonction)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16bb5af4c3acd4637b27a2b3c9c7e14436eabb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106545778"
---
# <a name="reusewhere-function"></a><span data-ttu-id="103e6-103">ReuseWhere fonction)</span><span class="sxs-lookup"><span data-stu-id="103e6-103">ReuseWhere Function</span></span>

<span data-ttu-id="103e6-104">La clause [Where](-search-sql-where.md) d’une requête spécifie un ensemble d’éléments pour lesquels faire correspondre les résultats.</span><span class="sxs-lookup"><span data-stu-id="103e6-104">The [WHERE](-search-sql-where.md) clause in a query specifies a set of items to match results against.</span></span> <span data-ttu-id="103e6-105">Les requêtes suivantes peuvent partager le travail effectué pour une requête précédente à l’aide de la fonction ReuseWhere dans une nouvelle clause WHERE de la requête.</span><span class="sxs-lookup"><span data-stu-id="103e6-105">Subsequent queries can share the work performed for a previous query by using the ReuseWhere function in a new query WHERE clause.</span></span> <span data-ttu-id="103e6-106">Les requêtes qui tirent parti de cette fonction s’exécutent plus rapidement.</span><span class="sxs-lookup"><span data-stu-id="103e6-106">Queries that take advantage of this function execute faster.</span></span>

## <a name="examples"></a><span data-ttu-id="103e6-107">Exemples</span><span class="sxs-lookup"><span data-stu-id="103e6-107">Examples</span></span>

<span data-ttu-id="103e6-108">Le scénario suivant montre comment utiliser la fonction ReuseWhere :</span><span class="sxs-lookup"><span data-stu-id="103e6-108">The following scenario shows how to use the ReuseWhere function:</span></span>

1.  <span data-ttu-id="103e6-109">Vous exécutez la requête suivante :</span><span class="sxs-lookup"><span data-stu-id="103e6-109">You issue the following query:</span></span>
    ```
    SELECT System.ItemName FROM SystemIndex 
    WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5'
    ```

    

2.  <span data-ttu-id="103e6-110">À partir de l’ensemble de lignes retourné, vous recevez un [ID WHERE](-search-sql-rowset-properties.md), *Query1WhereID*.</span><span class="sxs-lookup"><span data-stu-id="103e6-110">From the returned rowset, you get a [Where ID](-search-sql-rowset-properties.md), *Query1WhereID*.</span></span>

    <span data-ttu-id="103e6-111">Où ID est une propriété d’ensemble de lignes avec PROPSET {aa6ee6b0-e828-11D0-B2-3e-00-AA-00-47-FC-01}, PROPID 8 et le type UI4.</span><span class="sxs-lookup"><span data-stu-id="103e6-111">The Where ID is a rowset property with PROPSET {aa6ee6b0-e828-11d0-b2-3e-00-aa-00-47-fc-01 }, PROPID 8, and type UI4.</span></span>

3.  <span data-ttu-id="103e6-112">Vous émettez une deuxième requête avec la fonction ReuseWhere, en transmettant le *Query1WhereID* de l’étape 2 :</span><span class="sxs-lookup"><span data-stu-id="103e6-112">You issue a second query with the ReuseWhere function, passing in the *Query1WhereID* from step 2:</span></span>
    ```
    SELECT System.ItemUrl FROM SystemIndex 
    WHERE ReuseWhere(Query1WhereID) AND SCOPE='file:'
    ```

    

<span data-ttu-id="103e6-113">La deuxième requête équivaut à ce qui suit :</span><span class="sxs-lookup"><span data-stu-id="103e6-113">The second query is equivalent to the following:</span></span>


```
SELECT System.ItemUrl, System.ItemName FROM SystemIndex 
WHERE CONTAINS(*, 'pencil') AND System.ItemDate > '2007-3-5' AND Scope='file:'
```



<span data-ttu-id="103e6-114">La fonction ReuseWhere peut être utilisée anwhere dans la clause [Where](-search-sql-where.md) .</span><span class="sxs-lookup"><span data-stu-id="103e6-114">The ReuseWhere function can be used anwhere in the [WHERE](-search-sql-where.md) clause.</span></span>

## <a name="related-topics"></a><span data-ttu-id="103e6-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="103e6-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="103e6-116">**Informations de référence**</span><span class="sxs-lookup"><span data-stu-id="103e6-116">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="103e6-117">Clause WHERE</span><span class="sxs-lookup"><span data-stu-id="103e6-117">WHERE Clause</span></span>](-search-sql-where.md)
</dt> <dt>

[<span data-ttu-id="103e6-118">Propriétés du rowset</span><span class="sxs-lookup"><span data-stu-id="103e6-118">Rowset Properties</span></span>](-search-sql-rowset-properties.md)
</dt> </dl>

 

 



