---
description: Threads et sections critiques
ms.assetid: e55acb06-03f4-4191-bffe-3196f41ef2c7
title: Threads et sections critiques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d13473a917ae49e80ec658b0d6187fdfdff80c6e3a080a229aca7ccbbe536c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651401"
---
# <a name="threads-and-critical-sections"></a>Threads et sections critiques

cette section décrit les threads dans les filtres de DirectShow, ainsi que les étapes à suivre pour éviter les blocages ou les blocages dans un filtre personnalisé.

Les exemples de cette section utilisent un pseudocode pour illustrer le code que vous devrez écrire. ils supposent qu’un filtre personnalisé utilise des classes dérivées des classes de base DirectShow, comme suit :

-   CMyInputPin : dérivée de [**CBaseInputPin**](cbaseinputpin.md).
-   CMyOutputPin : dérivée de [**CBaseOutputPin**](cbaseoutputpin.md).
-   CMyFilter : dérivée de [**CBaseFilter**](cbasefilter.md).
-   CMyInputAllocator : Allocator du code confidentiel d’entrée, dérivé de [**CMemAllocator**](cmemallocator.md). Tous les filtres n’ont pas besoin d’un allocateur personnalisé. Pour de nombreux filtres, la classe **CMemAllocator** est suffisante.

Cette section contient les rubriques suivantes :

-   [Threads de diffusion en continu et d’application](the-streaming-and-application-threads.md)
-   [Suspension](pausing.md)
-   [Réception et envoi d’exemples](receiving-and-delivering-samples.md)
-   [Transmission de la fin du flux](delivering-the-end-of-stream.md)
-   [Vidage des données](flushing-data.md)
-   [En cours d’arrêt](stopping.md)
-   [Obtention de mémoires tampons](getting-buffers.md)
-   [Streaming threads et Filter Graph Manager](streaming-threads-and-the-filter-graph-manager.md)
-   [Résumé du thread de filtre](summary-of-filter-threading.md)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Flow de données pour les développeurs de filtres](data-flow-for-filter-developers.md)
</dt> <dt>

[écriture de filtres de DirectShow](writing-directshow-filters.md)
</dt> </dl>

 

 



