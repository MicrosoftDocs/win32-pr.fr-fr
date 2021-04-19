---
description: Votre application peut restaurer un ordinateur qui se trouve dans un état de veille à l’état de fonctionnement à l’aide d’un minuteur planifié ou d’un événement d’appareil.
ms.assetid: b7326b09-0829-4e76-80d0-e4ecdf7f556e
title: Événements de mise en éveil du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f13332305ef023d932f2912f7299aa12cd402733
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531937"
---
# <a name="system-wake-up-events"></a>Événements de mise en éveil du système

Les informations suivantes s’appliquent aux éveils de [veille (S3) et de mise en veille prolongée (S4)](/windows-hardware/drivers/kernel/system-sleeping-states). Pour les réveils à partir de la mise en veille moderne (mode faible consommation S0), reportez-vous aux [transitions de inactif à actif](/windows-hardware/design/device-experiences/transition-from-idle-to-active).

Votre application peut restaurer un ordinateur qui se trouve dans un état de veille à l’état de fonctionnement à l’aide d’un minuteur planifié ou d’un événement d’appareil. C’est ce qu’on appelle un *événement de mise en éveil*. Utilisez un [objet de minuteur](/windows/desktop/Sync/waitable-timer-objects) qui peut être utilisé pour spécifier l’heure à laquelle le système doit sortir de veille. Pour créer l’objet, utilisez la fonction [**CreateWaitableTimer**](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) . Pour définir le minuteur, utilisez la fonction [**SetWaitableTimer**](/windows/desktop/api/synchapi/nf-synchapi-setwaitabletimer) . Le paramètre *pDueTime* spécifie à quel moment la minuterie sera signalée. Pour spécifier que le système doit sortir de veille quand le minuteur est signalé, affectez la valeur **true** au paramètre *fResume* .

Lorsque le système sort automatiquement du mode veille en raison d’un événement (autre que le commutateur d’alimentation ou l’activité utilisateur), le système définit automatiquement un délai d’inactivité sans assistance à au moins 2 minutes. Ce minuteur donne aux applications suffisamment de temps pour appeler la fonction [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) pour indiquer qu’elles sont occupées. Cette fois, permet au système de revenir rapidement à l’état de veille une fois que l’ordinateur n’est plus nécessaire. Les critères suivants déterminent si le système revient à l’état de veille :

-   Si le système sort de veille automatiquement (c’est-à-dire qu’aucune activité utilisateur n’est présente), il s’arrête dès que le minuteur inactif sans assistance expire, en supposant qu’aucune application n’a appelé [**SetThreadExecutionState**](/windows/desktop/api/Winbase/nf-winbase-setthreadexecutionstate) pour indiquer que le système est requis.
-   Les réveils basés sur un appareil déclenchent la minuterie d’inactivité sans assistance par défaut, sauf si le pilote de périphérique indique la présence de l’utilisateur. Si le pilote indique la présence de l’utilisateur, la minuterie d’inactivité du système est utilisée.
-   Si le système sort de veille automatiquement, mais que l’utilisateur fournit une nouvelle entrée pendant que l’événement est géré, le système ne repasse pas automatiquement en mode veille en fonction de la minuterie d’inactivité en mode sans assistance. Au lieu de cela, le système revient en mode veille en fonction du minuteur d’inactivité du système.
-   Si le système sort de veille en raison de l’activité de l’utilisateur, le système ne repasse pas automatiquement en mode veille en fonction de la minuterie d’inactivité en mode sans assistance. Au lieu de cela, le système revient en mode veille en fonction du minuteur d’inactivité du système.

Lorsque le système sort automatiquement, il diffuse l’événement [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) à toutes les applications. Étant donné que l’utilisateur n’est pas présent, la plupart des applications ne doivent rien faire. Les applications de gestion des événements, telles que les serveurs de télécopie, doivent gérer leurs événements. Pour déterminer si le système est dans cet État, appelez la fonction [**IsSystemResumeAutomatic**](/windows/desktop/api/Winbase/nf-winbase-issystemresumeautomatic) . Lorsque le système sort automatiquement, l’affichage n’est pas automatiquement activé.

Si le système sort de veille en raison de l’activité de l’utilisateur, le système diffuse d’abord l’événement [PBT \_ APMRESUMEAUTOMATIC](pbt-apmresumeautomatic.md) suivi d’un événement [ \_ APMRESUMESUSPEND PBT](pbt-apmresumesuspend.md) . En outre, le système active l’affichage. Votre application doit rouvrir les fichiers qu’elle a fermés lorsque le système est passé en mode veille et se prépare à l’entrée utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> <dt>

[Critères de veille du système](system-sleep-criteria.md)
</dt> </dl>

 

 
