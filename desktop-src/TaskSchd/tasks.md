---
title: Tâches
description: Une tâche correspond au travail planifié effectué par le service Planificateur de tâches.
ms.assetid: 24c43834-5731-4b14-9409-7d7cf20b1a71
keywords:
- tâches Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efbb4ef41915ec70c98b59c9a7ba74c00f283ce6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510631"
---
# <a name="tasks"></a>Tâches

Une tâche correspond au travail planifié effectué par le service Planificateur de tâches. Une tâche est composée de différents composants, mais une tâche doit contenir un déclencheur que le Planificateur de tâches utilise pour démarrer la tâche et une action qui décrit le travail que le Planificateur de tâches effectuera.

Quand une tâche est créée, elle est stockée dans un dossier de tâches. Les dossiers de tâches sont accessibles par le biais de l’interface [**ITaskFolder**](/windows/desktop/api/taskschd/nn-taskschd-itaskfolder) ([**TaskFolder**](taskfolder.md) pour les scripts), et les tâches sont accessibles via l’interface [**IRegisteredTask**](/windows/desktop/api/taskschd/nn-taskschd-iregisteredtask) ([**RegisteredTask**](registeredtask.md) pour les scripts) lors de leur création. Vous pouvez modifier les listes de contrôle d’accès (ACL) pour les tâches et les dossiers de tâches afin d’accorder ou de refuser à certains utilisateurs et groupes l’accès à un dossier de tâches ou de tâches. Cela peut être fait à l’aide de la méthode [**IRegisteredTask :: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-setsecuritydescriptor) , de la méthode [**ITaskFolder :: SetSecurityDescriptor**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-setsecuritydescriptor) ou en spécifiant un descripteur de sécurité lorsqu’une tâche est inscrite à l’aide de la méthode [**RegisterTaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertaskdefinition) ou [**RegisterTask**](/windows/desktop/api/taskschd/nf-taskschd-itaskfolder-registertask) .

> [!Note]  
> Si le compte système local se voit refuser l’accès à un fichier de tâche ou à un dossier de tâches, le service Planificateur de tâches peut produire des résultats inattendus.

 

## <a name="components-of-a-task"></a>Composants d’une tâche

L’illustration suivante montre les composants de tâche.

![composants de tâche](images/taskcomponents.png)

La liste suivante contient une brève description de chaque composant de tâche :

-   Déclencheurs : Planificateur de tâches utilise des déclencheurs basés sur des événements ou sur le temps pour savoir quand démarrer une tâche. Chaque tâche peut spécifier un ou plusieurs déclencheurs pour démarrer la tâche.

    Pour plus d’informations sur les déclencheurs, consultez [déclencheurs de tâches](task-triggers.md).

-   Actions : actions, le travail réel, effectuées par la tâche. Chaque tâche peut spécifier une ou plusieurs actions pour terminer son travail.

    Pour plus d’informations sur les actions, consultez [actions des tâches](task-actions.md).

-   Principaux : les principaux définissent le contexte de sécurité dans lequel la tâche est exécutée. Par exemple, un principal peut définir un utilisateur ou un groupe d’utilisateurs spécifique qui peut exécuter la tâche.

    Pour plus d’informations sur les principaux, consultez [contextes de sécurité pour les tâches](security-contexts-for-running-tasks.md).

-   Paramètres : il s’agit des paramètres que le Planificateur de tâches utilise pour exécuter la tâche en ce qui concerne les conditions qui sont externes à la tâche elle-même. Par exemple, ces paramètres peuvent spécifier la priorité de la tâche par rapport à d’autres tâches, si plusieurs instances de la tâche peuvent être exécutées, comment la tâche est traitée lorsque l’ordinateur est dans une condition d’inactivité, ainsi que d’autres conditions.

    Pour plus d’informations sur les paramètres de tâche, consultez [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) ([**TaskSettings**](tasksettings.md) pour les scripts).

    > [!Note]  
    > Par défaut, une tâche sera arrêtée 72 heures après son démarrage. Vous pouvez modifier ce paramètre en modifiant le paramètre [**ExecutionTimeLimit**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_executiontimelimit) .

     

-   Informations d’inscription : il s’agit d’informations d’administration collectées lorsque la tâche est inscrite. Par exemple, ces informations décrivent l’auteur de la tâche, la date à laquelle la tâche a été inscrite, une description XML de la tâche et d’autres informations.

    Pour plus d’informations sur l’inscription des tâches, consultez [informations d’inscription des tâches](task-registration-information.md).

-   Données : il s’agit d’une documentation supplémentaire sur la tâche fournie par l’auteur de la tâche. Par exemple, ces données peuvent contenir une aide XML qui peut être utilisée par les utilisateurs lorsqu’ils exécutent la tâche.

## <a name="task-apis"></a>API de tâche

Planificateur de tâches 2,0 fournit deux ensembles d’API : un ensemble d’interfaces et d’objets de script pour Planificateur de tâches 2,0. Pour plus d’informations, consultez [Planificateur de tâches référence](task-scheduler-reference.md).

La compatibilité des tâches, définie par la propriété de [**compatibilité**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_compatibility) , doit uniquement être définie sur \_ compatibilité \_ des tâches v1 si une tâche doit être accessible ou modifiée à partir d’un ordinateur Windows XP, Windows Server 2003 ou Windows 2000. Dans le cas contraire, il est recommandé d’utiliser la compatibilité Planificateur de tâches 2,0, car elle a plus de fonctionnalités.

À compter de Planificateur de tâches 2,0, l’interface [**la**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) ([**TaskService**](taskservice.md) pour les scripts) est utilisée comme point de départ pour créer des tâches dans les dossiers spécifiés. L’interface [**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition) ([**TaskDefinition**](taskdefinition.md) pour les scripts) est utilisée pour contenir tous les composants d’une tâche, tels que les paramètres, les actions et les déclencheurs. Les API [**ITaskTrigger**](/windows/desktop/api/Mstask/nn-mstask-itasktrigger), [**IAction**](/windows/desktop/api/taskschd/nn-taskschd-iaction)et [**ITaskSettings**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings) fournissent des propriétés qui sont ensuite utilisées pour définir les autres composants de la tâche. Planificateur de tâches 1,0 fournit l’interface [**ITask**](/windows/desktop/api/Mstask/nn-mstask-itask) , qui est prise en charge uniquement pour la compatibilité descendante.

Pour les scripts, les interfaces de Planificateur de tâches mappent aux objets de script qui ont des noms, des propriétés et des méthodes similaires. Par exemple, l’objet de script [**TaskService**](taskservice.md) a les mêmes propriétés et méthodes que l’interface [**la**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice) .

Pour plus d’informations et des exemples sur l’utilisation des interfaces Planificateur de tâches, les objets de script et XML, consultez [utilisation du planificateur de tâches](using-the-task-scheduler.md).

### <a name="task-scheduler-10-tasks"></a>Planificateur de tâches les tâches 1,0

Une tâche Planificateur de tâches 1,0 est tout type d’application ou de fichier que le Planificateur de tâches peut exécuter. Il peut s’agir de l’un des éléments suivants (pris en charge par le système d’exploitation sur lequel la tâche s’exécute) : les applications Win32, les applications Win16, les applications du système d’exploitation/2, les applications MS-DOS, les fichiers de commandes ( \* . bat), les fichiers de commandes ( \* . cmd) ou tout type de fichier correctement inscrit.

Les données qui décrivent une tâche sont conservées dans un fichier de tâches qui est stocké dans le dossier tâches planifiées. Pour plus d’informations, consultez [*dossier tâches planifiées*](s.md). Le nom de ces fichiers de tâches inclut le nom de la tâche, suivi de l’extension de nom de fichier. job.

Pour plus d’informations sur l’ajout d’Planificateur de tâches tâches 1,0, consultez [Ajout d’éléments de travail](adding-work-items.md).

Pour plus d’informations sur l’énumération par le biais de Planificateur de tâches tâches 1,0, consultez [énumération de tâches](enumerating-tasks.md).

Pour qu’un ordinateur Windows Server 2003, Windows XP ou Windows 2000 crée, surveille ou contrôle des tâches sur un ordinateur Windows Vista, les opérations suivantes doivent être effectuées sur l’ordinateur Windows Vista, et l’utilisateur qui appelle la méthode [**ITaskScheduler :: SetTargetComputer**](/windows/desktop/api/Mstask/nf-mstask-itaskscheduler-settargetcomputer) doit être membre du groupe Administrateurs sur l’ordinateur Windows Vista distant.

**Pour activer l’exception de partage de fichiers et d’imprimantes dans le pare-feu Windows**

1.  Cliquez sur **Démarrer**, puis sur **Panneau de configuration**.
2.  Dans le **panneau de configuration**, cliquez sur **affichage classique** , puis double-cliquez sur l’icône **pare-feu Windows** .
3.  Dans la fenêtre **pare-feu Windows** , cliquez sur l’onglet **exceptions** et activez la case à cocher exception de **partage de fichiers et d’imprimantes** .

**Pour activer le service « Registre distant »**

-   Ouvrez une fenêtre d’invite de commandes et entrez la commande suivante : **net start « Remote Registry »**.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’Planificateur de tâches](about-the-task-scheduler.md)
</dt> <dt>

[Déclencheurs de tâche](task-triggers.md)
</dt> <dt>

[Actions de tâche](task-actions.md)
</dt> <dt>

[**ITaskDefinition**](/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition)
</dt> <dt>

[**TaskDefinition**](taskdefinition.md)
</dt> <dt>

[**La**](/windows/desktop/api/taskschd/nn-taskschd-itaskservice)
</dt> <dt>

[**TaskService**](taskservice.md)
</dt> </dl>

 

 




