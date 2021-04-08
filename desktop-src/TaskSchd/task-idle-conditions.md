---
title: Conditions d’inactivité de la tâche
description: Une tâche peut être gérée de plusieurs façons lorsque l’ordinateur entre dans un état d’inactivité. Cela comprend la définition d’un déclencheur inactif ou la définition des conditions d’inactivité pour le démarrage de la tâche.
ms.assetid: 1e480681-b77a-48fe-a732-dd1591eaa08d
keywords:
- conditions d’inactivité Planificateur de tâches
- conditions d’inactivité Planificateur de tâches, discussion
- création de déclencheurs inactifs Planificateur de tâches
- déclencheurs inactifs Planificateur de tâches
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 501be9b73e3ec355b998697fb5e87c5163224b71
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/19/2020
ms.locfileid: "103734668"
---
# <a name="task-idle-conditions"></a>Conditions d’inactivité de la tâche

Une tâche peut être gérée de plusieurs façons lorsque l’ordinateur entre dans un état d’inactivité. Cela comprend la définition d’un déclencheur inactif ou la définition des conditions d’inactivité pour le démarrage de la tâche.

## <a name="detecting-the-idle-state"></a>Détection de l’état inactif

Dans Windows 7, le Planificateur de tâches vérifie que l’ordinateur est en état d’inactivité toutes les 15 minutes. Planificateur de tâches recherche un état inactif à l’aide de deux critères : absence de l’utilisateur et consommation de ressources insuffisante. L’utilisateur est considéré comme absent s’il n’y a pas d’entrée de clavier ou de souris pendant cette période. L’ordinateur est considéré comme inactif si tous les processeurs et tous les disques étaient inactifs pendant plus de 90% du dernier intervalle de détection. (Une exception serait pour n’importe quelle application de type de présentation qui définit les ES \_ AFFICHER l' \_ indicateur obligatoire. Cet indicateur force la planification des tâches à ne pas considérer le système comme étant inactif, quelle que soit l’activité de l’utilisateur ou la consommation des ressources.)

Dans Windows 7, Planificateur de tâches considère qu’un processeur est inactif même lorsque les threads de faible priorité (priorité de thread < normale) s’exécutent.

Dans Windows 7, lorsque le Planificateur de tâches détecte que l’ordinateur est inactif, le service attend uniquement l’entrée utilisateur pour marquer la fin de l’état inactif.

Dans Windows 8, Planificateur de tâches effectue les mêmes vérifications générales d’absence et de consommation des ressources. Toutefois, Planificateur de tâches s’appuie sur le sous-système d’alimentation du système d’exploitation pour détecter la présence de l’utilisateur. Par défaut, l’utilisateur est considéré comme absent après quatre minutes, sans clavier ou entrée de souris. L’heure de vérification de la consommation des ressources est raccourcie à 10 minutes lorsque l’utilisateur est présent. Lorsque l’utilisateur est absent, la durée de la vérification est réduite à 30 secondes. Planificateur de tâches effectue des vérifications de la consommation des ressources supplémentaires pour les événements suivants :

-   État de présence de l’utilisateur modifié
-   Source d’alimentation AC/DC modifiée
-   Niveau de batterie modifié (uniquement sur les batteries)

Lorsque l’un des événements ci-dessus se produit, Planificateur de tâches teste l’ordinateur en cas d’inactivité depuis la dernière heure de vérification. En pratique, cela signifie que Planificateur de tâches pouvez déclarer le système comme inactif immédiatement après la détection de l’absence de l’utilisateur, si les autres conditions ont été remplies depuis la dernière heure de vérification.

Dans Windows 8, les seuils d’UC et d’e/s sont définis sur 80%.

Lors de la détection de l’état inactif dans Windows 8 Server, Planificateur de tâches ne prend pas en compte la présence ou l’absence d’un utilisateur. Pour marquer la fin de l’état inactif, Planificateur de tâches révise la consommation des ressources une fois en 90 minutes.

## <a name="defining-an-idle-trigger"></a>Définition d’un déclencheur inactif

Une tâche peut être démarrée lorsque l’ordinateur passe à l’état inactif en définissant un déclencheur inactif.

Un déclencheur inactif déclenche une action de tâche uniquement si l’ordinateur entre dans un état d’inactivité après la limite de démarrage du déclencheur.

Une application peut définir un déclencheur inactif à l’aide de l’interface [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

En cas de lecture ou d’écriture de code XML, le déclencheur inactif est spécifié par l’élément [**IdleTrigger**](taskschedulerschema-idletrigger-triggergroup-element.md) du schéma planificateur de tâches.

## <a name="task-settings-for-idle-conditions"></a>Paramètres de tâche pour les conditions d’inactivité

Les paramètres de tâche peuvent être utilisés pour définir la manière dont le Planificateur de tâches gère la tâche lorsque l’ordinateur entre dans un état d’inactivité.

Les illustrations suivantes fournissent trois chronologies possibles qui montrent comment ces différentes conditions d’inactivité sont liées les unes aux autres. N’oubliez pas que les illustrations démarrent lorsque le déclencheur de tâche est activé ou lorsque la tâche est démarrée à la demande (sans demander à [Ignorer les contraintes de tâche existantes](/windows/win32/api/taskschd/ne-taskschd-task_run_flags)).

> [!NOTE]
> Les paramètres *Duration* et *WaitTimeout* sont déconseillés. Elles sont toujours présentes dans l’interface utilisateur Planificateur de tâches et leurs méthodes d’interface peuvent toujours retourner des valeurs valides, mais elles ne sont plus utilisées.

![chronologie des conditions d’inactivité](images/idle-conditions2.png)

La liste suivante décrit les conditions d’inactivité.
- Démarrage inactif : heure à laquelle l’ordinateur passe à l’état inactif.
- Idle end : heure à laquelle l’ordinateur passe de l’état inactif. N’oubliez pas que la durée d’inactivité de l’ordinateur est indépendante de la durée d’inactivité décrite précédemment.

L’attente et la durée d’inactivité sont dépréciées.
- Attente d’inactivité : durée pendant laquelle l’Planificateur de tâches attend qu’un état inactif se produise après l’activation d’un déclencheur de tâche ou après le démarrage de la tâche à la demande.
- Durée d’inactivité : durée pendant laquelle vous souhaitez que l’ordinateur soit inactif avant de démarrer la tâche.

Par exemple, si une tâche est définie sur Démarrer uniquement si l’ordinateur est inactif pendant 30 minutes et que la tâche attend que l’ordinateur soit inactif pendant 10 minutes, la tâche est lancée dans les 5 minutes seulement si l’ordinateur a été inactif pendant 25 minutes avant l’activation du déclencheur. La tâche ne démarrera pas si l’ordinateur passe à l’état inactif 5 minutes après l’activation du déclencheur.

Par défaut, une propriété [**DisallowStartIfOnBatteries**](/windows/desktop/api/taskschd/nf-taskschd-itasksettings-get_disallowstartifonbatteries) de la tâche a la valeur true, ce qui signifie que le service Planificateur de tâches n’exécutera pas les tâches qui sont déclenchées par un déclencheur inactif (ou un déclencheur avec des conditions d’inactivité) lorsqu’un ordinateur fonctionne sur batterie. Vous pouvez modifier ce comportement en affectant à la propriété **DisallowStartIfOnBatteries** la valeur false.

Si une tâche est déclenchée par un déclencheur inactif, la propriété [**WaitTimeout**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_waittimeout) de l’interface [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) ([**IdleSettings**](idlesettings.md) pour l’écriture de scripts) est ignorée.

Les applications peuvent contrôler les conditions d’inactivité en définissant les propriétés dans les interfaces [**IIdleSettings**](/windows/desktop/api/taskschd/nn-taskschd-iidlesettings) et [**IIdleTrigger**](/windows/win32/api/taskschd/nn-taskschd-iidletrigger) .

En cas de lecture ou d’écriture de code XML, ces conditions sont spécifiées dans l’élément [**Settings**](taskschedulerschema-settings-tasktype-element.md) du schéma planificateur de tâches.

## <a name="cycling-idle-condition"></a>Condition d’inactivité du cycle

Si l’ordinateur est dans un état inactif et qu’il est hors de l’état inactif, vous pouvez arrêter et redémarrer la tâche à l’aide des conditions d’inactivité suivantes. Pour terminer et redémarrer une tâche, les propriétés et les éléments doivent avoir la valeur true :

-   Pour mettre fin à la tâche lorsque la condition d’inactivité se termine, affectez la valeur true à la propriété [**StopOnIdleEnd**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_stoponidleend) ou à l’élément [**StopOnIdleEnd**](taskschedulerschema-terminateonidleend-idlesettingstype-element.md) .
-   Pour redémarrer la tâche lorsque l’ordinateur est de nouveau recycle dans la condition d’inactivité, définissez la propriété [**RestartOnIdle**](/windows/desktop/api/taskschd/nf-taskschd-iidlesettings-get_restartonidle) ou l’élément [**RestartOnIdle**](taskschedulerschema-restartonidle-idlesettingstype-element.md) sur true.
