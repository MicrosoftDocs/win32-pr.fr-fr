---
title: Recherches asynchrones
description: L’activation de la recherche asynchrone (asynchrone) entraîne un appel à GetFirstRow ou le premier appel à la valeur de la ligne, jusqu’à ce que la première entrée soit retournée à partir du serveur.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Recherches asynchrones ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe8b8fff875af18b85cdffa4ce67d631d94ed14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939608"
---
# <a name="asynchronous-searches"></a>Recherches asynchrones

L’activation de la recherche asynchrone (asynchrone) entraîne un appel à **GetFirstRow** ou le premier **appel à la valeur de la** ligne, jusqu’à ce que la première entrée soit retournée à partir du serveur. Autrement dit, si la recherche sur le serveur nécessite plus de temps, les premiers résultats sont retournés rapidement. Cela peut être utile lors du remplissage d’une zone de liste avec les résultats de la recherche. Les résultats de la recherche s’affichent tels qu’ils sont retournés.

Si Async est désactivé, le premier appel à **GetFirstRow** ou **GetNextRow** se bloque jusqu’à ce que le serveur calcule le jeu de résultats entier et retourne. Seule la première ligne est retournée. Cela n’est pas recommandé si le jeu de résultats est supposé être volumineux.

Si la pagination et Async sont activés, le premier appel à **GetFirstRow** ou **GetNextRow** est bloqué jusqu’à ce que le serveur génère et envoie la première page de résultats. Si une taille de page raisonnable a été définie, les résultats s’affichent immédiatement. Plus important encore, si les résultats de recherche sont censés être très volumineux et que vous recherchez une entrée particulière, il n’est pas nécessaire de demander plus de résultats à partir du serveur une fois que vous avez trouvé les entrées qui vous intéressent.

Une recherche asynchrone paginée permet un contrôle précis d’une recherche. Cela est utile si les résultats de la recherche peuvent être très volumineux et nécessitent un temps considérable du serveur.

Pour plus d’informations sur l’utilisation des recherches asynchrones avec une interface de recherche spécifique, consultez :

-   [Recherches synchrones et asynchrones avec IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [Recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




