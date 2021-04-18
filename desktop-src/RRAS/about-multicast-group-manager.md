---
title: À propos du gestionnaire de groupe de multidiffusion
description: Cette documentation décrit la technologie du gestionnaire de groupe de multidiffusion (MGM).
ms.assetid: 55216742-d67c-4a17-aaf9-0b087938061e
keywords:
- Gestionnaire de groupe de multidiffusion RRAS
- Gestionnaire de groupe de multidiffusion RRAS, Description
- Routage et accès à distance service RRAS, gestionnaire de groupe de multidiffusion
- Routage et accès à distance service RRAS, gestionnaire de groupe de multidiffusion, décrit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 034d37b99aaa9ca0139b5425cd5b85e7b3f280e9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106512668"
---
# <a name="about-multicast-group-manager"></a>À propos du gestionnaire de groupe de multidiffusion

Cette documentation décrit la technologie du gestionnaire de groupe de multidiffusion (MGM).

La multidiffusion permet à un hôte d’envoyer des données uniquement aux destinations qui demandent spécifiquement de recevoir les données. De cette façon, la multidiffusion diffère de l’envoi des données de diffusion, car les données de diffusion sont envoyées à tous les ordinateurs hôtes.

La multidiffusion économise la bande passante réseau, car les données de multidiffusion ne sont reçues que par les hôtes qui demandent les données, et les données transitent sur n’importe quel lien une seule fois. La multidiffusion économise la bande passante du serveur, car un serveur ne doit envoyer qu’un seul message de multidiffusion par réseau au lieu d’un message de monodiffusion par récepteur. Les réunions en ligne et la radio Internet sont des exemples d’applications de multidiffusion populaires.

L’API MGM permet aux développeurs d’écrire des protocoles de routage multidiffusion qui interagissent avec les routeurs exécutant le gestionnaire de groupe de multidiffusion.

Lorsque plusieurs protocoles de routage multidiffusion sont activés sur un routeur, le gestionnaire de groupe de multidiffusion coordonne les opérations entre tous les protocoles de routage. Le gestionnaire de groupe de multidiffusion informe chaque protocole de routage lorsque des modifications d’appartenance au groupe se produisent, et lorsque des données de multidiffusion provenant d’une nouvelle source ou qui sont destinées à un nouveau groupe sont reçues.

L’API MGM offre les fonctionnalités suivantes :

-   Inscription de protocole
-   Gestion des groupes
-   Énumération de l’entrée de transfert multidiffusion (MFE)
-   Définitions de rappel pour les protocoles de routage de multidiffusion

Cette vue d’ensemble décrit les composants de l’architecture de multidiffusion, les scénarios clients utilisés pour interagir avec le gestionnaire de groupe de multidiffusion, ainsi que les considérations en matière de programmation pour l’utilisation de l’API MGM.

 

 




