---
title: Tri des résultats de la recherche avec IDirectorySearch
description: Par défaut, les résultats d’une recherche sont retournés dans aucun ordre garanti. La \_ préférence SEARCHPREF \_ \_ de tri des publicités indique au serveur de trier le jeu de résultats sur une valeur d’attribut spécifiée avant qu’il ne soit retourné au client.
ms.assetid: 1e44a572-7927-4fd5-a3eb-6dad0760d6e5
ms.tgt_platform: multiple
keywords:
- Tri des résultats de la recherche avec IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, tri des résultats de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8433d24b06ac4d361d6520d8af3376ea12acac1f
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730237"
---
# <a name="sorting-the-search-results-with-idirectorysearch"></a><span data-ttu-id="7a135-106">Tri des résultats de la recherche avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="7a135-106">Sorting the Search Results with IDirectorySearch</span></span>

<span data-ttu-id="7a135-107">Par défaut, les résultats d’une recherche sont retournés dans aucun ordre garanti.</span><span class="sxs-lookup"><span data-stu-id="7a135-107">By default, the results of a search are returned in no guaranteed order.</span></span> <span data-ttu-id="7a135-108">La **préférence \_ SEARCHPREF \_ \_ de tri des publicités** indique au serveur de trier le jeu de résultats sur une valeur d’attribut spécifiée avant qu’il ne soit retourné au client.</span><span class="sxs-lookup"><span data-stu-id="7a135-108">The **ADS\_SEARCHPREF\_SORT\_ON** preference instructs the server to sort the result set on a specified attribute value before it is returned to the client.</span></span>

<span data-ttu-id="7a135-109">Il est recommandé d’utiliser des attributs indexés pour le tri.</span><span class="sxs-lookup"><span data-stu-id="7a135-109">It is recommended that indexed attributes be used for sorting.</span></span> <span data-ttu-id="7a135-110">Dans le cas contraire, le serveur doit récupérer le jeu de résultats complet et le trier avant d’envoyer les résultats au client.</span><span class="sxs-lookup"><span data-stu-id="7a135-110">Otherwise, the server must retrieve the complete result set and sort it before sending any results to the client.</span></span> <span data-ttu-id="7a135-111">Cela s’applique également aux recherches paginées.</span><span class="sxs-lookup"><span data-stu-id="7a135-111">This also applies to paged searches.</span></span> <span data-ttu-id="7a135-112">Sachez que les performances d’une recherche triée sont augmentées si le filtre comprend un attribut indexé et que cet attribut est spécifié comme clé de tri. dans ce cas, Active Directory peut satisfaire le tri lors du traitement du filtre.</span><span class="sxs-lookup"><span data-stu-id="7a135-112">Be aware that performance of a sorted search will be increased if the filter includes an indexed attribute and that attribute is specified as the sort key; in this case, Active Directory can satisfy the sort while processing the filter.</span></span> <span data-ttu-id="7a135-113">Par exemple, une requête de tri efficace pour un ensemble d’utilisateurs peut avoir un filtre inclus (SN>Smith) et une clé de tri SN.</span><span class="sxs-lookup"><span data-stu-id="7a135-113">For example, an efficient sort query for a set of users could have a filter that included (sn>smith) and a sort key of sn.</span></span>

<span data-ttu-id="7a135-114">Le tri côté serveur à l’aide de l’option **\_ \_ \_ de tri SEARCHPREF ADS sur** la recherche permet de réduire les performances du serveur.</span><span class="sxs-lookup"><span data-stu-id="7a135-114">Server-side sorting with the **ADS\_SEARCHPREF\_SORT\_ON** search option will reduce the performance of the server.</span></span> <span data-ttu-id="7a135-115">Si vous effectuez de nombreuses recherches, envisagez de trier les résultats manuellement du côté client afin de réduire la charge de travail sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="7a135-115">If you will be performing many searches, consider sorting the results manually on the client side to reduce the workload on the server.</span></span>

<span data-ttu-id="7a135-116">Par défaut, le tri des résultats est désactivé.</span><span class="sxs-lookup"><span data-stu-id="7a135-116">By default, result sorting is disabled.</span></span> <span data-ttu-id="7a135-117">Pour activer le tri des résultats, définissez un **\_ SEARCHPREF ADS \_ \_ sur** l’option de recherche avec un **ADSTYPE \_ Prov \_ spécifique** qui pointe vers une structure de type de clé ( [**\_ SortKey**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) ) ads dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="7a135-117">To enable result sorting, set an **ADS\_SEARCHPREF\_SORT\_ON** search option with an **ADSTYPE\_PROV\_SPECIFIC** that points to an [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="7a135-118">La **structure \_ SortKey ADS** est utilisée pour spécifier l’attribut à utiliser pour le tri et l’ordre de tri.</span><span class="sxs-lookup"><span data-stu-id="7a135-118">The **ADS\_SORTKEY** structure is used to specify the attribute to sort on and the order of the sort.</span></span>

<span data-ttu-id="7a135-119">L’exemple de code suivant montre comment activer le tri des résultats.</span><span class="sxs-lookup"><span data-stu-id="7a135-119">The following code example shows how to enable result sorting.</span></span>


```C++
ADS_SORTKEY SortKey;
SortKey.pszAttrType = L"cn";
SortKey.pszReserved = NULL;
SortKey.fReverseorder = FALSE;

ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SORT_ON;
SearchPref.vValue.dwType = ADSTYPE_PROV_SPECIFIC;
SearchPref.vValue.ProviderSpecific.dwLength = sizeof(SortKey);
SearchPref.vValue.ProviderSpecific.lpValue = (LPBYTE)&SortKey;
```



<span data-ttu-id="7a135-120">Active Directory ne prend pas en charge le tri sur les attributs construits, il n’est donc pas possible de spécifier un attribut construit pour le tri.</span><span class="sxs-lookup"><span data-stu-id="7a135-120">Active Directory does not support sorting on constructed attributes, so it is not possible to specify a constructed attribute for sorting.</span></span> <span data-ttu-id="7a135-121">L’attribut [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) ne peut pas non plus être utilisé pour le tri.</span><span class="sxs-lookup"><span data-stu-id="7a135-121">The [**distinguishedName**](/windows/desktop/ADSchema/a-distinguishedname) attribute also cannot be used for sorting.</span></span> <span data-ttu-id="7a135-122">Active Directory ne permet pas non plus d’effectuer un tri sur plusieurs attributs, l’option SEARCHPREF de l’option Trier sur les publicités ne peut donc contenir qu’une [**seule structure \_**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) **\_ \_ \_ de type de clé** .</span><span class="sxs-lookup"><span data-stu-id="7a135-122">Active Directory also does not allow sorting on more than one attribute, so the **ADS\_SEARCHPREF\_SORT\_ON** search option can only contain one [**ADS\_SORTKEY**](/windows/desktop/api/Iads/ns-iads-ads_sortkey) structure.</span></span>

 

 