---
title: Création d’une clause WHERE pour le fournisseur Registry
description: Les points principaux à prendre en compte lors de la création d’une clause WHERE correcte pour le fournisseur de Registre système sont que chaque requête d’événement doit être complète et explicite. Le fait de ne pas être terminé et explicite entraîne un message d’erreur.
ms.assetid: cdef2900-8d1a-4f0b-8318-7463d90e4152
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d1c7031d376fbd6b9d946fb9e41561ce4c4b1c7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485737"
---
# <a name="creating-a-where-clause-for-the-registry-provider"></a>Création d’une clause WHERE pour le fournisseur Registry

Les points principaux à prendre en compte lors de la création d’une clause WHERE correcte pour le fournisseur de Registre système sont que chaque requête d’événement doit être complète et explicite. Le fait de ne pas être terminé et explicite entraîne un message d’erreur.

Pour être terminé, chaque requête d’événement dans le paramètre *bstrQuery* de [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) doit contenir une clause WHERE incluant chacune des propriétés de la classe d’événements spécifiée.

L’exemple suivant montre comment définir *bstrQuery* pour l’enregistrement des événements de modification d’arborescence dans l' \_ arborescence « HKEY local \_ machine \\ Software ».


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



Pour être explicite, le fournisseur doit être en mesure de déduire de la requête une liste de valeurs possibles pour chaque propriété de la classe d’événements.

L’exemple suivant montre la requête d’événement qui s’inscrit correctement pour les événements de modification d’arborescence.


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



Voici un exemple d’inscription incorrecte.


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



Étant donné qu’il n’existe aucun moyen d’évaluer les valeurs possibles pour chacune des propriétés, WMI rejette avec l’erreur WBEM \_ E \_ trop \_ large toute requête qui n’a pas de clause WHERE ou si la clause WHERE est trop étendue pour être utilisée.

 

 



