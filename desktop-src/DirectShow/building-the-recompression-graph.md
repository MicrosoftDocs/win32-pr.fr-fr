---
description: Génération de la Graph de recompression
ms.assetid: 8f25c60e-30be-4cc4-b924-b8d6654604d3
title: Génération de la Graph de recompression
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b8ea604bead34c22c123bbabe5d88e985006a9e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111397"
---
# <a name="building-the-recompression-graph"></a>Génération de la Graph de recompression

Un graphique de filtre classique pour la recompression de fichiers AVI ressemble à ce qui suit :

![graphique de recompression AVI](images/avi2avi4.png)

Le [filtre de séparateur AVI](avi-splitter-filter.md) extrait les données du [filtre source de fichier (Async)](file-source--async--filter.md) et les analyse dans des flux vidéo et audio. Le décompresseur vidéo décode la vidéo compressée, où elle est recompressée par le compresseur vidéo. Le choix des décompresseurs dépend du fichier source ; il sera géré automatiquement par les [connecter intelligentes](intelligent-connect.md). L’application doit choisir le compresseur, généralement en présentant une liste à l’utilisateur. (Voir [choix d’un filtre de compression](choosing-a-compression-filter.md).)

La vidéo compressée passe alors au [filtre multiplex MUX](avi-mux-filter.md). Le flux audio de cet exemple n’étant pas compressé, il passe directement du séparateur AVI à AVI Mux. Le multiplexeur de fichiers AVI entrelace les deux flux et le [filtre du writer de fichier](file-writer-filter.md) écrit la sortie sur le disque. Notez que le multiplexeur de données AVI est requis même si le fichier d’origine n’a pas de flux audio.

le moyen le plus simple de créer ce graphique de filtre consiste à utiliser la [Graph de capture](capture-graph-builder.md), qui est un composant DirectShow pour générer des graphiques de capture et d’autres graphiques de filtres personnalisés.

commencez par appeler CoCreateInstance pour créer le générateur de Graph de Capture :


```C++
ICaptureGraphBuilder2 *pBuild = NULL;
hr = CoCreateInstance(CLSID_CaptureGraphBuilder2, 
                        NULL, CLSCTX_INPROC_SERVER,
    IID_ICaptureGraphBuilder2, (void **)&pBuild);
```



utilisez ensuite le générateur de Graph de Capture pour générer le graphique de filtre :

1.  Générez la section de rendu du graphique, qui comprend le filtre multiplex MUX et le [writer de fichier](file-writer-filter.md).
2.  Ajoutez le filtre source et le filtre de compression au graphique.
3.  Connecter le filtre de la source au filtre MUX. Le générateur de graphiques de capture insère les filtres de séparateur et de décodeur nécessaires pour analyser le fichier source. Il peut également acheminer les flux vidéo et audio via des filtres de compression.

Les sections suivantes décrivent chacune de ces étapes.

Générer la section de rendu

Pour générer la section de rendu du graphique, appelez la méthode [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) . Cette méthode accepte les paramètres d’entrée qui spécifient le sous-type de média pour la sortie et le nom du fichier de sortie. Elle retourne des pointeurs vers le filtre MUX et le writer de fichier. Le filtre MUX est nécessaire pour l’étape suivante de la génération de graphiques. Le pointeur vers le writer de fichier n’est pas nécessaire pour cet exemple, afin que le paramètre puisse être **null**:


```C++
IBaseFilter *pMux = NULL;
hr = pBuild->SetOutputFileName(
        &MEDIASUBTYPE_Avi, // File type. 
        wszOutputFile,     // File name, as a wide-character string.
        &pMux,             // Receives a pointer to the multiplexer.
        NULL);             // Receives a pointer to the file writer. 
```



Lorsque la méthode est retournée, le filtre MUX a un nombre de références en suspens. par conséquent, veillez à libérer le pointeur ultérieurement.

Le diagramme suivant montre le graphique de filtre à ce stade.

![section de rendu du graphique de filtre](images/avi2avi1.png)

Le filtre MUX expose deux interfaces pour le contrôle du format AVI :

-   [**Interface IConfigInterleaving**](/windows/desktop/api/Strmif/nn-strmif-iconfiginterleaving): définit le mode d’entrelacement.
-   [**Interface IConfigAviMux**](/windows/desktop/api/Strmif/nn-strmif-iconfigavimux): définit le flux principal et l’index de compatibilité avi.

Ajouter les filtres source et de compression

L’étape suivante consiste à ajouter les filtres source et de compression au graphique de filtre. le générateur de Graph de Capture crée automatiquement une instance du gestionnaire de Graph de filtre quand vous appelez SetOutputFileName. Pour obtenir un pointeur vers cette dernière, appelez la méthode [**ICaptureGraphBuilder2 :: GetFiltergraph**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-getfiltergraph) :


```C++
IGraphBuilder *pGraph = NULL;
hr = pBuild->GetFiltergraph(&pGraph);
```



À présent, appelez la méthode [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter le filtre de source de fichier Async et la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) pour ajouter le compresseur vidéo :


```C++
IBaseFilter *pSrc = NULL;
hr = pGraph->AddSourceFilter(wszInputFile, L"Source Filter", &pSrc);
hr = pGraph->AddFilter(pVComp, L"Compressor");
```



À ce stade, le filtre source et le filtre de compression ne sont pas connectés à d’autres éléments dans le graphique, comme indiqué dans l’illustration suivante :

![filtrer le graphique avec les filtres source et de compression](images/avi2avi2.png)

Connecter la Source au multiplexeur

La dernière étape consiste à connecter le filtre source au filtre multiplex MUX par le biais du compresseur vidéo. Utilisez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) , qui connecte une broche de sortie sur le filtre source à un filtre de récepteur spécifié, éventuellement à l’aide d’un filtre de compression.

Les deux premiers paramètres spécifient les codes confidentiels du filtre source à connecter, en désignant une catégorie de code confidentiel et un type de média. Le filtre de source de fichier Async n’a qu’une seule broche de sortie. ces paramètres doivent donc avoir la **valeur null**. Les trois paramètres suivants spécifient le filtre source, le filtre de compression (le cas échéant) et le filtre Mux.

L’exemple de code suivant affiche le flux vidéo via le compresseur vidéo :


```C++
hr = pBuild->RenderStream(
        NULL,       // Output pin category
        NULL,       // Media type
        pSrc,       // Source filter
        pVComp,     // Compression filter
        pMux);      // Sink filter (the AVI Mux)
```



Le diagramme suivant illustre le graphique de filtre jusqu’à présent.

![flux vidéo rendu](images/avi2avi3.png)

En supposant que le fichier source possède un flux audio, le filtre de [fractionnement AVI](avi-splitter-filter.md) a créé une broche de sortie pour l’audio. Pour connecter ce code confidentiel, appelez à nouveau RenderStream :


```C++
hr = pBuild->RenderStream(NULL, NULL, pSrc, NULL, pMux);
```



Ici, aucun filtre de compression n’est spécifié. La broche de sortie du filtre source est déjà connectée, de sorte que la méthode RenderStream recherche une broche de sortie non connectée sur le filtre Splitter. Il recherche le code confidentiel audio et le connecte directement au filtre MUX. Si le fichier source n’a pas de flux audio, le deuxième appel à RenderStream échoue. Ce comportement est normal. Le graphique étant terminé après le premier appel à RenderStream, l’échec dans le deuxième appel est sans conséquence.

Dans cet exemple, l’ordre des deux appels RenderStream est important. Étant donné que le deuxième appel ne spécifie pas de compresseur, il connecte tout code confidentiel non connecté du séparateur AVI. Si vous effectuez cet appel avant l’autre, il peut connecter le flux vidéo au AVI MUX, sans votre compresseur vidéo. Par conséquent, l’appel plus spécifique (avec le filtre de compression) doit se produire en premier.

La discussion précédente suppose que le fichier source est un fichier AVI. Toutefois, cette technique fonctionne également avec d’autres types de fichiers, tels que les fichiers MPEG. Le graphique de filtre résultant est quelque peu différent.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Recompression d’un fichier AVI](recompressing-an-avi-file.md)
</dt> </dl>

 

 



