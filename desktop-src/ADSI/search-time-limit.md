---
title: Limite de durée de recherche
description: Lorsque vous demandez une recherche sur un serveur qui se trouve sous une charge de travail lourde, vous pouvez demander au serveur de limiter la recherche à une limite de temps spécifiée.
ms.assetid: 199ac73b-3624-4cd5-a1ee-6db418cd77ba
ms.tgt_platform: multiple
keywords:
- Temps de recherche limité par ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e11ff9de38a17fe6ebac4ebb045e2f8b896bc764
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106513443"
---
# <a name="search-time-limit"></a><span data-ttu-id="da30d-104">Limite de durée de recherche</span><span class="sxs-lookup"><span data-stu-id="da30d-104">Search Time Limit</span></span>

<span data-ttu-id="da30d-105">Lorsque vous demandez une recherche sur un serveur qui se trouve sous une charge de travail lourde, vous pouvez demander au serveur de limiter la recherche à une limite de temps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="da30d-105">When you request a search on a server that is under a heavy workload, you may want to instruct the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="da30d-106">Par exemple, pour exécuter une application afin de générer un rapport hebdomadaire sur un serveur qui s’exécute presque, et pour éviter de maximiser le temps processeur et empêcher l’exécution d’autres tâches, vous pouvez définir la durée de la recherche sur une valeur faible et réexécuter l’application ultérieurement si elle ne parvient pas à générer le rapport.</span><span class="sxs-lookup"><span data-stu-id="da30d-106">For example, to execute an application to generate a weekly report on a server that is running near capacity, and to avoid maximizing the CPU time and preventing other jobs from running, you can set the search time to a small value and rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="da30d-107">Certains serveurs peuvent imposer leur propre limite de temps d’administration.</span><span class="sxs-lookup"><span data-stu-id="da30d-107">Some servers can impose their own administrative time limit.</span></span> <span data-ttu-id="da30d-108">Dans ce cas, si vous spécifiez une valeur de limite de temps de recherche supérieure à la limite de temps d’administration, le serveur ignore votre spécification et utilise plutôt sa limite de temps d’administration interne.</span><span class="sxs-lookup"><span data-stu-id="da30d-108">In these cases, if you specify a search time limit value greater than the administrative time limit, the server ignores your specification and use its internal administrative time limit instead.</span></span>

<span data-ttu-id="da30d-109">Pour plus d’informations sur l’utilisation de l’option de limite de temps de recherche avec une interface de recherche spécifique, consultez :</span><span class="sxs-lookup"><span data-stu-id="da30d-109">For more information about using the search time limit option with a specific search interface, see:</span></span>

-   [<span data-ttu-id="da30d-110">Limite de temps du serveur avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="da30d-110">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="da30d-111">Recherche avec ActiveX Data Objects</span><span class="sxs-lookup"><span data-stu-id="da30d-111">Searching with ActiveX Data Objects</span></span>](searching-with-activex-data-objects-ado.md)
-   [<span data-ttu-id="da30d-112">Recherche avec OLE DB</span><span class="sxs-lookup"><span data-stu-id="da30d-112">Searching with OLE DB</span></span>](searching-with-ole-db.md)

 

 




