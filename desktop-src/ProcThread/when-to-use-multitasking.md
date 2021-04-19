---
description: 'Il existe deux façons d’implémenter le multitâche : en tant que processus unique avec plusieurs threads ou en plusieurs processus, chacun avec un ou plusieurs threads.'
ms.assetid: ac0a8163-1498-4274-acfc-6a36b4c02a27
title: Quand utiliser le multitâche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b17e52f39a08120d3038663a95307ad72f228cfc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106523250"
---
# <a name="when-to-use-multitasking"></a>Quand utiliser le multitâche

Il existe deux façons d’implémenter le multitâche : en tant que processus unique avec plusieurs threads ou en plusieurs processus, chacun avec un ou plusieurs threads. Une application peut placer chaque thread qui requiert un espace d’adressage privé et des ressources privées dans son propre processus, afin de le protéger des activités d’autres threads de processus.

Un processus multithread peut gérer des tâches mutuellement exclusives à l’aide de threads, tels que la fourniture d’une interface utilisateur et l’exécution de calculs en arrière-plan. La création d’un processus multithread peut également être un moyen pratique de structurer un programme qui exécute plusieurs tâches similaires ou identiques simultanément. Par exemple, un serveur de canaux nommés peut créer un thread pour chaque processus client qui se connecte au canal. Ce thread gère la communication entre le serveur et le client. Votre processus peut utiliser plusieurs threads pour effectuer les tâches suivantes :

-   Gérer l’entrée pour plusieurs fenêtres.
-   Gérer l’entrée à partir de plusieurs appareils de communication.
-   différencier des tâches de priorités différentes (par exemple, un thread prioritaire gère les tâches soumises à des contraintes de temps, et un thread de priorité inférieure effectue d’autres tâches) ;
-   autoriser l’interface utilisateur à rester réactive, tout en allouant du temps aux tâches en arrière-plan.

Il est généralement plus efficace pour une application d’implémenter le multitâche en créant un processus multithread unique, plutôt que de créer plusieurs processus, pour les raisons suivantes :

-   Le système peut effectuer un basculement de contexte plus rapidement pour les threads que les processus, car un processus a plus de charge mémoire qu’un thread ne le fait (le contexte de processus est plus grand que le contexte de thread).
-   Tous les threads d’un processus partagent le même espace d’adressage et peuvent accéder aux variables globales du processus, ce qui peut simplifier la communication entre les threads.
-   Tous les threads d’un processus peuvent partager des handles ouverts aux ressources, tels que des fichiers et des canaux.

Vous pouvez utiliser d’autres techniques à la place du multithreading. Les plus importantes sont les suivantes : les entrées et sorties asynchrones, les ports de terminaison d’e/s, les appels de procédure asynchrones (APC) et la possibilité d’attendre plusieurs événements.

Un thread unique peut lancer plusieurs demandes d’e/s consommatrices de temps qui peuvent s’exécuter simultanément à l’aide d’e/s asynchrones. Les e/s asynchrones peuvent être effectuées sur des fichiers, des canaux et des appareils de communication série. Pour plus d’informations, consultez [synchronisation et entrée et sortie avec chevauchement](../sync/synchronization-and-overlapped-input-and-output.md).

Un seul thread peut bloquer sa propre exécution en attendant qu’un ou plusieurs événements se produisent. Cela est plus efficace que l’utilisation de plusieurs threads, chacun en attente d’un événement unique et plus efficace que l’utilisation d’un thread unique qui consomme le temps processeur en recherchant continuellement les événements à effectuer. Pour plus d’informations, consultez [fonctions Wait](../sync/wait-functions.md).

 

 
