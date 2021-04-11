---
title: Limite de temps du serveur avec IDirectorySearch
description: Pour éviter d’utiliser tout le temps processeur et empêcher les autres opérations de s’exécuter, spécifiez la limite de durée de recherche sur une petite valeur, puis réexécutez l’application ultérieurement si elle ne parvient pas à générer le rapport.
ms.assetid: 0fd4d8a2-36fc-4179-aeee-1cd3f3996e19
ms.tgt_platform: multiple
keywords:
- Limite de temps du serveur avec l’interface ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, limite de temps du serveur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5f80f9b83f20affaf7ad03de6b1609e9951b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939576"
---
# <a name="server-time-limit-with-idirectorysearch"></a>Limite de temps du serveur avec IDirectorySearch

Lorsque vous demandez une recherche sur un serveur occupé, vous souhaiterez peut-être demander que le serveur limite la recherche à une limite de temps spécifiée. Par exemple, vous souhaitez exécuter une application pour générer un rapport hebdomadaire sur un serveur qui exécute près de sa capacité. Pour éviter d’utiliser tout le temps processeur et empêcher les autres opérations de s’exécuter, spécifiez la limite de durée de recherche sur une petite valeur, puis réexécutez l’application ultérieurement si elle ne parvient pas à générer le rapport.

Certains serveurs peuvent imposer leur propre limite de temps d’administration. Dans ce cas, si vous spécifiez une valeur de limite de temps de recherche supérieure à la limite de temps d’administration, le serveur ignore votre spécification et utilise sa valeur de limite de temps interne à la place.

La valeur par défaut de la limite de durée du serveur est illimitée. Pour définir une limite de temps de serveur, définissez une option de recherche de **\_ \_ \_ limite de temps SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** qui contient la limite de temps du serveur, en secondes, dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) . Cette opération est illustrée dans l’exemple de code suivant. Une limite de délai de serveur de zéro indique qu’il n’existe aucune limite de temps.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_TIME_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 10;
```



 

 




