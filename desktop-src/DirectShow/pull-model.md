---
description: Modèle d’extraction
ms.assetid: b5246dfe-e6ee-4b91-bfe3-2ec8b8723938
title: Modèle d’extraction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9832f719e21d85fd09fbf92303e404290d7d99efd6953ace398f77167d0263a1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747889"
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

[données Flow dans le filtre Graph](data-flow-in-the-filter-graph.md)
</dt> </dl>

 

 



