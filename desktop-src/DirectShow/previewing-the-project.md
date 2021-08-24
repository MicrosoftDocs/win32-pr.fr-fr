---
description: Aperçu de l’Project
ms.assetid: 00d72a39-f848-47ea-8460-8b826684eeea
title: Aperçu de l’Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d17d5fd0c87d98db2dac0a7ace97a72e2107eeb252561bbc535a5bd8b4a56d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119748259"
---
# <a name="previewing-the-project"></a>Aperçu de l’Project

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

pour afficher un aperçu du projet, vous avez besoin d’un composant appelé « *moteur de rendu*», qui génère un graphique de filtre DirectShow à partir d’une chronologie. Le graphique de filtre est ce qui restitue réellement le projet. Vous pouvez utiliser le moteur de rendu pour afficher un aperçu d’un projet ou écrire le fichier de sortie final.

Cet article ne décrit pas en détail le moteur de rendu. Pour la version préliminaire, vous n’avez besoin que de quelques appels de méthode. Vous pouvez trouver une discussion plus approfondie, y compris comment écrire des fichiers de sortie, dans le [rendu d’un Project](rendering-a-project.md). L’exemple de code suivant montre comment construire un graphique d’aperçu.


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, CLSCTX_INPROC_SERVER,
            IID_IRenderEngine, (void**) &pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd( );
hr = pRender->RenderOutputPins( );
```



Créez le moteur de rendu à l’aide de la fonction **CoCreateInstance** . Appelez ensuite les méthodes suivantes sur l’interface [**IRenderEngine**](irenderengine.md) du moteur de rendu :

-   [**SetTimelineObject**](irenderengine-settimelineobject.md). Spécifie la chronologie à utiliser.
-   [**ConnectFrontEnd**](irenderengine-connectfrontend.md). Génère un graphique de filtre partiel, avec une broche de sortie pour chaque groupe dans la chronologie.
-   [**RenderOutputPins**](irenderengine-renderoutputpins.md). Termine le graphique d’aperçu en connectant chaque broche de sortie à un convertisseur audio ou vidéo.

une fois le graphique créé, vous pouvez afficher un aperçu du projet en exécutant le graphique, comme vous le feriez avec n’importe quel DirectShow graphique de filtre. Tout d’abord, obtenez un pointeur vers le graphique de filtre en appelant la méthode [**IRenderEngine :: GetFilterGraph**](irenderengine-getfiltergraph.md) .


```C++
IGraphBuilder   *pGraph = NULL;
hr = pRender->GetFilterGraph(&pGraph);
```



Interrogez le graphique de filtre pour les interfaces [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) et [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) . Utilisez ces deux interfaces pour exécuter le graphique et attendre la fin de la lecture. Pour obtenir une explication de l’utilisation de ces interfaces, consultez [Comment lire un fichier](how-to-play-a-file.md) et [répondre à des événements](responding-to-events.md). Le code suivant illustre une façon d’utiliser ces interfaces.


```C++
IMediaControl   *pControl = NULL;
IMediaEvent     *pEvent = NULL;
long evCode;
pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
hr = pControl->Run();
hr = pEvent->WaitForCompletion(INFINITE, &evCode);
pControl->Stop();
```



Le code de cet exemple bloque l’exécution du programme jusqu’à la fin de la lecture, en raison du paramètre infini dans l’appel de la méthode [**IMediaEvent :: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) . En cas de problème lors de la lecture, toutefois, cela peut entraîner le blocage du programme. Dans une application réelle, utilisez une boucle de messages pour attendre la fin de la lecture. Il est également recommandé de fournir à l’utilisateur un moyen d’interrompre la lecture.

Lorsque vous avez terminé d’utiliser le moteur de rendu, appelez toujours la méthode [**IRenderEngine :: ScrapIt**](irenderengine-scrapit.md) . Cette méthode supprime le graphique de filtre et libère toutes les ressources détenues par le moteur de rendu.


```C++
pRender->ScrapIt();
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Chargement et prévisualisation d’un Project](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



