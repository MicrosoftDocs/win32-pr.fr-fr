---
title: Préparation d’une connexion par le serveur
description: Quand un programme serveur commence à s’exécuter, il doit d’abord inscrire l’interface ou les interfaces qu’il contient avec la bibliothèque Runtime RPC.
ms.assetid: 3e78e095-f4a4-4ce7-b4a9-936a6c10316b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9787cc0f4a10da99f1401843450a6e00073e135b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310353"
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

 

 




