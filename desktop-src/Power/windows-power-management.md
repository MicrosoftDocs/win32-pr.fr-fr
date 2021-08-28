---
description: Windows la gestion de l’alimentation permet aux utilisateurs d’accéder instantanément aux ordinateurs à la touche d’un bouton ou d’une touche.
ms.assetid: 388dadb9-b722-43f8-ab2b-a9bbd96600a3
title: Windows Gestion de l’alimentation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7335b521b22b762468d2b542ea3c4fdbfcacb798860d4997f4a512d8135bcf46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032719"
---
# <a name="windows-power-management"></a>Windows Gestion de l’alimentation

Windows la gestion de l’alimentation permet aux utilisateurs d’accéder instantanément aux ordinateurs à la touche d’un bouton ou d’une touche. Il garantit également que tous les éléments du système (applications, périphériques et interface utilisateur) peuvent tirer parti des améliorations apportées à la technologie et aux fonctionnalités de gestion de l’alimentation.

le système d’exploitation Windows utilise le matériel de gestion de l’alimentation pour mettre l’ordinateur dans un *état de veille* faible au lieu de s’arrêter complètement, afin que le système puisse reprendre rapidement son travail. Le système d’exploitation passe automatiquement en état de veille lorsque l’ordinateur est inactif ou lorsque l’utilisateur appuie sur un bouton pour indiquer que la session de travail active est terminée. Pour l’utilisateur, le système semble être désactivé. En état de veille, le processeur de l’ordinateur n’exécute pas de code et aucun travail n’est effectué pour l’utilisateur. Toutefois, les événements du système à partir des périphériques matériels et de l’horloge en temps réel peuvent être activés pour forcer le système à quitter l’état de veille (c’est-à-dire « réveiller ») et à revenir rapidement à l’état de travail.

Lorsque l’ordinateur est en état de veille, le matériel de l’ordinateur, le système et les applications qui s’exécutent sur l’ordinateur doivent être en capacité de répondre immédiatement au bouton d’alimentation, aux événements de communication et à d’autres actions. Si toutes les applications gèrent les transitions d’état d’alimentation normalement, l’utilisateur perçoit un système plus élégant et plus intégré. Les applications qui ne gèrent pas ces transitions peuvent échouer lorsque l’alimentation est désactivée puis activée, en raison d’une perte de données ou d’une dépendance sur un appareil qui a peut-être été supprimé.

voici les avantages de la gestion de l’alimentation Windows :

-   Élimine les délais de démarrage et d’arrêt. L’ordinateur n’a pas besoin d’effectuer un démarrage système complet en quittant l’état de veille ou un arrêt complet du système lorsque l’utilisateur démarre l’état de veille.
-   Permet aux tâches automatisées de s’exécuter pendant que l’ordinateur est en état de veille. Le Planificateur de tâches permet à l’utilisateur de planifier l’exécution des applications. les événements planifiés peuvent s’exécuter même lorsque le système est en état de veille. Le Planificateur de tâches utilise des [minuteries waitables](/windows/desktop/Sync/waitable-timer-objects) pour s’assurer que le système est prêt lorsque l’application est planifiée pour s’exécuter. Pour plus d’informations, consultez le fichier d’aide inclus avec l’Planificateur de tâches.
-   Active la gestion de l’alimentation par appareil. Les appareils qui ne sont pas en cours d’utilisation peuvent économiser de l’énergie en entrant l’état de veille.
-   Améliore l’efficacité de l’alimentation. L’efficacité de l’alimentation est particulièrement importante sur les ordinateurs portables. La réduction de la consommation d’énergie du système se traduit directement par des coûts d’énergie réduits et une durée de vie de batterie plus longue.
-   Permet aux utilisateurs de créer des [modes d’alimentation](power-schemes.md), de définir des alarmes et de spécifier des options de batterie par le biais de l’application options d’alimentation dans le panneau de configuration. Le système d’exploitation coordonne toutes les activités de gestion de l’alimentation, en fonction des paramètres de stratégie d’alimentation. Pour plus d’informations, consultez le fichier d’aide inclus avec l’application options d’alimentation.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la gestion de l’alimentation](about-power-management.md)
</dt> <dt>

[Planificateur de tâches](/windows/desktop/TaskSchd/task-scheduler-start-page)
</dt> </dl>

 

 
