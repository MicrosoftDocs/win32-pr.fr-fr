---
title: Comportement du pool système
description: Discussion sur les actions effectuées par le pool système lorsque des notifications d’événements sont envoyées et lorsqu’aucune opération biométrique n’est en attente.
ms.assetid: cc1f8ffa-ce69-48ff-8509-81d85807d12a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 923cfff4b36bd14d100ce1f73db455be5261d75dc2c5be1eddc8f9d6af87fce0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911592"
---
# <a name="system-pool-behavior"></a>Comportement du pool système

La discussion suivante met en évidence les actions effectuées par le pool système lorsque les notifications d’événements sont envoyées et qu’aucune opération biométrique n’est en attente.

## <a name="event-dispatching"></a>Distribution d’événements

Lorsqu’une unité biométrique génère un avis d’événement, le pool système utilise un filtre en cascade pour distribuer l’avis et lui attribuer l’un des niveaux de priorité suivants :

-   La haute priorité est assignée aux demandes de correspondance et d’inscription explicites générées par les clients.
-   La priorité moyenne est assignée à des événements de correspondance ou d’inscription inattendus ou non revendiqués.
-   La priorité basse est assignée aux événements de navigation.

Les événements de capture sont fournis dans l’ordre suivant :

-   Si la fenêtre active active attend une opération de mise en correspondance ou d’inscription, l’exemple est traité et envoyé au client qui possède la fenêtre active active.
-   si l’événement de capture n’est pas réclamé par la fenêtre active active et qu’un gestionnaire d’événements non réclamés a été inscrit auprès du service de biométrique Windows, l’événement de capture est envoyé à ce gestionnaire.
-   Si l’événement reste non réclamé, il est ignoré.

si l’événement est un événement de navigation et qu’un gestionnaire d’événements de navigation a été inscrit auprès du service de biométrie Windows, l’événement de capture est envoyé à ce gestionnaire. S’il n’existe aucun gestionnaire d’événements, l’événement est ignoré.

## <a name="idle-mode"></a>Mode inactif

Si aucun client n’attend la fin des demandes de correspondance explicite ou d’inscription, le pool système détermine s’il faut générer automatiquement des demandes de capture répétées et envoyer l’avis d’événement résultant au gestionnaire d’événements non réclamés ou attendre les événements de navigation et les envoyer au gestionnaire d’événements de navigation.

si un gestionnaire d’événements non réclamé a été inscrit auprès du service de biométrique Windows, le pool système effectue les actions suivantes :

-   Le mode de navigation du capteur est désactivé.
-   Les opérations non réclamées sont envoyées au gestionnaire d’événements indépendamment du focus de la fenêtre.
-   S’il n’y a aucune demande en suspens pour une opération biométrique, une capture automatique est effectuée.

si un gestionnaire de navigation a été inscrit auprès du service de biométrique Windows, le pool système effectue les opérations suivantes :

-   Les unités biométriques du pool système sont placées dans un état de navigation si aucune opération biométrique n’est en attente.
-   Les événements de navigation sont désactivés si une notification d’événement de correspondance ou d’inscription est envoyée par un client.
-   Si un gestionnaire d’événements non réclamés a été enregistré, les événements de navigation sont désactivés.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Pool de capteurs privés](private-sensor-pool.md)
</dt> <dt>

[Pools de capteurs](sensor-pools.md)
</dt> <dt>

[Pool de capteurs système](system-sensor-pool.md)
</dt> </dl>

 

 




