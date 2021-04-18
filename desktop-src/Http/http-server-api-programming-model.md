---
title: Modèle de programmation
description: Le modèle de programmation de l’API du serveur HTTP comprend cinq groupes d’activités.
ms.assetid: 8485cbdc-803f-4c10-ae4c-9ca53965d747
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: def54ac8a34d6c53ea4e2825ef39884f0141df99
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/06/2021
ms.locfileid: "104563598"
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

 

 




