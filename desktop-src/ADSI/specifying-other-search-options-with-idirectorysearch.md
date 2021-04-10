---
title: Spécification d’autres options de recherche avec IDirectorySearch
description: L’interface IDirectorySearch offre un contrôle supplémentaire sur la manière dont la recherche est effectuée par le biais des options de recherche.
ms.assetid: 91b7ba90-99b3-4137-8e4e-8d0ccfb0ec13
ms.tgt_platform: multiple
keywords:
- Spécification d’autres options de recherche avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7064a291c3a299a5435ec454a17b1a666f20d0a9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939574"
---
# <a name="specifying-other-search-options-with-idirectorysearch"></a><span data-ttu-id="a4fb2-105">Spécification d’autres options de recherche avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-105">Specifying Other Search Options with IDirectorySearch</span></span>

<span data-ttu-id="a4fb2-106">L’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) offre un contrôle supplémentaire sur la manière dont la recherche est effectuée par le biais des options de recherche.</span><span class="sxs-lookup"><span data-stu-id="a4fb2-106">The [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface provide additional control over how the search is performed through the use of search options.</span></span> <span data-ttu-id="a4fb2-107">Ces options de recherche sont définies en remplissant un tableau de [**\_ SEARCHPREF d' \_ informations sur les publicités**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) et en appelant la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="a4fb2-107">These search options are set by filling in an array of [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) structures and calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="a4fb2-108">Pour plus d'informations, voir les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="a4fb2-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="a4fb2-109">Utilisation de la méthode SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="a4fb2-109">Using the SetSearchPreference Method</span></span>](using-the-setsearchpreference-method.md)
-   [<span data-ttu-id="a4fb2-110">Recherches synchrones et asynchrones avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-110">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-111">Pagination avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-111">Paging with IDirectorySearch</span></span>](paging-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-112">Mise en cache des résultats avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-112">Result Caching with IDirectorySearch</span></span>](result-caching-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-113">Exécution d’une requête d’étendue d’attribut</span><span class="sxs-lookup"><span data-stu-id="a4fb2-113">Performing an Attribute Scope Query</span></span>](performing-an-attribute-scoped-query.md)
-   [<span data-ttu-id="a4fb2-114">Tri des résultats de la recherche avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-114">Sorting the Search Results with IDirectorySearch</span></span>](sorting-the-search-results-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-115">Repérage de références avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-115">Referral Chasing with IDirectorySearch</span></span>](referral-chasing-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-116">Limite de taille avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-116">Size Limit with IDirectorySearch</span></span>](size-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-117">Limite de temps du serveur avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-117">Server Time Limit with IDirectorySearch</span></span>](server-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-118">Limite de temps du client avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-118">Client Time Limit with IDirectorySearch</span></span>](client-time-limit-with-idirectorysearch.md)
-   [<span data-ttu-id="a4fb2-119">Retour uniquement des noms d’attributs avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="a4fb2-119">Returning Only Attribute Names with IDirectorySearch</span></span>](returning-only-attribute-names-with-idirectorysearch.md)

 

 




