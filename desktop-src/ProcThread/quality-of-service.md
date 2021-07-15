---
description: La qualité de service indique les performances et l’efficacité énergétique d’un thread, ce qui peut influencer la planification des threads et la gestion de l’alimentation du processeur.
title: Qualité de service
ms.topic: article
ms.date: 07/09/2021
ms.openlocfilehash: c506e810bafad41e9a5f14112c1398b0d6fb3ffc
ms.sourcegitcommit: 2805e19a2738a408d3c5ab69a8d84ec92ca25e36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/14/2021
ms.locfileid: "113989790"
---
# <a name="quality-of-service"></a>Qualité de service

La qualité de service (QoS) associée à un thread est utilisée pour indiquer les performances souhaitées et l’efficacité énergétique. Chaque thread est affecté à un niveau de qualité de service (QoS). Alors que la priorité de planification reste la mesure principale par laquelle le système détermine le thread à planifier ensuite, la qualité de service peut influencer la sélection de base et la gestion de l’alimentation du processeur. Sur les plateformes avec des processeurs hétérogènes, la qualité de service d’un thread peut limiter la planification à un sous-ensemble de processeurs ou indiquer une préférence pour une classe particulière de processeur.

Les développeurs utilisent peut-être déjà d’autres installations pour contrôler le moment de leur exécution, par exemple lorsque l’utilisateur n’est pas présent, uniquement en secteur ou en charge, ou en fonction du niveau de la batterie. La qualité de service (QoS) fournit une fonctionnalité permettant d’influencer l’exécution. Cette fonctionnalité peut aider à améliorer l’efficacité du processeur et donc à accroître la durée de vie de la batterie. En outre, ce processus peut aider à réduire la consommation d’énergie de l’UC tout en fonctionnant sur une alimentation secteur pour réduire la sortie thermique, ce qui peut entraîner un bruit de ventilateur élevé ou même une limitation thermique.

## <a name="quality-of-service-levels"></a>Qualité des niveaux de service

Le système gère plusieurs niveaux de QoS, chacun avec des performances différenciées et une efficacité énergétique. Windows fournit des paramètres par défaut standard pour la planification et la gestion de l’alimentation du processeur pour chaque niveau de QoS. le réglage précis de chaque niveau de qualité de service pour la gestion de l’alimentation du processeur et la planification hétérogène peut être modifié par le biais de l’approvisionnement Windows. Pour plus d’informations sur l’optimisation et l’approvisionnement des performances, consultez Options de gestion de l' [alimentation du processeur](/windows-hardware/customize/power-settings/configure-processor-power-management-options).

| Niveau de QoS | Description|Performances et puissance | Libérer |
| --- | --- | --- | --- |
| Élevé | Applications avec fenêtre qui sont au premier plan et activées, ou audibles | Haute performance standard |1709 |
| Moyenne | Applications à fenêtres qui peuvent être visibles par l’utilisateur final, mais qui ne sont pas activées | Varie selon la plateforme, entre haut et bas | 1709 |
| Faible | Applications à fenêtres qui ne sont pas visibles ou audibles à l’utilisateur final | Sur batterie, sélectionne la fréquence et les planifications d’UC les plus efficaces pour les cœurs efficaces. | 1709 |
| Écologique | Applications qui balisent explicitement des processus avec [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) ou des threads avec [SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) | Sélectionne toujours la fréquence et les planifications d’UC les plus efficaces pour les cœurs efficaces | Windows 11 |
| Média | Threads explicitement balisés par le [service Planificateur de classes multimédias](/windows/desktop/procthread/multimedia-class-scheduler-service) pour indiquer la mise en mémoire tampon des lots multimédias | Fréquence UC réduite pour un traitement par lots efficace | 2004 |
| Échéance | Threads balisés explicitement par le [service Planificateur de classes multimédias](/windows/desktop/procthread/multimedia-class-scheduler-service) pour indiquer que les threads audio requièrent des performances pour respecter les échéances | Hautes performances pour respecter les délais de support | 2004 |

## <a name="quality-of-service-classification"></a>Classification de la qualité de service

Le tableau suivant indique les classifications de qualité de service prises en charge.

| Source | Description |
| --- | --- |
| Fondation multimédia | Le [service Planificateur de classes multimédias](/windows/desktop/procthread/multimedia-class-scheduler-service) hiérarchise les ressources du processeur pour les scénarios multimédias. Le service marque les threads spécifiques responsables du traitement multimédia à l’aide des niveaux de QoS Media et échéance pour fournir une efficacité énergétique tout en respectant les délais de performance.  |
| API | [SetProcessInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) permet aux développeurs de baliser explicitement un processus en tant que HighQoS ou EcoQoS en basculant la `PROCESS_POWER_THROTTLING_EXECUTION_SPEED` fonctionnalité dans **ProcessPowerThrottling**.</br>[SetThreadInformation](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-setprocessinformation) permet aux développeurs de baliser explicitement un thread en tant que HighQoS ou EcoQoS en basculant la `THREAD_POWER_THROTTLING_EXECUTION_SPEED` fonctionnalité dans **ThreadPowerThrottling** .  |
| Seraient | Les processus qui sont déterminés à la lecture de l’audio sont HighQoS. |
| Visible | Les processus qui possèdent directement une fenêtre (ou qui sont des descendants de processus possédant des fenêtres) se voient attribuer un niveau de qualité de service en fonction de leur visibilité et de leur état de Focus :</br></br><table><tr><th>État de la fenêtre</th><th>Qualité de service</th></tr><tr><td>Dans le focus</td><td>Élevé</td></tr><tr><td>Visible</td><td>Moyenne</td></tr><tr><td>Réduit ou entièrement bloqués</td><td>Faible</td></tr></table> |
| Heuristique | Les threads qui ne sont pas classés par les sources ci-dessus reçoivent automatiquement un niveau de QoS par le système. Ces heuristiques incluent (mais ne sont pas limitées à) la priorité des threads, où les threads qui s’exécutent avec une priorité de thread réduite peuvent impliquer un niveau de QoS inférieur. |
