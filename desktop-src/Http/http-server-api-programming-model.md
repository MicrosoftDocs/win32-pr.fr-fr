---
title: Modèle de programmation
description: Le modèle de programmation de l’API du serveur HTTP comprend cinq groupes d’activités.
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30fe49dd9a50af72fc89efa6c10c56176966fda949fa177b3f081761a0d2a568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014730"
---
# <a name="programming-model"></a>Modèle de programmation

Le modèle de programmation de l’API du serveur HTTP comprend cinq groupes d’activités :

-   [Configuration](setup-configuration.md)
-   [Configuration de l’exécution](run-time-configuration.md)
-   [Création et liaison à une file d’attente de demandes](creating-and-binding-to-a-request-queue.md)
-   [Traitement des requêtes](processing-requests.md)
-   [Arrêt et nettoyage](shutdown-and-cleanup.md)

![Diagramme qui montre le modèle de programmation P I t P du serveur H T.](images/http-server-api-programming-model.png)

Pour obtenir un exemple d’application qui montre comment gérer les actions HTTP d’obtention et de demande ultérieure et comment envoyer une erreur 503 (**non \_ implémentée**) si des actions sont présentes dans la demande que l’application ne gère pas, consultez [exemple d’application serveur http](http-server-sample-application.md).

 

 




