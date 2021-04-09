---
description: Création d’un graphique de filtre VMR-9
ms.assetid: fd83a89c-f1b6-48a3-971e-04ae4ac14c66
title: Création d’un graphique de filtre VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7fc1eb0982b47f5ef50a00a1c7a275dd8bf60
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846566"
---
# <a name="building-a-vmr-9-filter-graph"></a>Création d’un graphique de filtre VMR-9

Étant donné que le filtre de mixage vidéo 9 Filter (VMR-9) n’est pas le convertisseur vidéo par défaut, une application qui utilise VMR-9 doit l’ajouter explicitement au graphique et la connecter. Cette section présente deux approches différentes de la création de graphiques de filtre avec VMR-9.

Utilisation du générateur de graphiques de capture

Le générateur de graphiques de capture est un objet d’assistance pour la création de graphiques de filtres personnalisés. Vous pouvez l’utiliser pour générer des graphiques VMR-9 comme suit :

1.  Créez et initialisez le générateur de graphiques de capture, comme décrit dans la rubrique [à propos du générateur de graphiques de capture](about-the-capture-graph-builder.md).
2.  Appelez CoCreateInstance pour créer VMR-9 :
    ```C++
    IBaseFilter *pVmr = NULL;
    hr = CoCreateInstance(CLSID_VideoMixingRenderer9, 0, 
        CLSCTX_INPROC_SERVER, IID_IBaseFilter, (void**)&pVmr);
    ```

    

3.  Appelez [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) sur le gestionnaire de graphique de filtre pour ajouter VMR-9 au graphique de filtre :
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

Utilisation du gestionnaire de graphique de filtre

Si vous préférez ne pas utiliser le générateur de graphiques de capture, vous pouvez créer un graphique VMR-9 en utilisant simplement des méthodes sur le gestionnaire de graphique de filtre, comme suit :

1.  Créez VMR-9 et ajoutez-le au graphique, comme indiqué dans la procédure précédente.
2.  Utilisez AddSourceFilter pour ajouter un filtre source pour le fichier vidéo, comme indiqué dans la procédure précédente.
3.  Si vous souhaitez restituer l’audio, créez une instance du filtre de [convertisseur DirectSound](directsound-renderer-filter.md) et ajoutez-la au graphique de filtre.
4.  Utilisez la méthode IBaseFilter :: EnumPins pour rechercher une broche de sortie sur le filtre source. Pour plus d’informations, consultez [énumération des codes confidentiels](enumerating-pins.md) .
5.  Interrogez le gestionnaire du graphique de filtre pour l’interface IFilterGraph2.
6.  Appelez [**IFilterGraph2 :: RenderEx**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph2-renderex) avec l' \_ indicateur AM RenderEx \_ RENDERTOEXISTINGRENDERERS. Cet appel génère le rendu de la broche de sortie, en utilisant uniquement les filtres de convertisseur déjà présents dans le graphique, dans ce cas, VMR-9 et le convertisseur DirectSound. Cela empêche la logique de connexion intelligente d’ajouter le convertisseur vidéo par défaut au graphique, ce qui laisse le VMR-9 non connecté.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de graphiques à l’aide du générateur de graphiques de capture](building-graphs-with-the-capture-graph-builder.md)
</dt> </dl>

 

 



