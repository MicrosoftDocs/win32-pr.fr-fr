---
description: Gestionnaire de graphique de filtre
ms.assetid: b1a53193-27c6-4e86-a5b9-f3c1e4401690
title: Gestionnaire de graphique de filtre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7161f15ea04e1404425d4671ca7991420e0aa993
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845790"
---
# <a name="filter-graph-manager"></a>Gestionnaire de graphique de filtre

Le gestionnaire de graphique de filtre génère et contrôle les graphiques de filtre. Cet objet est le composant central de DirectShow. Les applications l’utilisent pour générer et contrôler les graphiques de filtre. Le gestionnaire de graphes de filtre gère également la synchronisation, la notification d’événements et d’autres aspects du graphique de filtre de contrôle. Créez cet objet en appelant **CoCreateInstance**.

### <a name="clsid"></a>CLSID

Il existe deux CLSID pour créer le gestionnaire de graphes de filtre :



| CLSID                      | Description                                                 |
|----------------------------|-------------------------------------------------------------|
| CLSID \_ FilterGraph         | Crée le gestionnaire de graphes de filtre sur un thread de travail partagé. |
| CLSID \_ FilterGraphNoThread | Crée le gestionnaire de graphes de filtre sur le thread d’application. |



 

En règle générale, les applications doivent utiliser le CLSID \_ FilterGraph. Les deux CLSID créent le même objet, mais ils utilisent différents modèles de thread :

-   \_Le CLSID FilterGraph crée le gestionnaire de graphes de filtre sur un thread de travail, qui est partagé par toutes les \_ instances du CLSID FilterGraph au sein du même processus. Le thread distribue les messages envoyés par les filtres et contrôle la durée de vie des fenêtres créées par des filtres.
-   CLSID \_ FilterGraphNoThread crée le gestionnaire de graphes de filtre sur le thread de l’application. Si vous utilisez ce CLSID, le thread qui appelle **CoCreateInstance** doit avoir une boucle de message qui distribue les messages ; dans le cas contraire, des interblocages peuvent se produire. De plus, avant que le thread d’application ne s’arrête, il doit libérer le gestionnaire de graphique de filtre et tous les objets de graphique (tels que les filtres, les broches, les horloges de référence, etc.).

### <a name="interfaces"></a>Interfaces

Le gestionnaire de graphique de filtre expose les interfaces suivantes :

-   [**IAMGraphStreams**](/windows/desktop/api/Strmif/nn-strmif-iamgraphstreams)
-   [**IAMStats**](/windows/desktop/api/Control/nn-control-iamstats)
-   [**IBasicAudio**](/windows/desktop/api/Control/nn-control-ibasicaudio)
-   [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo)
-   [**IBasicVideo2**](/windows/desktop/api/Control/nn-control-ibasicvideo2)
-   [**IFilterChain**](/windows/desktop/api/Strmif/nn-strmif-ifilterchain)
-   [**IFilterGraph**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph)
-   [**IFilterGraph2**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph2)
-   [**IFilterGraph3**](/windows/desktop/api/Strmif/nn-strmif-ifiltergraph3)
-   [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2)
-   [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder)
-   [**IGraphConfig**](/windows/desktop/api/Strmif/nn-strmif-igraphconfig)
-   [**IGraphVersion**](/windows/desktop/api/Strmif/nn-strmif-igraphversion)
-   [**Appel**](/windows/desktop/api/Control/nn-control-imediacontrol)
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent)
-   [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex)
-   [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink)
-   [**IMediaFilter**](/windows/desktop/api/Strmif/nn-strmif-imediafilter)
-   [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)
-   [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)
-   [**IQueueCommand**](/windows/desktop/api/Control/nn-control-iqueuecommand)
-   [**IRegisterServiceProvider**](/windows/desktop/api/Strmif/nn-strmif-iregisterserviceprovider)
-   [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager)
-   **IServiceProvider**
-   [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep)
-   [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets DirectShow](directshow-objects.md)
</dt> </dl>

 

 



