---
title: Mise en cache des résultats avec IDirectorySearch
description: La \_ préférence des résultats du cache SEARCHPREF ADS \_ \_ met en cache le jeu de résultats sur le client.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Mise en cache des résultats avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, mise en cache des résultats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95016699eb4de36344b7e40f35e1a4a9cce761b8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309226"
---
# <a name="result-caching-with-idirectorysearch"></a><span data-ttu-id="ee6c2-105">Mise en cache des résultats avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="ee6c2-105">Result Caching with IDirectorySearch</span></span>

<span data-ttu-id="ee6c2-106">La préférence des **\_ \_ \_ résultats du cache SEARCHPREF ADS** met en cache le jeu de résultats sur le client.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-106">The **ADS\_SEARCHPREF\_CACHE\_RESULTS** preference caches the result set on the client.</span></span> <span data-ttu-id="ee6c2-107">La mise en cache des résultats permet à une application de conserver un jeu de résultats récupéré et de repasser les lignes récupérées.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-107">Result caching enables an application to retain a retrieved result set and go through the retrieved rows again.</span></span> <span data-ttu-id="ee6c2-108">Il permet également la prise en charge des curseurs là où les méthodes [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) et [**IDirectorySearch :: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) peuvent être utilisées pour monter et descendre dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-108">It also enables cursor support where the [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) and [**IDirectorySearch::GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) methods can be used to move up and down the result set.</span></span>

<span data-ttu-id="ee6c2-109">Par défaut, la mise en cache des résultats est désactivée.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-109">By default, result caching is disabled.</span></span> <span data-ttu-id="ee6c2-110">La mise en cache des résultats doit être activée si l’une des conditions suivantes est vraie :</span><span class="sxs-lookup"><span data-stu-id="ee6c2-110">Result caching should be enabled if any one of the following is true:</span></span>

-   <span data-ttu-id="ee6c2-111">Si le même jeu de résultats doit être énuméré plusieurs fois sans effectuer à nouveau la recherche sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-111">If the same result set must be enumerated multiple times without performing the search again on the server.</span></span>
-   <span data-ttu-id="ee6c2-112">Si l’exécution de la recherche est gourmande en ressources sur le serveur (connexion lente, jeu de résultats volumineux ou requête complexe).</span><span class="sxs-lookup"><span data-stu-id="ee6c2-112">If performing the search is resource-intensive on the server (slow connection, large result set, or complex query).</span></span>
-   <span data-ttu-id="ee6c2-113">Si la prise en charge du curseur est requise.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-113">If cursor support is required.</span></span>

<span data-ttu-id="ee6c2-114">Désactivez la mise en cache si votre application doit réduire les besoins en mémoire pour la mise en cache d’un jeu de résultats volumineux sur le client.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-114">Turn off caching if your application must reduce memory requirements for caching a large result set at the client.</span></span>

<span data-ttu-id="ee6c2-115">La mise en cache des résultats augmente les besoins en mémoire sur le client, donc la mise en cache des résultats doit être désactivée si cela pose problème.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-115">Result caching increases the memory requirements on the client, so result caching should be disabled if this is a concern.</span></span>

<span data-ttu-id="ee6c2-116">Pour activer la mise en cache des résultats, définissez une option de recherche de **\_ \_ \_ cache SEARCHPREF ADS** avec la valeur **\_ booléenne ADSTYPE** **true** dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) transmis à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="ee6c2-116">To enable result caching, set an **ADS\_SEARCHPREF\_CACHE\_RESULTS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="ee6c2-117">L’exemple de code suivant montre comment activer la mise en cache des résultats.</span><span class="sxs-lookup"><span data-stu-id="ee6c2-117">The following code example shows how to enable result caching.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




