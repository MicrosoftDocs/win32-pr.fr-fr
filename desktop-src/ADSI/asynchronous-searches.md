---
title: Recherches asynchrones
description: L’activation de la recherche asynchrone (asynchrone) entraîne un appel à GetFirstRow ou le premier appel à la valeur de la ligne, jusqu’à ce que la première entrée soit retournée à partir du serveur.
ms.assetid: f80e2c62-71c5-4a05-bd17-465962be3c2d
ms.tgt_platform: multiple
keywords:
- Recherches asynchrones ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bca36a30b3b0a46f983da54ecaee753a4b15a455b0e69f9399eacdec68aecd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082783"
---
# <a name="asynchronous-searches"></a>Recherches asynchrones

L’activation de la recherche asynchrone (asynchrone) entraîne un appel à **GetFirstRow** ou le premier **appel à la valeur de la** ligne, jusqu’à ce que la première entrée soit retournée à partir du serveur. Autrement dit, si la recherche sur le serveur nécessite plus de temps, les premiers résultats sont retournés rapidement. Cela peut être utile lors du remplissage d’une zone de liste avec les résultats de la recherche. Les résultats de la recherche s’affichent tels qu’ils sont retournés.

Si Async est désactivé, le premier appel à **GetFirstRow** ou **GetNextRow** se bloque jusqu’à ce que le serveur calcule le jeu de résultats entier et retourne. Seule la première ligne est retournée. Cela n’est pas recommandé si le jeu de résultats est supposé être volumineux.

Si la pagination et Async sont activés, le premier appel à **GetFirstRow** ou **GetNextRow** est bloqué jusqu’à ce que le serveur génère et envoie la première page de résultats. Si une taille de page raisonnable a été définie, les résultats s’affichent immédiatement. Plus important encore, si les résultats de recherche sont censés être très volumineux et que vous recherchez une entrée particulière, il n’est pas nécessaire de demander plus de résultats à partir du serveur une fois que vous avez trouvé les entrées qui vous intéressent.

Une recherche asynchrone paginée permet un contrôle précis d’une recherche. Cela est utile si les résultats de la recherche peuvent être très volumineux et nécessitent un temps considérable du serveur.

Pour plus d’informations sur l’utilisation des recherches asynchrones avec une interface de recherche spécifique, consultez :

-   [Recherches synchrones et asynchrones avec IDirectorySearch](synchronous-and-asynchronous-searches-with-idirectorysearch.md)
-   [recherche avec ActiveX Data Objects](searching-with-activex-data-objects-ado.md)
-   [Recherche avec OLE DB](searching-with-ole-db.md)

 

 




