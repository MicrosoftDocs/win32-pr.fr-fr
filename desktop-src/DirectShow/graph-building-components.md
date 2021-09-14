---
description: Composants Graph-Building
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Composants Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127219044"
---
# <a name="graph-building-components"></a>Composants Graph-Building

DirectShow fournit plusieurs composants qui peuvent être utilisés pour créer des graphiques de filtres. Leurs thèmes sont les suivants :

-   [gestionnaire de Graph de filtre](filter-graph-manager.md). Cet objet contrôle le graphique de filtre. Il prend en charge les interfaces [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder), [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)et [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , entre autres. toutes les applications DirectShow utilisent cet objet à un moment donné, même si, dans certains cas, un autre objet crée le filtre Graph Manager pour l’application.
-   [générateur de Graph de Capture](capture-graph-builder.md). Cet objet fournit des méthodes supplémentaires pour créer des graphiques de filtre. Elle a été conçue à l’origine pour la création de graphiques qui effectuent la capture vidéo (par conséquent, le nom), mais elle est utile pour de nombreux autres types de graphiques de filtre personnalisés. Il prend en charge l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .
-   [Mappeur de filtre](filter-mapper.md) et [énumérateur de périphérique système](system-device-enumerator.md). Ces objets localisent les filtres qui sont enregistrés sur le système de l’utilisateur ou qui représentent des périphériques matériels.
-   [générateur de Graph DVD](dvd-graph-builder.md). Cet objet génère des graphiques de filtre pour la lecture et la navigation sur DVD. Il prend en charge l’interface [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .

### <a name="intelligent-connect"></a>Connecter intelligente

le terme « Connecter Intelligent » couvre un ensemble d’algorithmes que le gestionnaire de Graph de filtre utilise pour créer tout ou partie d’un graphique de filtre. chaque fois que le gestionnaire de Graph de filtre requiert des filtres supplémentaires pour compléter le graphique, il effectue approximativement les opérations suivantes :

1.  si le graphique contient actuellement un filtre, avec au moins une broche d’entrée non connectée, le gestionnaire de Graph de filtre tente d’utiliser ce filtre.
2.  dans le cas contraire, le gestionnaire de Graph de filtre recherche dans le registre les filtres qui peuvent accepter le type de média approprié pour la connexion. Chaque filtre a une valeur de Registre appelée « mérite », qui indique à peu près la probabilité que le filtre soit utile pour compléter le graphique. le gestionnaire de Graph de filtre tente de filtrer dans l’ordre de valeur mérite. Pour chaque type de flux (audio, vidéo ou MIDI), le convertisseur par défaut a une valeur élevée. Les décodeurs ont également une mérite élevée. Les filtres à usage spécial ont une faible mérite.

si le gestionnaire de Graph de filtre est bloqué, il réessaie et tente une combinaison différente de filtres. Vous trouverez les détails exacts dans la rubrique [connecter intelligente](intelligent-connect.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération du filtre Graph](building-the-filter-graph.md)
</dt> </dl>

 

 



