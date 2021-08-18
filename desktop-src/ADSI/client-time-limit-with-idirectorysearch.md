---
title: Limite de temps du client avec IDirectorySearch
description: Un client peut imposer une limite de temps pour qu’un serveur retourne le jeu de résultats. Lorsque le serveur ne parvient pas à répondre à une requête dans le délai spécifié, le client peut abandonner la recherche et essayer à nouveau ultérieurement.
ms.assetid: fe8a8b08-b34d-4aa5-a925-bcda6e72d437
ms.tgt_platform: multiple
keywords:
- Limite de temps du client avec IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, limite de temps du client
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1798094a980c41de2e1902533415839020cfd690384f0e56a37bff918d4ecc2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118692508"
---
# <a name="client-time-limit-with-idirectorysearch"></a>Limite de temps du client avec IDirectorySearch

Un client peut imposer une limite de temps pour qu’un serveur retourne le jeu de résultats. Lorsque le serveur ne parvient pas à répondre à une requête dans le délai spécifié, le client peut abandonner la recherche et essayer à nouveau ultérieurement.

La préférence de limite de temps client est utile lorsqu’un client demande une recherche asynchrone. Dans une recherche asynchrone, le client effectue une demande, puis poursuit avec d’autres tâches en attendant que le serveur retourne les résultats. Il est possible que le serveur puisse passer en mode hors connexion sans en avertir le client. Dans ce cas, le client n’aura aucune notification indiquant si le serveur est toujours en cours de traitement de la requête ou s’il n’est plus en ligne. La préférence de limite de temps du client donne au client un contrôle de situations comme celle-ci.

La valeur par défaut de la limite de durée du client est illimitée. Pour définir une limite de temps client, définissez une option de recherche de **\_ \_ délai d’attente SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** qui contient la limite de temps du client, en secondes, dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Une limite de temps du client de zéro n’indique aucune limite de durée.

L’exemple de code suivant montre comment définir la limite de temps du client.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIMEOUT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




