---
description: Génération d’un filtre VMR-9 Graph
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Génération d’un filtre VMR-9 Graph
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127111425"
---
# <a name="building-a-vmr-9-filter-graph"></a>Génération d’un filtre VMR-9 Graph

Étant donné que le filtre de mixage vidéo 9 Filter (VMR-9) n’est pas le convertisseur vidéo par défaut, une application qui utilise VMR-9 doit l’ajouter explicitement au graphique et la connecter. Cette section présente deux approches différentes de la création de graphiques de filtre avec VMR-9.

utilisation du générateur de Graph de Capture

le générateur de Graph de Capture est un objet d’assistance pour la création de graphiques de filtres personnalisés. Vous pouvez l’utiliser pour générer des graphiques VMR-9 comme suit :

1.  créez et initialisez le générateur de Graph de capture, comme décrit dans la rubrique [à propos du générateur de Graph de capture](about-the-capture-graph-builder.md).
2.  Appelez CoCreateInstance pour créer VMR-9 :
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) sur le gestionnaire de Graph de filtre pour ajouter VMR-9 au graphique de filtre :
    ```C++
    hr = pGraph->AddFilter(pVmr, L"VMR9");
    ```

    

4.  Appelez [**IGraphBuilder :: AddSourceFilter**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-addsourcefilter) pour ajouter un filtre source pour le fichier vidéo :
    ```C++
    IBaseFilter *pSource;
    hr = pGraph->AddSourceFilter(L"C:\\Example.avi", L"Source1", &pSource);
    ```

    

5.  Appelez la méthode [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour afficher le flux vidéo dans VMR :
    ```C++
    hr = pBuild->RenderStream(0, 0, pSource, 0, pVmr);  
    ```

    

6.  Vous pouvez également appeler RenderStream à nouveau pour afficher le flux audio :
    ```C++
    hr = pBuild->RenderStream(0, &MEDIATYPE_Audio, pSource, 0, NULL);
    ```

    

Vous pouvez mélanger plusieurs flux vidéo en appelant AddSourceFilter et RenderStream pour chaque fichier source.

utilisation du gestionnaire de Graph de filtre

si vous préférez ne pas utiliser le générateur de Graph de Capture, vous pouvez créer un graphique VMR-9 en utilisant simplement des méthodes sur le gestionnaire de Graph de filtre, comme suit :

1.  Créez VMR-9 et ajoutez-le au graphique, comme indiqué dans la procédure précédente.
2.  Utilisez AddSourceFilter pour ajouter un filtre source pour le fichier vidéo, comme indiqué dans la procédure précédente.
3.  Si vous souhaitez restituer l’audio, créez une instance du filtre de [convertisseur DirectSound](directsound-renderer-filter.md) et ajoutez-la au graphique de filtre.
4.  Utilisez la méthode IBaseFilter :: EnumPins pour rechercher une broche de sortie sur le filtre source. Pour plus d’informations, consultez [énumération des codes confidentiels](enumerating-pins.md) .
5.  interrogez le gestionnaire de Graph de filtre de l’interface IFilterGraph2.
6.  Appelez [**IFilterGraph2 :: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) avec l' \_ indicateur AM RenderEx \_ RENDERTOEXISTINGRENDERERS. Cet appel génère le rendu de la broche de sortie, en utilisant uniquement les filtres de convertisseur déjà présents dans le graphique, dans ce cas, VMR-9 et le convertisseur DirectSound. cela empêche la logique de Connecter intelligente d’ajouter le convertisseur vidéo par défaut au graphique, ce qui laisse le VMR-9 non connecté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[création de graphiques avec le générateur de Graph de Capture](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



