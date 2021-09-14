---
description: Capturer un fichier DV de type 2
ms.assetid: c7d49c86-1b5d-43bf-98a5-78b297682375
title: Capturer un fichier DV de type 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b919928a4c02ce9e3f3f3e6fcf3d2cd376f880a8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094885"
---
# <a name="capture-a-type-2-dv-file"></a>Capturer un fichier DV de type 2

Un fichier AVI DV type-2 a deux flux, un qui contient une vidéo DV et un autre qui contient des données audio. Pour capturer un fichier de type 2 lors de l’aperçu, utilisez le graphique de filtre illustré dans le diagramme suivant.

![capture de type 2 avec aperçu](images/dv2-cap.png)

Ce graphique est quasiment identique au graphique pour la capture de type 1 (voir [capture d’un fichier DV de type 1](capture-a-type-1-dv-file.md)). Toutefois, le flux de capture traverse le filtre de [séparateur DV](dv-splitter-filter.md) avant d’atteindre le filtre [multiplex MUX](avi-mux-filter.md) . Le multiplexeur de données AVI reçoit donc deux flux, un flux audio et un flux vidéo encodé au format DV.

Générez ce graphique comme suit :


```C++
ICaptureGraphBuilder2 *pBuilder;  // Capture graph builder.
IBaseFilter           *pDV;       // DV capture filter (MSDV)
IBaseFilter           *pAviMux    // Avi Mux filter.
IBaseFilter           *pDVSplit;  // DV Splitter

// Initialize pDV (not shown). 
// Create and initialize the Capture Graph Builder (not shown).

// Create the DV Splitter and add it to the filter graph.
hr = CoCreateInstance(CLSID_DVSplitter, 0, CLSCTX_INPROC_SERVER,
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVSplit));
hr = pGraph->AddFilter(pDVSplit, L"DV Splitter");

// Create the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi,
    OLESTR("C:\\Example2.avi"), &pAviMux, 0);

// Connect the capture pin to the DV Splitter, and render one stream from
// the DV Splitter to the AVI Mux. 
hr = pBuilder->RenderStream(&PIN_CATEGORY_CAPTURE, &MEDIATYPE_Interleaved, 
    pDV, pDVSplit, pAviMux);

// Render the other stream from the DV splitter to the AVI Mux.
hr = pBuilder->RenderStream(0, 0, pDVSplit, 0, pAviMux);

// Render the preview stream.
hr = pBuilder->RenderStream(&PIN_CATEGORY_PREVIEW, &MEDIATYPE_Interleaved, 
    pDV, 0, 0);

// Remember to release all interfaces.
```



1.  Créez le séparateur DV et ajoutez-le au graphique de filtre.
2.  Appelez [**ICaptureGraphBuilder2 :: SetOutputFileName**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-setoutputfilename) pour connecter le filtre multiplex MUX au filtre du writer de fichier.
3.  Appelez [**ICaptureGraphBuilder2 :: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream) pour connecter le filtre de capture MSDV au séparateur DV. Cet appel connecte également l’une des broches de sortie du séparateur DV à AVI Mux.
4.  Appelez à nouveau RenderStream pour connecter l’autre code confidentiel DV au multiplexeur AVI.
5.  Appelez RenderStream une troisième fois pour afficher le flux d’aperçu. Ignorez cette étape si vous ne souhaitez pas afficher un aperçu de la vidéo.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



