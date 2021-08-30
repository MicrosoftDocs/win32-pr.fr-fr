---
title: Récupération de plage d’attributs
description: Un attribut à valeurs multiples peut avoir presque n’importe quel nombre de valeurs. Dans de nombreux cas, il peut être avantageux, voire nécessaire, de limiter la plage de valeurs récupérées par une requête.
ms.assetid: 3a0eb764-fca9-4ca6-9991-b85f293961af
ms.tgt_platform: multiple
keywords:
- ADSI-récupération de plage d’attributs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc140a713feb141890478f830bbd24a95a4e7ef7
ms.sourcegitcommit: 3fbe7c00125bed49e333b44b2ed733079e4a1cac
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/16/2021
ms.locfileid: "122208165"
---
# <a name="attribute-range-retrieval"></a>Récupération de plage d’attributs

Un attribut à valeurs multiples peut avoir presque n’importe quel nombre de valeurs. Dans de nombreux cas, il peut être avantageux, voire nécessaire, de limiter la plage de valeurs récupérées par une requête.

La récupération de plage implique de demander un nombre limité de valeurs d’attribut dans une seule requête. Le nombre de valeurs demandé doit être inférieur ou égal au nombre maximal de valeurs prises en charge par le serveur. Pour réduire le nombre de fois que la requête doit contacter le serveur, le nombre de valeurs demandé doit être aussi proche que possible de cette valeur maximale. pour permettre à une application de fonctionner correctement avec tous les serveurs Windows, un nombre maximal de 1000 doit être utilisé.

Les spécificateurs de plage pour une requête de propriété requièrent la forme suivante :


```C++
range=<low range>-<high range>
```



où « &lt; Low Range &gt; » est l’index de base zéro de la première valeur de propriété à récupérer et « &lt; High range &gt; » est l’index de base zéro de la dernière valeur de propriété à récupérer. La valeur zéro est utilisée pour &lt; la « plage inférieure &gt; » pour spécifier la première entrée. Le caractère générique ( \* ) peut être utilisé pour la « &lt; plage supérieure &gt; » afin de spécifier toutes les entrées restantes.

Le tableau suivant répertorie des exemples de spécificateurs de plage.



| Exemple      | Description                                                                                   |
|--------------|-----------------------------------------------------------------------------------------------|
| plage = 0-\*   | Récupérez toutes les valeurs de propriété. Cela est soumis à des limites imposées par le serveur.                |
| plage = 0-500  | Récupérer des valeurs de 1er à 501st inclusivement.                                                |
| plage = 2-3    | Récupérez les 3e et 4e valeurs.                                                                  |
| plage = 501-\* | Récupérez le 502nd et toutes les valeurs restantes. Cela est soumis à des limites imposées par le serveur. |



 

Il existe plusieurs façons de récupérer une plage de valeurs de propriété. La méthode [**IADs. GetInfoEx**](/windows/desktop/api/Iads/nf-iads-iads-getinfoex) peut être utilisée dans un langage Automation ou C++. La méthode **IADs. GetInfoEx** est la méthode recommandée pour effectuer une récupération de plage. Pour plus d’informations sur l’utilisation de **IADs. GetInfoEx** pour la récupération de plages, consultez [utilisation de IADs :: GetInfoEx pour la récupération de plages](using-iads--getinfoex-for-range-retrieval.md).

si un langage automation est utilisé, les objets d’annuaire d’ActiveX (ADO) peuvent être utilisés pour récupérer une plage de valeurs de propriété. Pour plus d’informations sur l’utilisation d’ADO pour la récupération de plages, consultez [utilisation d’ADO pour la récupération de plages](using-ado-for-range-retrieval.md).

Si vous utilisez C++, les interfaces [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) et [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) peuvent être utilisées pour récupérer une plage de valeurs de propriété. Pour plus d’informations sur l’utilisation de **IDirectorySearch** et **IDirectoryObject** pour la récupération de plages, consultez [utilisation de IDirectorySearch et IDirectoryObject pour la récupération de plages](using-idirectorysearch-and-idirectoryobject-for-range-retrieval.md).  Ce type de récupération doit être effectué sur les requêtes avec un type d’étendue de base (ADS_SCOPE_BASE).

 

 




