---
title: Configuration de Run-Time
description: L’API HTTP permet aux applications d’effectuer une configuration dynamique au moment de l’exécution.
ms.assetid: 5118b48b-b44c-4cf5-9754-ce23c5a0b87e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b240438ada7fce186f334df3175b8ecc5b557626c5f1f085cdf82965fb32365
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393751"
---
# <a name="run-time-configuration"></a>Configuration de Run-Time

L’API HTTP permet aux applications d’effectuer une configuration dynamique au moment de l’exécution. La configuration au moment de l’exécution n’est pas persistante, nécessite uniquement des privilèges de bas niveau et affecte uniquement votre application. La configuration au moment de l’exécution peut inclure l’une des activités suivantes :

-   Initialisation du service HTTP et création d’une session serveur. Une application initialise le service HTTP en appelant la fonction [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize) . Le serveur doit être initialisé avant de pouvoir appeler d’autres fonctions serveur. L’application crée ensuite une session serveur en appelant la fonction [**HttpCreateServerSession**](/windows/desktop/api/Http/nf-http-httpcreateserversession) . La session serveur est un conteneur pour les propriétés qui s’appliquent à tous les groupes d’URL appartenant à cette session serveur. En général, chaque allication n’a qu’une seule session de serveur. Pour plus d’informations sur la définition des propriétés de session serveur et sur leur étendue, consultez [**HttpSetServerSessionProperty**](/windows/desktop/api/Http/nf-http-httpsetserversessionproperty).
-   Inscription pour les URL. Une fois la session serveur créée, une application peut s’inscrire pour les URL en créant un ou plusieurs groupes d’URL. Un groupe d’URL est un groupe d’URL auquel les mêmes propriétés sont appliquées. Une application crée un groupe d’URL en appelant la fonction [**HttpCreateUrlGroup**](/windows/desktop/api/Http/nf-http-httpcreateurlgroup) , puis ajoute les URL souhaitées en appelant la fonction [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup) . Une fois qu’une application est inscrite pour les URL en créant un groupe d’URL et qu’elle a associé le groupe d’URL à une file d’attente de demandes (voir [création et liaison à une file d’attente de](creating-and-binding-to-a-request-queue.md)demandes), toutes les demandes provenant de ces URL sont routées vers la file d’attente de demandes associée à cette application. Pour plus d’informations sur les propriétés de groupe d’URL définition, consultez [ **HttpSetUrlGroupProperty**](/windows/desktop/api/Http/nf-http-httpseturlgroupproperty)
-   Activation des fonctionnalités en définissant les propriétés du serveur HTTP, telles que [l’authentification](authentication-in-http-version-2-0.md), la [journalisation](server-side-logging-in-http-version-2-0.md), les paramètres de QoS, les délais d’attente, l’état activé et les informations de liaison. Pour plus d’informations sur la définition des propriétés, consultez [**\_ \_ propriété du serveur http**](/windows/desktop/api/Http/ne-http-http_server_property).

 

 




