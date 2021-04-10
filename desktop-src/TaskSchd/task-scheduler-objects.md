---
title: Planificateur de tâches des objets de script
description: Les objets de script décrits dans les rubriques suivantes fournissent un accès par programme aux fonctionnalités disponibles dans le Planificateur de tâches pour les développeurs de scripts Visual Basic et Visual Basic.
ms.assetid: 632bc9ae-b300-42ed-9d2c-f1d2d53d44fb
keywords:
- Planificateur de tâches Planificateur de tâches, référence, objets de script
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: acf9d74ae2bf586941f3b93a6c2cbb3a84836144
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104199916"
---
# <a name="task-scheduler-scripting-objects"></a>Planificateur de tâches des objets de script

Les objets de script décrits dans les rubriques suivantes fournissent un accès par programme aux fonctionnalités disponibles dans le Planificateur de tâches pour les développeurs de scripts Visual Basic et Visual Basic.


Les objets suivants sont introduits dans Planificateur de tâches 2,0.



| Object                                                         | Description                                                                                                                                                                                                                                           |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Action**](action.md)                                       | Fournit les propriétés communes qui sont héritées par tous les objets d’action.                                                                                                                                                                              |
| [**ActionCollection**](actioncollection.md)                   | Contient les actions effectuées par la tâche.                                                                                                                                                                                                           |
| [**BootTrigger**](boottrigger.md)                             | Représente un déclencheur qui démarre une tâche au démarrage du système.                                                                                                                                                                                    |
| [**ComHandlerAction**](comhandleraction.md)                   | Représente une action qui déclenche un gestionnaire.                                                                                                                                                                                                            |
| [**DailyTrigger**](dailytrigger.md)                           | Représente un déclencheur qui démarre une tâche basée sur une planification quotidienne.                                                                                                                                                                                    |
| [**EmailAction**](emailaction.md)                             | Représente une action qui envoie un message électronique.                                                                                                                                                                                                     |
| [**EventTrigger**](eventtrigger.md)                           | Représente un déclencheur qui démarre une tâche lorsqu’un événement système se produit.                                                                                                                                                                                   |
| [**ExecAction**](execaction.md)                               | Représente une action qui exécute une opération de ligne de commande.                                                                                                                                                                                          |
| [**IdleSettings**](idlesettings.md)                           | Spécifie comment l’Planificateur de tâches effectue des tâches lorsque l’ordinateur est en état d’inactivité.                                                                                                                                                            |
| [**IdleTrigger**](idletrigger.md)                             | Représente un déclencheur qui démarre une tâche lorsqu’une condition d’inactivité se produit.                                                                                                                                                                                |
| [**LogonTrigger**](logontrigger.md)                           | Représente un déclencheur qui démarre une tâche lorsqu’un utilisateur ouvre une session.                                                                                                                                                                                          |
| [**MonthlyDOWTrigger**](monthlydowtrigger.md)                 | Représente un déclencheur qui démarre une tâche sur une planification mensuelle de jour de semaine.                                                                                                                                                                            |
| [**MonthlyTrigger**](monthlytrigger.md)                       | Représente un déclencheur qui démarre une tâche basée sur une planification mensuelle.                                                                                                                                                                                  |
| [**NetworkSettings**](networksettings.md)                     | Fournit les paramètres utilisés par le service de Planificateur de tâches pour obtenir un profil réseau.                                                                                                                                                               |
| [**Directeur**](principal.md)                                 | Fournit les informations d’identification de sécurité pour un principal.                                                                                                                                                                                                    |
| [**RegisteredTask**](registeredtask.md)                       | Fournit les méthodes utilisées pour exécuter immédiatement la tâche, pour récupérer les instances en cours d’exécution de la tâche, pour récupérer ou définir les informations d’identification utilisées pour enregistrer la tâche et les propriétés qui décrivent la tâche.                                      |
| [**RegisteredTaskCollection**](registeredtaskcollection.md)   | Contient toutes les tâches qui sont inscrites.                                                                                                                                                                                                           |
| [**RegistrationInfo**](registrationinfo.md)                   | Fournit les informations d’administration qui peuvent être utilisées pour décrire la tâche. Ces informations incluent des détails tels que la description de la tâche, l’auteur de la tâche, la date à laquelle la tâche est inscrite et le descripteur de sécurité de la tâche. |
| [**RegistrationTrigger**](registrationtrigger.md)             | Représente un déclencheur qui démarre une tâche lorsque la tâche est inscrite.                                                                                                                                                                                  |
| [**RepetitionPattern**](repetitionpattern.md)                 | Définit la fréquence d’exécution de la tâche et la durée de répétition du modèle de répétition après le démarrage de la tâche.                                                                                                                                          |
| [**RunningTask**](runningtask.md)                             | Fournit les méthodes pour obtenir des informations à partir de et contrôler une tâche en cours d’exécution.                                                                                                                                                                              |
| [**RunningTaskCollection**](runningtaskcollection.md)         | Utilisé pour récupérer une tâche en cours d’exécution.                                                                                                                                                                                                                      |
| [**SessionStateChangeTrigger**](sessionstatechangetrigger.md) | Utilisé pour déclencher des tâches pour la connexion à la console ou la déconnexion, la connexion à distance ou la déconnexion, ou les notifications de verrouillage ou de déverrouillage de station                                                                                                                   |
| [**ShowMessageAction**](showmessageaction.md)                 | Représente une action qui affiche une boîte de message lorsqu’une tâche est activée.                                                                                                                                                                               |
| [**TaskDefinition**](taskdefinition.md)                       | Définit tous les composants d’une tâche, tels que les paramètres de tâche, les déclencheurs, les actions et les informations d’inscription.                                                                                                                                     |
| [**TaskFolder**](taskfolder.md)                               | Fournit les méthodes utilisées pour inscrire (créer) des tâches dans le dossier, supprimer des tâches du dossier et créer ou supprimer des sous-dossiers du dossier.                                                                                           |
| [**TaskFolderCollection**](taskfoldercollection.md)           | Compte le nombre de dossiers dans la collection et récupère un dossier spécifié de la collection.                                                                                                                                                   |
| [**TaskNamedValuePair**](tasknamedvaluepair.md)               | Crée une paire nom-valeur dans laquelle le nom est associé à la valeur.                                                                                                                                                                             |
| [**TaskNamedValueCollection**](tasknamedvaluecollection.md)   | Contient une collection de paires nom-valeur de l’objet [**TaskNamedValuePair**](tasknamedvaluepair.md) .                                                                                                                                                    |
| [**TaskService**](taskservice.md)                             | Fournit l’accès au service Planificateur de tâches pour la gestion des tâches inscrites.                                                                                                                                                                          |
| [**TaskSettings**](tasksettings.md)                           | Fournit les paramètres utilisés par les services Planificateur de tâches pour effectuer la tâche.                                                                                                                                                                      |
| [**TaskVariables**](taskvariables.md)                         | Définit les variables de tâche qui peuvent être passées en tant que paramètres aux gestionnaires de tâches et aux exécutables externes qui sont lancés par les tâches.                                                                                                                         |
| [**TimeTrigger**](timetrigger.md)                             | Représente un déclencheur qui démarre une tâche lorsque le déclencheur est activé.                                                                                                                                                                                |
| [**Stead**](trigger.md)                                     | Fournit les propriétés communes qui sont héritées par tous les objets déclencheurs.                                                                                                                                                                             |
| [**TriggerCollection**](triggercollection.md)                 | Permet d’ajouter, de supprimer et de récupérer les déclencheurs d’une tâche.                                                                                                                                                                                     |
| [**WeeklyTrigger**](weeklytrigger.md)                         | Représente un déclencheur qui démarre une tâche basée sur une planification hebdomadaire.                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence Planificateur de tâches](task-scheduler-reference.md)
</dt> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> </dl>

 

 




