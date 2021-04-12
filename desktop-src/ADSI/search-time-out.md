---
title: Délai d’expiration de la recherche
description: Un client peut également imposer une limite de temps pendant laquelle il doit attendre qu’un serveur retourne le jeu de résultats.
ms.assetid: a31bc8b2-9adf-4dff-a6df-67d6bf304e04
ms.tgt_platform: multiple
keywords:
- Rechercher dans le délai d’expiration ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cdfdc63dd4490a840a16eb61598b2461c3e1a40
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309221"
---
# <a name="search-time-out"></a><span data-ttu-id="b7397-104">Délai d’expiration de la recherche</span><span class="sxs-lookup"><span data-stu-id="b7397-104">Search Time Out</span></span>

<span data-ttu-id="b7397-105">Un client peut également imposer une limite de temps pendant laquelle il doit attendre qu’un serveur retourne le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="b7397-105">A client can also impose a time limit that it will wait for a server to return the result set.</span></span> <span data-ttu-id="b7397-106">La valeur de l’option « délai de recherche » spécifie cette limite.</span><span class="sxs-lookup"><span data-stu-id="b7397-106">The value of the "search time out" option specifies this limit.</span></span> <span data-ttu-id="b7397-107">Lorsque le serveur ne parvient pas à répondre à une requête dans le délai spécifié, le client peut arrêter la recherche et réessayer plus tard.</span><span class="sxs-lookup"><span data-stu-id="b7397-107">When the server fails to respond to a query within the specified time period, the client can stop the search and try again later.</span></span>

<span data-ttu-id="b7397-108">La propriété de délai d’attente est utile lorsqu’un client demande une recherche asynchrone.</span><span class="sxs-lookup"><span data-stu-id="b7397-108">The time-out property is useful when a client requests an asynchronous search.</span></span> <span data-ttu-id="b7397-109">Dans une recherche asynchrone, le client effectue une demande, puis poursuit avec d’autres tâches en attendant que le serveur retourne les résultats.</span><span class="sxs-lookup"><span data-stu-id="b7397-109">In an asynchronous search, the client makes a request and then proceeds with other tasks while waiting for the server to return the results.</span></span> <span data-ttu-id="b7397-110">Il est possible que le serveur puisse passer en mode hors connexion sans en avertir le client.</span><span class="sxs-lookup"><span data-stu-id="b7397-110">It is possible that the server can go offline without notifying the client.</span></span> <span data-ttu-id="b7397-111">Dans ce cas, le client n’a aucun moyen de reconnaître que le serveur est en train de traiter la requête, ou s’il a cessé d’être en ligne.</span><span class="sxs-lookup"><span data-stu-id="b7397-111">In this case, the client has no way of recognizing that the server is still processing the query, or if it has ceased to be live.</span></span> <span data-ttu-id="b7397-112">La propriété de délai d’attente fournit au client un contrôle sur ces instances.</span><span class="sxs-lookup"><span data-stu-id="b7397-112">The time-out property provides the client some control in such instances.</span></span>

<span data-ttu-id="b7397-113">Pour plus d’informations sur l’utilisation de l’option de délai d’attente de recherche avec une interface de recherche spécifique, consultez :</span><span class="sxs-lookup"><span data-stu-id="b7397-113">For more information about using the search time-out option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="b7397-114">Limite de temps du client avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="b7397-114">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="b7397-115">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="b7397-115">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="b7397-116">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="b7397-116">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




