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
# <a name="creating-a-where-clause-for-the-registry-provider"></a><span data-ttu-id="92ae9-104">Création d’une clause WHERE pour le fournisseur Registry</span><span class="sxs-lookup"><span data-stu-id="92ae9-104">Creating a WHERE clause for the registry provider</span></span>

<span data-ttu-id="92ae9-105">Les points principaux à prendre en compte lors de la création d’une clause WHERE correcte pour le fournisseur de Registre système sont que chaque requête d’événement doit être complète et explicite.</span><span class="sxs-lookup"><span data-stu-id="92ae9-105">The main points to consider when creating a proper WHERE clause for the System Registry provider is that each event query must be complete and explicit.</span></span> <span data-ttu-id="92ae9-106">Le fait de ne pas être terminé et explicite entraîne un message d’erreur.</span><span class="sxs-lookup"><span data-stu-id="92ae9-106">Failure to be complete and explicit will result in an error message.</span></span>

<span data-ttu-id="92ae9-107">Pour être terminé, chaque requête d’événement dans le paramètre *bstrQuery* de [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) doit contenir une clause WHERE incluant chacune des propriétés de la classe d’événements spécifiée.</span><span class="sxs-lookup"><span data-stu-id="92ae9-107">To be complete, each event query in the *bstrQuery* parameter of [**ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) must contain a WHERE clause that includes each of the properties in the specified event class.</span></span>

<span data-ttu-id="92ae9-108">L’exemple suivant montre comment définir *bstrQuery* pour l’enregistrement des événements de modification d’arborescence dans l' \_ arborescence « HKEY local \_ machine \\ Software ».</span><span class="sxs-lookup"><span data-stu-id="92ae9-108">The following example shows how to set *bstrQuery* to register for tree change events in the "HKEY\_LOCAL\_MACHINE\\Software" tree.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE Hive = "HKEY_LOCAL_MACHINE" AND Rootpath = "Software"
```



<span data-ttu-id="92ae9-109">Pour être explicite, le fournisseur doit être en mesure de déduire de la requête une liste de valeurs possibles pour chaque propriété de la classe d’événements.</span><span class="sxs-lookup"><span data-stu-id="92ae9-109">To be explicit, the provider should be able to infer from the query a list of possible values for every property in the event class.</span></span>

<span data-ttu-id="92ae9-110">L’exemple suivant montre la requête d’événement qui s’inscrit correctement pour les événements de modification d’arborescence.</span><span class="sxs-lookup"><span data-stu-id="92ae9-110">The following example shows the event query that correctly registers for tree change events.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent 
    WHERE (hive = "hkey_local_machine" AND rootpath = "software") 
    OR    (hive = "hkey_current_user" AND rootpath = "console")
```



<span data-ttu-id="92ae9-111">Voici un exemple d’inscription incorrecte.</span><span class="sxs-lookup"><span data-stu-id="92ae9-111">The following is an example of an incorrect registration.</span></span>


```sql
SELECT * FROM RegistryTreeChangeEvent  WHERE hive = "hkey_local_machine" OR rootpath ="software"
```



<span data-ttu-id="92ae9-112">Étant donné qu’il n’existe aucun moyen d’évaluer les valeurs possibles pour chacune des propriétés, WMI rejette avec l’erreur WBEM \_ E \_ trop \_ large toute requête qui n’a pas de clause WHERE ou si la clause WHERE est trop étendue pour être utilisée.</span><span class="sxs-lookup"><span data-stu-id="92ae9-112">Because there is no way to evaluate the possible values for each of the properties, WMI rejects with the error WBEM\_E\_TOO\_BROAD any query that either does not have a WHERE clause or if the WHERE clause is too broad to be of any use.</span></span>

 

 



