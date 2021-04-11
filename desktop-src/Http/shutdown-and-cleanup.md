---
title: Arrêt et nettoyage
description: Pour qu’une application s’arrête normalement, elle doit effectuer les opérations de nettoyage suivantes.
ms.assetid: fc07adb8-103c-42d8-8187-3f5ee083c6d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf1c59534b73fee21489439c7818c286874185d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029315"
---
# <a name="shutdown-and-cleanup"></a>Arrêt et nettoyage

Pour qu’une application s’arrête normalement, elle doit effectuer les opérations de nettoyage suivantes :

-   Supprimez toutes les URL inscrites du groupe d’URL en appelant la fonction [**HttpRemoveUrlFromUrlGroup**](/windows/desktop/api/Http/nf-http-httpremoveurlfromurlgroup) pour annuler l’inscription des URL précédemment inscrites dans l’appel à [**HttpAddUrlToUrlGroup**](/windows/desktop/api/Http/nf-http-httpaddurltourlgroup).
-   Fermez le groupe d’URL en appelant la fonction [**HttpCloseUrlGroup**](/windows/desktop/api/Http/nf-http-httpcloseurlgroup) . Tous les groupes d’URL créés sous une session serveur doivent être fermés avant de fermer la session serveur.
-   Fermez la session serveur en appelant [**HttpCloseServerSession**](/windows/desktop/api/Http/nf-http-httpcloseserversession).
-   Fermez le descripteur de la file d’attente de demandes en appelant [**HttpCloseRequestQueue**](/windows/desktop/api/Http/nf-http-httpcloserequestqueue).
-   Arrêtez les ressources créées par l’API du serveur HTTP en appelant la fonction [**HttpTerminate**](/windows/desktop/api/Http/nf-http-httpterminate) avec les paramètres d’indicateur correspondants pour chaque appel de l’application initialement effectuée à [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize). Chacun de ces appels met fin à toutes les ressources créées dans l’appel à [**HttpInitialize**](/windows/desktop/api/Http/nf-http-httpinitialize).

 

 




