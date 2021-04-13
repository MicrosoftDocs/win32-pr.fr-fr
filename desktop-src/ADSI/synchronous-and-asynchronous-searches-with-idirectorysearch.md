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
# <a name="synchronous-and-asynchronous-searches-with-idirectorysearch"></a>Recherches synchrones et asynchrones avec IDirectorySearch

Lorsque vous effectuez une recherche à l’aide de l’interface [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) , la méthode [**IDirectorySearch :: ExecuteSearch**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-executesearch) n’envoie pas la demande de recherche au serveur. Cette méthode enregistre uniquement les paramètres de recherche. La demande de recherche est en fait envoyée lorsque vous appelez [**IDirectorySearch :: GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow).

Pour les recherches Active Directory, la principale différence entre synchrone et asynchrone est lorsque la première ligne du résultat est retournée, c’est-à-dire lorsque le premier appel [**GetFirstRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getfirstrow) ou [**GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) retourne.

Dans une recherche synchrone, si la pagination n’est pas activée, la première ligne est retournée lorsque le serveur a créé et retourné le jeu de résultats entier au client. Si la pagination est activée, la première ligne est retournée lorsque la première page du jeu de résultats est retournée.

Dans une recherche asynchrone, si la pagination n’est pas activée, la première ligne est retournée lorsque le serveur a construit la première ligne du jeu de résultats. Si la pagination est activée, la première ligne est retournée lorsque la première page du jeu de résultats est retournée.

Le type de recherche par défaut est synchrone. Pour spécifier une recherche asynchrone, définissez une option de recherche **\_ \_ asynchrone SEARCHPREF ADS** avec la valeur **\_ booléenne ADSTYPE** **true** dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) transmis à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Cette opération est illustrée dans l’exemple de code suivant.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_ASYNCHRONOUS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




