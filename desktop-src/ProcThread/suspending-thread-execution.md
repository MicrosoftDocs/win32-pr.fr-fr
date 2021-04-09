---
description: Un thread peut suspendre et reprendre l’exécution d’un autre thread. Lorsqu’un thread est suspendu, il n’est pas planifié pour l’heure sur le processeur.
ms.assetid: b76d7af7-e3ec-4663-a9e7-832c01733c8c
title: Interruption de l’exécution des threads
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3688b0327ecf5fd21f07e9be6be6ecab17d64617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951976"
---
# <a name="suspending-thread-execution"></a>Interruption de l’exécution des threads

Un thread peut suspendre et reprendre l’exécution d’un autre thread. Lorsqu’un thread est suspendu, il n’est pas planifié pour l’heure sur le processeur.

Si un thread est créé dans un état suspendu (avec l’indicateur de [**création \_ suspendu**](process-creation-flags.md) ), il ne commence pas à s’exécuter jusqu’à ce qu’un autre thread appelle la fonction [**ResumeThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-resumethread) avec un handle vers le thread suspendu. Cela peut être utile pour initialiser l’état du thread avant qu’il commence à s’exécuter. La suspension d’un thread au moment de la création peut être utile pour une synchronisation ponctuelle, car cela garantit que le thread suspendu exécutera le point de départ de son code lorsque vous appelez **ResumeThread**.

La fonction [**SuspendThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-suspendthread) n’est pas destinée à être utilisée pour la synchronisation de threads, car elle ne contrôle pas le point dans le code où l’exécution du thread est suspendue. Cette fonction est principalement conçue pour être utilisée par les débogueurs.

Un thread peut générer temporairement son exécution pour un intervalle spécifié en appelant les fonctions [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) ou [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex) . cela est particulièrement utile dans les cas où le thread répond à l’interaction de l’utilisateur, car il peut retarder l’exécution suffisamment longtemps pour permettre aux utilisateurs d’observer les résultats de leurs actions. Pendant l’intervalle de veille, le thread n’est pas planifié pour l’heure sur le processeur.

La fonction [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) est similaire à [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) et [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex), sauf que vous ne pouvez pas spécifier l’intervalle. **SwitchToThread** autorise le thread à abandonner sa tranche de temps.

 

 
