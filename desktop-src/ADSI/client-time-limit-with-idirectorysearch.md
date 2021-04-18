---
title: Limite de temps du client avec IDirectorySearch
description: Un client peut imposer une limite de temps pour qu’un serveur retourne le jeu de résultats. Lorsque le serveur ne parvient pas à répondre à une requête dans le délai spécifié, le client peut abandonner la recherche et essayer à nouveau ultérieurement.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite de temps du client avec IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, limite de temps du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed25bd8499f7166d7ea494f71e6f78193f9c778a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511809"
---
# <a name="client-time-limit-with-idirectorysearch"></a><span data-ttu-id="a9783-106">Limite de temps du client avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a9783-106">Client Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="a9783-107">Un client peut imposer une limite de temps pour qu’un serveur retourne le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="a9783-107">A client can impose a time limit for a server to return the result set.</span></span> <span data-ttu-id="a9783-108">Lorsque le serveur ne parvient pas à répondre à une requête dans le délai spécifié, le client peut abandonner la recherche et essayer à nouveau ultérieurement.</span><span class="sxs-lookup"><span data-stu-id="a9783-108">When the server fails to respond to a query within the specified time period, the client can abandon the search and try it again later.</span></span>

<span data-ttu-id="a9783-109">La préférence de limite de temps client est utile lorsqu’un client demande une recherche asynchrone.</span><span class="sxs-lookup"><span data-stu-id="a9783-109">The client time limit preference is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="a9783-110">Dans une recherche asynchrone, le client effectue une demande, puis poursuit avec d’autres tâches en attendant que le serveur retourne les résultats.</span><span class="sxs-lookup"><span data-stu-id="a9783-110">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="a9783-111">Il est possible que le serveur puisse passer en mode hors connexion sans en avertir le client.</span><span class="sxs-lookup"><span data-stu-id="a9783-111">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="a9783-112">Dans ce cas, le client n’aura aucune notification indiquant si le serveur est toujours en cours de traitement de la requête ou s’il n’est plus en ligne.</span><span class="sxs-lookup"><span data-stu-id="a9783-112">In this case, the client will have no notification of whether the server is still processing the query, or if it no longer live.</span></span> <span data-ttu-id="a9783-113">La préférence de limite de temps du client donne au client un contrôle de situations comme celle-ci.</span><span class="sxs-lookup"><span data-stu-id="a9783-113">The client time limit preference gives the client some control of situations like this.</span></span>

<span data-ttu-id="a9783-114">La valeur par défaut de la limite de durée du client est illimitée.</span><span class="sxs-lookup"><span data-stu-id="a9783-114">The default for the client time limit is no limit.</span></span> <span data-ttu-id="a9783-115">Pour définir une limite de temps client, définissez une option de recherche de **\_ \_ délai d’attente SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** qui contient la limite de temps du client, en secondes, dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="a9783-115">To set a client time limit, set an **ADS\_SEARCHPREF\_TIMEOUT** search option with an **ADSTYPE\_INTEGER** value that contains the client time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="a9783-116">Une limite de temps du client de zéro n’indique aucune limite de durée.</span><span class="sxs-lookup"><span data-stu-id="a9783-116">A client time limit of zero indicates no time limit.</span></span>

<span data-ttu-id="a9783-117">L’exemple de code suivant montre comment définir la limite de temps du client.</span><span class="sxs-lookup"><span data-stu-id="a9783-117">The following code example shows how to set the client time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




