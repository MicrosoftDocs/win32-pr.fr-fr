---
title: Limite de taille avec IDirectorySearch
description: Le client peut se concentrer sur un petit nombre d’objets renvoyés par le serveur et ignorer le reste du jeu de résultats.
ms.assetid: 55393177-f49b-4163-8e33-2ec24a64b99a
ms.tgt_platform: multiple
keywords:
- Limite de taille avec l’ADSI IDirectorySearch
- ADSI, recherche, IDirectorySearch, autres options de recherche, limite de taille
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25127ea945edcf669e71d7d5b3f969d9eb2cb112
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512018"
---
# <a name="size-limit-with-idirectorysearch"></a>Limite de taille avec IDirectorySearch

Pour réduire les besoins en mémoire ou à d’autres fins, le client peut se concentrer sur un petit nombre d’objets retournés par le serveur et ignorer le reste du jeu de résultats qui ne sont pas intéressants. Pour ce faire, le client spécifie la limite de taille de recherche et d’autres critères de recherche appropriés. Par exemple, si l’annuaire stocke les scores de test d’une circonscription scolaire, vous pouvez interroger les dix meilleurs étudiants avec les meilleurs scores de test en spécifiant une limite de taille de dix (10) et un ordre de tri décroissant.

La valeur par défaut de la limite de taille est illimitée. Pour définir une limite de taille, définissez une option de recherche de **\_ limite de \_ taille \_ de SEARCHPREF ADS** avec une valeur **\_ entière ADSTYPE** qui contient la taille maximale dans le tableau d' [**\_ \_ informations SEARCHPREF ADS**](/windows/desktop/api/Iads/ns-iads-ads_searchpref_info) passé à la méthode [**IDirectorySearch :: SetSearchPreference**](/windows/desktop/api/Iads/nf-iads-idirectorysearch-setsearchpreference) .

L’exemple de code suivant montre comment définir la limite de taille. Une valeur de limite de taille de zéro indique aucune limite de taille.


```C++
ADS_SEARCHPREF_INFO SearchPref;
SearchPref.dwSearchPref = ADS_SEARCHPREF_SIZE_LIMIT;
SearchPref.vValue.dwType = ADSTYPE_INTEGER;
SearchPref.vValue.Integer = 1000;
```



Par Active Directory, la limite de taille spécifie le nombre maximal d’objets qui doivent être retournés par la recherche. Par ailleurs, pour Active Directory, le nombre maximal d’objets renvoyés par une recherche est de 1000 objets.

 

 




