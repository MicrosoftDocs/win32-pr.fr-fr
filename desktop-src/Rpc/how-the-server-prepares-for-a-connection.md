---
title: Préparation d’une connexion par le serveur
description: Quand un programme serveur commence à s’exécuter, il doit d’abord inscrire l’interface ou les interfaces qu’il contient avec la bibliothèque Runtime RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66314c55ad8e78922f7afcc74c6de3b4afad8234293373cf0cd35a560a1942ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929490"
---
# <a name="how-the-server-prepares-for-a-connection"></a>Préparation d’une connexion par le serveur

Quand un programme serveur commence à s’exécuter, il doit d’abord inscrire l’interface ou les interfaces qu’il contient avec la bibliothèque Runtime RPC. Il crée ensuite les informations de liaison nécessaires. Le programme serveur doit également inscrire le ou les points de terminaison qu’il écoute. Il peut ensuite commencer à écouter les appels des clients. Ce processus est illustré dans le diagramme suivant.

![une application serveur RPC se prépare aux connexions clientes](images/srvrcon.png)

Selon la conception choisie, une application serveur peut choisir un autre ensemble d’étapes. l’exemple précédent et l’illustration ci-dessus fournissent une approche.

Cette section fournit des informations sur les étapes qu’un processus serveur doit effectuer pour préparer une connexion. La discussion comprend les sections suivantes :

-   [Inscription de l’interface](registering-the-interface.md)
-   [Mise à disposition du serveur sur le réseau](making-the-server-available-on-the-network.md)
-   [Inscription des points de terminaison](registering-endpoints.md)
-   [Écoute des appels clients](listening-for-client-calls.md)

 

 




