---
title: RPC asynchrone
description: L’appel de procédure distante (RPC) asynchrone est une extension Microsoft qui répond à plusieurs limitations du modèle RPC traditionnel, tel que défini par l’Open Software Foundation \ 8211 ; Distributed Computing Environment (OSF-DCE).
ms.assetid: 2586c10e-8284-419f-a200-4f6b11953688
keywords:
- Appel de procédure distante RPC, décrit, RPC asynchrone
- RPC asynchrone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36ac79a30fd01aeba1efb3cbd2b7cc741f26238
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127123502"
---
# <a name="asynchronous-rpc"></a>RPC asynchrone

L’appel de procédure distante (RPC) asynchrone est une extension Microsoft qui répond à plusieurs limitations du modèle RPC traditionnel, tel que défini par l’environnement OSF-DCE (Open Software Foundation). RPC asynchrone sépare un appel de procédure distante de sa valeur de retour, ce qui résout les limitations suivantes du RPC synchrone traditionnel :

-   **Plusieurs appels en attente à partir d’un client monothread.** Dans le modèle RPC traditionnel, un client est bloqué dans un appel de procédure distante jusqu’à ce que l’appel retourne. Cela empêche un client d’avoir plusieurs appels en attente, tout en gardant son thread disponible pour effectuer d’autres tâches.
-   **Clients lents ou retardés.** Un client qui est lent à produire des données peut souhaiter effectuer un appel de procédure distante avec les données initiales, puis fournir des données supplémentaires au fur et à mesure de leur production. Cela n’est pas possible avec RPC (synchrone) conventionnel.
-   **Serveurs lents ou retardés.** Un appel de procédure distante qui prend beaucoup de temps pour s’exécuter va lier le thread de dispatch pour la durée de la tâche. Avec RPC asynchrone, le serveur peut démarrer une opération distincte (asynchrone) pour traiter la demande et renvoyer la réponse lorsqu’elle est disponible. Le serveur peut également envoyer la réponse de manière incrémentielle lorsque les résultats deviennent disponibles sans avoir à lier un thread de dispatch pour la durée de l’appel distant. En rendant l’application cliente asynchrone, vous pouvez empêcher un serveur lent d’endiguer inutilement une application cliente.
-   **Transfert de grandes quantités de données.** Le transfert de grandes quantités de données entre le client et le serveur, en particulier sur des liaisons lentes, associe le thread client et le thread du gestionnaire de serveur pour la durée du transfert. Avec les canaux et RPC asynchrones, le transfert de données peut avoir lieu de façon incrémentielle et sans empêcher le client ou le serveur d’effectuer d’autres tâches.

Vous tirez parti des mécanismes RPC asynchrones en déclarant des fonctions avec l' \[ [](/windows/desktop/Midl/async) \] attribut Async. Étant donné que vous faites cette déclaration dans un fichier de configuration d’attribut (ACF), vous n’avez pas besoin d’apporter des modifications au fichier IDL (Interface Definition Language); RPC asynchrone n’a aucun effet sur le protocole Wire (mode de transmission des données entre le client et le serveur). Cela signifie que les clients synchrones et asynchrones peuvent communiquer avec une application serveur asynchrone.

Cette section présente une vue d’ensemble de la façon de développer des applications distribuées à l’aide de RPC asynchrone. La vue d’ensemble est présentée dans les sections suivantes :

-   [Déclaration de fonctions asynchrones](declaring-asynchronous-functions.md)
-   [RPC asynchrone côté client](client-side-asynchronous-rpc.md)
-   [RPC asynchrone côté serveur](server-side-asynchronous-rpc.md)
-   [Ordre de causalité des appels asynchrones](causal-ordering-of-asynchronous-calls.md)
-   [Gestion des erreurs](error-handling.md)
-   [RPC asynchrone sur le protocole de canal nommé](asynchronous-rpc-over-the-named-pipe-protocol.md)
-   [Utilisation de RPC asynchrone avec les canaux DCE](using-asynchronous-rpc-with-dce-pipes.md)
-   [DCOM asynchrone](asynchronous-dcom.md)

 

 