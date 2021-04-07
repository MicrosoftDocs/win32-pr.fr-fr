---
title: Pagination avec IDirectorySearch
description: La pagination spécifie le nombre de lignes que le serveur retourne au client.
ms.assetid: cf4aa56a-c6f7-47c8-956d-512a5cffbf22
ms.tgt_platform: multiple
keywords:
- Pagination avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, pagination
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e9fdf001f5908f6c3fc7321c8c94cda09f1b96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939584"
---
# <a name="paging-with-idirectorysearch"></a><span data-ttu-id="ed597-105">Pagination avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="ed597-105">Paging with IDirectorySearch</span></span>

<span data-ttu-id="ed597-106">La pagination spécifie le nombre de lignes que le serveur retourne au client.</span><span class="sxs-lookup"><span data-stu-id="ed597-106">Paging specifies how many rows that the server returns to the client.</span></span> <span data-ttu-id="ed597-107">Une page peut être définie par le nombre de lignes ou une limite de temps.</span><span class="sxs-lookup"><span data-stu-id="ed597-107">A page can be defined by the number of rows or a time limit.</span></span> <span data-ttu-id="ed597-108">L’objet COM ADSI récupère chaque page de résultats en fonction des valeurs indiquées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="ed597-108">The ADSI COM object retrieves each page of results based on the values listed in the following table.</span></span> <span data-ttu-id="ed597-109">L’appelant appelle [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) lorsqu’il a atteint la fin de la page et l’objet com ADSI récupère la page suivante.</span><span class="sxs-lookup"><span data-stu-id="ed597-109">The caller calls [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) when it has reached the page end, and the ADSI COM object retrieves the next page.</span></span>



| <span data-ttu-id="ed597-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="ed597-110">Value</span></span>                                   | <span data-ttu-id="ed597-111">Description</span><span class="sxs-lookup"><span data-stu-id="ed597-111">Description</span></span>                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed597-112">**\_pages de SEARCHPREF ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ed597-112">**ADS\_SEARCHPREF\_PAGESIZE**</span></span>           | <span data-ttu-id="ed597-113">Spécifie le nombre maximal de lignes à retourner dans une page.</span><span class="sxs-lookup"><span data-stu-id="ed597-113">Specifies the maximum number of rows to return in a page.</span></span>                                                                                                                                                                                            |
| <span data-ttu-id="ed597-114">**\_limite de \_ temps paginée SEARCHPREF \_ ADS \_**</span><span class="sxs-lookup"><span data-stu-id="ed597-114">**ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT**</span></span> | <span data-ttu-id="ed597-115">Spécifie la durée maximale, en secondes, pendant laquelle le serveur doit collecter une page de résultats avant de renvoyer la page au client.</span><span class="sxs-lookup"><span data-stu-id="ed597-115">Specifies the maximum time, in seconds, that the server should spend collecting a page of results before returning the page to the client.</span></span> <span data-ttu-id="ed597-116">Si la limite est atteinte, le serveur arrête la recherche et retourne les lignes déjà récupérées pour la page.</span><span class="sxs-lookup"><span data-stu-id="ed597-116">If the limit is reached, the server stops the search and returns the rows already retrieved for the page.</span></span> |



 

<span data-ttu-id="ed597-117">Si aucune de ces préférences de recherche n’est définie, la valeur par défaut est aucune pagination.</span><span class="sxs-lookup"><span data-stu-id="ed597-117">If neither of these search preferences is set, the default is no paging.</span></span> <span data-ttu-id="ed597-118">Les recherches des Active Directory effectuées sans pagination sont limitées au fait de retourner un maximum de 1000 premiers enregistrements. vous devez donc utiliser une recherche paginée s’il est possible que le jeu de résultats contienne plus de 1000 éléments.</span><span class="sxs-lookup"><span data-stu-id="ed597-118">Searches of the Active Directory performed without paging are limited to returning a maximum of the first 1000 records, so you must use a paged search if there is the possibility that the result set will contain more than 1000 items.</span></span>

<span data-ttu-id="ed597-119">Une opération de recherche peut entraîner le renvoi d’un grand nombre d’objets.</span><span class="sxs-lookup"><span data-stu-id="ed597-119">A search operation may result in a large number of objects being returned.</span></span> <span data-ttu-id="ed597-120">Si le serveur retourne le résultat dans un jeu, il peut réduire les performances du client et du serveur, ainsi que affecter la charge réseau.</span><span class="sxs-lookup"><span data-stu-id="ed597-120">If the server returns the result in one set, it could decrease the performance of the client and server, as well as affect the network load.</span></span> <span data-ttu-id="ed597-121">Les recherches paginées peuvent être utilisées pour éviter cela.</span><span class="sxs-lookup"><span data-stu-id="ed597-121">Paged searches can be used to prevent this.</span></span> <span data-ttu-id="ed597-122">Dans une recherche paginée, le client peut accepter les résultats dans des paquets plus petits.</span><span class="sxs-lookup"><span data-stu-id="ed597-122">In a paged search, the client can accept results in smaller packets.</span></span> <span data-ttu-id="ed597-123">La taille d’un paquet est connue sous le nom de taille de page de recherche.</span><span class="sxs-lookup"><span data-stu-id="ed597-123">The size of a packet is known as the search page size.</span></span>

<span data-ttu-id="ed597-124">Les recherches paginées offrent des avantages au client et au serveur.</span><span class="sxs-lookup"><span data-stu-id="ed597-124">Paged searches offer benefits to both the client and the server.</span></span> <span data-ttu-id="ed597-125">Le client peut être plus réactif pour présenter les résultats aux utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="ed597-125">The client can be more responsive in presenting the results to users.</span></span> <span data-ttu-id="ed597-126">Cela s’applique particulièrement aux outils d’interface utilisateur graphique qui peuvent démarrer le processus d’affichage de la fenêtre pendant que l’autre thread reçoit simultanément les données.</span><span class="sxs-lookup"><span data-stu-id="ed597-126">This is especially relevant to graphical user interface tools that can begin the window display process while the other thread concurrently receives the data.</span></span>

<span data-ttu-id="ed597-127">Côté serveur, les recherches paginées rendent l’opération évolutive.</span><span class="sxs-lookup"><span data-stu-id="ed597-127">On the server side, paged searches make the operation scalable.</span></span> <span data-ttu-id="ed597-128">Par exemple, si les clients 100 émettent des demandes de recherche simultanément et, en moyenne, chaque client reçoit 200 objets.</span><span class="sxs-lookup"><span data-stu-id="ed597-128">For example, if one hundred clients issue search requests simultaneously and, on the average, each client receives two hundred objects.</span></span> <span data-ttu-id="ed597-129">Si aucune taille de page n’est spécifiée, dans le pire des cas, le serveur doit disposer de suffisamment de mémoire pour contenir 20 000 objets.</span><span class="sxs-lookup"><span data-stu-id="ed597-129">If no page size is specified, in the worst-case scenario, the server must have sufficient memory to hold 20,000 objects.</span></span> <span data-ttu-id="ed597-130">À l’inverse, si chaque client spécifie une taille de page, par exemple, dix objets, la mémoire requise sur le serveur est donc réduite d’un facteur de 20.</span><span class="sxs-lookup"><span data-stu-id="ed597-130">Conversely, if each client specifies a page size to be, for example, ten objects, the memory requirement on the server is thus reduced by a factor of 20.</span></span>

<span data-ttu-id="ed597-131">En outre, à l’aide d’une recherche paginée, un client peut abandonner l’opération en cours.</span><span class="sxs-lookup"><span data-stu-id="ed597-131">In addition, using a paged search, a client can abandon the operation in progress.</span></span> <span data-ttu-id="ed597-132">En revanche, dans une recherche non paginée, le client reçoit un jeu de résultats dans un paquet.</span><span class="sxs-lookup"><span data-stu-id="ed597-132">In contrast, in a non-paged search, the client receives a result set in one packet.</span></span> <span data-ttu-id="ed597-133">Cela peut réduire les performances du réseau.</span><span class="sxs-lookup"><span data-stu-id="ed597-133">This can decrease network performance.</span></span>

<span data-ttu-id="ed597-134">ADSI gère la taille de page du client.</span><span class="sxs-lookup"><span data-stu-id="ed597-134">ADSI handles the page size for the client.</span></span> <span data-ttu-id="ed597-135">Le client n’a pas besoin de compter le nombre d’objets en cours.</span><span class="sxs-lookup"><span data-stu-id="ed597-135">The client does not have to count the number of objects in progress.</span></span> <span data-ttu-id="ed597-136">ADSI encapsule l’interaction du serveur pour le client.</span><span class="sxs-lookup"><span data-stu-id="ed597-136">ADSI encapsulates the server interaction for the client.</span></span> <span data-ttu-id="ed597-137">Du point de vue du client, la recherche retourne un jeu de résultats complet.</span><span class="sxs-lookup"><span data-stu-id="ed597-137">From the client perspective, the search returns a complete result set.</span></span>

<span data-ttu-id="ed597-138">Il est recommandé d’utiliser la pagination.</span><span class="sxs-lookup"><span data-stu-id="ed597-138">It is recommended that paging is used.</span></span>

<span data-ttu-id="ed597-139">Pour spécifier une taille de page maximale, définissez une option de recherche **\_ SEARCHPREF \_ pages ADS** avec une valeur **\_ entière ADSTYPE** définie sur le nombre maximal de lignes par page dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="ed597-139">To specify a maximum page size, set an **ADS\_SEARCHPREF\_PAGESIZE** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of rows per page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="ed597-140">L’exemple de code suivant montre comment définir la taille de page maximale.</span><span class="sxs-lookup"><span data-stu-id="ed597-140">The following code example shows how to set the maximum page size.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="ed597-141">Pour spécifier une heure de page, définissez une option de recherche de **\_ \_ \_ \_ limite de temps paginée de SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** définie sur le nombre maximal de secondes que le serveur doit consacrer à la récupération d’une page dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="ed597-141">To specify a page time, set an **ADS\_SEARCHPREF\_PAGED\_TIME\_LIMIT** search option with an **ADSTYPE\_INTEGER** value set to the maximum number of seconds that the server should spend retrieving a page in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="ed597-142">L’exemple de code suivant montre comment spécifier le temps de la page.</span><span class="sxs-lookup"><span data-stu-id="ed597-142">The following code example shows how to specify page time.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




