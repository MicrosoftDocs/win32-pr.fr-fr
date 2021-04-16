---
description: Modèle d’extraction
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modèle d’extraction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8dd4becd54bffb39acf30b6d29fca45e6a117989
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521343"
---
# <a name="pull-model"></a>Modèle d’extraction

Dans l’interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , le filtre amont détermine les données à envoyer et envoie les données vers le filtre en aval. Pour certains filtres, un modèle d' *extraction* est plus approprié. Ici, le filtre en aval demande des données à partir du filtre en amont. Les échantillons sont toujours en aval, de la broche de sortie à la broche d’entrée, mais le filtre en aval lance le Workflow. Ce type de connexion utilise l’interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .

Le modèle d’extraction est généralement utilisé pour la lecture de fichiers. Par exemple, dans un graphique de lecture AVI, le filtre de [source de fichier Async](file-source--async--filter.md) effectue des opérations de lecture de fichier génériques et remet les données sous forme de flux d’octets, sans informations de mise en forme. Le filtre de [séparateur AVI](avi-splitter-filter.md) lit les en-têtes AVI et analyse le flux dans des exemples vidéo et audio. Le séparateur AVI peut déterminer les données dont il a besoin mieux que le filtre de source de fichier Async, et utilise donc **IAsyncReader** au lieu de **IMemInputPin**.

Pour demander des données à partir de la broche de sortie, la broche d’entrée appelle l’une des méthodes suivantes :

-   [**IAsyncReader :: Request**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-request)
-   [**IAsyncReader::SyncRead**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncread)
-   [**IAsyncReader :: SyncReadAligned**](/windows/desktop/api/Strmif/nf-strmif-iasyncreader-syncreadaligned).

La première méthode est asynchrone, pour prendre en charge plusieurs lectures avec chevauchement. Les autres sont synchrones.

En théorie, tout filtre peut prendre en charge **IAsyncReader**, mais dans la pratique il est conçu pour les filtres sources qui se connectent aux filtres de l’analyseur. L’analyseur fonctionne très bien comme un filtre source dans le modèle push. Lorsqu’il est suspendu, il crée un thread de streaming qui extrait les données de la connexion **IAsyncReader** et les pousse en aval. Les broches de sortie utilisent **IMemInputPin** et le reste du graphique utilise le modèle push standard.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Data Flow dans le graphique de filtre](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



