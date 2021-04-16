---
title: I (Planificateur de tâches)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 84a58712-72fb-47c6-8d92-e2a0ebfccaca
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8492f707a171c6811b4702d2a07de47d29482a8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104508229"
---
# <a name="i-task-scheduler"></a><span data-ttu-id="29de5-103">I (Planificateur de tâches)</span><span class="sxs-lookup"><span data-stu-id="29de5-103">I (Task Scheduler)</span></span>

<span data-ttu-id="29de5-104">A B C D [e](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="29de5-104">A B C D [E](e.md) F G H I J K L M N O [P](p.md) Q R [S](s.md) [T](t.md) U V [W](w.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="29de5-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**conditions d’inactivité**</span><span class="sxs-lookup"><span data-stu-id="29de5-105"><span id="_msb_idle_conditions_gly"></span><span id="_MSB_IDLE_CONDITIONS_GLY"></span>**idle conditions**</span></span>
</dt> <dd>

<span data-ttu-id="29de5-106">Période pendant laquelle il n’y a aucune entrée d’utilisateur sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="29de5-106">A period of time in which there is no user input on the computer.</span></span> <span data-ttu-id="29de5-107">Les conditions d’inactivité sont associées à l’heure de début planifiée pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="29de5-107">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="29de5-108">Ces conditions sont définies en appelant [**IScheduledWorkItem :: SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span><span class="sxs-lookup"><span data-stu-id="29de5-108">These conditions are set by calling [**IScheduledWorkItem::SetFlags**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setflags).</span></span>

</dd> <dt>

<span data-ttu-id="29de5-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**déclencheurs inactifs**</span><span class="sxs-lookup"><span data-stu-id="29de5-109"><span id="_msb_idle_triggers_gly"></span><span id="_MSB_IDLE_TRIGGERS_GLY"></span>**idle triggers**</span></span>
</dt> <dd>

<span data-ttu-id="29de5-110">Déclencheur basé sur les événements qui est déclenché lorsque l’ordinateur devient inactif pendant un laps de temps spécifique.</span><span class="sxs-lookup"><span data-stu-id="29de5-110">An event-based trigger that is fired when the computer becomes idle for a specific amount of time.</span></span>

<span data-ttu-id="29de5-111">Les déclencheurs inactifs sont créés en définissant le \_ \_ type de déclencheur de tâche de la structure de [**\_ déclencheur**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) de tâche \_ sur déclencheur d’événements de tâche en mode \_ \_ \_ inactif.</span><span class="sxs-lookup"><span data-stu-id="29de5-111">Idle triggers are created by setting the TASK\_TRIGGER\_TYPE member of the [**TASK\_TRIGGER**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) structure to TASK\_EVENT\_TRIGGER\_ON\_IDLE.</span></span>

</dd> <dt>

<span data-ttu-id="29de5-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**temps d’attente d’inactivité**</span><span class="sxs-lookup"><span data-stu-id="29de5-112"><span id="_msb_idle_wait_time_gly"></span><span id="_MSB_IDLE_WAIT_TIME_GLY"></span>**idle wait time**</span></span>
</dt> <dd>

<span data-ttu-id="29de5-113">Intervalle de temps (en minutes) utilisé par un déclencheur inactif ou une condition d’inactivité.</span><span class="sxs-lookup"><span data-stu-id="29de5-113">The time interval (in minutes) used by an idle trigger or idle condition.</span></span> <span data-ttu-id="29de5-114">Les déclencheurs inactifs sont des déclencheurs basés sur des événements qui ne sont pas associés à une heure planifiée.</span><span class="sxs-lookup"><span data-stu-id="29de5-114">Idle triggers are event-based triggers that are not associated with a scheduled time.</span></span> <span data-ttu-id="29de5-115">Les conditions d’inactivité sont associées à l’heure de début planifiée pour la tâche.</span><span class="sxs-lookup"><span data-stu-id="29de5-115">Idle conditions are associated with the scheduled start time for the task.</span></span>

<span data-ttu-id="29de5-116">La durée d’inactivité est définie par un appel à [**IScheduledWorkItem :: SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span><span class="sxs-lookup"><span data-stu-id="29de5-116">The idle time is set by a call to [**IScheduledWorkItem::SetIdleWait**](/windows/desktop/api/Mstask/nf-mstask-ischeduledworkitem-setidlewait).</span></span>

</dd> </dl>

 

 




