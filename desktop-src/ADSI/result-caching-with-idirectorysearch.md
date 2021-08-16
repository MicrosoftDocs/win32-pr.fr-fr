---
title: Mise en cache des résultats avec IDirectorySearch
description: La \_ préférence des résultats du cache SEARCHPREF ADS \_ \_ met en cache le jeu de résultats sur le client.
ms.assetid: bb286879-7d84-4085-88e1-600c848b8af8
ms.tgt_platform: multiple
keywords:
- Mise en cache des résultats avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, mise en cache des résultats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4febc2f02e03759861978e062ee972d8e90df27b996c8161d6163e764fefe9a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838855"
---
# <a name="result-caching-with-idirectorysearch"></a>Mise en cache des résultats avec IDirectorySearch

La préférence des **\_ \_ \_ résultats du cache SEARCHPREF ADS** met en cache le jeu de résultats sur le client. La mise en cache des résultats permet à une application de conserver un jeu de résultats récupéré et de repasser les lignes récupérées. Il permet également la prise en charge des curseurs là où les méthodes [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) et [**IDirectorySearch :: GetPreviousRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getpreviousrow) peuvent être utilisées pour monter et descendre dans le jeu de résultats.

Par défaut, la mise en cache des résultats est désactivée. La mise en cache des résultats doit être activée si l’une des conditions suivantes est vraie :

-   Si le même jeu de résultats doit être énuméré plusieurs fois sans effectuer à nouveau la recherche sur le serveur.
-   Si l’exécution de la recherche est gourmande en ressources sur le serveur (connexion lente, jeu de résultats volumineux ou requête complexe).
-   Si la prise en charge du curseur est requise.

Désactivez la mise en cache si votre application doit réduire les besoins en mémoire pour la mise en cache d’un jeu de résultats volumineux sur le client.

La mise en cache des résultats augmente les besoins en mémoire sur le client, donc la mise en cache des résultats doit être désactivée si cela pose problème.

Pour activer la mise en cache des résultats, définissez une option de recherche de **\_ \_ \_ cache SEARCHPREF ADS** avec la valeur **\_ booléenne ADSTYPE** **true** dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) transmis à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

L’exemple de code suivant montre comment activer la mise en cache des résultats.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_CACHE_RESULTS;
SearchPref.vValue.dwType = ADSTYPE_BOOLEAN;
SearchPref.vValue.Boolean = TRUE;
```



 

 




