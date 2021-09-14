---
description: définition de l’horloge de Graph
ms.assetid: 23deab26-6c9a-4f94-b750-11c9b1a14ce3
title: définition de l’horloge de Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe98c8dce1ab5f94664fbe1406c682e5d4e50b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126999575"
---
# <a name="setting-the-graph-clock"></a>définition de l’horloge de Graph

quand vous générez un graphique de filtre, le gestionnaire de Graph de filtre choisit automatiquement une horloge de référence pour le graphique. Tous les filtres du graphique sont synchronisés avec l’horloge de référence. En particulier, les filtres de convertisseur utilisent l’horloge de référence pour déterminer l’heure de présentation de chaque échantillon.

il n’y a généralement aucune raison pour qu’une application remplace le choix de l’horloge de référence du gestionnaire Graph Manager. toutefois, vous pouvez le faire en appelant la méthode [**IMediaFilter :: SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) sur le gestionnaire de Graph de filtre. Cette méthode prend un pointeur vers l’interface **IReferenceClock** de l’horloge. Appelez la méthode pendant que le graphique est arrêté.

Si un filtre fournit une horloge, vous pouvez obtenir le pointeur **IReferenceClock** en appelant **QueryInterface** sur le filtre. Vous pouvez également implémenter une horloge de référence externe qui n’est pas fournie par un filtre, à condition que votre horloge externe implémente **IReferenceClock**. L’exemple suivant montre comment spécifier une horloge :


```C++
IGraphBuilder *pGraph = 0;
IReferenceClock *pClock = 0;

CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
    IID_IGraphBuilder, (void **)&pGraph);

// Build the graph.
pGraph->RenderFile(L"C:\\Example.avi", 0);

// Create your clock.
hr = CreateMyPrivateClock(&pClock);
if (SUCCEEDED(hr))
{
    // Set the graph clock.
    IMediaFilter *pMediaFilter = 0;
    pGraph->QueryInterface(IID_IMediaFilter, (void**)&pMediaFilter);
    pMediaFilter->SetSyncSource(pClock);
    pClock->Release();
    pMediaFilter->Release();
}
```



Cet exemple suppose que CreateMyPrivateClock est une fonction définie par l’application qui crée une horloge et retourne un pointeur **IReferenceClock** .

Vous pouvez également définir le graphique de filtre pour qu’il s’exécute sans horloge, en appelant **SetSyncSource** avec la valeur **null**. S’il n’y a pas d’horloge, le graphique s’exécute aussi rapidement que possible. Sans horloge, les filtres de convertisseur n’attendent pas l’heure de la présentation d’un exemple. Au lieu de cela, ils affichent chaque échantillon dès qu’il arrive. La définition du graphique pour qu’il s’exécute sans horloge est utile si vous souhaitez traiter les données rapidement, plutôt que de les afficher en temps réel.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[tâches de base DirectShow](basic-directshow-tasks.md)
</dt> <dt>

[**CBaseReferenceClock, classe**](cbasereferenceclock.md)
</dt> <dt>

[Temps et horloges dans DirectShow](time-and-clocks-in-directshow.md)
</dt> </dl>

 

 



