---
title: Recherches synchrones et asynchrones avec IDirectorySearch
description: Lorsque vous effectuez une recherche à l’aide de l’interface IDirectorySearch, la méthode IDirectorySearch ExecuteSearch n’envoie pas la demande de recherche au serveur.
ms.assetid: c4387202-22a0-497a-af0a-20aa8ede905d
ms.tgt_platform: multiple
keywords:
- Recherches synchrones et asynchrones avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, recherches synchrones et asynchrones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f369d45aaf4453d310c4bac2259bfa9cd089f567
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104379587"
---
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a><span data-ttu-id="4ac29-105">Recherches synchrones et asynchrones avec IDirectorySearch</span><span class="sxs-lookup"><span data-stu-id="4ac29-105">Synchronous and Asynchronous Searches with IDirectorySearch</span></span>

<span data-ttu-id="4ac29-106">Lorsque vous effectuez une recherche à l’aide de l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) n’envoie pas la demande de recherche au serveur.</span><span class="sxs-lookup"><span data-stu-id="4ac29-106">When you perform a search using the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface, the [**IDirectorySearch::ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) method does not send the search request to the server.</span></span> <span data-ttu-id="4ac29-107">Cette méthode enregistre uniquement les paramètres de recherche.</span><span class="sxs-lookup"><span data-stu-id="4ac29-107">This method only saves the search parameters.</span></span> <span data-ttu-id="4ac29-108">La demande de recherche est en fait envoyée lorsque vous appelez [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span><span class="sxs-lookup"><span data-stu-id="4ac29-108">The search request is actually sent when you call [**IDirectorySearch::GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**IDirectorySearch::GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).</span></span>

<span data-ttu-id="4ac29-109">Pour les recherches Active Directory, la principale différence entre synchrone et asynchrone est lorsque la première ligne du résultat est retournée, c’est-à-dire lorsque le premier appel [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) retourne.</span><span class="sxs-lookup"><span data-stu-id="4ac29-109">For Active Directory searches, the primary difference between synchronous and asynchronous is when the first row of the result is returned, that is, when the first [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) or [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) call returns.</span></span>

<span data-ttu-id="4ac29-110">Dans une recherche synchrone, si la pagination n’est pas activée, la première ligne est retournée lorsque le serveur a créé et retourné le jeu de résultats entier au client.</span><span class="sxs-lookup"><span data-stu-id="4ac29-110">In a synchronous search, if paging is not enabled, the first row is returned when the server has constructed and returned the entire result set to the client.</span></span> <span data-ttu-id="4ac29-111">Si la pagination est activée, la première ligne est retournée lorsque la première page du jeu de résultats est retournée.</span><span class="sxs-lookup"><span data-stu-id="4ac29-111">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="4ac29-112">Dans une recherche asynchrone, si la pagination n’est pas activée, la première ligne est retournée lorsque le serveur a construit la première ligne du jeu de résultats.</span><span class="sxs-lookup"><span data-stu-id="4ac29-112">In an asynchronous search, if paging is not enabled, the first row is returned when the server has constructed the first row of the result set.</span></span> <span data-ttu-id="4ac29-113">Si la pagination est activée, la première ligne est retournée lorsque la première page du jeu de résultats est retournée.</span><span class="sxs-lookup"><span data-stu-id="4ac29-113">If paging is enabled, the first row is returned when the first page of the result set is returned.</span></span>

<span data-ttu-id="4ac29-114">Le type de recherche par défaut est synchrone.</span><span class="sxs-lookup"><span data-stu-id="4ac29-114">The default search type is synchronous.</span></span> <span data-ttu-id="4ac29-115">Pour spécifier une recherche asynchrone, définissez une option de recherche **\_ \_ asynchrone SEARCHPREF ADS** avec la valeur **\_ booléenne ADSTYPE** **true** dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) transmis à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .</span><span class="sxs-lookup"><span data-stu-id="4ac29-115">To specify an asynchronous search, set an **ADS\_SEARCHPREF\_ASYNCHRONOUS** search option with an **ADSTYPE\_BOOLEAN** value of **TRUE** in the [**ADS\_SEARCHPREF\_INFO**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) array passed to the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method.</span></span> <span data-ttu-id="4ac29-116">Cette opération est illustrée dans l’exemple de code suivant.</span><span class="sxs-lookup"><span data-stu-id="4ac29-116">This operation is shown in the following code example.</span></span>


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




