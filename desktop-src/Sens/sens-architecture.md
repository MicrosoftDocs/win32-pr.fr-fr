---
description: Le service de notification d’événements système fonctionne avec le système d’événements COM+.
ms.assetid: c51d1f61-6087-4480-b989-31241829781b
title: Architecture SENSe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e32976a716ab0ba5651ce6605fe524d639820696
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520106"
---
# <a name="sens-architecture"></a>Architecture SENSe

Le service de notification d’événements système fonctionne avec le système d’événements COM+. SENS est un éditeur d’événements pour les classes d’événements qu’il surveille : le réseau, l’ouverture de session et les événements d’alimentation/batterie. L’application recevant une notification est appelée abonné aux événements.

Lorsqu’une application s’abonne pour recevoir des notifications, elle peut également spécifier des filtres associés aux événements souscrits. Les événements SENS et COM+ utilisent les filtres pour déterminer plus en détail quand l’application doit être notifiée.

Les notifications étant asynchrones, l’application qui reçoit la notification n’a pas besoin d’être active lorsque la notification est envoyée. Lorsqu’une application s’abonne pour recevoir des notifications, elle peut spécifier si elle doit être activée lorsque l’événement se produit ou être notifié plus tard quand elle est active.

L’abonnement peut être temporaire et valide uniquement jusqu’à ce que l’application cesse de s’exécuter, ou il peut être persistant et valide jusqu’à ce que l’application soit supprimée du système.

Un magasin de données d’événements COM+ contient des informations sur l’éditeur d’événements (SENS), les abonnés aux événements et les filtres. SENS prédéfinit également une interface sortante pour chaque classe d’événements dans une bibliothèque de types.



| Classe d'événements    | GUID                          | Interface    |
|----------------|-------------------------------|--------------|
| Événements réseau | \_réseau SENSGUID EVENTCLASS \_ | ISensNetwork |
| Événements de connexion   | \_ouverture de \_ session SENSGUID EVENTCLASS   | ISensLogon   |
| Événements d’alimentation   | SENSGUID \_ EVENTCLASS \_ ONNOW   | ISensOnNow   |



 

Pour recevoir des notifications pour l’un de ces événements, votre application doit effectuer deux opérations :

-   Abonnez-vous aux événements SENS qui vous intéressent. Pour vous abonner à un événement, utilisez les interfaces **IEventSubscription** et **IEventSystem** dans les événements com+. Vous devez fournir un identificateur pour les classes d’événements et l’identificateur d’éditeur SENSe, SENSGUID \_ Publisher. Les abonnements sont au niveau de chaque événement, de sorte que l’application d’abonnement doit également spécifier les événements de la classe qui sont intéressants. Chaque événement correspond à une méthode dans l’interface correspondant à sa classe d’événements.
-   Créez un objet récepteur avec une implémentation pour chaque interface que vous gérez. Pour plus d’informations sur ces interfaces et les événements pris en charge dans chacun d’eux, consultez [**ISensNetwork**](/windows/desktop/api/Sensevts/nn-sensevts-isensnetwork), [**ISensLogon**](/windows/desktop/api/Sensevts/nn-sensevts-isenslogon)et [**ISensOnNow**](/windows/desktop/api/Sensevts/nn-sensevts-isensonnow) .

Lorsque l’un des événements contrôlés se produit, SENS traite chaque abonnement avec les filtres associés et notifie les abonnés via le système d’événement COM+.

 

 



