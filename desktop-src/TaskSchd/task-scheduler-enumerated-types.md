---
title: Types énumérés Planificateur de tâches
description: Répertorie les énumérations utilisées par les API Planificateur de tâches.
ms.assetid: 9779d32b-0142-41bb-88e2-df79a3b0c1b2
keywords:
- Planificateur de tâches Planificateur de tâches, référence, types énumérés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a70c4a939d176516d47f6af8bc0825b414bf1de
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104508209"
---
# <a name="task-scheduler-enumerated-types"></a>Types énumérés Planificateur de tâches

Décrit les types énumérés qui définissent les constantes utilisées par les API Planificateur de tâches.


Les types énumérés suivants sont introduits dans Planificateur de tâches 2,0.



| Énumération                                                                  | Description                                                                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [**\_type d’action de tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_action_type)                               | Définit le type d’actions qu’une tâche peut effectuer.                                                             |
| [**compatibilité des tâches \_**](/windows/desktop/api/taskschd/ne-taskschd-task_compatibility)                            | Définit les versions de Planificateur de tâches ou la commande AT à laquelle la tâche est compatible.                      |
| [**création de tâches \_**](/windows/desktop/api/taskschd/ne-taskschd-task_creation)                                       | Définit le mode de création, de mise à jour ou de désactivation de la tâche par le service Planificateur de tâches.                                   |
| [**\_indicateurs d’énumération de tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_enum_flags)                                 | Définit le mode d’énumération du Planificateur de tâches par le biais des tâches inscrites.                                              |
| [**\_stratégie d’instances de tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_instances_policy)                     | Définit comment le Planificateur de tâches gère les instances existantes de la tâche lorsqu’il démarre une nouvelle instance de la tâche. |
| [**TYPE de connexion à la tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_logon_type)                                  | Définit la technique d’ouverture de session requise pour exécuter une tâche.                                                          |
| [**TYPE de PROCESSTOKENSID de la tâche \_**](/windows/win32/api/taskschd/ne-taskschd-task_processtokensid_type)              | Définit les types de SID de processus qui peuvent être utilisés par les tâches.                                                         |
| [**\_indicateurs d’exécution de tâches \_**](/windows/desktop/api/taskschd/ne-taskschd-task_run_flags)                                   | Définit le mode d’exécution d’une tâche.                                                                                       |
| [**\_type de RUNLEVEL de la tâche \_**](/windows/win32/api/taskschd/ne-taskschd-task_runlevel_type)                           | Définit les indicateurs d’élévation LUA qui spécifient avec quel niveau de privilège la tâche sera exécutée.                         |
| [**\_type de \_ changement d’état de session de tâche \_ \_**](/windows/desktop/api/taskschd/ne-taskschd-task_session_state_change_type) | Définit les genres de Terminal Server modification de l’état de session que vous pouvez utiliser pour déclencher l’exécution d’une tâche.               |
| [**État de la tâche \_**](/windows/desktop/api/taskschd/ne-taskschd-task_state)                                            | Définit les différents États dans lesquels une tâche inscrite peut se trouver.                                                   |
| [**\_Déclencheur de tâche \_ type2**](/windows/desktop/api/taskschd/ne-taskschd-task_trigger_type2)                                  | Définit le type de déclencheur qui peut être utilisé par les tâches.                                                          |



 


> [!WARNING]
> Les énumérations Planificateur de tâches 1,0 sont uniquement disponibles dans les systèmes d’exploitation Windows 2000, Windows XP et Windows Server 2003. Ils sont déconseillés à partir de Windows Vista et peuvent être supprimés complètement à l’avenir. Utilisez à la place les énumérations Planificateur de tâches 2,0 listées ci-dessus.

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[Référence Planificateur de tâches](task-scheduler-reference.md)
</dt> </dl>

 

 




