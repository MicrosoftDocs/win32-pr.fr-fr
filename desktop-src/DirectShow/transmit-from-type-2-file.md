---
description: Transmettre à partir du fichier de type 2
ms.assetid: c14c1798-aeff-44d8-a2e4-2fe4c146dfb9
title: Transmettre à partir du fichier de type 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23d1d6dec7c68cba177923dea04205d8dbc26faa8ff98cf5d6e79659fced46fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315713"
---
# <a name="transmit-from-type-2-file"></a>Transmettre à partir du fichier de type 2

Pour transmettre un fichier de type 2 lors de l’aperçu, utilisez le graphique de filtre illustré dans le diagramme suivant.

![type-2 transmettre avec la version préliminaire](images/dv2-transmit.png)

Un fichier de type 2 contient deux flux, un flux audio et un flux vidéo encodé au format DV. Ce graphique utilise le filtre [DV du multiplexeur](dv-muxer-filter.md) pour combiner les flux audio et vidéo. Elle envoie le flux entrelacé au filtre MSDV, mais fractionne à nouveau le flux pour l’aperçu.

Générez ce graphique comme suit :


```C++
// Add the DV Mux filter to the graph.
IBaseFilter *pDVMux;
hr = CoCreateInstance(CLSID_DVMux, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pDVMux));
hr = pGraph->AddFilter(pDVMux, L"DV Mux");

// Add the File Source filter to the graph.
IBaseFilter *pFileSource;
hr = pGraph->AddSourceFilter(L"C:\\Example2.avi", L"Source", 
    &pFileSource);

hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);
hr = pBuilder->RenderStream(0, 0, pFileSource, 0, pDVMux);

// Add the Infinite Pin Tee filter to the graph.
IBaseFilter *pTee;
hr = CoCreateInstance(CLSID_InfTee, 0, CLSCTX_INPROC_SERVER
    IID_IBaseFilter, reinterpret_cast<void**>)(&pTee));
hr = pGraph->AddFilter(pTee, L"Tee");

hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pTee);
hr = pBuilder->RenderStream(0, 0, pTee, 0, pDV);
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pTee, 0, 0);
```



Ce code effectue plusieurs appels à **RenderStream**:

Les deux premiers connectent le filtre source au séparateur AVI et le séparateur AVI au DV Mux. dans le premier appel, le générateur de Graph de Capture ajoute automatiquement le séparateur avi au graphique et connecte l’une des broches de sortie du séparateur avi au DV Mux. dans le deuxième appel, le générateur de Graph de Capture recherche la deuxième broche de sortie du séparateur AVI et le connecte au DV Mux.

Le troisième appel à **RenderStream** connecte la DV du multiplexeur au filtre tee du pin infini. L’appel suivant connecte un flux à partir du code confidentiel infini au filtre de capture MSDV. Ce flux est transmis à l’appareil. Le dernier appel à **RenderStream** génère la section d’aperçu du graphique.

Si vous ne souhaitez pas afficher un aperçu lors de la transmission, vous pouvez omettre le tee-pin infini et connecter simplement le multiplexeur multiplex au filtre MSDV :


```C++
hr = pBuilder->RenderStream(0, 0, pDVMux, 0, pDV);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



