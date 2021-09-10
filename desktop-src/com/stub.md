---
title: Talon
description: Le stub, comme le proxy, est constitué d’un ou plusieurs éléments d’interface et d’un responsable.
ms.assetid: ed7d5546-2d19-4055-b078-62b39d0317b7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 109936ae16827dce7779b080902dbca74a8dfc51
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124363660"
---
# <a name="stub"></a>Talon

Le stub, comme le proxy, est constitué d’un ou plusieurs éléments d’interface et d’un responsable. Chaque stub d’interface fournit du code pour démarshaler les paramètres et le code qui appelle l’une des interfaces prises en charge par l’objet. Chaque stub fournit également une interface pour la communication interne. Le gestionnaire de stub effectue le suivi des stubs d’interface disponibles.

Toutefois, il existe les différences suivantes entre le stub et le proxy :

-   La différence la plus importante est que le stub représente le client dans l’espace d’adressage de l’objet.
-   Le stub n’est pas implémenté comme un objet d’agrégation, car il n’est pas nécessaire que le client soit affiché en tant qu’unité unique ; chaque élément du stub est un composant distinct.
-   Les stubs d’interface sont privés et non publics.
-   Les stubs d’interface implémentent [**IRpcStubBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcstubbuffer), et non [**IRpcProxyBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcproxybuffer).
-   Au lieu d’empaqueter les paramètres à marshaler, le stub les décompresse après qu’ils ont été marshalés, puis empaquette la réponse.

## <a name="structure-of-the-stub"></a>Structure du stub

Le diagramme suivant illustre la structure du stub. Chaque stub d’interface est connecté à une interface sur l’objet. Le canal distribue les messages entrants au stub d’interface approprié. Tous les composants communiquent avec le canal via [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer), l’interface qui fournit l’accès à la bibliothèque Runtime RPC.

![Capture d’écran qui montre la structure du stub.](images/98714a22-733e-432f-bb90-408bbeecc23f.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Channel](channel.md)
</dt> <dt>

[Communication entre les objets](inter-object-communication.md)
</dt> <dt>

[Détails du marshaling](marshaling-details.md)
</dt> <dt>

[Microsoft RPC](microsoft-rpc.md)
</dt> <dt>

[Proxy](proxy.md)
</dt> </dl>

 

 