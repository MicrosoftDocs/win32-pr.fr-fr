---
description: Le service COM+ Queued Components prend entièrement en charge le concept de partitions. Autrement dit, lorsqu’un composant mis en file d’attente dans une partition est exécuté, le message est mis en file d’attente et le composant est exécuté dans la partition des composants.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Composants et partitions COM+ en file d’attente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523284"
---
# <a name="com-queued-components-and-partitions"></a>Composants et partitions COM+ en file d’attente

Le service COM+ Queued Components prend entièrement en charge le concept de partitions. Autrement dit, lorsqu’un composant mis en file d’attente dans une partition est exécuté, le message est mis en file d’attente et le composant est exécuté à l’intérieur de la partition du composant.

## <a name="queue-names-for-partitioned-components"></a>Noms des files d’attente pour les composants partitionnés

Traditionnellement, le service Queued Components utilise le nom de l’application comme nom de la file d’attente. Cela signifie que dans un scénario sans partitions, où une seule instance d’un nom d’application existe sur un ordinateur, chaque nom d’application possède sa propre file d’attente de messages.

Dans le cas de partitions, toutefois, lorsque plusieurs instances du même nom d’application peuvent exister sur un ordinateur, le service Queued Components utilise la même file d’attente pour tous les composants en file d’attente qui partagent le même nom d’application.

## <a name="activating-queued-components"></a>Activation des composants en file d’attente

Les mêmes règles relatives à l’utilisation de l’ID de partition pour activer un composant non mis en file d’attente s’appliquent à un composant mis en file d’attente, comme suit :

-   Si un moniker est utilisé pour activer le composant mis en file d’attente et qu’un ID de partition est inclus, cet ID de partition est utilisé pour localiser la partition. Cet ID de partition est prioritaire sur tout ID de partition qui peut exister dans le contexte du composant en cours d’activation.
-   Si aucun moniker n’est utilisé pour activer le composant, l’ID de partition qui est dans le contexte de l’objet est utilisé.
-   Si aucun ID de partition n’existe dans le contexte de l’objet, le mappage utilisateur à partition par défaut dans Active Directory est utilisé.

> [!Note]  
> Si un ordinateur serveur est déconnecté du réseau et si le mappage de l’ensemble utilisateur à partition est modifié alors que le serveur est déconnecté, le cache de partition peut contenir un mappage de jeu utilisateur à partition obsolète. Cela peut entraîner une erreur d’activation si le mappage d’un ensemble d’utilisateurs à partitions est le mécanisme utilisé pour activer un composant.

 

Les événements COM+ sont entièrement intégrés aux partitions. Cela signifie qu’un abonné peut s’abonner à un serveur de publication dont l’application réside dans une partition. Pour autoriser cet abonnement, la collection de classes d’abonnés comprend deux propriétés liées à la partition : l’ID de partition de la classe d’événements et l’ID d’application de la classe d’événements.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Restrictions relatives à la conception d’applications](application-design-restrictions.md)
</dt> <dt>

[Implémentation de la partition](partition-implementation.md)
</dt> <dt>

[Inscription et activation de composants dans des partitions](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Que sont les partitions COM+ ?](what-are-com--partitions-.md)
</dt> </dl>

 

 



