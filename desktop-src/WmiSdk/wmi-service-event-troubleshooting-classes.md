---
description: Les classes de dépannage des événements du service WMI sont générées par des événements au sein du service WMI, tels que la création d’un pool de threads.
ms.assetid: 1a1251c8-a2f7-47ac-9db1-d780d7d272f0
ms.tgt_platform: multiple
title: Classes de dépannage des événements du service WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99be30a6b2f0551cae4e0abe269da5341e34e1444eb1545ca96377a43b5415ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119502799"
---
# <a name="wmi-service-event-troubleshooting-classes"></a>Classes de dépannage des événements du service WMI

Les classes de dépannage des événements du service WMI sont générées par des événements au sein du service WMI, tels que la création d’un pool de threads.

Vous pouvez vous abonner aux notifications [**\_ WmiEssEvent msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent) de la classe de base abstraite pour obtenir tous les événements dérivés listés dans le tableau suivant.



|   Événement                                                                                        |   Description                                                                                             |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**\_WMIESSEVENT msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiessevent)                                   | classe parente pour tous les auto-événements du sous-système d’événement (ESS) Windows Management Instrumentation (WMI). |
| [**\_WMIREGISTERNOTIFICATIONEVENT msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmiregisternotificationevent) | Représente la création d’un récepteur d’événements pour la notification pour une requête d’événement.                       |
| [**\_WMICANCELNOTIFICATIONSINK msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmicancelnotificationsink)       | généré lorsqu’un récepteur d’événements est annulé.                                                           |
| [**\_WMITHREADPOOLEVENT msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolevent)                     | fournit une notification des événements de thread dans le sous-système d’événements WMI (ESS).                           |
| [**\_WMITHREADPOOLCREATED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpoolcreated)                 | Fournit une notification lorsqu’un thread est créé dans le sous-système d’événements WMI (ESS).                   |
| [**\_WMITHREADPOOLDELETED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmithreadpooldeleted)                 | Fournit une notification lorsqu’un thread est supprimé dans le sous-système d’événements WMI (ESS).                   |
| [**\_WMIFILTEREVENT msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterevent)                             | Classe parente pour tous les événements de filtre de consommateur d’événements permanents.                                        |
| [**\_WMIFILTERACTIVATED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilteractivated)                     | Définit la réussite de l’activation d’un filtre d’abonnement d’événement consommateur permanent.                |
| [**\_WMIFILTERDEACTIVATED msft**](/previous-versions/windows/desktop/wmisystemprov/msft-wmifilterdeactivated)                 | Définit la réussite de la désactivation d’un filtre d’abonnement consommateur permanent.                    |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes WMI](wmi-troubleshooting.md)
</dt> <dt>

Dépannage WMI
</dt> <dt>

[Événements d’analyse](monitoring-events.md)
</dt> <dt>

[Réception d’un événement WMI](receiving-a-wmi-event.md)
</dt> </dl>

 

 
