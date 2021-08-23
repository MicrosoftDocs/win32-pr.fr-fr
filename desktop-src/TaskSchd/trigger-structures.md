---
title: Structures de déclencheur pour Planificateur de tâches 1,0
description: Planificateur de tâches 1,0 utilise plusieurs structures pour définir les critères d’un déclencheur.
ms.assetid: dd2ae4f6-fb2d-41f8-9400-7426b7ca4546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a70688597f7684a6b6a0bedba90cb23d34135cd732aaed37cd74970867b3b02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119002055"
---
# <a name="trigger-structures-for-task-scheduler-10"></a>Structures de déclencheur pour Planificateur de tâches 1,0

Planificateur de tâches 1,0 utilise plusieurs structures pour définir les critères d’un déclencheur.

> [!Note]  
> Pour plus d’informations sur les déclencheurs Planificateur de tâches 2,0, consultez [interfaces de déclencheur](trigger-interfaces.md).

 

## <a name="task-scheduler-10-structures"></a>Structures Planificateur de tâches 1,0

L’illustration suivante montre la structure de [**\_ déclencheur de tâche**](/windows/desktop/api/Mstask/ns-mstask-task_trigger) . Il a trois membres requis (**wBeginYear**, **wBeginMonth** et **wBeginDay**) qui doivent être définis lors de la création d’un nouveau déclencheur. (Pour accéder à la page de référence de cette structure, cliquez sur le nom de la structure dans l’illustration.)

![structure de déclencheur de tâche](images/tsktri1.png)

Sachez que le membre **TriggerType** utilise l’énumération de [**\_ \_ type de déclencheur de tâche**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) et que le membre de **type** utilise une structure d' **\_ \_ Union de déclencheur de tâche** . L’énumération des types de **\_ \_ déclencheurs de tâches** permet de spécifier le type de déclencheur (types de déclencheurs basés sur les événements et les temps). La structure d' [**\_ \_ Union de type de déclencheur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) est utilisée pour combiner les structures [**quotidienne**](/windows/desktop/api/Mstask/ns-mstask-daily), [**hebdomadaire**](/windows/desktop/api/Mstask/ns-mstask-weekly), [**MONTHLYDATE**](/windows/desktop/api/Mstask/ns-mstask-monthlydate) (jour du mois) et [**MONTHLYDOW**](/windows/desktop/api/Mstask/ns-mstask-monthlydow) (jour de la semaine) utilisées pour spécifier quand un déclencheur basé sur l’heure sera activé.

Si **TriggerType** spécifie un déclencheur basé sur une heure ou un déclencheur basé sur les événements, le membre de **type** est ignoré. La structure d' [**\_ \_ Union de type de déclencheur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) est utilisée uniquement si le membre **TriggerType** spécifie un déclencheur basé sur le temps quotidien, hebdomadaire, quotidien ou mensuel.

En outre, le paramètre du membre de **type** indique quel membre de la structure d' [**\_ \_ Union de type de déclencheur**](/windows/desktop/api/Mstask/ns-mstask-trigger_type_union) est utilisé. L’illustration suivante montre la relation entre les valeurs de l’énumération de [**\_ \_ type de déclencheur de tâche**](/windows/desktop/api/Mstask/ne-mstask-task_trigger_type) et les membres de la structure de la **structure de \_ type \_ de déclencheur** . (Pour accéder aux pages de référence de ces structures, cliquez sur le nom de la structure dans l’illustration.)

![relation entre les valeurs d’énumération de type de déclencheur de tâche et les membres de la structure de structure de type de déclencheur](images/tsktri3.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Déclencheurs de tâche](task-triggers.md)
</dt> <dt>

[Types de déclencheurs](trigger-types.md)
</dt> <dt>

[Interfaces de déclencheur](trigger-interfaces.md)
</dt> </dl>

 

 




