---
title: Interopérabilité Direct3D 12
description: D3D12 peut être utilisé pour écrire des applications de composants.
ms.assetid: 51F7E715-82B6-48D8-A06A-CBBEDF6968F5
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b5fcfe2adf756c12f034031675d0c3ac5571b44
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404325"
---
# <a name="direct3d-12-interop"></a>Interopérabilité Direct3D 12

D3D12 peut être utilisé pour écrire des applications de composants.

-   [Vue d’ensemble de l’interopérabilité](#interop-overview)
-   [Raisons de l’utilisation de l’interopérabilité](#reasons-for-using-interop)
    -   [Partage d’une liste de commandes](#sharing-a-command-list)
    -   [Partage d’une file d’attente de commandes](#sharing-a-command-queue)
    -   [Partage de primitives de synchronisation](#sharing-sync-primitives)
    -   [Partage des ressources](#sharing-resources)
    -   [Choix d’un modèle d’interopérabilité](#choosing-an-interop-model)
-   [API d’interopérabilité](#interop-apis)
-   [Rubriques connexes](#related-topics)

## <a name="interop-overview"></a>Vue d’ensemble de l’interopérabilité

D3D12 peut être très puissant et permettre aux applications d’écrire du code graphique avec l’efficacité de la console, mais toutes les applications n’ont pas besoin de réinventer la roue et d’écrire l’intégralité du moteur de rendu à partir de zéro. Dans certains cas, un autre composant ou une autre bibliothèque l’a déjà fait mieux, ou dans d’autres cas, les performances d’une partie du code ne sont pas aussi critiques que l’exactitude et la lisibilité.

Cette section traite des techniques d’interopérabilité suivantes :

-   D3D12 et D3D12, sur le même appareil
-   D3D12 et D3D12, sur différents appareils
-   D3D12 et toute combinaison de D3D11, D3D10 ou D2D, sur le même appareil
-   D3D12 et toute combinaison de D3D11, D3D10 ou D2D sur différents appareils
-   D3D12 et GDI, ou D3D12 et D3D11 et GDI

## <a name="reasons-for-using-interop"></a>Raisons de l’utilisation de l’interopérabilité

Une application peut souhaiter D3D12 Interop avec d’autres API pour plusieurs raisons. Exemples :

-   Portage incrémentiel : souhaitant déplacer une application entière à partir de D3D10 ou D3D11 vers D3D12, tout en ayant la possibilité de fonctionner aux étapes intermédiaires du processus de Portage (pour activer le test et le débogage).
-   Code de boîte noire : souhaitant laisser une partie spécifique d’une application telle quelle lors du Portage du reste du code. Par exemple, il est possible que vous n’ayez pas besoin de déplacer les éléments d’interface utilisateur d’un jeu.
-   Composants non modifiables : vous devez utiliser des composants qui ne sont pas détenus par l’application, qui ne sont pas écrits dans la D3D12 cible.
-   Un nouveau composant : il ne souhaite pas porter sur l’ensemble de l’application, mais souhaite utiliser un nouveau composant écrit à l’aide de D3D12.

Il existe quatre techniques principales pour l’interopérabilité dans D3D12 :

-   Une application peut choisir de fournir une liste de commandes ouverte à un composant, qui enregistre certaines commandes de rendu supplémentaires sur une cible de rendu déjà liée. Cela revient à fournir un contexte de périphérique préparé à un autre composant dans D3D11, et est parfait pour des opérations telles que l’ajout d’une interface utilisateur/texte à une mémoire tampon d’arrière-plan déjà liée.
-   Une application peut choisir de fournir une file d’attente de commandes à un composant, ainsi qu’une ressource de destination souhaitée. Cela revient à utiliser des API [**ClearState**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-clearstate) ou [**DeviceContextState**](/windows/desktop/api/d3d11_1/nn-d3d11_1-id3ddevicecontextstate) dans d3d11 pour fournir un contexte de périphérique propre à un autre composant. C’est ainsi que les composants tels que D2D fonctionnent.
-   Un composant peut choisir un modèle dans lequel il produit une liste de commandes, éventuellement en parallèle, que l’application est responsable de l’envoi ultérieurement. Au moins une ressource doit être fournie au-delà des limites du composant. Cette même technique est disponible dans D3D11 à l’aide de contextes différés, bien que les performances dans D3D12 soient plus souhaitables.
-   Chaque composant possède ses propres files d’attente et/ou périphériques, et l’application et les composants doivent partager des informations de ressources et de synchronisation entre les limites des composants. Cela est similaire à l’héritage `ISurfaceQueue` et à la [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex)plus moderne.

Les différences entre ces scénarios sont les suivantes : exactement partagé entre les limites du composant. L’appareil est supposé être partagé, mais puisqu’il est fondamentalement sans État, il n’est pas vraiment pertinent. Les objets clés sont la liste de commandes, la file d’attente de commandes, les objets de synchronisation et les ressources. Chacun de ces éléments a leurs propres complications lors de leur partage.

### <a name="sharing-a-command-list"></a>Partage d’une liste de commandes

La méthode d’interopérabilité la plus simple requiert le partage d’une liste de commandes avec une partie du moteur. Une fois les opérations de rendu terminées, la propriété de la liste de commandes revient à l’appelant. La propriété de la liste de commandes peut être tracée dans la pile. Étant donné que les listes de commandes sont à thread unique, il n’existe aucun moyen pour une application d’effectuer une opération unique ou novatrice à l’aide de cette technique.

### <a name="sharing-a-command-queue"></a>Partage d’une file d’attente de commandes

C’est probablement la technique la plus courante pour plusieurs composants qui partagent un appareil dans le même processus.

Lorsque la file d’attente de commandes est l’unité de partage, il doit y avoir un appel au composant pour lui indiquer que toutes les listes de commandes en suspens doivent être envoyées immédiatement à la file d’attente de commandes (et que toutes les files d’attente de commandes internes doivent être synchronisées). Cela est équivalent à l’API de [**vidage**](/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-flush) d3d11 et est la seule façon dont l’application peut envoyer ses propres listes de commandes ou primitives de synchronisation.

### <a name="sharing-sync-primitives"></a>Partage de primitives de synchronisation

Le modèle attendu pour un composant qui s’exécute sur ses propres périphériques et/ou files d’attente de commandes est d’accepter un handle [**ID3D12Fence**](/windows/desktop/api/d3d12/nn-d3d12-id3d12fence) ou partagé, et UInt64 pair au début de son travail, qu’il attendra, puis à un deuxième descripteur ID3D12Fence ou partagé, et à une paire UInt64 qu’il signalera lorsque tout le travail sera terminé. Ce modèle correspond à l’implémentation actuelle de [**IDXGIKeyedMutex**](/windows/desktop/api/dxgi/nn-dxgi-idxgikeyedmutex) et de la conception de la synchronisation du modèle de retournement DWM/DXGI.

### <a name="sharing-resources"></a>Partage des ressources

La partie la plus complexe de l’écriture d’une application D3D12 qui tire parti de plusieurs composants est de savoir comment gérer les ressources partagées au-delà des limites des composants. Cela est principalement dû au concept d’États des ressources. Bien que certains aspects de la conception de l’état des ressources soient destinés à gérer la synchronisation intra-commande, les autres ont un impact sur les listes de commandes, affectant la disposition des ressources et des ensembles valides d’opérations ou des caractéristiques de performances d’accès aux données des ressources.

Il existe deux modèles de gestion de cette compliquation, qui impliquent essentiellement un contrat entre les composants.

-   Le contrat peut être défini par le développeur du composant et documenté. Cela peut être aussi simple que « la ressource doit être dans l’État par défaut lorsque le travail est démarré, et sera rétablie à l’État par défaut lorsque le travail est terminé » ou peut avoir des règles plus compliquées pour permettre des opérations telles que le partage d’une mémoire tampon de profondeur sans forcer les résolutions de profondeur intermédiaire.
-   Le contrat peut être défini par l’application lors de l’exécution, au moment où la ressource est partagée au-delà des limites du composant. Il se compose des deux mêmes informations : l’État dans lequel se trouve la ressource lorsque le composant commence à l’utiliser, et l’État dans lequel le composant doit le conserver lorsqu’il se termine.

### <a name="choosing-an-interop-model"></a>Choix d’un modèle d’interopérabilité

Pour la plupart des applications D3D12, le partage d’une file d’attente de commandes est probablement le modèle idéal. Il permet la propriété complète de la création et de l’envoi de travaux, sans surcharge de mémoire supplémentaire due à l’utilisation de files d’attente redondantes et sans l’impact des performances sur les primitives de synchronisation GPU.

Le partage de primitives de synchronisation est nécessaire une fois que les composants doivent traiter des propriétés de file d’attente différentes, telles que le type ou la priorité, ou une fois que le partage doit couvrir les limites du processus.

Le partage ou la génération de listes de commandes n’est pas largement utilisé en externe par les composants tiers, mais peut être largement utilisé dans les composants internes à un moteur de jeu.

## <a name="interop-apis"></a>API d’interopérabilité

La rubrique [Direct3D 11 sur 12](./direct3d-11-on-12.md) vous guide tout au long de l’utilisation d’une grande partie de la surface de l’API en rapport avec les types d’interopérabilité décrits dans cette rubrique.

consultez également la méthode [ID3D12Device :: CreateSharedHandle](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createsharedhandle) , que vous pouvez utiliser pour partager des surfaces entre des api Windows graphics.

## <a name="related-topics"></a>Rubriques connexes

* [Comprendre Direct3D 12](directx-12-getting-started.md)
* [Utilisation de Direct3D 11, Direct3D 10 et Direct2D](direct3d-12-interop.md)
* [Direct3D 11 sur 12](./direct3d-11-on-12.md)