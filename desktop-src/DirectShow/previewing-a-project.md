---
description: Aperçu d’un Project
ms.assetid: 2efa3f25-a93f-4362-b461-b67475e5d78c
title: Aperçu d’un Project
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8cd9d299a99a0a7315cec986fbc044d427385647
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223177"
---
# <a name="previewing-a-project"></a>Aperçu d’un Project

\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]

Pour afficher un aperçu d’un projet, appelez d’abord **CoCreateInstance** pour créer une instance du moteur de rendu de base. L’identificateur de classe est CLSID \_ RenderEngine. Appelez ensuite la méthode [**IRenderEngine :: SetTimelineObject**](irenderengine-settimelineobject.md) pour spécifier la chronologie que vous rendez.

La première fois que vous affichez un aperçu de la chronologie, effectuez les appels suivants dans l’ordre indiqué :

1.  Appelez [**IRenderEngine :: SetRenderRange**](irenderengine-setrenderrange.md) pour spécifier la partie de la chronologie à afficher. (facultatif)
2.  Appelez [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) pour créer le composant frontal du graphique.
3.  Appelez [**IRenderEngine :: RenderOutputPins**](irenderengine-renderoutputpins.md). Cette méthode connecte chaque broche de sortie à un convertisseur vidéo ou audio, en terminant le graphique.

L’exemple de code suivant illustre ces étapes :


```C++
IRenderEngine *pRender = NULL; 
hr = CoCreateInstance(CLSID_RenderEngine, NULL, 
    CLSCTX_INPROC_SERVER, IID_IRenderEngine, (void**)&pRender);

hr = pRender->SetTimelineObject(pTL);
hr = pRender->ConnectFrontEnd();
hr = pRender->RenderOutputPins();
```



Exécutez maintenant le graphique de filtre. tout d’abord, appelez la méthode [**IRenderEngine :: GetFilterGraph**](irenderengine-getfiltergraph.md) pour récupérer un pointeur vers l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) du gestionnaire de Graph. interrogez ensuite le gestionnaire de Graph de filtre pour l’interface [**imediacontrol**](/windows/desktop/api/Control/nn-control-imediacontrol) et appelez [**imediacontrol :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run), comme indiqué dans le code suivant :


```C++
IGraphBuilder   *pGraph = NULL;
IMediaControl   *pControl = NULL;
hr = pRender->GetFilterGraph(&pGraph);
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pControl->Run();
```



utilisez l’interface [**IMediaEventEx**](/windows/desktop/api/Control/nn-control-imediaeventex) du gestionnaire de Graph pour attendre la fin de la préversion. vous pouvez également rechercher le graphique à l’aide de l’interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) du gestionnaire de Graph, comme vous le feriez avec un graphique de lecture de fichier.

Pour réafficher un aperçu du projet, recherchez à nouveau le graphique sur l’heure zéro et rappelez l' **exécution** . Si vous modifiez le contenu de la chronologie, procédez comme suit :

1.  Appelez **SetRenderRange**. (facultatif)
2.  Appelez **ConnectFrontEnd**.
3.  Si la méthode **ConnectFrontEnd** retourne S \_ WARN \_ OUTPUTRESET, appelez **RenderOutputPins**. (Si **ConnectFrontEnd** retourne S \_ OK, vous pouvez ignorer cette étape.)
4.  Recherche le graphique sur l’heure zéro.
5.  Exécutez le graphique.

L’exemple suivant illustre ces étapes :


```C++
hr = pRender->ConnectFrontEnd();
if (hr == S_WARN_OUTPUTRESET)
{
    hr = pRender->RenderOutputPins();
}
LONGLONG llStart = 0; 
hr = pSeek->SetPositions(&llStart, AM_SEEKING_AbsolutePositioning, 0, 0); 
hr = pControl->Run();
```



Pour obtenir un exemple complet qui charge et affiche un aperçu d’un fichier projet, consultez [chargement et aperçu d’un Project](loading-and-previewing-a-project.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des projets de montage vidéo](managing-video-editing-projects.md)
</dt> <dt>

[Rendu d’un Project](rendering-a-project.md)
</dt> </dl>

 

 



