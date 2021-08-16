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
ms.openlocfilehash: 3e7f40d7af4069c9b67d9cd2634f6b7f58f51aafce95af9d4f9275b0e55fc1b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119637479"
---
# <a name="using-the-setsearchpreference-method"></a>Utilisation de la méthode SetSearchPreference

L’appel de la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) modifie la façon dont les résultats de la recherche sont obtenus et présentés via l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) .

La documentation du kit de développement logiciel (SDK) définit [**SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) comme suit :


```C++
HRESULT SetSearchPreference(
            //Search preferences to be set.
            PADS_SEARCHPREF_INFO pSearchPrefs,
            //Number of preferences.
            DWORD dwNumPrefs
            );
```



Plusieurs préférences peuvent être définies en passant un tableau en tant que premier paramètre et la taille du tableau comme deuxième paramètre.


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



Cet exemple définit la taille de la page sur 100 lignes et l’étendue sur \_ le \_ type de sous-arborescence étendue ads. Le paramètre taille de la page oblige le serveur à retourner immédiatement des données au client, après 100 lignes calculées. Le \_ paramètre de sous-arborescence étendue ADS \_ fait que la recherche englobe toutes les branches de l’arborescence sous le point à partir duquel la recherche est exécutée.

 

 




