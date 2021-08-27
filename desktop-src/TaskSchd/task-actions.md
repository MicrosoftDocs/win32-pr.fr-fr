---
title: Actions de tâche
description: Les éléments de travail exécutés par une tâche sont appelés actions. Une tâche peut avoir une seule action ou au maximum 32 actions. Sachez que lorsque plusieurs actions sont spécifiées, elles sont exécutées de manière séquentielle.
ms.assetid: 4cbe739d-4c4e-4469-8289-4be41b93950c
keywords:
- actions Planificateur de tâches
- actions Planificateur de tâches, Description
- actions Planificateur de tâches, exécuter l’action
- actions Planificateur de tâches, action du gestionnaire COM
- Planificateur de tâches d’exécution de l’action
- Action du gestionnaire COM Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54a7cc4a0e3ecbd4d55e4731379287f2cf4fd660
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470494"
---
# <a name="task-actions"></a>Actions de tâche

Les éléments de travail exécutés par une tâche sont appelés actions. Une tâche peut avoir une seule action ou au maximum 32 actions. Sachez que lorsque plusieurs actions sont spécifiées, elles sont exécutées de manière séquentielle.

## <a name="types-of-actions"></a>Types d'actions

Le tableau d’actions suivant décrit le type de travail ou les actions qui peuvent être accomplies par une tâche.

| Type d’action      | Description                                                             |
|---------------------|-------------------------------------------------------------------------|
| Action du comhandleur   | Cette action déclenche un gestionnaire COM.                                        |
| Action d’exécution         | cette action exécute une opération de ligne de commande telle que le démarrage de Bloc-notes. |
| Action de messagerie       | Cette action envoie un message électronique lorsqu’une tâche est déclenchée.                    |
| Afficher l’action du message | Cette action affiche une boîte de message avec un message et un titre spécifiés.     |



 

## <a name="specifying-actions"></a>Spécification des actions

Les actions d’une tâche sont spécifiées lorsque la tâche est définie et stockée dans une collection d’actions utilisées par le service Planificateur de tâches. Le tableau suivant répertorie des liens vers des rubriques de référence pour les API et les éléments XML associés à des actions.

Pour plus d’informations et des exemples sur l’utilisation des interfaces Planificateur de tâches, les objets de script et XML, consultez [utilisation du planificateur de tâches](using-the-task-scheduler.md).

### <a name="interface-apis-for-c-development"></a>API d’interface pour le développement C++



| API                                                                    | Description                                                  |
|------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Propriété actions de ITaskDefinition**](/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_actions) | Obtient ou définit les actions effectuées par la tâche.              |
| [**IActionCollection**](/windows/desktop/api/taskschd/nn-taskschd-iactioncollection)                         | Contient les actions effectuées par la tâche.                  |
| [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)                         | Représente une action qui déclenche un gestionnaire.                   |
| [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction)                                     | Représente une action qui exécute une opération de ligne de commande. |
| [**IEmailAction**](/windows/desktop/api/taskschd/nn-taskschd-iemailaction)                                   | Représente une action qui envoie un message électronique.            |
| [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction)                       | Représente une action qui affiche une boîte de message.               |



 

### <a name="scripting-object-apis-for-scripting-development"></a>Scripts des API objet pour le développement de scripts



| API                                                      | Description                                                  |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**TaskDefinition. actions**](taskdefinition-actions.md) | Obtient ou définit les actions effectuées par la tâche.              |
| [**ActionCollection**](actioncollection.md)             | Contient les actions effectuées par la tâche.                  |
| [**ComHandlerAction**](comhandleraction.md)             | Représente une action qui déclenche un gestionnaire.                   |
| [**ExecAction**](execaction.md)                         | Représente une action qui exécute une opération de ligne de commande. |
| [**EmailAction**](emailaction.md)                       | Représente une action qui envoie un message électronique.            |
| [**ShowMessageAction**](showmessageaction.md)           | Représente une action qui affiche une boîte de message.               |



 

### <a name="xml-elements"></a>Éléments XML



| Élément                                                                    | Description                                                  |
|----------------------------------------------------------------------------|--------------------------------------------------------------|
| [**Actions**](taskschedulerschema-actions-tasktype-element.md)            | Définit les actions effectuées par la tâche.                   |
| [**Comgérer**](taskschedulerschema-comhandler-actiongroup-element.md)   | Représente une action qui déclenche un gestionnaire.                   |
| [**Exécutable**](taskschedulerschema-exec-actiongroup-element.md)               | Représente une action qui exécute une opération de ligne de commande. |
| [**SendEmail**](taskschedulerschema-sendemail-actiongroup-element.md)     | Représente une action qui envoie un message électronique.            |
| [**ShowMessage**](taskschedulerschema-showmessage-actiongroup-element.md) | Représente une action qui affiche une boîte de message.               |



 

## <a name="using-variables-in-action-properties"></a>Utilisation de variables dans les propriétés d’action

Certaines propriétés d’action qui sont de type **BSTR** peuvent contenir des variables $ (arg0), $ (Arg1),..., $ (Arg32) dans leurs valeurs de chaîne. Ces variables sont remplacées par les valeurs spécifiées dans le paramètre *params* des méthodes [**IRegisteredTask :: Run**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-run) et [**IRegisteredTask :: RunEx**](/windows/desktop/api/taskschd/nf-taskschd-iregisteredtask-runex) ou sont contenues dans le déclencheur d’événement pour la tâche. Le tableau suivant répertorie les propriétés d’action qui peuvent utiliser des variables dans leurs valeurs de chaîne.


| Action | Propriétés | 
|--------|------------|
| Action du gestionnaire COM | C++ :<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid"><strong>Propriété ClassId de IComHandlerAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data"><strong>Propriété de données de IComHandlerAction</strong></a></li></ul><br /> Création de scripts :<ul><li><a href="comhandleraction-classid.md"><strong>ComHandlerAction. ClassId</strong></a></li><li><a href="comhandleraction-data.md"><strong>ComHandlerAction. Data</strong></a></li></ul><br /> | 
| Action de messagerie | C++ :<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body"><strong>Propriété Body de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server"><strong>Propriété Server de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject"><strong>Propriété Subject de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to"><strong>À la propriété de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc"><strong>Propriété CC de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc"><strong>Propriété BCC de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto"><strong>Propriété ReplyTo de IEmailAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from"><strong>De la propriété de IEmailAction</strong></a></li></ul><br /> Création de scripts :<ul><li><a href="emailaction-body.md"><strong>EmailAction. Body</strong></a></li><li><a href="emailaction-server.md"><strong>EmailAction. Server</strong></a></li><li><a href="emailaction-subject.md"><strong>EmailAction. Subject</strong></a></li><li><a href="emailaction-to.md"><strong>EmailAction.To</strong></a></li><li><a href="emailaction-cc.md"><strong>EmailAction.Cc</strong></a></li><li><a href="emailaction-bcc.md"><strong>EmailAction. CCI</strong></a></li><li><a href="emailaction-replyto.md"><strong>EmailAction. ReplyTo</strong></a></li><li><a href="emailaction-from.md"><strong>EmailAction. from</strong></a></li></ul><br /> | 
| Action d’exécution | C++ :<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments"><strong>Propriété arguments de IExecAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory"><strong>Propriété WorkingDirectory de IExecAction</strong></a></li></ul><br /> Création de scripts :<ul><li><a href="execaction-arguments.md"><strong>ExecAction. arguments</strong></a></li><li><a href="execaction-workingdirectory.md"><strong>ExecAction. WorkingDirectory</strong></a></li></ul><br /> | 
| Afficher l’action du message | C++ :<ul><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title"><strong>Propriété Title de IShowMessageAction</strong></a></li><li><a href="/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody"><strong>Propriété MessageBody de IShowMessageAction</strong></a></li></ul><br /> Création de scripts :<ul><li><a href="showmessageaction-title.md"><strong>ShowMessageAction. title</strong></a></li><li><a href="showmessageaction-messagebody.md"><strong>ShowMessageAction. MessageBody</strong></a></li></ul><br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de l’Planificateur de tâches](about-the-task-scheduler.md)
</dt> </dl>

 

 





