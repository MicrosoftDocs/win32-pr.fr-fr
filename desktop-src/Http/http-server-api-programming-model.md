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
# <a name="programming-model"></a><span data-ttu-id="712fa-103">Modèle de programmation</span><span class="sxs-lookup"><span data-stu-id="712fa-103">Programming Model</span></span>

<span data-ttu-id="712fa-104">Le modèle de programmation de l’API du serveur HTTP comprend cinq groupes d’activités :</span><span class="sxs-lookup"><span data-stu-id="712fa-104">The HTTP Server API programming model includes five groups of activities:</span></span>

-   [<span data-ttu-id="712fa-105">Configuration</span><span class="sxs-lookup"><span data-stu-id="712fa-105">Setup configuration</span></span>](setup-configuration.md)
-   [<span data-ttu-id="712fa-106">Configuration de l’exécution</span><span class="sxs-lookup"><span data-stu-id="712fa-106">Run-time configuration</span></span>](run-time-configuration.md)
-   [<span data-ttu-id="712fa-107">Création et liaison à une file d’attente de demandes</span><span class="sxs-lookup"><span data-stu-id="712fa-107">Creating and binding to a request queue</span></span>](creating-and-binding-to-a-request-queue.md)
-   [<span data-ttu-id="712fa-108">Traitement des requêtes</span><span class="sxs-lookup"><span data-stu-id="712fa-108">Processing requests</span></span>](processing-requests.md)
-   [<span data-ttu-id="712fa-109">Arrêt et nettoyage</span><span class="sxs-lookup"><span data-stu-id="712fa-109">Shutdown and cleanup</span></span>](shutdown-and-cleanup.md)

![Diagramme qui montre le modèle de programmation P I t P du serveur H T.](images/http-server-api-programming-model.png)

<span data-ttu-id="712fa-111">Pour obtenir un exemple d’application qui montre comment gérer les actions HTTP d’obtention et de demande ultérieure et comment envoyer une erreur 503 (**non \_ implémentée**) si des actions sont présentes dans la demande que l’application ne gère pas, consultez [exemple d’application serveur http](http-server-sample-application.md).</span><span class="sxs-lookup"><span data-stu-id="712fa-111">For a sample application that shows how to handle the HTTP GET and POST request actions and how to send a 503 (**NOT\_IMPLEMENTED**) error if actions are present in the request that the application does not handle, see [HTTP Server Sample Application](http-server-sample-application.md).</span></span>

 

 




