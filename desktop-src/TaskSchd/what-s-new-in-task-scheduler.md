---
title: Nouveautés de Planificateur de tâches
description: Liste des nouvelles fonctionnalités introduites par différentes versions de Planificateur de tâches.
ms.assetid: 43fbbbd2-6e97-4ba5-9474-23c5e2b33612
keywords:
- Planificateur de tâches Planificateur de tâches, nouveautés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5245ab4e681af937924cfbd217095009d80d6a11
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414633"
---
# <a name="whats-new-in-task-scheduler"></a>Nouveautés de Planificateur de tâches

Les modifications suivantes résument ce qui est nouveau dans les différentes versions de Planificateur de tâches.

## <a name="windows-10-and-windows-server-2016"></a>Windows 10 (et Windows Server 2016)

Les modifications de Planificateur de tâches suivantes sont introduites dans Windows 10.

-   lorsque l’économiseur de batterie est activé, Windows tâches Planificateur de tâches sont déclenchées uniquement si la tâche est :

    -   Non défini pour **Démarrer la tâche uniquement si l’ordinateur est inactif... (la** tâche n’utilise pas [**IdleSettings**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_idlesettings))
    -   Non défini pour s’exécuter pendant la maintenance automatique (la tâche n’utilise pas [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings))
    -   Est configuré pour **s’exécuter uniquement quand l’utilisateur a ouvert une session** (la tâche [**LogonType**](/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_logontype) est un **\_ \_ \_ jeton interactif d’ouverture de session de tâche** ou un **\_ \_ groupe d’ouverture de session de tâche**)

    Tous les autres déclencheurs sont retardés jusqu’à ce que l’économiseur de batterie soit désactivé. Pour plus d’informations sur l’accès à l’état de l’économiseur de batterie dans votre application, consultez [**\_ \_ État**](/windows/desktop/api/winbase/ns-winbase-system_power_status)de l’alimentation du système. Pour obtenir des informations générales sur l’économiseur de batterie, consultez [économiseur de batterie (dans les instructions relatives aux composants matériels)](/windows-hardware/design/component-guidelines/battery-saver).

-   pour des raisons de sécurité, un utilisateur non-administrateur ne peut pas afficher ni gérer un Windows Planificateur de tâches tâche qui a été créée par un autre utilisateur.

## <a name="windows-8"></a>Windows 8

Les modifications Planificateur de tâches 2,0 suivantes sont introduites dans Windows 8 :

-   Prise en charge de PowerShell : les utilisateurs peuvent gérer (créer, supprimer, modifier, démarrer explicitement, arrêter, etc.) Windows Planificateur de tâches des tâches à l’aide du module PowerShell ScheduledTasks.
-   Mots de passe managés : les administrateurs peuvent utiliser les comptes de mots de passe gérés Active Directory en tant que principaux de tâche. Ces tâches ne nécessitent plus une stratégie de réinitialisation de mot de passe appliquée.
-   Modifications de l’API : a introduit deux nouveaux paramètres de tâche avec l’interface [**ITaskSettings3**](/windows/desktop/api/taskschd/nn-taskschd-itasksettings3) .
    -   [**MaintenanceSettings**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_maintenancesettings): les tâches qui utilisent ces paramètres sont traitées comme un nouveau type de tâches planifiées qui sont appelées pendant la durée de maintenance automatique du système d’exploitation, en fonction de la périodicité et de l’échéance spécifiées.
    -   [**Volatile**](/windows/desktop/api/Taskschd/nf-taskschd-itasksettings3-get_volatile): les tâches qui sont configurées pour être volatiles sont toujours désactivées sur un démarrage du système d’exploitation et doivent être explicitement réactivées quand cela est nécessaire. Les tâches volatiles sont utilisées par les clusters de basculement pour s’assurer qu’une seule instance de tâche est planifiée sur un cluster à la fois.
-   Le moteur de planification unifiée prend désormais en charge les fonctionnalités suivantes :
    -   Type d’ouverture de session S4U, via l’élément [**LogonType**](taskschedulerschema-logontype-principaltype-element.md) .
    -   Valeurs de requête XPath pour les déclencheurs d’événements, via l’élément [**ValueQueries**](taskschedulerschema-valuequeries-eventtriggertype-element.md) .
    -   N’autorisez pas l’arrêt forcé de la tâche, via l’élément [**AllowHardTerminate**](taskschedulerschema-allowhardterminate-settingstype-element.md) .
-   Fonctionnalités dépréciées dans cette version
    -   Action : [**sendEmail**](taskschedulerschema-sendemail-actiongroup-element.md) (vous pouvez utiliser [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) avec [Windows PowerShell](https://technet.microsoft.com/library/bb978526.aspx)l’applet de commande [Send-MailMessage](/powershell/module/microsoft.powershell.utility/send-mailmessage?view=powershell-7&preserve-view=true) comme solution de contournement).
    -   Action : [**showMessage**](taskschedulerschema-showmessage-actiongroup-element.md).
    -   Utilitaire AT.exe cmdline

## <a name="windows-7"></a>Windows 7

les modifications suivantes Planificateur de tâches 2,0 sont introduites dans Windows 7 :

-   Utilisation du moteur de planification unifié fourni par le système d’exploitation sous-jacent.
-   Possibilité de rejeter les tâches de démarrage dans les sessions d’applications à distance intégrées (RAIL).
-   Renforcement de la sécurité des tâches (pour les tâches qui s’exécutent en tant que « SERVICE réseau » ou « SERVICE LOCAL » uniquement) :

    -   Possibilité d’assigner un type d’identificateur de sécurité (SID) de jeton de processus (par exemple, sans restriction ou aucune) à une tâche.
    -   Autorisez les développeurs de tâches à demander le jeu exact de privilèges requis par leur tâche.

-   Modifications de l’API :

    -   Prise en charge du renforcement de la sécurité des tâches : la nouvelle fonctionnalité de renforcement de la sécurité des tâches est introduite avec une nouvelle interface IPrincipal2.
    -   A introduit deux nouveaux paramètres de tâche avec la nouvelle interface ITaskSettings2.

        -   DisallowStartOnRemoteAppSession : le nouveau paramètre DisallowStartOnRemoteAppSession peut rejeter le démarrage d’une tâche si elle est déclenchée dans des sessions [intégrées (rail) intégrées à des applications distantes](/openspecs/windows_protocols/MS-WINPROTLP/df36f95e-6a6b-48d6-a3ae-35a17674f546) .
        -   UseUnifiedSchedulingEngine : l’utilisation du paramètre UseUnifiedSchedulingEngine fournit un comportement cohésif pour Windows les tâches et les Services, car elle est gérée de façon uniforme par un moteur de planification commun à l’ensemble du système. Bien qu’il soit recommandé d’utiliser un moteur unifié, il ne prend pas en charge certaines fonctionnalités de Planificateur de tâches. Si la combinaison de propriétés n’autorise pas l’exécution de la tâche sous un moteur unifié, son enregistrement est rejeté.
        -   Les fonctionnalités de tâche qui ne sont pas prises en charge par le moteur de planification unifié sont les suivantes :

            -   Types d’ouverture de session :

                -   [\_ \_ \_ jeton \_ ou \_ mot de passe interactif de connexion à la tâche](./taskschedulerschema-logontype-principaltype-element.md)

            -   Stratégie de plusieurs instances :

                -   [**les instances de tâche ne sont pas \_ \_ \_ existantes**](taskschedulerschema-multipleinstancespolicy-settingstype-element.md)

            -   Actions :

                -   [Envoi d’e-mail](./taskschedulerschema-sendemail-actiongroup-element.md)
                -   [Afficher un message](./taskschedulerschema-showmessage-actiongroup-element.md)

            -   Paramètres :

                -   [Paramètres réseau de la tâche](./taskschedulerschema-networksettings-settingstype-element.md)
                -   [Ne pas autoriser l’arrêt forcé des tâches](./taskschedulerschema-allowhardterminate-settingstype-element.md)

            -   Déclencheurs :

                -   [Limite de la durée d’exécution du déclencheur](./taskschedulerschema-executiontimelimit-triggerbasetype-element.md)
                -   [Modèles de répétition pour les déclencheurs de calendrier]( ./taskschedulerschema-repetition-triggerbasetype-element.md)
                -   [Valeurs de requête XPath pour les déclencheurs d’événements]( ./taskschedulerschema-valuequeries-eventtriggertype-element.md)
                -   Types de déclencheurs [de jour de semaine](./taskschedulerschema-schedulebymonthdayofweek-calendartriggertype-element.md) [mensuels et](./taskschedulerschema-schedulebymonth-calendartriggertype-element.md) mensuels

## <a name="windows-vista"></a>Windows Vista

l’API Planificateur de tâches 2,0 doit être utilisée pour développer des applications qui utilisent le service Planificateur de tâches sur Windows Vista. Pour plus d’informations, consultez [Planificateur de tâches référence](task-scheduler-reference.md) et [utilisation du planificateur de tâches](using-the-task-scheduler.md).

## <a name="windows-2000-windows-xp-and-windows-server-2003"></a>Windows 2000, Windows XP et Windows Server 2003

L’API Planificateur de tâches 2,0 n’est pas disponible. Utilisez Planificateur de tâches 1,0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Planificateur de tâches](task-scheduler-start-page.md)
</dt> <dt>

[À propos de l’Planificateur de tâches](about-the-task-scheduler.md)
</dt> </dl>

 

 
