---
description: Composants Graph-Building
ms.assetid: d803c56c-6fb1-4937-92e7-9ed2db2afc46
title: Composants Graph-Building
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea3ba346356109d8080d887a510cfcb85b6a6c80
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109891"
---
# <a name="graph-building-components"></a>Composants Graph-Building

DirectShow fournit plusieurs composants qui peuvent être utilisés pour créer des graphiques de filtres. Ces options en question sont les suivantes :

-   [Gestionnaire de graphes de filtre](filter-graph-manager.md). Cet objet contrôle le graphique de filtre. Il prend en charge les interfaces [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder), [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol)et [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) , entre autres. Toutes les applications DirectShow utilisent cet objet à un moment donné, même si, dans certains cas, un autre objet crée le gestionnaire de graphique de filtre pour l’application.
-   [Générateur de graphiques de capture](capture-graph-builder.md). Cet objet fournit des méthodes supplémentaires pour créer des graphiques de filtre. Elle a été conçue à l’origine pour la création de graphiques qui effectuent la capture vidéo (par conséquent, le nom), mais elle est utile pour de nombreux autres types de graphiques de filtre personnalisés. Il prend en charge l’interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) .
-   [Mappeur de filtre](filter-mapper.md) et [énumérateur de périphérique système](system-device-enumerator.md). Ces objets localisent les filtres qui sont enregistrés sur le système de l’utilisateur ou qui représentent des périphériques matériels.
-   [Générateur de graphiques DVD](dvd-graph-builder.md). Cet objet génère des graphiques de filtre pour la lecture et la navigation sur DVD. Il prend en charge l’interface [**IDvdGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-idvdgraphbuilder) .

### <a name="intelligent-connect"></a>Connexion intelligente

Le terme « connexion intelligente » couvre un ensemble d’algorithmes que le gestionnaire de graphique de filtre utilise pour créer tout ou partie d’un graphique de filtre. Chaque fois que le gestionnaire de graphique de filtre requiert des filtres supplémentaires pour compléter le graphique, ce qui est le suivant :

1.  Si le graphique contient actuellement un filtre, avec au moins une broche d’entrée non connectée, le gestionnaire de graphes de filtre tente d’utiliser ce filtre.
2.  Dans le cas contraire, le gestionnaire de graphique de filtre recherche dans le registre les filtres qui peuvent accepter le type de média approprié pour la connexion. Chaque filtre a une valeur de Registre appelée « mérite », qui indique à peu près la probabilité que le filtre soit utile pour compléter le graphique. Le gestionnaire de graphes de filtre tente des filtres dans l’ordre de valeur mérite. Pour chaque type de flux (audio, vidéo ou MIDI), le convertisseur par défaut a une valeur élevée. Les décodeurs ont également une mérite élevée. Les filtres à usage spécial ont une faible mérite.

Si le gestionnaire de graphe de filtre est bloqué, il réessaie et tente une combinaison différente de filtres. Vous trouverez les détails exacts dans la rubrique [connexion intelligente](intelligent-connect.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération du graphique de filtre](building-the-filter-graph.md)
</dt> </dl>

 

 



