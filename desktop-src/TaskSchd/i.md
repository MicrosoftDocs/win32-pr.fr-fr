---
title: I (Planificateur de tâches)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14bec8dd745aee798ebb6aa9cb296d7a0990b85b44562fb94ea844d2d5d3397
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120072639"
---
# <a name="i-task-scheduler"></a>I (Planificateur de tâches)

A B C D [e](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z

<dl> <dt>

<span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**conditions d’inactivité**
</dt> <dd>

Période pendant laquelle il n’y a aucune entrée d’utilisateur sur l’ordinateur. Les conditions d’inactivité sont associées à l’heure de début planifiée pour la tâche.

Ces conditions sont définies en appelant [**IScheduledWorkItem :: SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).

</dd> <dt>

<span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**déclencheurs inactifs**
</dt> <dd>

Déclencheur basé sur les événements qui est déclenché lorsque l’ordinateur devient inactif pendant un laps de temps spécifique.

Les déclencheurs inactifs sont créés en définissant le \_ \_ type de déclencheur de tâche de la structure de [**\_ déclencheur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de tâche \_ sur déclencheur d’événements de tâche en mode \_ \_ \_ inactif.

</dd> <dt>

<span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**temps d’attente d’inactivité**
</dt> <dd>

Intervalle de temps (en minutes) utilisé par un déclencheur inactif ou une condition d’inactivité. Les déclencheurs inactifs sont des déclencheurs basés sur des événements qui ne sont pas associés à une heure planifiée. Les conditions d’inactivité sont associées à l’heure de début planifiée pour la tâche.

La durée d’inactivité est définie par un appel à [**IScheduledWorkItem :: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).

</dd> </dl>

 

 




