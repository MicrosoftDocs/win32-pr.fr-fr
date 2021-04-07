---
title: Recherches asynchrones
description: L’activation de la recherche asynchrone (asynchrone) entraîne un appel à GetFirstRow ou le premier appel à la valeur de la ligne, jusqu’à ce que la première entrée soit retournée à partir du serveur.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Recherches asynchrones ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939608"
---
# <a name="asynchronous-searches"></a><span data-ttu-id="dd668-104">Recherches asynchrones</span><span class="sxs-lookup"><span data-stu-id="dd668-104">Asynchronous Searches</span></span>

<span data-ttu-id="dd668-105">L’activation de la recherche asynchrone (asynchrone) entraîne un appel à **GetFirstRow** ou le premier **appel à la valeur de la** ligne, jusqu’à ce que la première entrée soit retournée à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="dd668-105">Enabling asynchronous (async) search results in a call to **GetFirstRow** or the first call to **GetNextRow** blocks until the first entry is returned from the server.</span></span> <span data-ttu-id="dd668-106">Autrement dit, si la recherche sur le serveur nécessite plus de temps, les premiers résultats sont retournés rapidement.</span><span class="sxs-lookup"><span data-stu-id="dd668-106">That is, if the search on the server requires much time, the first few results are returned quickly.</span></span> <span data-ttu-id="dd668-107">Cela peut être utile lors du remplissage d’une zone de liste avec les résultats de la recherche.</span><span class="sxs-lookup"><span data-stu-id="dd668-107">This can help when populating a list box with search results.</span></span> <span data-ttu-id="dd668-108">Les résultats de la recherche s’affichent tels qu’ils sont retournés.</span><span class="sxs-lookup"><span data-stu-id="dd668-108">Search results are displayed as they are returned.</span></span>

<span data-ttu-id="dd668-109">Si Async est désactivé, le premier appel à **GetFirstRow** ou **GetNextRow** se bloque jusqu’à ce que le serveur calcule le jeu de résultats entier et retourne.</span><span class="sxs-lookup"><span data-stu-id="dd668-109">If async is disabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server computes the entire result set and returns.</span></span> <span data-ttu-id="dd668-110">Seule la première ligne est retournée.</span><span class="sxs-lookup"><span data-stu-id="dd668-110">Only then is the first row returned.</span></span> <span data-ttu-id="dd668-111">Cela n’est pas recommandé si le jeu de résultats est supposé être volumineux.</span><span class="sxs-lookup"><span data-stu-id="dd668-111">This is not recommended if the result set is expected to be large.</span></span>

<span data-ttu-id="dd668-112">Si la pagination et Async sont activés, le premier appel à **GetFirstRow** ou **GetNextRow** est bloqué jusqu’à ce que le serveur génère et envoie la première page de résultats.</span><span class="sxs-lookup"><span data-stu-id="dd668-112">If both paging and async are enabled, the first call to **GetFirstRow** or **GetNextRow** will block until the server generates and sends the first page of results.</span></span> <span data-ttu-id="dd668-113">Si une taille de page raisonnable a été définie, les résultats s’affichent immédiatement.</span><span class="sxs-lookup"><span data-stu-id="dd668-113">If a reasonable page size was set, results will appear immediately.</span></span> <span data-ttu-id="dd668-114">Plus important encore, si les résultats de recherche sont censés être très volumineux et que vous recherchez une entrée particulière, il n’est pas nécessaire de demander plus de résultats à partir du serveur une fois que vous avez trouvé les entrées qui vous intéressent.</span><span class="sxs-lookup"><span data-stu-id="dd668-114">More importantly, if the search results are expected to be very large, and you search for a particular entry, it is not required that you request more results from the server after you have found the entries that interest you.</span></span>

<span data-ttu-id="dd668-115">Une recherche asynchrone paginée permet un contrôle précis d’une recherche.</span><span class="sxs-lookup"><span data-stu-id="dd668-115">A paged async search provides fine control of a search.</span></span> <span data-ttu-id="dd668-116">Cela est utile si les résultats de la recherche peuvent être très volumineux et nécessitent un temps considérable du serveur.</span><span class="sxs-lookup"><span data-stu-id="dd668-116">This is useful if the search results may be very large and require extensive time from the server.</span></span>

<span data-ttu-id="dd668-117">Pour plus d’informations sur l’utilisation des recherches asynchrones avec une interface de recherche spécifique, consultez :</span><span class="sxs-lookup"><span data-stu-id="dd668-117">For more information about using asynchronous searches with a specific search interface, see:</span></span>

-   [<span data-ttu-id="dd668-118">Recherches synchrones et asynchrones avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="dd668-118">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="dd668-119">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="dd668-119">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="dd668-120">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="dd668-120">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




