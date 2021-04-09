---
title: Utilisation de la méthode SetSearchPreference
description: L’appel de la méthode IDirectorySearch SetSearchPreference modifie la façon dont les résultats de la recherche sont obtenus et présentés via l’interface IDirectorySearch.
ms.assetid: 37583276-8372-4478-82aa-3e456cc0f8f1
ms.tgt_platform: multiple
keywords:
- SetSearchPreference ADSI, à l’aide de la méthode SetSearchPreference
- ADSI ADSI, exemple de code C/C++, à l’aide de la méthode SetSearchPreference
- interroge ADSI à l’aide de SetSearchPreference
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29c357fd331ae8589bffdd3ff7a834a7bc9e0430
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028540"
---
# <a name="using-the-setsearchpreference-method"></a><span data-ttu-id="15940-106">Utilisation de la méthode SetSearchPreference</span><span class="sxs-lookup"><span data-stu-id="15940-106">Using the SetSearchPreference Method</span></span>

<span data-ttu-id="15940-107">L’appel de la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) modifie la façon dont les résultats de la recherche sont obtenus et présentés via l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .</span><span class="sxs-lookup"><span data-stu-id="15940-107">Calling the [**IDirectorySearch::SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) method changes the way in which the search results are obtained and presented through the [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) interface.</span></span>

<span data-ttu-id="15940-108">La documentation du kit de développement logiciel (SDK) définit [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) comme suit :</span><span class="sxs-lookup"><span data-stu-id="15940-108">The SDK documentation defines [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) as follows:</span></span>


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



<span data-ttu-id="15940-109">Plusieurs préférences peuvent être définies en passant un tableau en tant que premier paramètre et la taille du tableau comme deuxième paramètre.</span><span class="sxs-lookup"><span data-stu-id="15940-109">Multiple preferences may be set by passing an array as the first parameter and the array size as the second parameter.</span></span>


```C++
ADS_SEARCHPREF_INFO arSearchPrefs[2];
 
arSearchPrefs[0].dwSearchPref = ADS_SEARCHPREF_PAGESIZE; 
arSearchPrefs[0].vValue.dwType = ADSTYPE_INTEGER;
arSearchPrefs[0].vValue.Integer = 100;
 
arSearchPrefs[1].dwSearchPref = ADS_SEARCHPREF_SEARCH_SCOPE; 
arSearchPrefs[1].vValue.dwType = ADSTYPE_INTEGER; 
arSearchPrefs[1].vValue.Integer = ADS_SCOPE_SUBTREE; 
 
hr = pDSearch->SetSearchPreference(&arSearchPrefs, 2);
```



<span data-ttu-id="15940-110">Cet exemple définit la taille de la page sur 100 lignes et l’étendue sur \_ le \_ type de sous-arborescence étendue ads.</span><span class="sxs-lookup"><span data-stu-id="15940-110">This example sets the page size to 100 rows and the scope to the ADS\_SCOPE\_SUBTREE type.</span></span> <span data-ttu-id="15940-111">Le paramètre taille de la page oblige le serveur à retourner immédiatement des données au client, après 100 lignes calculées.</span><span class="sxs-lookup"><span data-stu-id="15940-111">The page size setting causes the server to immediately return data to the client, after 100 rows have been calculated.</span></span> <span data-ttu-id="15940-112">Le \_ paramètre de sous-arborescence étendue ADS \_ fait que la recherche englobe toutes les branches de l’arborescence sous le point à partir duquel la recherche est exécutée.</span><span class="sxs-lookup"><span data-stu-id="15940-112">The ADS\_SCOPE\_SUBTREE setting causes the search to encompass all branches in the tree below the point from which the search is being executed.</span></span>

 

 




