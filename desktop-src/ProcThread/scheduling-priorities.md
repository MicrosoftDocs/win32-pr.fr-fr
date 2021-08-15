---
description: Les threads sont planifiés pour s’exécuter en fonction de leur priorité de planification.
ms.assetid: 8710cd56-6bf3-4317-a1f6-1a159394ce2a
title: Planification des priorités
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 359f86e6ef78ffe1e549045eebbe435674b50f25f25bd30598fce8581c06092a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117793311"
---
# <a name="scheduling-priorities"></a>Planification des priorités

Les threads sont planifiés pour s’exécuter en fonction de leur *priorité de planification*. Une priorité de planification est affectée à chaque thread. La plage des niveaux de priorité est comprise entre zéro (priorité la plus basse) et 31 (priorité la plus élevée). Seul le thread de page zéro peut avoir une priorité de zéro. (Le thread de page zéro est un thread système chargé de la mise à zéro des pages libres lorsqu’il n’y a pas d’autres threads qui doivent s’exécuter.)

Le système traite tous les threads ayant la même priorité comme étant égaux. Le système affecte les tranches de temps dans un mode de tourniquet (Round Robin) à tous les threads ayant la priorité la plus élevée. Si aucun de ces threads n’est prêt à être exécuté, le système affecte les tranches de temps de manière répétée à tous les threads ayant la priorité la plus élevée suivante. Si un thread de priorité plus élevée est disponible pour exécution, le système cesse d’exécuter le thread de priorité inférieure (sans l’autoriser à terminer son tranche de temps) et affecte une tranche horaire complète au thread de priorité plus élevée. Pour plus d’informations, consultez [changements de contexte](context-switches.md).

La priorité de chaque thread est déterminée par les critères suivants :

-   Classe de priorité de son processus
-   Niveau de priorité du thread dans la classe de priorité de son processus

La classe de priorité et le niveau de priorité sont combinés pour former la *priorité de base* d’un thread. Pour plus d’informations sur la priorité dynamique d’un thread, consultez [augmentations de priorité](priority-boosts.md).

## <a name="priority-class"></a>Classe de priorité

Chaque processus appartient à l’une des classes de priorité suivantes :<dl> \_classe de priorité Idle \_  
classe de priorité inférieure à la \_ normale \_ \_  
\_classe de priorité normale \_  
classe de priorité supérieure à la \_ normale \_ \_  
\_classe de priorité élevée \_  
\_classe de priorité en temps réel \_  
</dl>

Par défaut, la classe de priorité d’un processus est une \_ classe de priorité normale \_ . Utilisez la fonction [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) pour spécifier la classe de priorité d’un processus enfant lorsque vous le créez. Si le processus appelant est une \_ classe de priorité inactive \_ ou une classe de \_ \_ priorité normale \_ , le nouveau processus hérite de cette classe. Utilisez la fonction [**GetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getpriorityclass) pour déterminer la classe de priorité actuelle d’un processus et la fonction [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) pour modifier la classe de priorité d’un processus.

Les processus qui surveillent le système, tels que les économiseurs d’écran ou les applications qui mettent régulièrement à jour un affichage, doivent utiliser la classe de priorité inactive \_ \_ . Cela empêche les threads de ce processus, qui n’ont pas de priorité élevée, d’interférer avec les threads de priorité supérieure.

Utilisez la \_ classe High Priority \_ avec précaution. Si un thread s’exécute au niveau de priorité le plus élevé pour des périodes prolongées, les autres threads du système n’obtiendront pas de temps processeur. Si plusieurs threads sont définis en priorité élevée en même temps, les threads perdent leur efficacité. La classe de priorité élevée doit être réservée pour les threads qui doivent répondre à des événements critiques dans le temps. Si votre application exécute une tâche qui requiert la classe de priorité élevée alors que le reste de ses tâches est une priorité normale, utilisez [**SetPriorityClass**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setpriorityclass) pour augmenter temporairement la classe de priorité de l’application ; Ensuite, réduisez-la après la fin de la tâche critique du temps. Une autre stratégie consiste à créer un processus de haute priorité qui a tous les threads bloqués la plupart du temps, en réveillent les threads uniquement quand des tâches critiques sont nécessaires. Le point important est qu’un thread à priorité élevée doit s’exécuter pendant une courte période, et uniquement lorsqu’il a un travail critique dans le temps.

Vous ne devriez presque jamais utiliser \_ la classe de priorité en temps réel \_ , car cela interrompt les threads système qui gèrent l’entrée de la souris, l’entrée au clavier et le vidage du disque en arrière-plan. Cette classe peut être appropriée pour les applications qui « communiquent » directement au matériel ou qui effectuent de brèves tâches qui doivent avoir des interruptions limitées.

## <a name="priority-level"></a>Niveau de priorité

Voici les niveaux de priorité de chaque classe de priorité :<dl> priorité de THREAD \_ \_ inactive  
priorité de THREAD la \_ \_ plus basse  
priorité de THREAD inférieure à la \_ \_ \_ normale  
priorité de THREAD \_ \_ normale  
priorité de THREAD supérieure à la \_ \_ \_ normale  
priorité de THREAD la \_ \_ plus élevée  
temps de priorité des THREADs \_ \_ \_ critique  
</dl>

Tous les threads sont créés à l’aide de la priorité de THREAD \_ \_ normal. Cela signifie que la priorité de thread est la même que la classe de priorité de processus. Après avoir créé un thread, utilisez la fonction [**SetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriority) pour ajuster sa priorité par rapport à d’autres threads dans le processus.

Une stratégie classique consiste à utiliser la priorité de THREAD supérieure à la \_ \_ \_ normale ou \_ \_ la priorité de thread la plus élevée pour le thread d’entrée du processus, afin de garantir la réactivité de l’application à l’utilisateur. Les threads d’arrière-plan, en particulier ceux qui utilisent beaucoup de ressources processeur, peuvent être définis sur la priorité de THREAD inférieure à la \_ \_ \_ normale ou la \_ priorité de thread la \_ plus faible, pour s’assurer qu’elles peuvent être anticipées si nécessaire. Toutefois, si un thread attend un autre thread avec une priorité plus basse pour terminer une tâche, veillez à bloquer l’exécution du thread en attente de haute priorité. Pour ce faire, utilisez une [fonction Wait](../sync/wait-functions.md), [une section critique](../sync/critical-section-objects.md)ou la fonction [**Sleep**](/windows/win32/api/synchapi/nf-synchapi-sleep) , [**SleepEx**](/windows/win32/api/synchapi/nf-synchapi-sleepex)ou [**SwitchToThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-switchtothread) . Cela est préférable à l’exécution d’une boucle par le thread. Dans le cas contraire, le processus peut être bloqué, car le thread avec une priorité plus faible n’est jamais planifié.

Pour déterminer le niveau de priorité actuel d’un thread, utilisez la fonction [**GetThreadPriority**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriority) .

## <a name="base-priority"></a>Priorité de base

La classe de priorité du processus et le niveau de priorité du thread sont combinés pour former la priorité de base de chaque thread.

Le tableau suivant indique la priorité de base pour les combinaisons de la classe de priorité du processus et la valeur de priorité du thread.


<table>
<tr>
<th colspan="2">Classe de priorité du processus</th>
<th>Niveau de priorité du thread</th>
<th>Priorité de base</th>
</tr>
<tr>
<td rowspan="7" colspan="2">IDLE_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>2</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>3</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">BELOW_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>4</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>5</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>6</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>7</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">ABOVE_NORMAL_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>8</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>9</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>10</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">HIGH_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>1</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>11</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>12</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>13</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>14</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>15</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>15</td>
</tr>
<tr>
<td rowspan="7" colspan="2">REALTIME_PRIORITY_CLASS </td>
<td>THREAD_PRIORITY_IDLE</td>
<td>16</td>
</tr>
<tr>
<td>THREAD_PRIORITY_LOWEST</td>
<td>22</td>
</tr>
<tr>
<td>THREAD_PRIORITY_BELOW_NORMAL</td>
<td>23</td>
</tr>
<tr>
<td>THREAD_PRIORITY_NORMAL</td>
<td>24</td>
</tr>
<tr>
<td>THREAD_PRIORITY_ABOVE_NORMAL</td>
<td>25</td>
</tr>
<tr>
<td>THREAD_PRIORITY_HIGHEST</td>
<td>26</td>
</tr>
<tr>
<td>THREAD_PRIORITY_TIME_CRITICAL</td>
<td>31</td>
</tr>
</table>

 

 

 
