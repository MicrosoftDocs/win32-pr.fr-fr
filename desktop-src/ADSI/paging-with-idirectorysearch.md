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
ms.openlocfilehash: 48494c01831e6b69931fc6b6f779ed9b042b7fecaaf17fa62286c094a926ba73
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117838939"
---
# <a name="paging-with-idirectorysearch"></a>Pagination avec IDirectorySearch

La pagination spécifie le nombre de lignes que le serveur retourne au client. Une page peut être définie par le nombre de lignes ou une limite de temps. L’objet COM ADSI récupère chaque page de résultats en fonction des valeurs indiquées dans le tableau suivant. L’appelant appelle [**IDirectorySearch :: GetNextRow**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-getnextrow) lorsqu’il a atteint la fin de la page et l’objet com ADSI récupère la page suivante.



| Valeur                                   | Description                                                                                                                                                                                                                                          |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_pages de SEARCHPREF ADS \_**           | Spécifie le nombre maximal de lignes à retourner dans une page.                                                                                                                                                                                            |
| **\_limite de \_ temps paginée SEARCHPREF \_ ADS \_** | Spécifie la durée maximale, en secondes, pendant laquelle le serveur doit collecter une page de résultats avant de renvoyer la page au client. Si la limite est atteinte, le serveur arrête la recherche et retourne les lignes déjà récupérées pour la page. |



 

Si aucune de ces préférences de recherche n’est définie, la valeur par défaut est aucune pagination. Les recherches des Active Directory effectuées sans pagination sont limitées au fait de retourner un maximum de 1000 premiers enregistrements. vous devez donc utiliser une recherche paginée s’il est possible que le jeu de résultats contienne plus de 1000 éléments.

Une opération de recherche peut entraîner le renvoi d’un grand nombre d’objets. Si le serveur retourne le résultat dans un jeu, il peut réduire les performances du client et du serveur, ainsi que affecter la charge réseau. Les recherches paginées peuvent être utilisées pour éviter cela. Dans une recherche paginée, le client peut accepter les résultats dans des paquets plus petits. La taille d’un paquet est connue sous le nom de taille de page de recherche.

Les recherches paginées offrent des avantages au client et au serveur. Le client peut être plus réactif pour présenter les résultats aux utilisateurs. Cela s’applique particulièrement aux outils d’interface utilisateur graphique qui peuvent démarrer le processus d’affichage de la fenêtre pendant que l’autre thread reçoit simultanément les données.

Côté serveur, les recherches paginées rendent l’opération évolutive. Par exemple, si les clients 100 émettent des demandes de recherche simultanément et, en moyenne, chaque client reçoit 200 objets. Si aucune taille de page n’est spécifiée, dans le pire des cas, le serveur doit disposer de suffisamment de mémoire pour contenir 20 000 objets. À l’inverse, si chaque client spécifie une taille de page, par exemple, dix objets, la mémoire requise sur le serveur est donc réduite d’un facteur de 20.

En outre, à l’aide d’une recherche paginée, un client peut abandonner l’opération en cours. En revanche, dans une recherche non paginée, le client reçoit un jeu de résultats dans un paquet. Cela peut réduire les performances du réseau.

ADSI gère la taille de page du client. Le client n’a pas besoin de compter le nombre d’objets en cours. ADSI encapsule l’interaction du serveur pour le client. Du point de vue du client, la recherche retourne un jeu de résultats complet.

Il est recommandé d’utiliser la pagination.

Pour spécifier une taille de page maximale, définissez une option de recherche **\_ SEARCHPREF \_ pages ADS** avec une valeur **\_ entière ADSTYPE** définie sur le nombre maximal de lignes par page dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

L’exemple de code suivant montre comment définir la taille de page maximale.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGESIZE;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Pour spécifier une heure de page, définissez une option de recherche de **\_ \_ \_ \_ limite de temps paginée de SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** définie sur le nombre maximal de secondes que le serveur doit consacrer à la récupération d’une page dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

L’exemple de code suivant montre comment spécifier le temps de la page.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_PAGED_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 60;
```



 

 




