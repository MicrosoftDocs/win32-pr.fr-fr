---
title: Mise en cache du résultat (côté client)
description: La mise en cache côté client stocke le jeu de résultats dans la mémoire du client, ce qui permet d’améliorer les performances côté client.
ms.assetid: 6e61b2f6-dd58-466e-9cef-5bc6301e983f
ms.tgt_platform: multiple
keywords:
- Mise en cache du résultat (côté client) ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb965da1da0c791db215dd7eee925a7c9f67ccf8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939603"
---
# <a name="caching-the-result-client-side"></a><span data-ttu-id="72f45-104">Mise en cache du résultat (côté client)</span><span class="sxs-lookup"><span data-stu-id="72f45-104">Caching the Result (Client Side)</span></span>

<span data-ttu-id="72f45-105">La mise en cache côté client stocke le jeu de résultats dans la mémoire du client, ce qui permet d’améliorer les performances côté client.</span><span class="sxs-lookup"><span data-stu-id="72f45-105">Client-side caching stores the result set in the client memory, providing performance enhancements for the client side.</span></span> <span data-ttu-id="72f45-106">Un client peut réexaminer un objet de façon répétée sans plusieurs allers-retours au serveur.</span><span class="sxs-lookup"><span data-stu-id="72f45-106">A client can revisit an object repeatedly without multiple trips to the server.</span></span> <span data-ttu-id="72f45-107">Par défaut, ADSI met en cache le jeu de résultats pour les clients.</span><span class="sxs-lookup"><span data-stu-id="72f45-107">By default, ADSI caches the result set for the clients.</span></span> <span data-ttu-id="72f45-108">Cela permet à ADSI de fournir aux clients une prise en charge des curseurs de type SQL.</span><span class="sxs-lookup"><span data-stu-id="72f45-108">This enables ADSI to provide clients with SQL-like cursor support.</span></span> <span data-ttu-id="72f45-109">Vous pouvez effectuer une itération à travers un jeu de résultats donné plusieurs fois.</span><span class="sxs-lookup"><span data-stu-id="72f45-109">You may iterate through a given result set several times.</span></span>

<span data-ttu-id="72f45-110">ADSI permet également aux clients de désactiver le cache pour réduire les besoins en mémoire.</span><span class="sxs-lookup"><span data-stu-id="72f45-110">ADSI also enables clients to turn off the cache to reduce memory requirements.</span></span> <span data-ttu-id="72f45-111">Si la mise en cache côté client est désactivée, le client ne conserve pas le jeu de résultats en mémoire.</span><span class="sxs-lookup"><span data-stu-id="72f45-111">If client-side caching is disabled, the client does not maintain the result set in memory.</span></span> <span data-ttu-id="72f45-112">Chaque ligne est libérée une fois que l’application l’a récupérée.</span><span class="sxs-lookup"><span data-stu-id="72f45-112">Each row is freed after the application retrieves it.</span></span> <span data-ttu-id="72f45-113">La désactivation de la mise en cache côté client peut être utile pour réduire les besoins en mémoire côté client dans ce cas, comme lorsque vous envisagez de faire une seule passe dans le jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="72f45-113">Disabling client-side caching can be useful for decreasing the client-side memory requirements in such cases as when you intend only to make a single pass through the result set.</span></span> <span data-ttu-id="72f45-114">Toutefois, lorsque les clients choisissent de ne pas mettre en cache le résultat, ils accèdent à la prise en charge des curseurs.</span><span class="sxs-lookup"><span data-stu-id="72f45-114">However, when clients elect not to cache the result, they give up cursor support.</span></span>

<span data-ttu-id="72f45-115">Pour plus d’informations sur la mise en cache des résultats avec une interface de recherche spécifique, consultez :</span><span class="sxs-lookup"><span data-stu-id="72f45-115">For more information about results caching with a specific search interface, see:</span></span>

-   [<span data-ttu-id="72f45-116">Mise en cache des résultats avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="72f45-116">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="72f45-117">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="72f45-117">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="72f45-118">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="72f45-118">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




