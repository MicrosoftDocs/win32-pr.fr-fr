---
description: Comment lire un fichier
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Comment lire un fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392816"
---
# <a name="how-to-play-a-file"></a>Comment lire un fichier

Cet article a pour but de vous offrir la version de la programmation DirectShow. Il présente une application console simple qui lit un fichier audio ou vidéo. Le programme n’a que quelques lignes de long, mais il illustre une partie de la puissance de la programmation DirectShow.

Comme l’explique l’article [sur la programmation d’applications DirectShow](introduction-to-directshow-application-programming.md) , une application DirectShow effectue toujours les mêmes étapes de base :

1.  Créez une instance du [Gestionnaire de graphes de filtre](filter-graph-manager.md).
2.  Utilisez le gestionnaire de graphe de filtre pour générer un graphique de filtre.
3.  Exécuter le graphique, ce qui provoque le déplacement des données dans les filtres.

Pour compiler et lier le code dans cette rubrique, incluez le fichier d’en-tête DShow. h et un lien vers le fichier de bibliothèque statique strmiids. lib. Pour plus d’informations, consultez [génération d’applications DirectShow](setting-up-the-build-environment.md).

Commencez par appeler [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) ou [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) pour initialiser la bibliothèque com :


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Pour simplifier les choses, cet exemple ignore la valeur de retour, mais vous devez toujours vérifier la valeur **HRESULT** à partir de n’importe quel appel de méthode.

Ensuite, appelez [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) pour créer le gestionnaire de graphique de filtre :


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Comme indiqué, l’identificateur de classe (CLSID) est CLSID \_ FilterGraph. Le gestionnaire de graphes de filtres étant fourni par une DLL in-process, le contexte d’exécution est **CLSCTX \_ InProc \_ Server**. DirectShow prend en charge le modèle de thread libre. vous pouvez donc également appeler [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) avec l’indicateur **coinit \_ multithread** .

L’appel à [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) retourne l’interface [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , qui contient principalement des méthodes pour générer le graphique de filtre. Deux autres interfaces sont nécessaires pour cet exemple :

-   L' [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) contrôle la diffusion en continu. Elle contient des méthodes pour l’arrêt et le démarrage du graphique.
-   [**IMediaEvent**](/windows/desktop/api/Control/nn-control-imediaevent) a des méthodes permettant d’obtenir des événements à partir du gestionnaire de graphique de filtre. Dans cet exemple, l’interface est utilisée pour attendre la fin de la lecture.

Ces deux interfaces sont exposées par le gestionnaire de graphe de filtre. Utilisez le pointeur [**IGraphBuilder**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) retourné pour effectuer une requête :


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Vous pouvez maintenant générer le graphique de filtre. Pour la lecture de fichiers, cette opération est effectuée par un appel de méthode unique :


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



La méthode [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) crée un graphique de filtre qui peut lire le fichier spécifié. Le premier paramètre est le nom de fichier, représenté sous la forme d’une chaîne de caractères larges (2 octets). Le deuxième paramètre est réservé et doit être égal à **null**.

Cette méthode peut échouer si le fichier spécifié n’existe pas ou si le format de fichier n’est pas reconnu. En supposant que la méthode aboutisse, toutefois, le graphique de filtre est maintenant prêt pour la lecture. Pour exécuter le graphique, appelez la méthode [**IMediaControl :: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :


```C++
hr = pControl->Run();
```



Lorsque le graphique de filtre s’exécute, les données se déplacent dans les filtres et sont rendues en tant que vidéo et audio. La lecture se produit sur un thread séparé. Vous pouvez attendre la fin de la lecture en appelant la méthode [**IMediaEvent :: WaitForCompletion**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Cette méthode bloque jusqu’à ce que le fichier soit terminé, ou jusqu’à ce que l’intervalle de délai d’attente spécifié se soit écoulé. La valeur infinie signifie que l’application se bloque indéfiniment jusqu’à ce que le fichier soit terminé. Pour obtenir un exemple plus réaliste de gestion des événements, consultez [réponse aux événements](responding-to-events.md).

Lorsque l’application est terminée, libérez les pointeurs d’interface et fermez la bibliothèque COM :


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Exemple de code

Voici le code complet de l’exemple décrit dans cet article :


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Tâches de base de DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 
