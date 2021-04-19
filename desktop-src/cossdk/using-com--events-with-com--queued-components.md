---
description: Le service événements COM+ est utilisé pour gérer la remise des événements des serveurs de publication aux abonnés.
ms.assetid: 0945163b-1276-47f6-ae7f-9d932a1b586d
title: Utilisation d’événements COM+ avec des composants en file d’attente COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4be31dd1088b720902295738c23173c28145cef2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515173"
---
# <a name="using-com-events-with-com-queued-components"></a>Utilisation d’événements COM+ avec des composants en file d’attente COM+

Le service événements COM+ est utilisé pour gérer la remise des événements des serveurs de publication aux abonnés. Le service composants en file d’attente COM+ peut être utilisé pour rendre le serveur de publication et le temps de traitement de l’abonné indépendant en mettant en file d’attente le message de l’éditeur et en le relisant ultérieurement sur l’abonné. La nécessité ou non d’utiliser le service Queued Components dépend de la logique métier sous-jacente de votre application. Si vous avez besoin d’événements qui sont indépendants de l’heure, vous pouvez les créer à l’aide du service événements COM+ avec les composants en file d’attente COM+.

> [!Note]  
> Pour plus d’informations sur l’utilisation du service COM+ Queued Components, consultez [composants en file d’attente com+](com--queued-components.md).

 

Le service Queued Components gère l’appel de méthode de méthode dans un message unique. L’enregistreur effectue un traitement par lots de tous les appels de méthode dans un message, puis le lecteur appelle ces méthodes dans l’ordre où le message est traité.

Un enregistreur et un lecteur de composants en file d’attente peuvent être positionnés dans l’un des deux emplacements suivants :

-   Entre le serveur de publication et l’objet d’événement
-   Entre l’objet d’événement et l’abonné

Si vous placez l’enregistreur et le lecteur entre le serveur de publication et l’objet d’événement, vous rendez la [classe d’événements](the-com--event-class-object.md) en tant que composant. Le composant de la classe d’événements doit être marqué pour la mise en file d’attente et être activé par le joueur dans un processus distinct du serveur de publication.

Pour remettre des événements de manière asynchrone, composez l’enregistreur et le lecteur entre l’objet d’événement et l’abonné, puis définissez l’attribut de mise en file d’attente de l’objet d’abonnement. Cela définit SubscriberMoniker comme suit : « queue:/New:/ {12345678-1234-1234-1234-123456789012} ».

Il y a un ordre de implication de livraison à prendre en compte lors de l’utilisation de composants en file d’attente dans une situation d’événement. Étant donné que les composants en file d’attente de service enregistrent et lisent tous les appels au cours de la durée de vie d’un objet unique dans un message, tous les appels sont relus dans l’ordre dans lequel ils ont été créés. Toutefois, s’il existe plusieurs sessions avec plusieurs objets, l’ordre ne peut pas être garanti. Si l’ordre est important, assurez-vous que les appels qui doivent être lus dans l’ordre résident sur la même instance d’objet.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtrage des événements dans COM+](filtering-events-in-com-.md)
</dt> <dt>

[Publication et diffusion d’événements dans COM+](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[Abonnements](subscriptions.md)
</dt> <dt>

[Objet de classe d’événements COM+](the-com--event-class-object.md)
</dt> </dl>

 

 



