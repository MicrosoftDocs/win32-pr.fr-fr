---
title: Comment un service compose ses SPN
description: Un service peut utiliser deux fonctions pour composer ses SPN DsGetSpn est une fonction à usage général pour composer des SPN et DsServerRegisterSpn est une fonction spécialisée pour composer et inscrire des SPN simples pour un service basé sur l’hôte.
ms.assetid: 8710409a-67b1-45e5-9cd7-5125443ab921
ms.tgt_platform: multiple
keywords:
- nom de principal du service AD, comment un service est composé
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35fb659eec3bb2d0f50fd109b39f356df1429535
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881394"
---
# <a name="how-a-service-composes-its-spns"></a>Comment un service compose ses SPN

Un service peut utiliser deux fonctions pour composer ses SPN : [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) est une fonction à usage général pour composer des SPN et [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) est une fonction spécialisée pour composer et inscrire des SPN simples pour un service basé sur l’hôte.

Un programme d’installation de service utilise généralement la fonction [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) pour composer des SPN, qu’il enregistre ensuite sur le compte d’ouverture de session du service à l’aide de la fonction [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna) . Le **DsGetSpn** peut exécuter les fonctions suivantes.

-   Créez un SPN simple avec le <service class> / &lt; format « hôte &gt; » pour un service basé sur l’hôte.
-   Créez un nom de principal du service (SPN) complexe qui comprend le &lt; composant « nom du service &gt; » utilisé par les services réplicables ou le &lt; composant « port &gt; » qui distingue plusieurs instances d’un service sur un seul hôte.
-   Créez un SPN unique avec le &lt; composant « hôte &gt; » défini sur le nom d’un ordinateur hôte spécifié ou sur le nom de l’ordinateur local par défaut.
-   Créez un tableau de noms de principal du service pour plusieurs instances de service qui s’exécuteront sur plusieurs hôtes dans l’ensemble de la forêt. Chaque SPN spécifie le nom de l’hôte pour une instance de service.
-   Créez un tableau de noms de principal du service pour plusieurs instances de service qui s’exécuteront sur le même hôte. Chaque SPN spécifie le nom de l’hôte et un numéro de port pour une instance de service.

Le tableau des noms retournés par [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna) doit être libéré en appelant la fonction [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya) .

N’oubliez pas que les fonctions [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna), [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)et [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna) ne vérifient pas que les noms principaux de service sont uniques. Étant donné que l’authentification mutuelle échoue si un client présente un nom de principal du service qui n’est pas unique, vérifiez l’unicité avant d’inscrire un SPN. Pour ce faire, recherchez dans le catalogue global (GC) les attributs **servicePrincipalName** qui correspondent à votre SPN. Pour plus d’informations sur la recherche dans le GC, consultez [recherche dans le catalogue global](searching-global-catalog-contents.md).

 

 




