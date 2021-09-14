---
description: Capturer le DV avec la couleur RVB non compressée
ms.assetid: 02b54070-09c8-45ab-8a08-1493008a5e1f
title: Capturer le DV avec la couleur RVB non compressée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b471bb8be6bc560fda6d3466cebaef8c490cfb8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127094881"
---
# <a name="capture-dv-to-uncompressed-rgb"></a>Capturer le DV avec la couleur RVB non compressée

Cet exemple montre comment capturer du DV à partir du caméscope et l’enregistrer dans un fichier au format RVB non compressé lors de l’aperçu. Utilisez le graphique de filtre illustré dans le diagramme suivant.

![capture de RGB non compressé dans un fichier](images/dv-rgb-cap.png)

Le filtre de séparateur DV divise le fichier audio/vidéo entrelacé en flux vidéo et audio distincts. la vidéo encodée en DV passe au filtre de [décodeur vidéo DV](dv-video-decoder-filter.md) , qui génère une vidéo RVB non compressée. La vidéo RVB est routée via le filtre tee intelligent vers le filtre multiplex Mux (pour la capture) et le convertisseur vidéo (pour la version préliminaire). Pendant ce temps, le flux audio du séparateur DV passe par le filtre tee de code confidentiel infini à AVI MUX et au convertisseur audio. le gestionnaire de Graph de filtre conserve tous ces flux synchronisés, en utilisant les horodatages sur les échantillons et l’horloge de référence du graphique.

Ce graphique peut paraître inutilement compliqué, mais il garantit que le flux vidéo encodé au format DV est décodé une seule fois, ce qui réduit les besoins en processeur. Notez également que la vidéo passe par le filtre tee intelligent pendant que l’audio passe par le filtre tee du pin infini. Le tee intelligent peut supprimer des images d’aperçu pour améliorer les performances de capture, ce qui est souhaitable pour la vidéo, mais pas pour l’audio, où les échantillons supprimés sont très perceptibles. En outre, étant donné que l’audio nécessite beaucoup plus de bande passante que la vidéo, il y a relativement peu de chance de déposer de l’audio dans le fichier.

Vous devez générer ce graphique une section à la fois, mais la méthode RenderStream peut encore vous aider. Utilisez le code suivant :


```C++
// Build the file-writing section of the graph.
hr = pBuilder->SetOutputFileName(&MEDIASUBTYPE_Avi, 
    OLESTR("C:\\Example3.avi"), &pMux, 0);

// MSDV to DV splitter.
IBaseFilter *pDVSplit;  // Create the DV Splitter (CLSID_DVSplitter)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Interleaved, pDV, 0, pDVSplit);

// Splitter to DV Decoder to Smart Tee.
IBaseFilter *pDVDec; // Create the DV Decoder (CLSID_DVVideoCodec)
IBaseFilter *pSmartTee; // Create the Smart Tee (CLSID_SmartTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Video, pDVSplit, pDVDec,
    pSmartTee);

// Smart Tee (video) to Avi Mux.
IPin *pPin1;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 0, &pPin1);
hr = pBuilder->RenderStream(0, 0, pPin1, 0, pMux);

// Smart Tee to preview.
IPin *pPin2;
hr = pBuilder->FindPin(pSmartTee, PINDIR_OUTPUT, 0, 0, TRUE, 1, &pPin2);
hr = pBuilder->RenderStream(0, 0, pPin2, 0, pMux);

// DV Splitter (audio) to Infinite Tee to Avi Mux.
IBaseFilter *pTee; // Create the Infinite Pin Tee (CLSID_InfTee)
hr = pBuilder->RenderStream(0, &MEDIATYPE_Audio, pDVSplit, pTee, pMux);

// Infinite Pin Tee to preview.
hr = pBuilder->RenderStream(0, 0, pTee, 0, 0);
```



Vous devez créer le séparateur DV, le décodeur vidéo DV, le tee intelligent et les filtres tee de pin infinis, et les ajouter au graphique de filtre. (Par souci de concision, ces étapes sont omises du code précédent.) Cet exemple utilise la méthode [**ICaptureGraphBuilder2 :: FindPin**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-findpin) pour rechercher les codes confidentiels de capture et de prévisualisation sur le filtre tee intelligent. la capture est toujours en sortie broche 0 et la version préliminaire est la broche 1 de sortie.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Vidéo numérique en DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



