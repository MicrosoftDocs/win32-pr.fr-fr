---
title: Maintenance automatique (Planificateur de tâches)
description: L’activité de maintenance fait référence à une application ou à un processus qui permet de maintenir l’intégrité et les performances d’un PC Windows.
ms.assetid: 1D38341B-15AA-422F-AED1-647FCDE69E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 456383eeb75c3b29bf575357d4b17d5f8a66234b
ms.sourcegitcommit: 857e701bbd35004661bb047e1f24622af9ff1dd7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/19/2020
ms.locfileid: "104383160"
---
# <a name="automatic-maintenance"></a>Maintenance automatique

L’activité de maintenance fait référence à une application ou à un processus qui permet de maintenir l’intégrité et les performances d’un PC Windows. La maintenance implique la mise à jour du système d’exploitation Windows et des applications, la vérification de la sécurité et l’exécution d’analyses de programmes malveillants. La gestion automatique de Windows (WAM) est un ensemble d’améliorations apportées à l’API Planificateur de tâches que vous pouvez utiliser pour lier vos applications à la planification de la maintenance de Windows. En particulier, WAM vous permet d’ajouter des activités qui nécessitent une planification régulière, mais qui n’ont pas d’exigences de temps exactes. Au lieu de cela, WAM s’appuie sur le système d’exploitation pour choisir l’heure appropriée pour activer la tâche tout au long de la journée. Le système choisit ces heures en fonction de l’impact minimal sur l’utilisateur, des performances du PC et de l’efficacité énergétique.

## <a name="how-scheduled-maintenance-works"></a>Fonctionnement de la maintenance planifiée

Planificateur de tâches tâches de maintenance sont des tâches opportunistes qui s’exécutent lorsque l’ordinateur est inactif et à l’alimentation secteur. L’un des principaux objectifs des tâches de maintenance est de réduire l’impact sur le PC en planifiant la maintenance uniquement lorsque le PC est branché à l’alimentation secteur et à l’inactivité (autrement dit, lorsque vous n’utilisez pas, ou que vous n’avez pas quitté la machine). L’idée de la maintenance aujourd’hui est que la machine fonctionne avec le moins de perturbations pour l’utilisateur. Par conséquent, l’ancienne heure de maintenance (nous en parlerons plus en détail dans la section **activation automatique de la maintenance &mdash; quotidienne** plus loin dans cette rubrique) a été améliorée afin de tirer parti de ces périodes inactives. Bien que l’heure de la maintenance puisse encore être exploitée, l’exécution de la maintenance opportuniste est mieux adaptée à l’intégrité du système.

Votre tâche peut être dépassée si un ordinateur ne passe pas beaucoup de temps en mode inactif et en alimentation secteur. Assurez-vous que votre scénario fournira toujours de la valeur à l’utilisateur, même s’il est retardé. Si l’utilisateur utilise l’ordinateur activement, le système diffère la maintenance jusqu’à une date ultérieure. Le système interrompt également toute tâche de maintenance en cours d’exécution si l’utilisateur revient à utiliser le PC.

Le système redémarre une tâche de maintenance suspendue pendant la période d’inactivité suivante ; Toutefois, le système n’interrompt aucune tâche marquée comme critique. Au lieu de cela, le système permet à une tâche critique de se terminer, quelle que soit l’action de l’utilisateur.

En raison de la nature de la planification, certaines tâches planifiées peuvent ne pas se terminer : peut-être que le nombre d’événements planifiés est trop important pour la fenêtre de maintenance de 1 heure, ou peut-être que l’ordinateur n’a pas été mis sous tension. Dans ce cas, vous pouvez définir une tâche avec une échéance. Une échéance est définie comme une période récurrente dans laquelle le système doit exécuter correctement la tâche au moins une fois.

Si une tâche n’a pas de délai d’expiration, le planificateur de maintenance continue à tenter d’exécuter la tâche pendant la fenêtre de maintenance. En outre, le planificateur ne se limite pas à la limite de 1 heure normale. Au lieu de cela, le planificateur prolonge la durée de la fenêtre de maintenance afin de terminer la tâche retardée.

Une fois que le système a terminé la tâche (même avec un code d’erreur d’échec), la tentative est considérée comme réussie. Après une tentative réussie, le planificateur se réinitialise à la planification de maintenance normale et tentera la tâche au cours de la période suivante.

## <a name="automatic-maintenancemdashdaily-wakeup"></a>Réveil quotidien de maintenance automatique &mdash;

Sur Windows 7, une tâche de maintenance s’exécute exclusivement pendant l’heure de la *maintenance*, avec la valeur par défaut 3 AM et configurable via stratégie de groupe. L’ordinateur sort de veille, exécute des tâches de maintenance et revient en mode veille. Cette session quotidienne était limitée à une durée maximale de 1 heure par tentative. Cela permet au système d’effectuer une maintenance quotidienne, à partir de 3 heures par défaut. Notez que l’utilisateur peut replanifier l’heure à laquelle la maintenance est déclenchée en configurant ces paramètres.

Avec l’avènement des ordinateurs portables et la concentration sur la durée de vie de la batterie, les machines ne sont plus configurées pour autoriser la réveil S3 dans la plupart des cas, et généralement Doze-to-S4 (veille prolongée) dès que possible, pour économiser la batterie. En réponse à ces modifications, Planificateur de tâches (> Win7) exécute des tâches de maintenance chaque fois qu’elles sont dues, et la machine est inactive et à l’alimentation secteur.

Ce paramètre peut être configuré dans le panneau de configuration.

Ouvrez **le panneau**  >  **de configuration système et sécurité sécurité**  >  **et** maintenance  >  **automatique**.

Par conséquent, en fonction de la façon dont vos machines et vos tâches sont configurées, le comportement de réveil quotidien peut ne pas se produire aujourd’hui comme prévu en raison de cette nouvelle configuration. Vous pouvez d’abord déterminer si votre ordinateur est en mesure de prendre en charge S3 ou le mode CS (veille connectée).
Pour ce faire, ouvrez une invite Power Shell avec élévation de privilèges et exécutez la commande suivante.

```console
powercfg /a
```

Heure de la maintenance, si la machine est configurée correctement, fonctionne toujours, mais si ce n’est pas le cas,
  - Vérifiez les paramètres de mise en éveil de vos paramètres BIOS. 
  - Vérifiez si l’option autoriser la minuterie de réveil est activée dans les options d’alimentation.
    Accédez à **panneau** de  >  **configuration matériel et sons**  >  **options d’alimentation**  >  **modifier les paramètres de plan** modifier les paramètres  >  **d’alimentation avancés** > cliquez sur mettre en **veille**  >  **autoriser le minuteur de réveil**.
  - Vérifiez si votre tâche planifiée est configurée comme suit.
      * MaintenanceSettings : la tâche doit être configurée avec period, échéance.
      * Activé : la tâche doit être activée.
      * WakeToRun : la tâche doit être autorisée à mettre l’ordinateur en éveil.
  - Pour la planification des éveils à partir de CS, la machine doit être compatible alimentation AOAC.
  - Pour la planification des éveils sur les ordinateurs S3,
      * Vérifiez si la machine a été mise en S3 sur secteur.
      * L’éveil par appel réseau doit être **activé** dans stratégie de groupe pour la maintenance.
 
La mise en veille connectée est l’état du système qu’un système alimentation AOAC peut entrer.

Consultez les différences entre la mise en veille moderne et S3 dans la rubrique [mise en veille moderne et S3](/windows-hardware/design/device-experiences/modern-standby-vs-s3).

## <a name="defining-an-automatic-maintenance-task"></a>Définition d’une tâche de maintenance automatique

Vous pouvez convertir n’importe quelle Planificateur de tâches tâche en tâche de maintenance. Pour ce faire, vous devez vérifier que votre application peut être suspendue. Ensuite, vous devez étendre la définition de tâche avec les nouveaux éléments [**MaintenanceSettings**](taskschedulerschema-maintenancesettings-maintenancesettingstype-element.md) et [**AllowStartOnDemand**](taskschedulerschema-allowstartondemand-settingstype-element.md) .

La principale préoccupation de la création d’une tâche de maintenance est de s’assurer que le système peut suspendre et redémarrer la tâche. Le système suspendra peut-être une tâche de maintenance plusieurs fois. par conséquent, vous devez vous assurer que votre application est en mesure d’enregistrer son propre État, puis de la reprendre à une heure arbitraire. Cela permet de s’assurer que le système n’exécute pas la même partie de votre tâche de manière répétée.

Une fois que vous avez vérifié que votre application peut être interrompue et reprise correctement, vous pouvez utiliser les éléments **MaintenanceSettings** et **AllowStartOnDemand** pour définir la planification. **MaintenanceSettings** est défini en fonction de la période, de l’échéance et de l’exclusivité.

-   La **période** est obligatoire et définit la fréquence à laquelle la tâche doit se produire. En règle générale, cela est défini en termes de cycle de plusieurs jours, par exemple « une fois tous les 5 jours ». Un point doit être au moins d’un jour, ce qui signifie que vous ne pouvez pas planifier une tâche qui se produit plusieurs fois par jour.
-   L' **échéance** est facultative et définit la durée pendant laquelle le planificateur peut échouer pour terminer la tâche avant de notifier l’utilisateur ou d’effectuer une maintenance d’urgence. L’échéance doit être supérieure à la période, ce qui signifie que le système doit avoir la possibilité d’essayer la tâche au moins une fois avant de notifier l’utilisateur.
-   En outre, une tâche de maintenance peut éventuellement être définie comme *exclusive*. Une tâche exclusive s’exécute séparément des autres tâches de maintenance. En règle générale, une tâche exclusive est une tâche qui utilise une grande quantité de ressources, par exemple un grand nombre de temps processeur ou un accès exclusif à une base de données. Le système effectue toutes les tâches de maintenance non exclusives avant de démarrer une tâche exclusive. Par conséquent, vous devez déclarer une tâche comme exclusive uniquement lorsque cela est nécessaire.

En revanche, **AllowStartOnDemand** indique simplement que le système ou l’utilisateur peut démarrer la tâche à tout moment. Cela permet au système de démarrer la tâche pendant une maintenance régulière. Dans le cas contraire, vous devez définir un déclencheur unique pour la tâche.
