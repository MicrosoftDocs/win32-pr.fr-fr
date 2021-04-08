---
description: Concepts des événements COM+
ms.assetid: 6bfe4852-4029-4dd4-92ad-3061618b1b23
title: Concepts des événements COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811dbca17c4e90ba5e8c2bcb8c918ce6634487e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749085"
---
# <a name="com-events-concepts"></a>Concepts des événements COM+

Le service d’événements COM+ est un système d’événements automatisé et *faiblement couplé* qui stocke les informations d’événements provenant de différents serveurs de publication dans le catalogue com+. Les abonnés peuvent interroger ce magasin d’événements et sélectionner les événements qu’ils souhaitent connaître.

> [!Note]  
> Un *événement* est identifié par une méthode dans une interface com+, appelée méthode d' *événement*, et provient d’un serveur de publication et distribué à l’abonné ou aux abonnés appropriés par le biais du service d’événements com+. Les méthodes d’événement doivent être nommées de manière unique et ne peuvent contenir que des paramètres d’entrée (pas de paramètres de sortie ou d’entrée/sortie). La valeur de retour doit être un **HRESULT**.

 

Le service événements COM+ gère la plupart des sémantiques d’événements pour le serveur de publication et l’abonné. Les éditeurs offrent la publication de types d’événements, et les abonnés demandent des types d’événements à partir des serveurs de publication. Contrairement à un système d' *événements étroitement couplé* , où les éditeurs doivent gérer directement la surcharge liée à l’appel d’abonnés, le service d’événements com+ gère les données d’abonnement dans le catalogue com+, indépendamment du serveur de publication et de l’abonné. Cela simplifie le modèle de programmation pour le serveur de publication et l’abonné, car le composant d’abonné COM+ n’a pas besoin de contenir la logique de création d’abonnements.

Étant donné que le cycle de vie des données d’abonnement aux événements COM+ est distinct de celui du serveur de publication ou de l’abonné, les abonnements peuvent être générés avant que l’abonné ou les applications du serveur de publication soient actifs. Cela signifie également que les serveurs de publication et les abonnés peuvent être développés et déployés séparément. Le serveur de publication peut être écrit sans connaître le nombre et l’emplacement des abonnés. Les abonnés utilisent le service événements COM+ pour rechercher le serveur de publication et gérer leurs abonnements.

Les rubriques suivantes de cette section fournissent des informations détaillées sur les éléments de base du service d’événements COM+ et expliquent comment les utiliser.

-   [Objet de classe d’événements COM+](the-com--event-class-object.md)
-   [Abonnements](subscriptions.md)
-   [Publication et diffusion d’événements dans COM+](publishing-and-delivering-events-in-com-.md)
-   [Filtrage des événements dans COM+](filtering-events-in-com-.md)
-   [Utilisation d’événements COM+ avec des composants en file d’attente COM+](using-com--events-with-com--queued-components.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Considérations sur la sécurité des événements COM+](com--events-security-considerations.md)
</dt> <dt>

[Tâches des événements COM+](com--events-tasks.md)
</dt> </dl>

 

 



