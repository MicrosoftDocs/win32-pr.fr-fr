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
ms.openlocfilehash: e120586cb05fa07baf1e26fa8c1db8e11eecdbd1b19ed7f4f9c2215a921409ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119262129"
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



 

 




