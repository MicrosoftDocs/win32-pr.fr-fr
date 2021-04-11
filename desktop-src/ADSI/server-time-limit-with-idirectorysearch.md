---
title: Limite de temps du serveur avec IDirectorySearch
description: Pour éviter d’utiliser tout le temps processeur et empêcher les autres opérations de s’exécuter, spécifiez la limite de durée de recherche sur une petite valeur, puis réexécutez l’application ultérieurement si elle ne parvient pas à générer le rapport.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Limite de temps du serveur avec l’interface ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, limite de temps du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939576"
---
# <a name="server-time-limit-with-idirectorysearch"></a><span data-ttu-id="fcb97-105">Limite de temps du serveur avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="fcb97-105">Server Time Limit with IDirectorySearch</span></span>

<span data-ttu-id="fcb97-106">Lorsque vous demandez une recherche sur un serveur occupé, vous souhaiterez peut-être demander que le serveur limite la recherche à une limite de temps spécifiée.</span><span class="sxs-lookup"><span data-stu-id="fcb97-106">When you request a search on a busy server, you may want to request that the server to restrict the search to a specified time limit.</span></span> <span data-ttu-id="fcb97-107">Par exemple, vous souhaitez exécuter une application pour générer un rapport hebdomadaire sur un serveur qui exécute près de sa capacité.</span><span class="sxs-lookup"><span data-stu-id="fcb97-107">For example, you want to run an application to generate a weekly report on a server that is running near its capacity.</span></span> <span data-ttu-id="fcb97-108">Pour éviter d’utiliser tout le temps processeur et empêcher les autres opérations de s’exécuter, spécifiez la limite de durée de recherche sur une petite valeur, puis réexécutez l’application ultérieurement si elle ne parvient pas à générer le rapport.</span><span class="sxs-lookup"><span data-stu-id="fcb97-108">To avoid using all the CPU time and preventing other operations from running, specify the search time limit to a small value and then rerun the application later if it fails to generate the report.</span></span>

<span data-ttu-id="fcb97-109">Certains serveurs peuvent imposer leur propre limite de temps d’administration.</span><span class="sxs-lookup"><span data-stu-id="fcb97-109">Some servers might impose their own administrative time limit.</span></span> <span data-ttu-id="fcb97-110">Dans ce cas, si vous spécifiez une valeur de limite de temps de recherche supérieure à la limite de temps d’administration, le serveur ignore votre spécification et utilise sa valeur de limite de temps interne à la place.</span><span class="sxs-lookup"><span data-stu-id="fcb97-110">In these cases, if you specify a search time limit value greater than the administrative time limit, the server will ignore your specification and use its internal time limit value instead.</span></span>

<span data-ttu-id="fcb97-111">La valeur par défaut de la limite de durée du serveur est illimitée.</span><span class="sxs-lookup"><span data-stu-id="fcb97-111">The default for the server time limit is no limit.</span></span> <span data-ttu-id="fcb97-112">Pour définir une limite de temps de serveur, définissez une option de recherche de **\_ \_ \_ limite de temps SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** qui contient la limite de temps du serveur, en secondes, dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="fcb97-112">To set a server time limit, set an **ADS\_SEARCHPREF\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the server time limit, in seconds, in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="fcb97-113">Cette opération est illustrée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="fcb97-113">This operation is shown in the following code example.</span></span> <span data-ttu-id="fcb97-114">Une limite de délai de serveur de zéro indique qu’il n’existe aucune limite de temps.</span><span class="sxs-lookup"><span data-stu-id="fcb97-114">A server time limit of zero indicates no time limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




