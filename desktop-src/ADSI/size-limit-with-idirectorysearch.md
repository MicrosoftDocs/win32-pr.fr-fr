---
title: Limite de taille avec IDirectorySearch
description: Le client peut se concentrer sur un petit nombre d’objets renvoyés par le serveur et ignorer le reste du jeu de résultats.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite de taille avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, limite de taille
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512018"
---
# <a name="size-limit-with-idirectorysearch"></a><span data-ttu-id="62a97-105">Limite de taille avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="62a97-105">Size Limit with IDirectorySearch</span></span>

<span data-ttu-id="62a97-106">Pour réduire les besoins en mémoire ou à d’autres fins, le client peut se concentrer sur un petit nombre d’objets retournés par le serveur et ignorer le reste du jeu de résultats qui ne sont pas intéressants.</span><span class="sxs-lookup"><span data-stu-id="62a97-106">To reduce the memory requirement or for other purposes, the client can focus on a small number of objects returned from the server and ignore the rest of the result set that are not of interest.</span></span> <span data-ttu-id="62a97-107">Pour ce faire, le client spécifie la limite de taille de recherche et d’autres critères de recherche appropriés.</span><span class="sxs-lookup"><span data-stu-id="62a97-107">To accomplish this, the client specifies the search size limit and other appropriate search criteria.</span></span> <span data-ttu-id="62a97-108">Par exemple, si l’annuaire stocke les scores de test d’une circonscription scolaire, vous pouvez interroger les dix meilleurs étudiants avec les meilleurs scores de test en spécifiant une limite de taille de dix (10) et un ordre de tri décroissant.</span><span class="sxs-lookup"><span data-stu-id="62a97-108">For example, if the directory stores the test scores of a school district, you can query the top ten students with the highest test scores by specifying a size limit of ten (10) and a descending sort order.</span></span>

<span data-ttu-id="62a97-109">La valeur par défaut de la limite de taille est illimitée.</span><span class="sxs-lookup"><span data-stu-id="62a97-109">The default for size limit is no limit.</span></span> <span data-ttu-id="62a97-110">Pour définir une limite de taille, définissez une option de recherche de **\_ limite de \_ taille \_ de SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** qui contient la taille maximale dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="62a97-110">To set a size limit, set an **ADS\_SEARCHPREF\_SIZE\_LIMIT** search option with an **ADSTYPE\_INTEGER** value that contains the maximum size in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span>

<span data-ttu-id="62a97-111">L’exemple de code suivant montre comment définir la limite de taille.</span><span class="sxs-lookup"><span data-stu-id="62a97-111">The following code example shows how to set the size limit.</span></span> <span data-ttu-id="62a97-112">Une valeur de limite de taille de zéro indique aucune limite de taille.</span><span class="sxs-lookup"><span data-stu-id="62a97-112">A size limit value of zero indicates no size limit.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



<span data-ttu-id="62a97-113">Par Active Directory, la limite de taille spécifie le nombre maximal d’objets qui doivent être retournés par la recherche.</span><span class="sxs-lookup"><span data-stu-id="62a97-113">For Active Directory, the size limit specifies the maximum number of objects to be returned by the search.</span></span> <span data-ttu-id="62a97-114">Par ailleurs, pour Active Directory, le nombre maximal d’objets renvoyés par une recherche est de 1000 objets.</span><span class="sxs-lookup"><span data-stu-id="62a97-114">Also for Active Directory, the maximum number of objects returned by a search is 1000 objects.</span></span>

 

 




