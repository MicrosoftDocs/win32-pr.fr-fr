---
title: Exécution et synchronisation de listes de commandes
description: Dans Microsoft Direct3D 12, le mode immédiat des versions précédentes n’est plus présent.
ms.assetid: D5013102-2302-4D66-8F59-079C03BA65FD
keywords:
- Liste des commandes
- synchronisation
- exécution
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90d5362d0f093c7c1034e03d396ad28c40d4d600
ms.sourcegitcommit: 170bc12e9724d00cecbb96d57c7226c51e135dee
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 07/07/2021
ms.locfileid: "113489177"
---
# <a name="executing-and-synchronizing-command-lists"></a>Exécution et synchronisation de listes de commandes

Dans Microsoft Direct3D 12, le mode immédiat des versions précédentes n’est plus présent. Au lieu de cela, les applications créent des listes de commandes et des offres groupées, puis enregistrent des jeux de commandes GPU. Les files d’attente de commandes sont utilisées pour envoyer des listes de commandes à exécuter. Ce modèle permet aux développeurs d’avoir davantage de contrôle sur l’utilisation efficace de l’unité de traitement graphique (GPU) et de l’UC.

-   [Présentation de la file d’attente de commandes](#command-queue-overview)
-   [Initialisation d’une file d’attente de commandes](#initializing-a-command-queue)
-   [Exécution de listes de commandes](#executing-command-lists)
-   [Accès aux ressources à partir de plusieurs files d’attente de commandes](#accessing-resources-from-multiple-command-queues)
-   [Synchronisation de l’exécution de la liste de commandes à l’aide des clôtures de file d’attente](#synchronizing-command-list-execution-using-command-queue-fences)
-   [Synchronisation des ressources accessibles par les files d’attente de commandes](#synchronizing-resources-accessed-by-command-queues)
-   [Prise en charge des files d’attente de commandes pour les ressources en mosaïque](#command-queue-support-for-tiled-resources)
-   [Rubriques connexes](#related-topics)

## <a name="command-queue-overview"></a>Présentation de la file d’attente de commandes

Les files d’attente de commandes Direct3D 12 remplacent la synchronisation du runtime et du pilote de la soumission de travail en mode immédiat, qui n’a pas été exposée au développeur, avec des API pour gérer explicitement la concurrence, le parallélisme et la synchronisation. Les files d’attente de commandes offrent les améliorations suivantes aux développeurs :

-   Permet aux développeurs d’éviter les inefficacités accidentelles provoquées par une synchronisation inattendue.
-   Permet aux développeurs d’introduire la synchronisation à un niveau supérieur où la synchronisation requise peut être déterminée plus efficacement et de manière plus précise. Cela signifie que le runtime et le pilote Graphics passent moins de temps à réactiver le parallélisme de manière réactive.
-   Rend les opérations coûteuses plus explicites.

Ces améliorations activent ou améliorent les scénarios suivants :

-   Parallélisme accru : les applications peuvent utiliser des files d’attente plus profondes pour les charges de travail en arrière-plan, telles que le décodage vidéo, lorsqu’elles ont des files d’attente distinctes pour le travail de premier plan.
-   Travail de GPU asynchrone et de faible priorité : le modèle de file d’attente de commandes permet l’exécution simultanée de tâches GPU de faible priorité et d’opérations atomiques qui permettent à un thread GPU de consommer les résultats d’un autre thread non synchronisé sans blocage.
-   Travail de calcul à priorité élevée : cette conception permet des scénarios qui requièrent l’interruption du rendu 3D pour effectuer une petite quantité de travail de calcul haute priorité afin que le résultat puisse être obtenu tôt pour un traitement supplémentaire sur le processeur.

## <a name="initializing-a-command-queue"></a>Initialisation d’une file d’attente de commandes

Les files d’attente de commandes peuvent être créées en appelant [**ID3D12Device :: CreateCommandQueue**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createcommandqueue). Cette méthode prend un [**\_ type de \_ liste \_ de commandes D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type) indiquant le type de file d’attente qui doit être créé et, par conséquent, le type de commande qui peut être soumis à cette file d’attente. N’oubliez pas que les offres groupées ne peuvent être appelées qu’à partir de listes de commandes directes et ne peuvent pas être envoyées directement à une file d’attente. Les types de file d’attente pris en charge sont les suivants :

-   [**\_Type de liste de commandes D3D12 \_ \_ \_ direct**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**D3D12 \_ type de liste de commandes \_ \_ \_ Compute**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)
-   [**\_Copie de \_ type de liste de commandes D3D12 \_ \_**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_command_list_type)

En général, les files d’attente directes et les listes de commandes acceptent toute commande, les files d’attente de calcul et les listes de commandes acceptent les commandes Compute et Copy connexes, et les files d’attente et les listes de commandes de copie acceptent uniquement les commandes de copie.

## <a name="executing-command-lists"></a>Exécution de listes de commandes

Une fois que vous avez enregistré une liste de commandes et que vous avez récupéré la file d’attente de commandes par défaut ou que vous en avez créé une, vous exécutez des listes de commandes en appelant [**ID3D12CommandQueue :: ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists).

Les applications peuvent envoyer des listes de commandes à n’importe quelle file d’attente de commandes à partir de plusieurs threads. Le Runtime effectue le travail de sérialisation de ces requêtes dans l’ordre d’envoi.

Le runtime validera la liste de commandes envoyée et supprimera l’appel à [**ExecuteCommandLists**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-executecommandlists) si l’une des restrictions n’est pas respectée. Les appels seront abandonnés pour les raisons suivantes :

-   La liste de commandes fournie est un bundle, pas une liste de commandes directe.
-   [**ID3D12GraphicsCommandList :: Close**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-close) n’a pas été appelé dans la liste de commandes fournie pour terminer l’enregistrement.
-   [**ID3D12CommandAllocator :: Reset**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandallocator-reset) a été appelé sur l’allocateur de commande associé à la liste de commandes depuis qu’il a été enregistré. Pour plus d’informations sur les allocateurs de commandes, consultez [création et enregistrement des listes de commandes et des offres groupées](recording-command-lists-and-bundles.md).
-   La limite de file d’attente de commandes indique qu’une exécution précédente de la liste de commandes n’est pas encore terminée. Les limites de la file d’attente des commandes sont décrites en détail ci-dessous.
-   Les États Before et after des requêtes, définis avec des appels à [**ID3D12GraphicsCommandList :: BeginQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-beginquery) et [**ID3D12GraphicsCommandList :: EndQuery**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-endquery), ne sont pas correctement mis en correspondance.
-   Les États avant et après des barrières de transition de ressources ne sont pas correctement mis en correspondance. Pour plus d’informations, consultez [utilisation de barrières de ressources pour synchroniser les États des ressources](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="accessing-resources-from-multiple-command-queues"></a>Accès aux ressources à partir de plusieurs files d’attente de commandes

Deux règles imposées par le runtime restreignent l’accès aux ressources à partir de plusieurs files d’attente de commandes. Ces règles sont les suivantes :

1. Une ressource ne peut pas être écrite à partir de plusieurs files d’attente de commandes simultanément. Lorsqu’une ressource est passée à un état accessible en écriture dans une file d’attente, elle est considérée comme appartenant exclusivement à cette file d’attente et doit passer à un état de lecture ou commun (reportez-vous à [**D3D12_RESOURCE_STATES**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_resource_states)) pour qu’elle soit accessible par une autre file d’attente.

2. Dans un état de lecture, une ressource peut être lue simultanément à partir de plusieurs files d’attente de commandes, y compris entre les processus, en fonction de son état de lecture.

Pour plus d’informations sur les restrictions d’accès aux ressources et sur l’utilisation de barrières de ressources pour synchroniser l’accès aux ressources, consultez [utilisation de barrières de ressources pour synchroniser les États des ressources](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="synchronizing-command-list-execution-using-command-queue-fences"></a>Synchronisation de l’exécution de la liste de commandes à l’aide des clôtures de file d’attente

La prise en charge de plusieurs files d’attente de commandes parallèles dans Direct3D 12 vous offre plus de souplesse et de contrôle sur la hiérarchisation des tâches asynchrones sur le GPU. Cette conception signifie également que les applications doivent gérer explicitement la synchronisation du travail, en particulier lorsque les listes de commandes dans une file d’attente dépendent des ressources qui sont utilisées par une autre file d’attente de commandes. Par exemple, l’attente d’une opération sur une file d’attente de calcul se termine pour que le résultat puisse être utilisé pour une opération de rendu sur la file d’attente 3D et en attendant la fin d’une opération 3D afin qu’une opération sur la file d’attente de calcul puisse accéder à une ressource pour l’écriture. Pour activer la synchronisation du travail entre les files d’attente, Direct3D 12 utilise le concept de délimitations, qui sont représentés dans l’API par l’interface [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) .

Une clôture est un entier qui représente l’unité de travail en cours de traitement. Lorsque l’application avance la clôture, en appelant [**ID3D12CommandQueue :: signal**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-signal), l’entier est mis à jour. Les applications peuvent vérifier la valeur d’une clôture et déterminer si une unité de travail a été effectuée pour décider si une opération ultérieure peut être démarrée.

## <a name="synchronizing-resources-accessed-by-command-queues"></a>Synchronisation des ressources accessibles par les files d’attente de commandes

Dans Direct3D 12, la synchronisation de l’état de certaines ressources est implémentée avec les barrières des ressources. À chaque barrière de ressources, une application déclare les États avant et après d’une ressource. Un exemple courant consiste à faire passer une ressource d’une vue de ressource de nuanceur à une vue de cible de rendu. Pour l’essentiel, ces barrières de ressources sont gérées dans des listes de commandes. Lorsque les couches de débogage sont activées, le système impose que les États avant et après de toutes les ressources correspondent, garantissant ainsi que la ressource est dans l’état correct pour une opération particulière à une transition de barrière.

Pour plus d’informations sur la synchronisation de l’état des ressources, consultez [utilisation de barrières de ressources pour synchroniser les États des ressources](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md).

## <a name="command-queue-support-for-tiled-resources"></a>Prise en charge des files d’attente de commandes pour les ressources en mosaïque

Les méthodes de gestion des ressources en mosaïque, exposées par le biais de l’interface [**ID3D11DeviceContext2**](/windows/desktop/api/d3d11_2/nn-d3d11_2-id3d11devicecontext2) dans Direct3D 11, sont fournies par l’interface [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) dans Direct3D 12. Ces méthodes incluent les tâches suivantes :



| Méthode                                                              | Description                                                                                              |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [**CopyTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-copytilemappings)     | Copie les mappages d’une ressource en mosaïque source vers une ressource en mosaïque de destination.<br/>                 |
| [**UpdateTileMappings**](/windows/desktop/api/d3d12/nf-d3d12-id3d12commandqueue-updatetilemappings) | Met à jour les mappages des emplacements de mosaïques dans des ressources en mosaïque à des emplacements de mémoire dans un tas de ressources.<br/> |



 

Pour plus d’informations sur l’utilisation des ressources en mosaïque dans les applications Direct3D 12, consultez la rubrique [ressources en mosaïque Direct3D11](/windows/desktop/direct3d11/tiled-resources).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Envoi de travail dans Direct3D 12](command-queues-and-command-lists.md)
</dt> </dl>

 

